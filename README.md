# Django User Authentication Project

Este é um projeto em Python/Django que implementa um sistema de autenticação de usuários com suporte a login com e-mail e autenticação social, além de fornecer uma API para gerenciar essas funcionalidades.

## Requisitos

- Python 3.10.9
- Django 4.2.1
- django-allauth
- dj-rest-auth
- Outras dependências listadas no arquivo `requirements.txt`

## Configuração do Ambiente

1. Clone este repositório para o seu ambiente local.

2. Crie e ative um ambiente virtual:

```python3 -m venv venv```

```source venv/bin/activate```

3. Instale as dependências do projeto:

```pip install -r requirements.txt```

4. Execute as migrações do banco de dados:

```python manage.py migrate```

5. Configure as credenciais de autenticação social:

- Para autenticação com o Google:
  - Crie um projeto no Google Developers Console e obtenha as credenciais (client ID e client secret).
  - No arquivo `settings.py`, adicione as credenciais do Google no bloco `SOCIALACCOUNT_PROVIDERS` ou utilize o `config` do python-decouple e crie um arquivo .env.

- Para autenticação com o Facebook:
  - Crie um aplicativo no Facebook for Developers e obtenha as credenciais (app ID e app secret).
  - No arquivo `settings.py`, adicione as credenciais do Facebook no bloco `SOCIALACCOUNT_PROVIDERS` ou utilize o `config` do python-decouple e crie um arquivo .env.

6. Inicie o servidor de desenvolvimento:

python manage.py runserver

## Uso

### Autenticação Web

- Para acessar a página de login, vá para `http://localhost:8000/accounts/login/`.
- Para criar uma nova conta, vá para `http://localhost:8000/accounts/signup/`.
- Após fazer login, você será redirecionado para a página inicial.

### Autenticação Social

- Na página de login, você encontrará botões para fazer login usando o Google e o Facebook.

### API

- A API de autenticação está disponível em `http://localhost:8000/dj-rest-auth/`.
- Consulte a documentação da biblioteca(`dj-rest-auth`) para obter mais detalhes sobre os endpoints e as operações disponíveis.

## Licença

Este projeto está licenciado sob a licença MIT. Consulte o arquivo `LICENSE` para obter mais informações.