---
layout: post
title: assignment 2 and readings
subtitle: ""
date: 2026-09-21
tags: networks-ongoing
---

What is ```mtr``` in ```sudo apt install mtr```?

What is ```dnf``` in ```sudo dnf install traceroute mtr```?

I do visit gmail.com a lot, but I also think lately I've been watching BBC animal videos on YouTube a lot. I like watching penguin and cat videos. HBO Max and Amazon.com because I was moving this weekend.

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

It gave the same error. I don't quite understand why specific links are not working.

Then, I just tried:

 ```traceroute www.youtube.com | sed -e 's/\s/\t/g'```

![trace-route](/i-am-in-itp-sometimes/assets/images/traceroute.jpg)
 
---

### on distributed communications

#### examination of a distributed network

> The term "redundancy level" is used as a measure of connectivity, as defined in Fig. 2. A minimum span network, one formed with the smallest number of links possible, is chosen as a reference point, and is called "a network of redundancy level one."

#### node destruction

> If the expected "noise" was destruction caused by conventional hardware failure, the failures would be randomly distributed through the network. But, if the disturbance were caused by enemy attack, the possible "worst cases" must be considered.