---
sidebar_position: 4
---

# Gateway

The Gateway defines how to establish connectivity with an external gateway such as; which IP-address, routing- and supervision-protocol(s) to use. The Gateway can also define specific protocol settings that differ from the default etc.

Notice that it normally is good practice and often required have "mirrored" settings shared between the external gateway and the Meridio FrontEnds to get the BGP and BFD sessions established. The used "retry" and "time-out" settings will dictate the time it takes traffic to fail-over in case of a link failure.

Notice that when static is chosen as routing protocol BFD link-supervision is by default turned on with default settings.

Note: In the Alpha release BGP with BFD is not a supported option.

### Configuration

Name | Type | Description | Required | Default
--- | --- | --- | --- | ---
name | string | Name of the Gateway | yes | 
address | string |  | yes | 
remote-asn | int |  | yes | 
local-asn | int |  | yes | 
remote-port | int |  | yes | 
local-port | int |  | yes | 
ip-family | string |  | yes | 
bfd | bool |  | yes | 
protocol | string |  | yes | 
hold-time | int |  | yes | 
min-tx | int |  | yes | 
min-rx | int |  | yes | 
multiplier | int |  | yes | 
trench | string | Name of the Trench the Gateway belongs to | yes | 
