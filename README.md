# DevOpsGram

An example project developed in Python with Flask, designed to run on Kubernetes or OpenShift with basic user authentication and registration features.

Note: English version of the documentation. Portuguese version and Italian version are available right after this version.

## 📋 Description

DevOpsGram is a web application that demonstrates:
- User authentication (login/registration)
- CI/CD with GitHub Actions
- Deployment on Kubernetes/OpenShift
- DevOps best practices

## ✨ Features

- **Authentication System**:
  - Login with credentials
  - New user registration
- **Automated Pipeline**:
  - Automated build, test, and deploy
- **Cloud Ready**:
  - Configurations for Kubernetes/OpenShift

## 🛠️ Technologies

- Python 3.9+
- Flask
- Kubernetes/OpenShift
- GitHub Actions
- Docker

## 🚀 Prerequisites

- Python 3.9+
- Docker
- Access to a Kubernetes/OpenShift cluster
- kubectl/oc CLI

## ⚙️ Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/felipecezaar/DevOpsGram.git
   cd DevOpsGram
   ```

2. Create a virtual environment (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # Linux/MacOS
   # or
   venv\Scripts\activate      # Windows
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## 🏃 Local Run

```bash
flask run
```
Access: http://localhost:5000

## 🔧 CI/CD Pipeline

The workflow `.github/workflows/build-test-deploy.yml` automates:
1. Docker image build
2. Running tests
3. Cluster deployment (configure your GitHub secrets)

## 🐳 Docker Build

```bash
docker build -t devopsgram:latest .
```

## ☸️ Deployment

### Kubernetes/OpenShift

```bash
kubectl apply -f k8s/
# or
oc apply -f ocp/
```

Access it via the route exposed by the service.

## 📂 Project Structure

```
DevOpsGram/
├── .github/
│   ├── pull_request_template.md  # PR template
│   └── workflows/
│       └── build-test-deploy.yml # CI/CD pipeline
├── ocp/                          # K8s/OCP manifests
│   ├── deployment.yaml
│   ├── route.yaml
│   └── service.yaml
├── templates/                    # Application views
│   ├── index.html
│   ├── login.html
│   └── signup.html
├── tests/                        # Automated tests
│   └── test_app.py
├── app.py                        # Flask application
├── Dockerfile                    # Docker configuration
├── README.md                     # This file
└── requirements.txt              # Python dependencies
```

## 🧪 Tests

Run the tests with:
```bash
python -m pytest tests/
```

## 🤝 Contributing

1. Fork the project
2. Create your branch (`git checkout -b feature/foo`)
3. Commit your changes (`git commit -am 'Add some foo'`)
4. Push to the branch (`git push origin feature/foo`)
5. Open a Pull Request

## 📄 License

MIT - See [LICENSE](LICENSE) for details.


#######################################################################################


# DevOpsGram

Um projeto de exemplo desenvolvido em Python com Flask, projetado para execução em Kubernetes ou OpenShift com funcionalidades básicas de autenticação e cadastro de usuários.

Nota: Versão da documentação em português.

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
├── ocp/                          # Manifestos K8s/OCP
│   ├── deployment.yaml
│   ├── route.yaml
│   └── service.yaml
├── templates/                    # Telas da aplicação
│   ├── index.html
│   ├── login.html
│   └── signup.html
├── tests/                        # Testes automatizados
│   └── test_app.py
├── app.py                        # Aplicação Flask
├── Dockerfile                    # Configuração Docker
├── README.md                     # Este arquivo
└── requirements.txt              # Dependências Python
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


#######################################################################################


# DevOpsGram

Un progetto di esempio sviluppato in Python con Flask, progettato per essere eseguito su Kubernetes o OpenShift con funzionalità base di autenticazione e registrazione utente.

Nota: versione della documentazione in italiano.

## 📋 Descrizione

DevOpsGram è un'applicazione web che dimostra:
- Autenticazione utente (login/registrazione)
- CI/CD con GitHub Actions
- Deployment su Kubernetes/OpenShift
- Best practice DevOps

## ✨ Funzionalità

- **Sistema di Autenticazione**:
  - Login con credenziali
  - Registrazione nuovi utenti
- **Pipeline Automatizzata**:
  - Build, test e deploy automatizzati
- **Pronto per il Cloud**:
  - Configurazioni per Kubernetes/OpenShift

## 🛠️ Tecnologie

- Python 3.9+
- Flask
- Kubernetes/OpenShift
- GitHub Actions
- Docker

## 🚀 Prerequisiti

- Python 3.9+
- Docker
- Accesso a un cluster Kubernetes/OpenShift
- CLI kubectl/oc

## ⚙️ Configurazione

1. Clona il repository:
   ```bash
   git clone https://github.com/felipecezaar/DevOpsGram.git
   cd DevOpsGram
   ```

2. Crea un ambiente virtuale (consigliato):
   ```bash
   python -m venv venv
   source venv/bin/activate  # Linux/MacOS
   # oppure
   venv\Scripts\activate      # Windows
   ```

3. Installa le dipendenze:
   ```bash
   pip install -r requirements.txt
   ```

## 🏃 Esecuzione Locale

```bash
flask run
```
Accesso: http://localhost:5000

## 🔧 Pipeline CI/CD

Il workflow `.github/workflows/build-test-deploy.yml` automatizza:
1. Build dell'immagine Docker
2. Esecuzione dei test
3. Deployment sul cluster (configura i tuoi GitHub secrets)

## 🐳 Build Docker

```bash
docker build -t devopsgram:latest .
```

## ☸️ Deployment

### Kubernetes/OpenShift

```bash
kubectl apply -f k8s/
# oppure
oc apply -f ocp/
```

Accedi tramite la route esposta dal servizio.

## 📂 Struttura del Progetto

```
DevOpsGram/
├── .github/
│   ├── pull_request_template.md  # Template per le PR
│   └── workflows/
│       └── build-test-deploy.yml # Pipeline CI/CD
├── ocp/                          # Manifest per K8s/OCP
│   ├── deployment.yaml
│   ├── route.yaml
│   └── service.yaml
├── templates/                    # Viste dell'applicazione
│   ├── index.html
│   ├── login.html
│   └── signup.html
├── tests/                        # Test automatizzati
│   └── test_app.py
├── app.py                        # Applicazione Flask
├── Dockerfile                    # Configurazione Docker
├── README.md                     # Questo file
└── requirements.txt              # Dipendenze Python
```

## 🧪 Test

Esegui i test con:
```bash
python -m pytest tests/
```

## 🤝 Contributi

1. Fai un fork del progetto
2. Crea il tuo branch (`git checkout -b feature/foo`)
3. Commit delle tue modifiche (`git commit -am 'Aggiungi qualche foo'`)
4. Push sul branch (`git push origin feature/foo`)
5. Apri una Pull Request

## 📄 Licenza

MIT - Vedi [LICENSE](LICENSE) per i dettagli.
