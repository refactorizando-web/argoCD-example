# ArgoCD Example

This is a Helm Chart to deploy a nginx image in Kubernetes with ArgoCD.

Argo CD is a Kubernetes-native continuous deployment (CD) tool. 
Unlike external CD tools that only enable push-based deployments, 
Argo CD can pull updated code from Git repositories and deploy it 
directly to Kubernetes resources.

If you want more information about how to use ArgoCD you can take a look into 
https://refactorizando.com/desplegando-aplicaciones-argocd-kubernetes

# How is it deployed in Kubernetes?

After configured your cluster and installed argocd as a client you 
can deploy this example with the next command:

    argocd app create jpastreamer --repo https://github.com/refactorizando-web/argoCD-example.git --path argocd-example --dest-server https://kubernetes.default.svc --dest-namespace default

