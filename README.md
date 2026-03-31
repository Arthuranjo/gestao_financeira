# gestao_financeira

#teste


faturamento_dashboard/
│
├── manage.py
│
├── core/                          # Configuração do projeto Django
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
│
├── apps/                          # Apps do sistema
│   ├── __init__.py
│
│   ├── usuarios/                  # Login e autenticação
│   │   ├── migrations/
│   │   ├── __init__.py
│   │   ├── models.py
│   │   ├── views.py
│   │   ├── forms.py
│   │   ├── urls.py
│   │   ├── admin.py
│   │   ├── services.py
│   │   └── tests.py
│   │
│   ├── vendas/                    # Dados principais de vendas
│   │   ├── migrations/
│   │   ├── __init__.py
│   │   ├── models.py
│   │   ├── views.py
│   │   ├── forms.py
│   │   ├── urls.py
│   │   ├── admin.py
│   │   ├── services.py           # regras de negócio (faturamento, ticket médio)
│   │   ├── selectors.py          # consultas (filtros, agregações)
│   │   └── tests.py
│   │
│   ├── produtos/                 # Produtos (inicialmente visual)
│   │   ├── migrations/
│   │   ├── __init__.py
│   │   ├── models.py
│   │   ├── views.py
│   │   ├── forms.py
│   │   ├── urls.py
│   │   ├── admin.py
│   │   └── tests.py
│   │
│   ├── dashboard/                # Lógica de exibição do dashboard
│   │   ├── migrations/
│   │   ├── __init__.py
│   │   ├── views.py
│   │   ├── urls.py
│   │   ├── services.py           # métricas e dados para gráficos
│   │   ├── admin.py
│   │   └── tests.py
│   │
│   ├── importacoes/              # 🔥 MÓDULO PRINCIPAL DO PROJETO
│   │   ├── migrations/
│   │   ├── __init__.py
│   │   ├── models.py             # controle de uploads
│   │   ├── views.py              # tela de upload
│   │   ├── forms.py              # form de upload CSV
│   │   ├── urls.py
│   │   ├── admin.py
│   │   ├── services.py           # orquestra importação
│   │   │
│   │   ├── parsers/              # 🔥 parsing por canal
│   │   │   ├── __init__.py
│   │   │   ├── base.py           # classe base
│   │   │   ├── mercado_livre.py
│   │   │   ├── tiktok.py
│   │   │   ├── shopee.py
│   │   │
│   │   └── tests.py
│
├── utils/                        # funções globais (fora dos apps)
│   ├── __init__.py
│   ├── helpers.py
│   ├── validators.py
│   └── constants.py
│
├── templates/                   # HTML global
│   ├── base.html
│   │
│   ├── components/
│   │   ├── sidebar.html
│   │   ├── navbar.html
│   │   └── alerts.html
│   │
│   ├── usuarios/
│   │   └── login.html
│   │
│   ├── dashboard/
│   │   ├── index.html
│   │   └── relatorios.html
│   │
│   ├── vendas/
│   │   ├── lista.html
│   │   └── form.html
│   │
│   ├── importacoes/
│   │   ├── upload.html
│   │   ├── resultado.html
│   │   └── erros.html
│   │
│   └── produtos/
│       ├── lista.html
│       └── form.html
│
├── static/                      # Arquivos estáticos
│   ├── css/
│   │   ├── style.css
│   │   └── dashboard.css
│   │
│   ├── js/
│   │   ├── main.js
│   │   ├── charts.js
│   │   └── upload.js
│   │
│   └── img/
│
├── media/                       # uploads de planilhas
│
├── samples/                     # exemplos de CSV (opcional, mas MUITO útil)
│   ├── mercado_livre.csv
│   ├── tiktok.csv
│   └── shopee.csv
│
├── .env
├── .gitignore
├── requirements.txt
└── README.md