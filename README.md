MLMonitor

Descrição:
MLMonitor é uma ferramenta robusta de monitoramento de produtos, capaz de buscar, comparar preços e gerenciar dados de múltiplas fontes automaticamente. Inclui serviço headless, caching, logging avançado e painel modular, oferecendo uma solução completa para análise de mercado.



 Funcionalidades

 Busca e comparação de produtos em múltiplas fontes
 Serviço headless para scraping seguro e eficiente
 Cache inteligente para reduzir requisições repetidas
 Logging detalhado para análise de erros e desempenho
 Testes automatizados para garantir estabilidade do sistema
 Fácil execução local e via Docker



 Estrutura do Projeto


mlmonitor/
├── .env.example           Exemplo de variáveis de ambiente
├── README.md              Documentação do projeto
├── requirements.txt       Dependências Python
├── Dockerfile             Dockerfile da aplicação principal
├── dockercompose.yml     Docker Compose para containers
├── run_local.sh           Script para rodar local
├── build_docker.sh        Script para build Docker
├── app.py                 Aplicação principal
├── search_engine.py       Módulo de busca de produtos
├── utils.py               Funções utilitárias
├── data_models.py         Modelos de dados
├── cache_manager.py       Gerenciamento de cache
├── logging_config.py      Configuração de logs
├── headless_service/      Serviço headless
│   ├── headless_server.py
│   └── Dockerfile.headless
└── tests/                 Testes automatizados
    ├── test_search_engine.py
    └── test_utils.py




 Instalação (Windows)

1. Clonar repositório


git clone https://github.com/billboy-sys/ML-Monitor.git

cd mlmonitor


2. Criar ambiente virtual


python m venv venv
venv\Scripts\activate


3. Instalar dependências


pip install upgrade pip
pip install r requirements.txt


4. Configurar variáveis de ambiente


copy .env.example .env


 Edite o .env com suas chaves e parâmetros necessários



 Uso

Rodar localmente


python app.py


Rodar headless service


python headless_service\headless_server.py


Testes


pytest tests




 Uso via Docker

1. Build da aplicação


docker build t mlmonitor .
docker build f headless_service/Dockerfile.headless t mlmonitorheadless .


2. Rodar com Docker Compose


dockercompose up




 Scripts úteis

 run_local.sh → Executa a aplicação localmente
 build_docker.sh → Build automático do Docker


 Contribuição

Contribuições são bemvindas

1. Fork o projeto
2. Crie sua branch (git checkout b feature/novafuncionalidade)
3. Commit suas alterações (git commit m 'Adiciona nova funcionalidade')
4. Push para a branch (git push origin feature/novafuncionalidade)
5. Abra um Pull Request


 Licença

MIT License © 2025
