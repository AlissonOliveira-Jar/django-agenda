# Django Agenda

Projeto de agenda feita totalmente em Django, com o intuito de explorar os recursos do framework

## Requisitos

- Python 3.12.5

## Instalação

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

## Licença

Este projeto está licenciado sob a Licença MIT. Veja o arquivo LICENSE para mais detalhes.
