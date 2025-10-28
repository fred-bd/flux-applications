# flux-applications

Configurations for deploying applications using **Flux** (GitOps)  
This repository contains application manifests, overlays and kustomizations to be used with Flux for automated deployments.

---

## 🚀 Table of Contents

- [Overview](#overview)  
- [Structure](#structure)  
- [Technologies & Tools](#technologies--tools)  
- [Getting Started](#getting-started)  
  - [Prerequisites](#prerequisites)  
  - [Setup](#setup)  
  - [Deploying](#deploying)  
- [Usage Examples](#usage-examples)  
- [Best Practices & Guidelines](#best-practices--guidelines)  
- [Contributing](#contributing)  
- [License](#license)  

---

## 📌 Overview

This repository stores the declarative configuration files for multiple applications that are deployed and managed via **Flux** in a GitOps workflow.  
It enables reproducible, versioned, and auditable deployments of application components (manifests, overlays, kustomizations) across environments.

---

## 🧱 Structure

Here’s a high-level view of the folder layout:


- `components/` — contains base Kubernetes manifests and common resources  
- `overlays/` — contains environment-specific variations / patches  
- (You can expand this, por exemplo para `flux/`, `apps/`, etc, conforme o repositório crescer)

---

## 🛠 Technologies & Tools

- **Flux / GitOps** — for continuous deployment and synchronization  
- **Kustomize / overlays** — to customize manifests per environment  
- **Kubernetes** — target cluster environment  
- (If applicable) other tools you integrate (e.g. cert-manager, external-secrets, etc.)  
- Git / versioning  

---

## 🧭 Getting Started

### Prerequisites

Before you begin, ensure you have:

- A Kubernetes cluster  
- [Flux v2 CLI](https://fluxcd.io) installed  
- `kubectl` with context pointing to your cluster  
- Permissions to apply manifests on the cluster  

### Setup

1. Clone this repository:  
   ```bash
   git clone https://github.com/fred-bd/flux-applications.git
   cd flux-applications

### All Tools configured
- cert-manager
- cilium
- external-secrets
- flagger
- flagger-grafana
- flagger-loadtester
- grafana
- istio
- istio-ambient
- k8s-gateway-crds
- kiali
- kubernetes-dashboard
- kustomization.yaml
- kyverno
- metallb
- netshoot
- nginx
- podinfo
- podinfo2
- prometheus
- repository.yaml
- secret-replicator
- tools.yaml

### Generate a token to use on kube-dashboard

```sh
kubectl -n kube-dashboard create token admin-user --duration=999999h
```