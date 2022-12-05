---
sidebar_position: 5
---

# Conduit

The Conduit defines a physical path of chained network services the traffic will pass before it can be consumed by the target application. The Traffic is assigned to the Conduit by Stream. Currently, the only supported network service function is stateless load balancing.

The picture below describes 2 conduits. the left one is a stateless load-balancer and the right one is a SCTP network service. The left user pod has subscribed to one or more stream the stateless load-balancer is handling, so it is connected to it via a new network interface. The right user pod has subscribed to streams the stateless load-balancer and the SCTP network services are handling, so it is connected to them via two new network interfaces, one connected to the stateless load-balancer network service, and the other one connected to the SCTP network service. 

<img src="resources/Overview-Conduit.svg" width="50%" />

## Configuration

Name | Type | Description | Required | Default
--- | --- | --- | --- | ---
name | string | Name of the Conduit | yes |
trench | string | Name of the Trench the Conduit belongs to | yes | 
destination-port-nats | []PortNat | List of destination ports to NAT. | no | 

### PortNat

Name | Type | Description | Required | Default
--- | --- | --- | --- | ---
port | uint16 | Destination Port exposed by the service (exposed in flows). Traffic containing this property will be NATted. | yes |
target-port | uint16 | Represents the port the traffic will be NATted to. Targets will receive traffic on that port. | yes | 
vips | []string | VIPs exposed by the service (exposed in flows). Traffic containing this property will be NATted. | yes | 
protocol | string | Protocol exposed by the service (exposed in flows). Traffic containing this property will be NATted. | yes | 