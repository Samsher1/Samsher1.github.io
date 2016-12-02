---
layout: post
title: "Samsher Kumar, Launches Site"
date: 2016-09-19
---
<link href="http://Samsher1.github.io/post/index.html"/>

Introduction of SIP (Session Initiation Protocol) :

        SIP is limited to only the setup,modification and termission of session.
        It allows for the establishment of user location i.e translating from a user's name to their current network address.
        It provides for feature negotiation so that all of the participants in a session can agree on the features to be       supported among them.
        It is a mechanism for call management.For example adding,dropping or transferring participants. 
        It allows for changing features of a session while it is in progress.
        It has nothing to do with quality of service(QoS).

User Agents :

        There are following two types of User Agents:
        
        1) User Agent Client
        
        2) User Agent Server
        
        
User Agent Client :

        It generates request and send those to servers.
        
User Agent Server :

        It gets request,process those requests and generates responses.

Types of Servers :

        There are following types of Servers:
        
        1) Proxy Server
        
        2) Redirect Server
        
        3) Registrar
        
        4) Location Server
        
        
Proxy Server :

        When a request is generated,the exact address of the recipient is not known in advance,so client sends the request to a proxy server.The server on behalf of  the client (as if giving a proxy for it) forwards the request to another proxy server or the recipient itself.
        
Redirect Server :

        A redirect server redirects the request back to the client indicating that the client needs to try a different route to get to the recipient.It generaly happen when a recipient has moved from its original position either temporarily or permamently.
        
Registrar :

        One of the prime jobs of these servers is to detect the location of an user in a network.Users from time refreshes their locations by registering (sending a special type of message) to registrar server.
        
Location Server :

        The addresses registered to a registrar server are stored in a location server.
        
        
