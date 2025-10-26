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

<img width="497" height="52" alt="Image" src="https://github.com/user-attachments/assets/c360dbbf-f5eb-4af0-b2f2-f54c33f80653" />

<img width="941" height="451" alt="Image" src="https://github.com/user-attachments/assets/acda5ef2-6a39-4c21-9ac5-3f98b0db4193" />

<img width="956" height="406" alt="Image" src="https://github.com/user-attachments/assets/56f1cf60-84e7-405a-8cf2-423214c2d117" />

<img width="663" height="233" alt="Image" src="https://github.com/user-attachments/assets/f15796b6-b015-4adc-aef9-a1ad3ee39539" />

<img width="704" height="410" alt="Image" src="https://github.com/user-attachments/assets/f9339ea8-20b1-4aa7-802c-be1dff490c5a" />

<img width="943" height="391" alt="Image" src="https://github.com/user-attachments/assets/a08c43a5-cedd-4e85-9eca-c47a969b860a" />

<img width="815" height="397" alt="Image" src="https://github.com/user-attachments/assets/b7340d7b-df17-4d47-b83a-747f4fa59b4c" />
