# gestao_financeira

#teste


arquitetura das pastas:
faturamento_dashboard/
│
├── manage.py
│
├── core/                          # Configurações do projeto
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
│
├── apps/                          # Apps do sistema
│   ├── __init__.py
│
│   ├── usuarios/
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
│   ├── vendas/
│   │   ├── migrations/
│   │   ├── __init__.py
│   │   ├── models.py
│   │   ├── views.py
│   │   ├── forms.py
│   │   ├── urls.py
│   │   ├── admin.py
│   │   ├── services.py           # cálculos de faturamento
│   │   └── tests.py
│   │
│   ├── produtos/
│   │   ├── migrations/
│   │   ├── __init__.py
│   │   ├── models.py
│   │   ├── views.py
│   │   ├── forms.py
│   │   ├── urls.py
│   │   ├── admin.py
│   │   └── tests.py
│   │
│   ├── dashboard/
│   │   ├── migrations/
│   │   ├── __init__.py
│   │   ├── models.py            # pode ficar vazio
│   │   ├── views.py
│   │   ├── urls.py
│   │   ├── services.py          # métricas e gráficos
│   │   ├── admin.py
│   │   └── tests.py
│   │
│   └── utils/                   # utilitários globais
│       ├── __init__.py
│       ├── helpers.py
│       └── validators.py
│
├── templates/                   # HTML global
│   ├── base.html
│   │
│   ├── components/
│   │   ├── sidebar.html        # menu lateral
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
│   │   ├── form.html
│   │   └── upload.html
│   │
│   └── produtos/
│       ├── lista.html
│       └── form.html
│
├── static/                      # Arquivos estáticos
│   ├── css/
│   │   └── style.css
│   │
│   ├── js/
│   │   ├── main.js
│   │   └── charts.js           # gráficos (Chart.js)
│   │
│   └── img/
│
├── media/                       # Uploads (planilhas)
│
├── .env                         # variáveis de ambiente
├── .gitignore
├── requirements.txt
└── README.md
