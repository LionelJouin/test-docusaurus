---
sidebar_position: 7
---

# Flow

The Flow classifies incoming traffic based on the 5-tuple in the IP-header containing: Source and destination IP-addresses, source and destination ports and protocol type.

The traffic that match the classification are mapped to a logically stream.

It is allowed to configure flows having overlapping IP-addresses and port ranges. In this case the priority setting is used to decide which flow will be tried matched first. 

Traffic that do not match the classification for any flow will be dropped.

Notice that destination IP-address is provided by referencing one or more Vip.

![Overview-Stream-Flow](../resources/Overview-Stream-Flow.svg)

## Configuration

Name | Type | Description | Required | Default
--- | --- | --- | --- | ---
Name | string | Name of the Flow | yes |
source-subnets | []string |  | yes | 
destination-port-ranges | []string |  | yes | 
source-port-ranges | []string |  | yes | 
protocols | []string |  | yes | 
vips | []string |  | yes | 
priority | int |  | yes | 
stream | string | Name of the Stream the Flow belongs to | yes | 
