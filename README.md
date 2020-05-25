# cis-istio-integration
**Integration of F5 CIS Ingress Controller with Istio Service Mesh for Kubernetes and Openshift**

Service Mesh is used for communication between Micro-Services usually with in a kubernetes cluster or sometimes across the
clusters as well. Service Mesh provides alot of features like security, routing, accessibility betweem the services using 
the Mesh Layer. Istio is an Opensource ServiceMesh solution for Kubernetes and Openshift Container Orchestration Platforms.

Now, What if one of your services in the Mesh Layer wants to communicate outside the Mesh? istio-ingressgateway is a solution
when you can expose it to a type LoadBalancer. 
This brings two important considerations
- What if you are using a on-prem kubernetes solution.
- LoadBalancer vs Ingress Controller.

Ingress Controllers are far matured and better solutions compared to external LoadBalancers. F5 CIS ingress Controller supports
various features like security, advanced load balancing techniques, WAF, DDOS, TLS and more.

This Repo will make use of istio's bookinfo application for deploying pods, services, virtual service and gateway. This Repo
does not cover the installation of istio.

Please refer to istio website for setup, installation and configuration of bookinfo-application.
- https://istio.io/docs/setup/getting-started/

I would strongly recommend to look at the architecture of bookinfo-application before you get started.
- https://istio.io/docs/examples/bookinfo/

# Note
**You need to modify the istio-ingressgateway service present in istio-system namespace from type LoadBalancer to 
type Nodeport**
