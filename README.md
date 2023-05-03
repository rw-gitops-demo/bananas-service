# Bananas Service

This repository is one of a set providing a demonstration of a [GitOps](https://www.weave.works/technologies/gitops/) approach using [Argo CD](https://argo-cd.readthedocs.io/en/stable/) as the deployment tool and Kustomise for defining the Kubernetes manifests.
The full set of repositories in the demo are:
- [ops-manifests](https://github.com/rw-gitops-demo/ops-manifests) - the Kubernetes ops manifests, including Argo CD
- [app-manifests](https://github.com/rw-gitops-demo/app-manifests) - the Kubernetes application manifests
- [apples-service](https://github.com/rw-gitops-demo/apples-service) - an example Node.js application deployed via the GitOps workflow
- [bananas-service](https://github.com/rw-gitops-demo/bananas-service) - an example Node.js application with a traditional push deployment for comparison
- [gitops-scripts](https://github.com/rw-gitops-demo/gitops-scripts) - a set of scripts installed into the manifests repos as a git submodule

Please follow the [ops-manifests](https://github.com/rw-gitops-demo/ops-manifests) and [app-manifests](https://github.com/rw-gitops-demo/app-manifests) READMEs to set up the cluster before pushing changes to this repo.

The purpose of this repository is to provide an example microservice that uses a traditional push deployment, to allow comparison with the [apples-service](https://github.com/rw-gitops-demo/apples-service), which is deployed via the GitOps workflow.

## Setting up the demo

The example workflow will build and push a Docker image to a GitHub packages registry.
By default, this registry is private, so go to the package settings to change the visibility to public.
This first requires enabling the option to allow organisation members to create public packages in the organisation settings.
