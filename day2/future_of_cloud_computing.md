## The future of Cloud Computing
_Cloud_

_Dariusz Dwornikowski, Nordcloud_

[Darek Dwornikowski ☁ (@7d1) on Twitter](https://twitter.com/7d1)

Where are we going to put all apps that are going to pop up in next year? Probably more than in last 40 years. 
How to accommodate the apps in cost effective way? 

Dev-centricism and abstracting out irrelevant are the key factors.
The idea is abut making as much lines of codes connected to business as it is possible, thus abstracting the commons.

In the future we can expect that:
- Even less infra and less language from on prem. For now cloud provides feeling that it's a well-known environment.
- Thinking out of box will be required, let's think about cloud as an API not a bare metal machine

K8s is transition technology and it's needs to stabilize. And as a devops I don't want to be a yaml developer.

Kubernetes really helps in cloud native transformation:
- K8s will make workloads truly portable
- k8s will help move legacy to cloud. Even if it's done with anti-pattern of putting all legacy code in one container and moving it to a cloud (lift a shit). But with that you can easily add sidecar APIs and start removing legacy code bit by bit.

Cloud will commoditize APIs:
- cloud APIs will converge
- probably there will be something like **common event format**
- competitive with added value and pricing

Low code approaches will take over:
- lack of skill will affect 90% of EU organizations by 2020
- only 15% of organizations push code weekly
- scaffolding of apps including auth and other common things

Nordcloud create even a scaffolding tool for building cloud native apps:
[How we built a roadmapper tool in just 3 hours using Amplify and CI/CD pipelines.](https://medium.com/nordcloud-engineering/how-we-built-a-roadmapper-tool-in-just-3-hours-using-amplify-and-ci-cd-pipelines-45c3826feca6)

Roles will change:
- we need builders who can connect blocks

Pubic cloud will abstract k8s:
- why you need to care for nodes?
- dev should not care for yaml
- abstraction, abstraction, abstraction
