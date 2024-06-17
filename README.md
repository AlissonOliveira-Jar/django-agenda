# Iniciar o projeto Django

```bash
python -m venv venv
. venv/bin/activate  # No Windows use: venv\Scripts\activate
pip install -r requirements.txt
```

## Configurar o git

```bash
git config --global user.name 'Seu nome'
git config --global user.email 'seu_email@gmail.com'
git config --global init.defaultBranch main
# Configure o .gitignore
git init
git add .
git commit -m 'Mensagem'
git remote add origin URL_DO_GIT
```

## Migrando a base de dados do Django

```bash
python manage.py makemigrations
python manage.py migrate
```

## Criando e modificando a senha de um super usuário Django

```bash
python manage.py createsuperuser
python manage.py changepassword USERNAME
```
