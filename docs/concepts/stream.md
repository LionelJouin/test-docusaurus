---
sidebar_position: 6
---

# Stream

The Stream reflects a logical grouping of traffic flows. The stream points out the conduit the traffic will pass before it can be consumed by the target application.

Stream is a logical configuration entity, which cannot directly be found in the payload traffic.

The stream is the "network service entity" to be known and referred in the target application. The different target application pods can sign up for consumption of traffic from different streams. When more target pods are signed up for the same stream the traffic will be load-balanced between the pods.

Notice that a target pod concurrently only can sign up for streams belonging to the same trench.

![Overview-Stream-Flow](../resources/Overview-Stream-Flow.svg)

## Configuration

Name | Type | Description | Required | Default
--- | --- | --- | --- | ---
name | string | Name of the Stream | yes |
conduit | string | Name of the Conduit the Stream belongs to | yes | 
