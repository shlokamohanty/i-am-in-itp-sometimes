---
layout: post
title: assignment 1 and readings
subtitle: ""
date: 2026-09-13
tags: networks-ongoing
---

I was supposed to do this much earlier, but I started much later. Now, I feel like I'm one of those hackers from the movies, except right now I'm just trying to figure out how to set up my virtual host. The only thing akin to the hackers from the movies is the dim light from my lamp, except it's a warm shade instead of a cool one.

---

Okay, setting up a virtual host was not bad at all. Sometimes, I think of the terminal as this scary thing — the commands. I don't know why. But I open Jupyter Notebook almost every day. 

Actually, I think I've set up a virtual host once in undergrad. I used a Google Cloud Virtual Machine then. But I don't remember much from then. The thing is, a lot of times in undergrad, I did a lot of things, but I didn't absorb the information as well. I’m trying to actively change that.

```ssh shlokamohanty@161.35.107.157```

Along with Node.js, I also decided to install the Python package installer, python3-pip. Ubuntu comes with Python 3 pre-installed.

I noticed that if I add '-y' such as:

```sudo apt install nodejs -y```

It automatically answers "yes" to all prompts.

![networks](/i-am-in-itp-sometimes/assets/images/terminal1.jpg)

Even doing this small setup makes me feel a little nostalgic of how much I used to code in undergrad. I miss that sometimes. 

--- 

I did ufw (uncomplicated firewall) configuration. 

In all honesty, I think I don't really remember what Linux is. I forgot what Ethernet was in the last class. I feel embarrassed. I’ve been having a lot of embarrassing moments lately, mostly with words. I think of words, and I notice I don’t truly know their meaning. But it’s better accepting that I don’t really know than to pretend that I know, I’ve realised.

> [Linux®](https://www.redhat.com/en/topics/linux/what-is-linux) is an open source operating system (OS) created by Linus Torvalds in 1991. Today, it has a massive user base, and is used in the world’s 500 most powerful supercomputers.

> [Unix](https://en.wikipedia.org/wiki/Unix) is a family of multitasking, multi-user computer operating systems that trace their origins back to the original AT&T Unix developed in 1969 at Bell Labs.

--- 

**firewall log analysis**

![networks](/i-am-in-itp-sometimes/assets/images/terminal2.jpg)

![networks](/i-am-in-itp-sometimes/assets/images/terminal3.jpg)

![networks](/i-am-in-itp-sometimes/assets/images/terminal4.jpg)

I thought it is 1453 attempts to connect to my computer, so far. But, I forgot to do a line count.

![networks](/i-am-in-itp-sometimes/assets/images/terminal5.jpg)

```sudo tail -10 /var/log/ufw.log | sed -e 's/\s/\t/g'```

![networks](/i-am-in-itp-sometimes/assets/images/sheets.jpg)

This was interesting. I didn't know that 10 unique external IP addresses were attempting to connect to my server. Given that I looked at only the last 10 results, I wasn't expecting all 10 to be unique, though. I did this at home, as opposed to school. Maybe the results would have been different in school.

They all have the same MAC address.

---

**readings**

[**How Infrastructure Shapes Us**](https://untappedjournal.com/stories/deb-chachra-how-infrastructure-shapes-us), Deb Chachra, 2023

> One definition of infrastructure is that it’s all the underlying systems whose presence we take for granted when we start on something new.
> Much of the value of transportation and telecommunications networks lies in the nature and number of connections between nodes: The more people who are connected together, the more valuable the networks become for each user.

**[Why Google Went Offline Today and a Bit about How the Internet Works](http://blog.cloudflare.com/why-google-went-offline-today-and-a-bit-about)** Tom Paseka, CloudFlare, 2006

> The Internet is a collection of networks, known as "Autonomous Systems" (AS). Each network has a unique number to identify it known as AS number.
> The networks are connected together by what is known as Border Gateway Protocol (BGP). BGP is the glue of the Internet — announcing what IP addresses belong to each network and establishing the routes from one AS to another.
> Networks trust each other to say which IP addresses and other networks are behind them. When you send a packet or make a request across the network, your ISP connects to its upstream providers or peers and finds the shortest path from your ISP to the destination network.
> Unfortunately, if a network starts to send out an announcement of a particular IP address or network behind it, when in fact it is not, if that network is trusted by its upstreams and peers then packets can end up misrouted. That is what was happening here.

- It’s like spreading rumors

**[We finally know what caused the global tech outage – and how much it cost](https://www.cnn.com/2024/07/24/tech/crowdstrike-outage-cost-cause/index.html)** Brian Fung, CNN, 2024

> The issue affected only Windows devices, not Mac or Linux machines, and only those that were switched on and able to receive updates during those early morning hours.
> When Windows devices using CrowdStrike’s cybersecurity tools tried to access the flawed file, it caused an “out-of-bounds memory read” that “could not be gracefully handled, resulting in a Windows operating system crash,” CrowdStrike said.
> CrowdStrike said that the testing and validation system that approved the bad software update had appeared to function normally for other releases made earlier in the year.