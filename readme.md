# Azure Quickstarts

These quickstarts are designed to be quick, small, and concise. Each repository focuses on 1 aspect of the feature (sometimes two or more if closely-related) so that if a quick demostration, sandbox, or refresher is needed, it can quickly be stood up with little to no configuration. Most quickstart repositories simply involve invoking `.\setup.ps1` to get it going. 

> **NOTE:** These repositories began as simple sandboxes and have grown over time. Not all may be polished or fully up-to-date. If there is a particular scenario you need, create an Issue.

## Requirements

- Powershell
- Azure CLI

### For Kubernetes/AKS-focused quickstarts:

- Kubectl
- Helm

Optionally:

- K9s
- Kubens/Kubectx

## Quickstart Repositories List

### Azure Kubernetes Service

- [**AKS Automatic**](https://github.com/ryanpeters-MSFT/aks-automatic) - Creates an AKS Automatic cluster on a custom VNet with managed Istio application routing; an optional script adds Application Gateway for Containers.
- [**Private AKS with Terraform**](https://github.com/ryanpeters-MSFT/aks-terraform) - Deploys a private, baseline-informed AKS cluster with Cilium, managed Gateway API, workload identity, and Azure Bastion access.
- [**AKS with the Terraform Azure Verified Module**](https://github.com/ryanpeters-MSFT/aks-terraform-avm) - Uses the AKS Azure Verified Module to deploy a private cluster with Cilium, managed Gateway API, multiple node pools, and Azure Bastion access.
- [**Azure Service Operator (ASO) for Kubernetes**](https://github.com/ryanpeters-MSFT/aks-azure-service-operator) - Creates an AKS cluster with workload identity, installs cert-manager and Azure Service Operator, and includes sample manifests for provisioning Azure resources from Kubernetes.
- [**Egress Routing with UDR and Azure Firewall**](https://github.com/ryanpeters-MSFT/aks-udr-egress) - Provisions an AKS cluster, Azure Firewall, and a user-defined route so selected outbound traffic is steered through the firewall while other egress keeps its default path.
- [**Static Egress Gateway**](https://github.com/ryanpeters-MSFT/aks-static-egress-gateway) - Provisions a public or private Static Egress Gateway cluster and test `curl` scripts. The private instance includes a public Linux VM jumpbox.
- [**AKS Node and Pod MTU Testing**](https://github.com/ryanpeters-MSFT/aks-mtu) - Tests cross-node traffic when a DaemonSet changes node MTU and existing pod interfaces retain a different MTU.
- [**AKS LocalDNS**](https://github.com/ryanpeters-MSFT/AksLocalDns) - Enables managed LocalDNS on AKS Standard node pools and demonstrates pod DNS resolution through the node-local cache.
- [**Custom CoreDNS on AKS**](https://github.com/ryanpeters-MSFT/aks-coredns-custom) - Deploys a separate opt-in CoreDNS service with caching, prefetching, and Prometheus metrics without modifying AKS-managed CoreDNS.
- [**Cilium mTLS on AKS**](https://github.com/ryanpeters-MSFT/aks-cilium-mesh) - Enables ACNS Cilium mTLS preview and deploys an enrolled client/server workload to demonstrate pod-to-pod encryption.
- [**AKS Advanced Container Networking Services**](https://github.com/ryanpeters-MSFT/aks-acns) - Enables ACNS network observability with Hubble, container network logs, and Azure Monitor metrics.
- [**AKS Observability**](https://github.com/ryanpeters-MSFT/aks-observability) - Sets up Container Insights, managed Prometheus, Application Insights autoinstrumentation, and ACNS for a sample workload.
- [**AKS Firewall Ingress Operator**](https://github.com/ryanpeters-MSFT/aks-firewall-ingress-operator) - Deploys an operator that watches annotated LoadBalancer services in AKS and automatically creates matching Azure Firewall DNAT rules to expose them through the firewall public IP.
- [**Azure Application Gateway for Containers**](https://github.com/ryanpeters-MSFT/aks-agc) - Creates an AKS environment for Application Gateway for Containers and includes sample Ingress and Gateway API manifests, including a weighted canary route between two workloads.
- [**AKS Managed App Routing with Private Link Service and Azure Front Door**](https://github.com/ryanpeters-MSFT/aks-app-routing-front-door) - Deploys AKS with the managed application routing add-on, exposes a private ingress through Private Link Service, and connects it to Azure Front Door for public access.
- [**AKS + Application Gateway + Azure Front Door**](https://github.com/ryanpeters-MSFT/aks-app-gateway-front-door) - Deploys AKS using a standard internal load balancer, with a regional Application Gateway, and connectivity via an Azure Front Door origin over Private Link Service. 
- [**AKS Istio App Routing Gateway API**](https://github.com/ryanpeters-MSFT/aks-istio-app-routing) - Creates an AKS cluster with App Routing, Gateway API, and Istio integration enabled, then deploys a minimal httpbin sample behind a Gateway and HTTPRoute.
- [**AKS Managed Istio with Gateway API**](https://github.com/ryanpeters-MSFT/aks-istio-gateway-api) - Deploys AKS with the managed Istio add-on and Gateway API, then exposes a sample nginx workload through an Istio-managed ingress gateway backed by a static public IP.
- [**AKS Application Network Demo**](https://github.com/ryanpeters-MSFT/aks-application-network) - Provisions two peered AKS clusters and Azure Kubernetes Application Network with Istio ambient mode to demonstrate a multi-cluster app and globally shared service.
- [**Azure Kubernetes Fleet Manager**](https://github.com/ryanpeters-MSFT/aks-fleet-manager) - Demonstrates hub and hubless fleets across four AKS clusters for update orchestration and, with a hub, multi-cluster resource placement.
- [**AKS with Managed Flux**](https://github.com/ryanpeters-MSFT/aks-flux) - Installs the managed Flux extension and reconciles a sample workload from Git onto AKS.
- [**AKS with Managed Argo CD**](https://github.com/ryanpeters-MSFT/aks-argocd-managed) - Installs the managed Argo CD extension and syncs a sample web workload from Git.
- [**AKS Dapr Actor Demo**](https://github.com/ryanpeters-MSFT/aks-dapr-actor) - Enables the Dapr extension, builds .NET actor services in Azure Container Registry, and exposes a demo API backed by Redis actor state.
- [**CloudNativePG with Node Auto-Provisioning**](https://github.com/ryanpeters-MSFT/aks-cloudnativepg) - Uses zonal AKS node auto-provisioning and a three-instance PostgreSQL cluster to observe database failover during node drift.
- [**CloudNativePG Regional Disaster Recovery**](https://github.com/ryanpeters-MSFT/aks-cloudnativepg-dr) - Deploys PostgreSQL across two peered AKS clusters with private asynchronous replication and a backup-region promotion demo.
- [**AKS Virtual Machine Node Pools**](https://github.com/ryanpeters-MSFT/aks-virtual-machine-node-pool) - Creates a mixed-size Virtual Machines node pool and demonstrates per-SKU autoscaling with a priority expander.
- [**AKS Node Auto-Provisioning**](https://github.com/ryanpeters-MSFT/aks-node-auto-provisioning) - Runs node auto-provisioning and cluster autoscaler side by side using separate pools and workloads.
- [**AKS Managed Blue-Green Node Pool Upgrade**](https://github.com/ryanpeters-MSFT/aks-blue-green-managed) - Creates an AKS cluster with a blue-green-enabled user node pool and a sample workload so you can observe, pause, resume, and roll back a managed node pool upgrade.
- [**StatefulSet Blue-Green Node Pool Upgrade**](https://github.com/ryanpeters-MSFT/aks-statefulset-upgrade) - Demonstrates how a three-replica Azure Disk-backed StatefulSet behaves during a managed blue-green node pool upgrade.
- [**AKS Node Pool Rollback Demo**](https://github.com/ryanpeters-MSFT/aks-upgrade-rollback) - Creates an AKS cluster, upgrades the control plane and node pool, and leaves you with a real rollback scenario to test current AKS node pool rollback behavior.

### APIM and AI

- [**Azure OpenAI Behind APIM**](https://github.com/ryanpeters-MSFT/ai-apim-openai) - Provisions Azure OpenAI behind API Management using APIM managed identity auth and includes direct and APIM-fronted test scripts plus example gateway policies.
- [**APIM with OpenAI and Semantic Cache**](https://github.com/ryanpeters-MSFT/ai-apim-semantic-cache) - Deploys APIM, Azure OpenAI, Redis Enterprise with RediSearch, and Application Insights to demonstrate semantic caching for chat completions with helper scripts to invoke and inspect cache hits.