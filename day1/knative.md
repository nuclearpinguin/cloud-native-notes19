## Serverless On Your Own Terms using Knative
_Serverless Track_

_Mark Chmarny, Serverless at Google_

Context: 
- Srverless **is more than** function
- Serverless **and** container 
- Serverless **and** Portability

#### Knative
Knative is a layer between developer-facing services and kubernetes.
Knative is OSS project. 

knative.dev | slides will be avialable

#### Knative serving
Notion of autoscaling, activates / scales workload on request. The
`kn`cli lags a little bit behind knative. Whatever way of deploy you choose (cli, yaml, G cloud run etc.) autoscaling is provided.

Deployment options (other than manual):
- CI / CD
- local build: docker build > docker push > kn service create 
- on cluster: kubectl apply
- ko, google only: ko apply
