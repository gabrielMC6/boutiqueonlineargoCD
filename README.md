# boutiqueonlineargoCD
Conecta nosso cluster Kubernetes local com um repositório Git através do ArgoCD para gerenciamento automatizado via GitOps usando Rancher Desktop.
# 🚀 GitOps na Prática: Online Boutique com ArgoCD

## 🎯 Objetivo do Projeto
Executar um conjunto de microserviços (Online Boutique) em Kubernetes local usando Rancher Desktop, controlado por GitOps com ArgoCD, a partir de um repositório público no GitHub.



## 📋 Passo a Passo da Implementação

### 1. 📁 PREPARAÇÃO DOS REPOSITÓRIOS

#### 1.1 - Fork do Repositório Oficial
- Fork criado do `GoogleCloudPlatform/microservices-demo`
- **Propósito:** Obter o arquivo `kubernetes-manifests.yaml`

#### 1.2 - Criação do Repositório GitOps
- Repositório:](https://github.com/gabrielMC6/gitops-microservices/blob/main/k8s/online-boutique.yaml)
- Estrutura conforme especificação:
- gitops-microservices/
└── k8s/
└── online-boutique.yaml


### 2. 🐮 CONFIGURAÇÃO DO RANCHER DESKTOP

#### 2.1 - Instalação e Configuração
- Download: https://rancherdesktop.io
- Configuração via interface gráfica
- Kubernetes habilitado
- Container runtime: **containerd**

#### 2.2 - Verificação do Cluster
```powershell
kubectl get nodes

https://private-user-images.githubusercontent.com/210919597/505750435-c360dbbf-f5eb-4af0-b2f2-f54c33f80653.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NjE1MDAwMzAsIm5iZiI6MTc2MTQ5OTczMCwicGF0aCI6Ii8yMTA5MTk1OTcvNTA1NzUwNDM1LWMzNjBkYmJmLWY1ZWItNGFmMC1iMmYyLWY1NGMzM2Y4MDY1My5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUxMDI2JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MTAyNlQxNzI4NTBaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT05YTM1ZDkyMmE0NWIwNWQ4OWUzNzM4ZGM5M2ZkMmJkYjZjNDExOGM1YjAxY2FiZjA0Nzg1YTAxMzc2OTc2YjY3JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.FImO1czD04Eqco860HJrpxsWsTxPgCQxSqALafVexHA
