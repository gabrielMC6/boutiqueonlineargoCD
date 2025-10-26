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
NAME              STATUS   ROLES                  AGE    VERSION
desktop-086q4jn   Ready    control-plane,master   4d1h   v1.33.5+k3s1


3. ⚙️ Instalação e Configuração do ArgoCD
3.1 Instalação no Cluster
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

3.2 Acesso à Interface Web
kubectl port-forward svc/argocd-server -n argocd 8080:443


Acesse: https://localhost:8080

Ignore o aviso de certificado (ambiente local)

3.3 Obtenção da Senha Admin
$password = kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}"
[System.Text.Encoding]::UTF8.GetString([System.Convert]::FromBase64String($password))

3.4 Login no ArgoCD

Usuário: admin

Senha: (valor obtido no passo anterior)

4. 🔄 Configuração do GitOps no ArgoCD

Application: online-boutique
Repositório: https://github.com/gabrielMC6/gitops-microservices

Path: k8s
Cluster: https://kubernetes.default.svc
Namespace: default

5. 🔁 Sincronização

Sincronização manual com prune habilitado

Auto-create namespace habilitado

Aplicação: Synced ✅ e Healthy 💚

6. 🌐 Acesso à Aplicação
Frontend
kubectl port-forward svc/frontend 8081:80


Acesse: http://localhost:8081

ArgoCD

Interface: https://localhost:8080
