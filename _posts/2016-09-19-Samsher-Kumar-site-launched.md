---
layout: post
title: "Samsher Kumar, Launches Site"
date: 2016-09-19
---
Sip interview questions.


1. What is a Request-URI and its purpose?

It indicates the user or service to which this request is being sent or addressed. It may support a SIP, SIPS or TEL URI or any generic URI. It should be noted that the initial value of the R-URI is set as the To header field.

Example:
Alice calls Bob.

INVITE sip:bob@alpha.com SIP/2.0
From: Alice;tag=1928301774
To: Bobbob@alpha.com>

Break the R-URI as "userinfo" and "@' components of the SIP URI, so
R-URI = bob@alpha.com
