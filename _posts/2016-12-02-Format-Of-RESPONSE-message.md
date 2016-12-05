---
layout: post
title: "Format of RESPONSE message"
---



Format of RESPONSE message :
<br>
<br>
SIP/2.0 200OK
Via: SIP/2.0/UDP site4.server2.com;branch=z9hg4bknashds8;recieved=192.0.2.3
Via: SIP/2.0/UDP site3.server1.com;branch=z9hg4bk77ef4c23129831;recieved=192.0.2.2
Via: SIP/2.0/UDP PC33.server1.com;branch=z9hg4bk776asdhds8;recieved=192.0.2.1
To: user2<SIP:user2@server2.com>;tag=a6cs58f
From: user1<SIP:user1@server1.com>;tag=1928301774
Call-Id: a84b4c76e66710@PC33.server1.com
CSeq: 314159 INVITE
Contact: <SIP:user2@192.0.2.4>
Content-type: application/sdp
Content-length: 131

The first line in a response is called status line.

<h2>Header Fields :</h2>
<h4>Via :</h4>

    There are more than one via field.This is because each element through which the INVITE request has passed has added its    identity in the via field.Three via fields are added by softphone of user1,server1 the first proxy server and server2 the second proxy server.The response retraces the path of INVITE using the via fields.On its way back,each element removes the corresponding Via field before forwarding it back to the caller.
    
<h4>To :</h4>

    To field now contains a tag.This tag is used to represent the colee in a dialog.
    
<h4>Contact :</h4>

    It contains the exact address of user2.So user1 doesn't need to use the proxy servers to find user2 in the future.
    
It is 2xx response.However responses can be different depending on particular situations.

<h2>Types of Responses :</h2>

<h4>1xx(Provisional) :</h4>

                  Request recieved,continuing to process the request.                  
<h4>2xx(Success)     :</h4>
                  The action was successfully recieved,understood and accepted.
                  
<h4>3xx(Redirection)  :</h4>

                  Further action needs to be taken in order to complete the request.
                  
<h4>4xx(Client Error) :</h4>

                  The request contains bad syntax or cannot be fulfilled at this servers.
                  
<h4>5xx(Server Error) :</h4>

                  The server failed to fulfill an apparently valid request.
                  
<h4>6xx(Global Failure) :</h4>

                   The request can't be fulfilled at any server.
                   
If a response is recieved having a status code of the form Yxx which is not understood by the recieving party ,it treats the response
as a Y00 response i.e if a client recieves an unknown response 345,it treats that as 300 response.An unknown 1xx is treated as 
183(Session in progress).
