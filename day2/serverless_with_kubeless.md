## Serverless on Kubernetes with Kubeless: Native, lightweight and ready to scale

_Serverless Track_

_Andrés Martínez, VMware/Bitnami_

[Kubeless](https://kubeless.io)

Kubeless is k8s native serverless framework. It provides an easy way to create and manage FaaS.
**Cloud agnostic, k8s native, multiple language, multiple triggers.** Kubeless provides out of th box methods to monitor and get metrics.

#### Demo
The code for the demo is here:
[GitHub - andresmgot/cncf-warsaw: Demos for conference](https://github.com/andresmgot/cncf-warsaw)

Each function gets `event` and `context`. The context represents the environment (runtime, memory-limits, timeouts etc.).
Triggers:
- http
- cronjob
- kafka
- Amazon kinesis

**Functions are built just once, stored as docker and easy to use.**

#### QA
**Why should I use kubeless instead of knative?** Knative is for creating service, it's not a framework.
**Can you compare to lambdas on AWS?** There's no vendor locking.
**Can we deploy it on GKE?** Sure.
**Can I use code from AWS lambdas?** Depends on use-case, as long as the function is self-contained you can move it easily.
