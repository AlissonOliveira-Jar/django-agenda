# Django Agenda

Projeto de agenda feita totalmente em Django, com o intuito de explorar os recursos do framework

## Requisitos

- Python 3.12.5
- Postgresql

## Instalação Postgresql

1. Comando para instalar Postgresql:

    ```bash
    sudo apt install postgresql postgresql-contrib
    ```

2. Comando para iniciar o serviço do Postgresql:

    ```bash
    sudo service postgresql start
    ```

3. Comando para entrar no terminal do Postresql:

    ```bash
    sudo -u postgres psql
    ```

## Configuração do PostgreSQL

Certifique-se de que o PostgreSQL está instalado e em execução. Você pode criar o banco de dados e o usuário com os seguintes comandos SQL:

```bash
CREATE DATABASE your_db_name;
CREATE USER your_db_user WITH PASSWORD 'your_db_password';
ALTER ROLE your_db_user SET client_encoding TO 'utf8';
ALTER ROLE your_db_user SET default_transaction_isolation TO 'read committed';
ALTER ROLE your_db_user SET timezone TO 'UTC';
GRANT ALL PRIVILEGES ON DATABASE your_db_name TO your_db_user;
```

## Instalação do projeto

1. Clone o repositório:

    ```bash
    git clone https://github.com/AlissonOliveira-Jar/django-agenda.git
    cd seu-repositorio
    ```

2. Crie um ambiente virtual e ative-o:

    ```bash
    python -m venv venv
    source venv/bin/activate  # No Windows use `venv\Scripts\activate`
    ```

3. Instale as dependências:

    ```bash
    pip install -r requirements.txt
    ```

4. Configure o banco de dados:

    ```bash
    python manage.py makemigrations
    python manage.py migrate
    ```

5. Inicie o servidor de desenvolvimento:

    ```bash
    python manage.py runserver
    ```

## Configuração do Ambiente

1. Crie um arquivo `.env` na raiz do projeto com base no arquivo `.env.sample`:

    ```bash
    cp .env.sample .env
    ```

2. Comando para gerar SECRET_KEY:

    ```bash
    python -c "import string as s;from secrets import SystemRandom as SR;print(''.join(SR().choices(s.ascii_letters + s.digits + s.punctuation, k=64)));"
    ```

3. Preencha as variáveis de ambiente no arquivo `.env` com suas configurações:

    ```bash
    SECRET_KEY=your_secret_key
    DEBUG=True  # ou False em produção
    ALLOWED_HOSTS=localhost, 127.0.0.1  # ou seu domínio em produção

    DB_NAME=your_db_name
    DB_USER=your_db_user
    DB_PASSWORD=your_db_password
    DB_HOST=your_db_host
    DB_PORT=your_db_port
    ```

## Licença

Este projeto está licenciado sob a Licença MIT. Veja o arquivo LICENSE para mais detalhes.
