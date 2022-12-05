---
sidebar_position: 2
---

# Vip

The Vip defines a virtual IP address towards which external traffic can be attracted and load-balanced over a scaling set of target application pods. 

As soon as a Vip has been applied to a working trench and attractor the VIP address will be announced by all FEs using BGP. 

### Configuration

Name | Type | Description | Required | Default
--- | --- | --- | --- | ---
name | string | Name of the VIP | yes | 
address | string | The virtual IPaddress. Both ipv4 and ipv6 addresses are supported. The VIP address must be a valid network prefix. | yes | 
trench | string | Name of the Trench the VIP belongs to | yes | 
