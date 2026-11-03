# gitops-practice

Practice files for the Argo CD and Monitoring tracks on [kwamib.dev](https://kwamib.dev/resources/argocd).

A local Kubernetes cluster, made with kind in Docker on your own computer, and
Argo CD inside it, keeping the cluster matching this repository.

    kind create cluster --name gitops --config kind-gitops.yaml
    kubectl get nodes

When you're done for the day, `docker stop gitops-control-plane gitops-worker`
pauses the cluster and `docker start gitops-control-plane gitops-worker` brings it back.
`kind delete cluster --name gitops` deletes it, and the lessons rebuild it.
