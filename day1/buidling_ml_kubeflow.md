## Building Machine Learning with Kubeflow and serving them with Kfserving.
_Serverless Track_

_Wojciech Barczyński_

_hypatos.ai | SMACC.io_

How does the engineering part looks like in data science field?
Wojciech saw some mess in startups and decided to become system architect. In MAchine Learning it's quite popular to test in production because they never know which model will be better. That's why they use AB testing.

It's quite easy to observe that ML pipeline look like CI/ CD ones. Everybody hates the CI/CD (really?). The same feeling is shared by guys in data science. Kubeflow helps to ease the pain. One to rule them all. 

Kubeflow will become a standard in data science as kubernetes became standard in normal delivery.
Kubeflow focuses on:
- scalability
- composition
- portability
- enabling ML(dev)ops culture

Kubeflow allows to use:
- pipelines
- notebooks
- artifacts and metadat
- more

Pipelines are the heart of the Kubeflow. This includes preparing, training, analysing and deploying. 
The component of the pipelines are kube jobs, meaning that at a single moment the system  tries to run the least number of instances as possible.
In Kubeflow you can create notebooks and new jupyter servers. That makes the work of DS guy same as it is.
The kubeflow jobs generate metadata that can be used in tensorboard, confusion matrix etc. 
The params of the Jupyter servers can be set for example CPU/ GPU numbers.

#### YAML vs Python SDK
Instead of defining pipelines in YAML (ex. ARGO)  data science guys can do this in python:
[Introduction to the Pipelines SDK \| Kubeflow](https://www.kubeflow.org/docs/pipelines/sdk/sdk-overview/)

#### How Kubeflow helps to deploy the model?
How to serve a model? 
- Modelservers - docker containers that serves models (TFserving, PyTorchServing etc)
- seldom.io - mote comples uscases, when you have to wrap your model in Flask or gunicorn
- kfserving - serving models in cloud native way, yaml with model type and path to model on bucket

#### QA

People think that defining pipelines in YAML is awesome 👀

**Can you schedule pipelines?** Kubeflow allows you to schedule pipelines using calendar object in argo yaml.
