## Cloud Native - effective computing at scale
_Kubernetes_

_Ignacy Kowalczyk, Google CLoud Warsaw_

_ignac@google.com_

Google always build something in an other way than others. This software engineer perspective. 
What is cloud? Storage, network and some vms that's how I saw cloud at the beginning.
What is cloud native? That means that from the beginning we prepare for running out apps and everything on a cloud.

#### History sketch: 
Google was a startup and built the infrastructure by bundling some PCs and running free. It was not the most reliable infrastructure. However, with a time they started using distributed computing. They accepted that failure is a norm and sometimes something must be built from scratch. That's what Google did:

- The Google File System ( Leung, Sanjay)
- MapReduce: Simplified Data Processing on Large Clusters (Dean)
- Bigtabe: A distributed storage system for structured data
- Large-scale cluster management at Google with Borg (managing and pulling machines, there is boglets and bogmaster)
- Some author of the paper are now working on Kubernetes. 

In 2001 the distributed computing was a design choice, today in 2019 it's necessity for Google and for many other companies.

#### Cloud natives benefits: 
- scalability
- high availability (HA)
- velocity
- cost efficiency 

Why velocity? In 2003 the average age of a company joining S&P500 was 25 year, in 2013 it was only 10 year. That shows how fast companies are maturing now.


#### Cloud native design principles:
- use redundancy - to achieve scalability and HA (replicate distributed service, prefer stateless, master election, paxos)
    - if dev understands paxos algorithm that means he knows something on distributed systems
    - failure domains in k8s: container (restarted by kubelet), node (rescheduled by node), availability zone (clusters across availability zones))
    - Warsaw team built the replication mechanism for cluster (?)
    - Beyond kubernetes: canarying, avoid cascading failures, 
- use distributed storage - storage is hard (prefere managed solutions), There is no silver bullet => read CAP Theorem !
    - You cannot optimise from all C, A , P. Spanner seems to be optimize from CAP
- use containers- to achieve velocity, ha, cost efficiency (packaging with deps, versioning, isolation, faster deployment)
    - CERN was able to use containers to pack higgs computation in container and move it to k8s.
- microservices - efficient autoscaling, fast, automated CI/CD
- introduce SRE culture (very important):
    - automate everything
    - measure everything
    - blameless postmortems
    - gradual, frequent change

SRE means there's proper monitoring, canarying process, and it’s super important to be blameless in case of fuckups. In such situations learn and improve, that will help the whole company.

#### Transformational ideas:
- distributed computing, redundancy
- containers
- orchestration: kubernetes
- service management
- SRE culture

#### QA
**What about security?** It's very important but that was not the focus of talk.

**What about multi-tenancy apps?** Hot topic in kubernetes world. Kubernetes was not very well designed for that. GKE introduced advanced metering for cost attribution. Mostly people choose instance per service to obtain multi tenancy.

**What about different implementations on k8s?** There are conformant test to check (developed in community) if the implementations are proper.

**What are google working on istio?** I am not sure if I can talk about that.
