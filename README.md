# API Transporte Urbano
<<<<<<< HEAD
=======

A **API Transporte Urbano** é um sistema desenvolvido em **Python/Flask** que fornece informações em tempo real sobre **trânsito** e **transportes públicos**.  
Ela integra dados de fontes externas como o **Google Maps Traffic API** (congestionamento e velocidade média) e a **API da SPTrans** (posição e status de linhas de ônibus em São Paulo).

---

## 🎯 Objetivo
- Centralizar informações de mobilidade urbana em um único serviço.  
- Permitir que aplicativos móveis consumam dados atualizados via endpoints REST.  
- Apoiar usuários na tomada de decisão sobre deslocamentos, reduzindo tempo perdido em congestionamentos e atrasos.  

---

## 📂 Estrutura do projeto
api-transporte-urbano/
├── app/
│   ├── init.py
│   ├── rotas.py
│   ├── servicos/
│   │   ├── google_maps.py
│   │   └── sptrans.py
│   └── configuracao.py
├── requirements.txt
├── Dockerfile
├── docker-compose.yml
├── .env
└── README.md

Código

---

## 🔧 Instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/gabriele-dias/api-transporte-urbano.git
   cd api-transporte-urbano
Crie um ambiente virtual e instale as dependências:

bash
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows
pip install -r requirements.txt
Configure suas chaves de API no arquivo .env:

Código
GOOGLE_API_KEY=SUA_CHAVE_DO_GOOGLE
SPTRANS_TOKEN=SEU_TOKEN_DA_SPTRANS
🚀 Uso
Execute a aplicação:

bash
flask run
A API estará disponível em:

Código
http://localhost:5000
📌 Endpoints
GET /traffic
Retorna dados de trânsito e transportes públicos.

Exemplo de requisição:

bash
curl "http://localhost:5000/traffic?origem=-23.55,-46.63&destino=-23.56,-46.64"
Resposta:

json
{
  "origem": "-23.55,-46.63",
  "destino": "-23.56,-46.64",
  "distancia": "2.1 km",
  "tempo_estimado": "8 mins",
  "tempo_trafego": "12 mins",
  "public_transport": [...]
}
📊 Benefícios
Centralização: o app mobile consome apenas esta API.

Escalabilidade: pode ser expandida para outras cidades e serviços.

Interdisciplinaridade

Interdisciplinaridade: conecta TI, urbanismo e mobilidade sustentável.
>>>>>>> 28e4864975dfa53fd8bfab43648f84ed6de8ce69
