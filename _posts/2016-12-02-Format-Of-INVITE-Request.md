---
layout: post
title: "Format of INVITE Request"
date: 2016-09-19
---

INVITE sip:user2@server2.com SIP/2.0
Via:SIP/2.0/UDP Pc33.server1.com;branch=z9hg4bk776asdhds
Max-Forwards:70
To:User2<sip:user2@server2.com>;tag=1928301774
Call-Id:a84b4c76e66710@PC33.server1.com
CSeq:314159 INVITE
Contact:<sip:user1@PC33.server1.com>
Content-Type:application/sdp
Content-Length:142

The first line of text encoded message is called request line.It identifies that the message is a request.
Here method is "INVITE",request uri is "user2@server2.com" and SIP version is 2.

<h4> Header Fields </h4>
There are following header fields:

<h4> Via :</h4>
It contains the local address of user1 i.e PC33.server1.com where it is expecting the response to come.

<h4> Max-Forward :</h4>
It is used to limit the number of hopes that this request may take before reaching the recipient.It is decreased by one at each hop.
It is necessary to prevent the request from travelling forever incase it is trapped in a loop.

<h4> To : </h4>
It contains a display name "user2" and a SIP or SIPS uri <user2@server2.com>.

<h4> From : </h4>
It also contains a display name "user1" and a SIP or SIPS uri <user1@server1.com>.It also contains a tag which is a pseudo-random 
sequence inserted by the SIP application.It works as an identifier of the caller in the dialog.

<h4> Call-Id : </h4>
It is a globaly unique identifier of the call generated as the combination of a pseudo-random string and the softphone's Ip address.
NOTE:~ The Call-Id is unique for a call.A call may contain several "dialogs".

<h4> CSeq : </h4>
It contains an integer and a method name.When a transaction starts,the first message is given a random CSeq.After that it is increamented
by one with each new message.It is used to detect non-delivery of a message or out of order delivery of messages.

<h4> Contact : </h4>
It contains a SIP or SIPS uri that is a direct route to user1.It contains an username and a fully qualified domain name(FQDN).It
may also have an ip address.
NOTE:~Via field is used to send the response to the request.
Contact field is used to send the future requests that is why the 200 OK response from user2 goes to user1 through proxies,but 
when user2 generates a BYE request(a new request,& not a response to INVITE),it goes directly to user1 bypassing the proxies.

<h4> Content-Type </h4>
It contains a description of the message body.

<h4> Content-Length </h4>
It is an octet(byte) count of the message body.

The header may contain other header fields also.However those fields are optional.
