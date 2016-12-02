---
layout: post
title: "Introduction of SIP :"
---

<h4>Introduction of SIP (Session Initiation Protocol) :</h4>

        SIP is limited to only the setup,modification and termission of session.
        It allows for the establishment of user location i.e translating from a user's name to their current network address.
        It provides for feature negotiation so that all of the participants in a session can agree on the features to be       supported among them.
        It is a mechanism for call management.For example adding,dropping or transferring participants. 
        It allows for changing features of a session while it is in progress.
        It has nothing to do with quality of service(QoS).

<h4>User Agents :</h4>

        There are following two types of User Agents:
        
        1) User Agent Client
        
        2) User Agent Server
        
        
<h4>User Agent Client :</h4>

        It generates request and send those to servers.
        
<h4>User Agent Server :</h4>

        It gets request,process those requests and generates responses.

<h4>Types of Servers :</h4>

        There are following types of Servers:
        
        1) Proxy Server
        
        2) Redirect Server
        
        3) Registrar
        
        4) Location Server
        
        
<h4>Proxy Server :</h4>

        When a request is generated,the exact address of the recipient is not known in advance,so client sends the request to a proxy server.The server on behalf of  the client (as if giving a proxy for it) forwards the request to another proxy server or the recipient itself.
        
<h4>Redirect Server :</h4>

        A redirect server redirects the request back to the client indicating that the client needs to try a different route to get to the recipient.It generaly happen when a recipient has moved from its original position either temporarily or permamently.
        
<h4>Registrar :</h4>

        One of the prime jobs of these servers is to detect the location of an user in a network.Users from time refreshes their locations by registering (sending a special type of message) to registrar server.
        
<h4>Location Server :</h4>

        The addresses registered to a registrar server are stored in a location server.
        
        
