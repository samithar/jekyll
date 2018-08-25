---
title:  Ubuntu and Microsoft Exchange Email
header:
  teaser: false
categories: 
  - Ubuntu
tags:
  - Work
---

#Ubuntu and Microsoft Exchange

Ok, lets make this short and straight forward. Recently, I had to stay home and work. And to make the things more brighter, I forgot to bring my laptop from work. To make it even better, I did not have a Windows running laptop at home, as most of my work home work things done in an Ubuntu.

Since my work use Windows, specifically Microsoft Exchange as the email service, I had to find a quick trick to get/reply to my emails. 

Fortunately, it turned out to be extremely easy to do so.

Add exchange as online account in Ubuntu.

![ ](/assets/img/ubuntu_acc.png  "Online Accounts")

After successful authentication, install evolution.

```bash
sudo apt-get install evolution
```

Then I noticed that there is no exchange service by default. So I exit evolution and install

```bash
sudo apt-get install evoloution-ews
```
Then I started evolution again. Really, that was it. All my emails were in there, including calender items.