# Route 53

Route53 is a Managed DNS, a collection of rules and records which helps clients understand how to reach a server through URLs.

## AWS Common Records

* __A__: URL to IPv4
* __AAAA__: URL to IPv6
* __CNAME__: URL to URL
* __Alias__: URL to AWS Resource
	* Prefer Alias over CNAME for AWS resource (better performance)

![A record](./routing.png)

## Overview

#### Domain Names

Route53 can use:
* Public domain names.
* Private domain names (that can be resolved by your instances in your VPCs).

#### Advances Features

* Load Balancing (through DNS - client load balancing)
* Health Checks
* Routing Policy:
	* Simple
	* Failover
	* Geolocation
	* Geoproximity
	* Latency
	* Weighted	
