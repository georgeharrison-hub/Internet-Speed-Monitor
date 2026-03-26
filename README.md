# Internet Speed Monitor

Um aplicativo full-stack para monitorar a velocidade da internet utilizando o serviço do Speedtest.

## 🚀 Tecnologias

### Backend
- **Node.js** - Runtime JavaScript
- **Express** - Framework web
- **Mongoose** - ODM para MongoDB
- **Jest** - Framework de testes

### Frontend
- **React 17** - Biblioteca UI
- **Create React App** - Build tooling

### Outros
- **Speedtest CLI** - Ferramenta de medição de velocidade

## 📋 Pré-requisitos

- Node.js (v14 ou superior)
- npm ou yarn
- Speedtest CLI instalado ([instruções](https://www.speedtest.net/apps/cli))
- MongoDB (opcional, para persistência de dados)

## 🛠️ Instalação

1. Clone o repositório:
```bash
git clone <repository-url>
cd Internet-Speed-Monitor
```

2. Instale as dependências do backend:
```bash
npm install
```

3. Instale as dependências do frontend:
```bash
cd client
npm install
cd ..
```

## ▶️ Como Rodar

### Desenvolvimento (Backend + Frontend)
```bash
npm run dev
```

### Apenas Backend
```bash
npm run server
```
O servidor rodará em `http://localhost:5000`

### Apenas Frontend
```bash
npm run client
```
O frontend rodará em `http://localhost:3000`

## 📡 API Endpoints

| Método | Endpoint | Descrição |
|--------|----------|-----------|
| `GET` | `/api/v1/speedtest` | Executa o teste de velocidade e retorna os resultados em JSON |
| `GET` | `/api/v1/mensagem` | Endpoint de health check |

### Exemplo de Resposta
```json
{
  "download": 100.5,
  "upload": 50.2,
  "ping": 20.5,
  ...
}
```

## 🧪 Testes

Execute os testes com:
```bash
npm test
```

## 📁 Estrutura do Projeto

```
Internet-Speed-Monitor/
├── server.js                 # Entry point do backend
├── model/                    # Modelos de dados
│   └── speedtest.js          # Execução do Speedtest CLI
├── api/                      # Camada de API
│   ├── controller/           # Controladores
│   │   └── speedtest-controller.js
│   └── router/               # Rotas
│       └── speedtest-router.js
├── client/                   # Frontend React
│   ├── public/
│   └── src/
├── __tests__/                # Testes Jest
│   ├── config.spec.js
│   └── speedtest.spec.js
└── package.json
```

## 📄 Licença

Este projeto está licenciado sob a MIT License - veja o arquivo [LICENSE](LICENSE) para detalhes.
