
## Attacking Kubernetes
_Kubernetes Track_

_Nidaa Saffarini_

Why k8s is a target? There are no special purposes that those already common:
- steal/leak data
- disrupt services
- money 💸

Audience when asked "who think that k8s increases security" was silent. But it's not totally true. There are pros and cons but that depends on how dev-ops configure k8s. 
Kubernetes have a lot more ways to access the interior those include:
- users apps
- images
- dev tools
- hooks and other integrations etc.

There's also a lot of communication between nodes and pods that could be disturbed. More channels means more possibilities for hackers.

What k8s do for security:
 - pod security policy
 - authentication and authorization
 - RBAC
 - data encryption


and what it doesn't:
 - k8s can control plenty of things
 - network security
 - host security - k8s does nothing to protect host
 - vulnerabilities in containers

K8s can face the same vulnerabilities as host machines including those that are related to kernels.

Using GitHub access one can get your k8s yamls and that may help the attacker understand how your infrastructure works.

Tips:
- Check [GitHub - aquasecurity/kube-hunter: Hunt for security weaknesses in Kubernetes clusters](https://github.com/aquasecurity/kube-hunter)
- use minimal base docker images
- enforce resource quota (CPU, Memory, Storage)
- scan docker images for vulnerabilities
- use kube-bench to see k8s benchmarks
- monitor and logs