## Using GitHub Action Workflow  `kustomize`

### Workflow `.github/workflows/deploy.yaml`

This Workflow will need to be triggered manually after merging Pull Requests.

Pull Requests will be created when you build container images in Frontend and Backend Repositories
- https://github.com/Faust0506007/frontEndToDoApp/pulls
- https://github.com/Faust0506007/backEndToDoApp/pulls

Steps:

1. Authenticate to GCP Project using Workload Identity Feature
2. Authorize to target GKE Cluster
3. Install Kustomize
4. Apply Kubernetes Manifest Files. Replace value using `sed`


## Migration to Helm Chart
Note: IMO, Kustomize's template feature does not support provide variables dynamically.

That's why I used `sed` command to replace values in Manifest Files as a workaround.

I've decided to use Helm Chart with ArgoCD.



