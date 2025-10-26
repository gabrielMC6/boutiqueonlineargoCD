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

<img width="497" height="52" alt="505750435-c360dbbf-f5eb-4af0-b2f2-f54c33f80653" src="https://github.com/user-attachments/assets/1b1cec58-a058-4bb4-a29d-e24d0b77e635" />
<img width="941" height="451" alt="505748366-acda5ef2-6a39-4c21-9ac5-3f98b0db4193" src="https://github.com/user-attachments/assets/4ab24f32-fa33-48dd-8b5a-707dee059702" />
<img width="956" height="406" alt="505747851-56f1cf60-84e7-405a-8cf2-423214c2d117" src="https://github.com/user-attachments/assets/682fa3f9-4c3b-4c7b-8bde-c2e8dd45d3a3" />
