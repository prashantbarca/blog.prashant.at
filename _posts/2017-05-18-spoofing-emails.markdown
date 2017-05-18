---
author: prashant
comments: false
date: 2017-05-18 08:00:30+00:00
layout: post
slug: spoofing-emails
title: Spoofing Emails from other Servers
wordpress_id: 10
---

In this tutorial you will see how you can spoof an email from anyone to anyone using SMTP and telnet. Although, a lot of mail servers are smart about this and reject emails sent from this. My experiments have shown that a lot of servers still accept these messages due to inadequate security.

The first thing to do is finding the MX record for the server you will be spoofing from.

```shell
dig mx example.com
```

Look for the answer section in the response, and you should see a resolved domain name (sometimes this has the word "protection" in it, nothing to worry about!).

Next, we will use telnet to login to the server. Port 25 is for SMTP.

```shell
telnet example.com 25
```

At the prompt, you will have to enter the following commands.

```shell
EHLO abcd
MAIL FROM: <abcd@example.com>
RCPT TO: <xyz@example.com>
DATA
from:  <abcd@example.com>
to: <xyz@example.com>
subject: Random
body: Random again

.

```

EHLO, MAIL FROM, RCPT TO and DATA are commands.


