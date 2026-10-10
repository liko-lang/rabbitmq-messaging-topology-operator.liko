<p align="center">
  <img src="assets/camille.png" alt="Camille, the mascot of Liko" width="240">
</p>

<h1 align="center">rabbitmq-messaging-topology-operator.liko</h1>

**This repository contains the RabbitMQ Messaging Topology Operator module for the Liko data language. This module is officially maintained by the Liko team.**

It contains the complete set of RabbitMQ Messaging Topology Operator schema definitions from the official [RabbitMQ Messaging Topology Operator repository](https://github.com/rabbitmq/messaging-topology-operator/releases).

---

## Installation

Initialize a local module with `liko init`, then add `rabbitmq-messaging-topology-operator.liko` as a dependency.

```bash
liko init
```
```bash
liko add rabbitmq-messaging-topology-operator
```

```bash
liko install
```

## Usage

The module can now be used from any directory within the current module.

```liko
#Topo: import "rabbitmq-messaging-topology-operator/v1beta1"

$: {
    queue: #Topo.Queue {
        metadata: {
            name: "orders"
        }
        spec: {
            name: "orders"
            rabbitmqClusterReference: {
                name: "broker" 
            } 
        } 
    }
}
```
