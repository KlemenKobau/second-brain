[Awesome Kubernetes](https://github.com/rust-unofficial/awesome-rust)

## Versions
- [OKD](https://www.okd.io/)

## Learning
- [learnk8s](https://learnk8s.io/) - Kubernetes training for engineers
- [Kubernetes best practices](https://learnk8s.io/production-best-practices) - Kubernetes production best practices. A curated checklist of best practices designed to help you release to production
- [Kubernetes comic](https://cloud.google.com/kubernetes-engine/kubernetes-comic/)

## Development
- [Helm](https://github.com/helm/helm)- Helm is a tool for managing Charts. Charts are packages of pre-configured Kubernetes resources.
- [Helm dashboard](https://github.com/komodorio/helm-dashboard)- _Helm Dashboard_ is an **open-source project** which offers a UI-driven way to view the installed Helm charts, see their revision history and corresponding k8s resources.
- [Okteto](https://github.com/okteto/okteto)- A Tool to Develop Applications on Kubernetes. Okteto allows you to develop inside a container. When you run `okteto up` your Kubernetes deployment is replaced by a development container that contains your development tools (e.g. maven and jdk, or npm, python, go compiler, debuggers, etc). This development container can be any [docker image](https://okteto.com/docs/reference/development-environments/).
- [Skaffold](https://github.com/GoogleContainerTools/skaffold)- Skaffold is a command line tool that facilitates continuous development for Kubernetes applications. You can iterate on your application source code locally then deploy to local or remote Kubernetes clusters. Skaffold handles the workflow for building, pushing and deploying your application. It also provides building blocks and describe customizations for a CI/CD pipeline.

## Dev ops
- [Gerden](https://github.com/garden-io/garden)- Garden is a tool that combines rapid development, testing, and DevOps automation in one platform.

## Cluster management
- [Popeye](https://github.com/derailed/popeye)- Popeye is a utility that scans live Kubernetes cluster and reports potential issues with deployed resources and configurations.
- [Kube bench](https://github.com/aquasecurity/kube-bench)- kube-bench is a tool that checks whether Kubernetes is deployed securely by running the checks documented in the [CIS Kubernetes Benchmark](https://www.cisecurity.org/benchmark/kubernetes/).
- [Open cluster management](https://open-cluster-management.io/)

## Functionality
- [Cilium](https://github.com/cilium)- open source, cloud native solution for providing, securing, and observing network connectivity between workloads, fueled by the revolutionary Kernel technology [eBPF](https://ebpf.io/).
	- [Hubble](https://github.com/cilium/hubble) - Hubble is a fully distributed networking and security observability platform for cloud native workloads.
- [Agones](https://github.com/googleforgames/agones)- Agones is a library for hosting, running and scaling [dedicated game servers](https://en.wikipedia.org/wiki/Game_server#Dedicated_server) on [Kubernetes](https://kubernetes.io).
	- [Google for games](https://github.com/googleforgames)
- [Kube virt](https://kubevirt.io/)- KubeVirt technology addresses the needs of development teams that have adopted or want to adopt [Kubernetes](https://kubernetes.io/) but possess existing Virtual Machine-based workloads that cannot be easily containerized.
- [Dapr](https://github.com/dapr/dapr)- Dapr is a portable, serverless, event-driven runtime that makes it easy for developers to build resilient, stateless and stateful microservices that run on the cloud and edge and embraces the diversity of languages and developer frameworks.
- [Kubeflow](https://www.kubeflow.org/)- The Kubeflow project is dedicated to making deployments of machine learning (ML) workflows on Kubernetes simple, portable and scalable.

## Metrics and logs

- [Scaphandre](https://github.com/hubblo-org/scaphandre) - Scaphandre is a metrology agent dedicated to electrical power consumption metrics. The goal of the project is to permit to any company or individual to measure the power consumption of its tech services and get this data in a convenient form, sending it through any monitoring or data analysis toolchain.
- [Node Feature Discovery](https://github.com/kubernetes-sigs/node-feature-discovery) - A Kubernetes add-on for detecting hardware features and system configuration
- [Kube state metrics](https://github.com/kubernetes/kube-state-metrics) - A simple service that listens to the Kubernetes API server and generates metrics about the state of the objects. It is not focused on the health of the individual Kubernetes components, but rather on the health of the various objects inside, such as deployments, nodes and pods.
- Open telemetry
- Blog post: https://thenewstack.io/how-opentelemetry-works-with-kubernetes/
- Kubernetes monitoring: https://opentelemetry.io/docs/kubernetes/getting-started/
- Kubernetes operator: https://opentelemetry.io/docs/kubernetes/operator/

## Security
Penetration testing:
- [Kube hunter](https://github.com/aquasecurity/kube-hunter)
- [MS threat matrix](https://microsoft.github.io/Threat-Matrix-for-Kubernetes/)

Relevant: [[Containers]]