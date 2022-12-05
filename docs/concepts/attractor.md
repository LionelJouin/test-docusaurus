---
sidebar_position: 3
---

# Attractor

The Attractor defines a group of Front-Ends (FEs) sharing commonalities, for example; external interface to utilize, IP-address assignment method, gateway(s) to establish connection with, VIP-addresses to announce etc. 

### Configuration

Name | Type | Description | Required | Default
--- | --- | --- | --- | ---
name | string | Name of the Attractor | yes | 
vips | []string |  | yes | 
gateways | []string |  | yes | 
trench | string | Name of the Trench the Attractor belongs to | yes | 
