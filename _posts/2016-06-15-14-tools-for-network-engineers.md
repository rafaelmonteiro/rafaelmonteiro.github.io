---
layout: post
title: "14 tools for network engineers"
description:
headline:
modified: 2016-06-15
category: Information Security
tags: [tools, infosec]
image:
  feature:
comments: true
mathjax:
---

## Introduction  
To overcome daily issues, it's interesting that a network professional know some
tools which can increase his productivity and make his work easier.

Although some tools - especially ARPSpoof, nmap, TCPTraceroute and AirCrack -
can be used in malicious contexts - as to perform reconnaissance and probe for
weaknesses in preparation for attacks - they also have value for legitimate
purposes.

## Tools

**AirCrack** – Can reveal who’s using the wireless network and can be used to
troubleshoot issues. Also it's a great tool for discovering nearby wireless
networks.

**ARPSpoof** – Hackers use it to send spoofed ARP requests trying to pair MAC
and IP addresses of networked devices. But it can also be used to create
man-in-the-middle monitoring of activity without having to install a device on
the span port of a router, for instance.

**Cacti** – It gathers and graphs SNMP values over time, giving a picture of
device utilization.

**cURL** – Basically this tool moves data to and from servers and it is really
useful in measuring the response time of Web sites.

**Elasticsearch** – It is a search server that can be paired with Logstash
and Kibana (ELK) to gather log data and create dashboards. Elasticsearch
provides the search capabilities and Kibana renders the data to create the
dashboards.

**fprobe** – Listening to specified interfaces and gathering NetFlow data
about traffic going through is the primary purpose of fprobe. It can be used to
detect undesired traffic types, such as video streaming services in a corporate
environment.

**iperf** – This tool measures throughput, packet loss and jitter, and
supports both UDP and TCP packets to determine quality of connections between
devices on a network. It can graph the data it gathers to see how network
conditions vary over time.

**nfdump** – Flow information gathered by fprobe can be exported to nfdump,
which stores it in a file system that it can read and use to display the data
based on protocols and rank top users. One kind of application is to discover
time-of-day congestion issues, for example.

**Nmap** – This is a powerful tool for network, device and service discovery
useful for network scanning and for performing security audits. It can scan for
specific ports and determine, for example, whether they are open or not. It can
scan devices by subnet and deliver valuable information such as what type of
traffic devices are putting out. In addition to discovering what
devices are on the network, Nmap can scan for services that are active and
perform pointer-record lookups and reverse DNS lookups which may help ID what
kind of device it has found.

**OpenNMS** – This tool, which monitors devices and services, issues alerts
when they go down and can write availability reports on devices.

**Smokeping** – It measures latency and packet loss that can be analyzed over
time to reveal changes in latency that can be used for troubleshooting or
network planning. It does this by firing off Ping packets at regular intervals
and recording the response times. Spikes that show up on graphs of the data
gathered indicate when response-time troubles arise and can help narrow down
investigations into their causes.

**Snort** – This is a intrusion detection ID tool that can be used
to live-monitor networks, but it can also be used to apply rules to a set of
trace files captured. It can be paired with logging tools like ElasticSearch
and LogStash, and the gathered data can be analyzed, with rules set to look
for specific conditions and send alerts.

**TCPTraceroute** – This tool traces paths through networks using TCP rather
than ICMP. It’s good for finding what’s blocking traffic in transit, such as
firewalls configured to block the ports the traffic needs to use.

**Wireshark** – It captures and analyzes packets to find malformed
frames, mis-ordered packets and the like. Users can write rules to capture
only certain protocols such as wireless, TCP or http to troubleshoot slow
server response time, for example.
