# DevOpsGram

Um projeto de exemplo desenvolvido em Python com Flask, projetado para execução em Kubernetes ou OpenShift com funcionalidades básicas de autenticação e cadastro de usuários.

## 📋 Descrição

O DevOpsGram é uma aplicação web que demonstra:
- Autenticação de usuários (login/cadastro)
- CI/CD com GitHub Actions
- Implantação em Kubernetes/OpenShift
- Boas práticas de DevOps

## ✨ Funcionalidades

- **Sistema de Autenticação**:
  - Login com credenciais
  - Cadastro de novos usuários
- **Pipeline Automatizada**:
  - Build, teste e deploy automatizados
- **Pronto para Cloud**:
  - Configurações para Kubernetes/OpenShift

## 🛠️ Tecnologias

- Python 3.9+
- Flask
- Kubernetes/OpenShift
- GitHub Actions
- Docker

## 🚀 Pré-requisitos

- Python 3.9+
- Docker
- Acesso a cluster Kubernetes/OpenShift
- kubectl/oc CLI

## ⚙️ Configuração

1. Clone o repositório:
   ```bash
   git clone https://github.com/felipecezaar/DevOpsGram.git
   cd DevOpsGram
   ```

2. Crie um ambiente virtual (recomendado):
   ```bash
   python -m venv venv
   source venv/bin/activate  # Linux/MacOS
   # ou
   venv\Scripts\activate      # Windows
   ```

3. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```

## 🏃 Execução Local

```bash
flask run
```
Acesse: http://localhost:5000

## 🔧 Pipeline CI/CD

O workflow `.github/workflows/build-test-deploy.yml` automatiza:
1. Build da imagem Docker
2. Execução dos testes
3. Deploy no cluster (configure seus secrets no GitHub)

## 🐳 Construção Docker

```bash
docker build -t devopsgram:latest .
```

## ☸️ Implantação

### Kubernetes/OpenShift

```bash
kubectl apply -f k8s/
# ou
oc apply -f ocp/
```

Acesse via rota exposta pelo serviço.

## 📂 Estrutura do Projeto

```
DevOpsGram/
├── .github/
│   ├── pull_request_template.md  # Template para PRs
│   └── workflows/
│       └── build-test-deploy.yml # Pipeline CI/CD
├── ocp/                         # Manifestos K8s/OCP
│   ├── deployment.yaml
│   ├── route.yaml
│   └── service.yaml
├── templates/                   # Telas da aplicação
│   ├── index.html
│   ├── login.html
│   └── signup.html
├── tests/                       # Testes automatizados
│   └── test_app.py
├── app.py                       # Aplicação Flask
├── Dockerfile                   # Configuração Docker
├── README.md                    # Este arquivo
└── requirements.txt             # Dependências Python
```

## 🧪 Testes

Execute os testes com:
```bash
python -m pytest tests/
```

## 🤝 Contribuição

1. Fork o projeto
2. Crie sua branch (`git checkout -b feature/foo`)
3. Commit suas mudanças (`git commit -am 'Add some foo'`)
4. Push para a branch (`git push origin feature/foo`)
5. Abra um Pull Request

## 📄 Licença

MIT - Veja [LICENSE](LICENSE) para detalhes.