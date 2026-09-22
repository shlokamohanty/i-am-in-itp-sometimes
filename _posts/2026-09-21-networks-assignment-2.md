---
layout: post
title: assignment 2 and readings
subtitle: ""
date: 2026-09-21
tags: networks-ongoing
---

What is ```mtr``` in ```sudo apt install mtr```?

From Wikipedia:
[**My traceroute**](https://en.wikipedia.org/wiki/MTR_(software)), originally named **Matt's traceroute** (**MTR**), is a computer program that combines the functions of the traceroute and ping programs in one network diagnostic tool.

What is ```dnf``` in ```sudo dnf install traceroute mtr```?

[Dandified YUM](https://en.wikipedia.org/wiki/DNF_(software))

I do visit Gmail a lot, but I also think lately I've been watching BBC animal videos on YouTube a lot. I like watching penguin and cat videos. HBO Max too.

I'll start with one of the BBC animal videos that I was watching. This is one is of a [baby penguin](https://youtu.be/q3uXXh1sHcI?si=6aZCV8gzCwug9nEL).

 ```traceroute https://www.youtube.com/watch?v=q3uXXh1sHcI | sed -e 's/\s/\t/g'``` 

On doing so I got this as an error:

> https://www.youtube.com/watch?v=q3uXXh1sHcI: Name or service not known

> Cannot handle "host" cmdline arg `https://www.youtube.com/watch?v=q3uXXh1sHcI' on position 1 (argc 1)

From last assignment, I learnt that this separates whitespace into tabs, which makes it easy to copy paste it on google sheets.

So when I went to reddit, I learnt

> So since traceroutes works using ICMP, running a traceroute with HTTP packets might not work using standard traceroute tools or native Windows utilities.

> Since you're limited to native Windows utilities, you might try using `telnet` or PowerShell to test connectivity to the specific port the HTTP service is listening on (typically port 80 or 443 for HTTPS). It won't give you a hop-by-hop analysis like traceroute, it can confirm whether you're able to establish a TCP connection to the HTTP service from your machine.

> Have you tried 'pathping' it can provide more detailed information about where packet loss is occurring. Try this:

> `pathping example.com`

> And see if you get anything from that

There's a Unix and Linux stack exchange: https://unix.stackexchange.com/

So I tried:

 ```traceroute www.youtube.com/watch?v=q3uXXh1sHcI | sed -e 's/\s/\t/g'```

It gave the same error. I don't quite get why specific links are not working.

Then, I just tried:

 ```traceroute www.youtube.com | sed -e 's/\s/\t/g'```

![trace-route](/i-am-in-itp-sometimes/assets/images/traceroute.jpg)
 
---

### the dawn of the stupid network

> So what exactly is a Stupid Network? George Gilder observed more than five years ago, "In a world of dumb terminals and telephones, networks had to be smart. But in a world of smart terminals, networks have to be dumb."

> Bits go in one end and come out the other. Data flows – like water – define the movements and channels within the system.

> Consider the local exchange, represented by the three digits of a telephone number that follow the area code (the nxx in the pattern nxn-nxx-xxxx). The local exchange "owns" the last four digits of a telephone number. Theoretically, a local exchange can serve up to 10,000 telephones, e.g., with numbers 762-0000 through 762-9999.

> Today, network providers routinely put several tens of gigabits – a few hundred thousand calls – on a single glass fiber as thin as a human hair. Switching used to be scarce, too, but now it is equally abundant.

### on distributed communications

> The centralized network is obviously vulnerable as destruction of a single central node destroys communication between the end stations.

#### examination of a distributed network

> The term "redundancy level" is used as a measure of connectivity, as defined in Fig. 2. A minimum span network, one formed with the smallest number of links possible, is chosen as a reference point, and is called "a network of redundancy level one."

#### node destruction

> If the expected "noise" was destruction caused by conventional hardware failure, the failures would be randomly distributed through the network. But, if the disturbance were caused by enemy attack, the possible "worst cases" must be considered.

> We have briefly considered network behavior when all links are working. But, we are also interested in determining network behavior with real world links—some destroyed, while others are being repaired.

> This implements a form of sceptical learning. Learning will take place even with occasional errors. Thus, by the simple device of using only two separate "learning constants," depending whether the measured value is greater or less than the table value, we can provide a mechanism that permits the network routing to be responsive to varying loads, breaks, and repairs.