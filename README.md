# API Transporte Urbano

A API Transporte Urbano é um sistema desenvolvido em Python/Flask que fornece informações em tempo real sobre trânsito e transportes públicos.
Integra dados do Google Maps (tráfego) e da SPTrans (posição e status de ônibus).

## Estrutura principal
- rotas.py → define os endpoints da API, como /traffic.
- servicos/google_maps.py → conecta com a API do Google Maps para obter congestionamento e velocidade média.
- servicos/sptrans.py → conecta com a API da SPTrans para obter posição dos ônibus e status das linhas.
- configuracao.py → centraliza as chaves de API e configurações.
- .env → guarda suas credenciais (GOOGLE_API_KEY, SPTRANS_TOKEN).
- Dockerfile → garante que a API rode em qualquer ambiente.
- docker-compose.yml → útil se quiser adicionar banco de dados ou cache (Redis).

## Instalação rápida
1. git clone https://github.com/gabriele-dias/api-transporte-urbano.git
2. python -m venv venv && source venv/bin/activate
3. pip install -r requirements.txt
4. Configure .env com suas chaves e rode flask run.
