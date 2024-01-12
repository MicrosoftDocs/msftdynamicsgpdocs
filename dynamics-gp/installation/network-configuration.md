---
title: "Dynamics GP network requirements"
description: "Learn about network configuration that must be in place before installing Dynamics GP."
keywords: ""
author: jswymer
ms.author: jswymer
manager: annbe
applies_to: 
ms.date: 08/23/2018
ms.topic: article
ms.assetid: 40e41526-13c6-4111-b472-d78f9f1d7099
ms.reviewer: jswymer
---
# Network configuration

This chapter contains information about network configuration that must be in place before installing Dynamics GP.  

## Domain

To use Dynamics GP, your Web server, back office server, Remote Desktop Services (if applicable), and client workstations must belong to a domain.

A domain is a group of computers that are part of a network and share a common directory database. A domain is administered as a unit with common rules and procedures. Each domain has a unique name.

## Network protocol tuning

To optimize your network for Microsoft SQL Server and Dynamics GP, refer to the following guidelines.

- Limit the network to one protocol. (TCP/IP is required.)

- Remove unused network protocols.

- Use 1 GB Ethernet for optimal performance. For more information, see [System requirements](https://go.microsoft.com/fwlink/?LinkId=263763).

- Use switches rather than hubs, if optimal performance is required.

## TCP/IP

Transport Control Protocol/Internet Protocol (TCP/IP) is required for Dynamics GP.

If you’re using TCP/IP, review the information in this section to be sure that the network is set up properly. Then use your networking protocol documentation to install and test the protocol on all clients and servers before you install Dynamics GP.

### IP addresses

Each computer that you use with Dynamics GP must have a unique IP number (Internet Protocol address) associated with it. For more information about IP addresses, consult your network administrator or refer to your networking protocol software documentation.

### TCP/IP name resolution

You should use some type of name resolution in your network, so that each computer is identified by a unique host name. Name resolution is a method of identifying each computer and can be accomplished by having a specific server act as a domain name server or putting a hosts file on each client and server.

For more information about name resolution using either a domain name server or hosts files, consult your network administrator or refer to your networking protocol software documentation.

### Testing TCP/IP connectivity

To test connectivity between clients and servers, use an application distributed with most TCP/IP packages called ping. The ping application will attempt to send a network message or set of messages to a designated computer and inform you whether the message arrived at that computer. Be sure you ping the host name and the ID address of every computer in your system before installing Dynamics GP.
