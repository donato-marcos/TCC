nginx-server/
├── ansible.cfg                     # Configurações do Ansible
├── inventory/
│   ├── group_vars/
│   │   ├── all.yml                 # Variáveis globais
│   │   └── web_nginx_service.yml   # Variáveis específicas do Nginx
│   ├── host_vars/
│   │   ├── web_nginx_host1.yml     # Variáveis por host
│   │   └── web_nginx_host2.yml
│   ├── production                  # Inventário de produção
│   ├── staging                     # Inventário de staging
│   └── testing                     # Inventário de teste
├── playbooks/
│   ├── all.yml                     # Playbook para todos os hosts
│   └── web_nginx.yml               # Playbook específico para Nginx
├── roles/
│   ├── common/                     # Role com configurações comuns
│   └── web_nginx/                  # Role específica para Nginx
│       ├── files/                    # Arquivos estáticos
│       │   ├── atv1_web/               # Site 1
│       │   ├── site1/                  # Site 2
│       │   └── site2/                  # Site 3
│       ├── tasks/                    # Tarefas de configuração
│       │   ├── main.yml                # Arquivo principal de tasks
│       │   ├── cron.yml                # Configurações de cron jobs
│       │   ├── nginx.yml               # Instalação Nginx
│       │   ├── firewall.yml            # Configuração de firewall
│       │   └── selinux.yml             # Configuração SELinux
│       └── templates/                # Templates Jinja2
│           └── site.conf.j2            # Template de configuração do Nginx
└── vars/                           # Variáveis globais adicionais
    └── main.yml
