# Primeira API utilizando Django

## Descrição
 API RESTful criada utilizando Django REST framework e PostgreSQL.
 
## O que foi utilizado nesse projeto
 - Python 3.11
 - Django 4.2
 - Django REST framework 3.14.0
 - PostgreSQL

## Passos que foi utilizado para a criação desse projeto:
 1. Instale o venv(se não tiver instalado):
  ```bash
pip install venv
```
 2. no terminal, rode o comando:
  ```bash
python3 -m venv ./venv
```
 3. ative o venv:
  - Comando para linux/mac:
  ```bash
source venv/bin/activate
```
  - Comando para windows:
  ```shell
venv\Scripts\activate.bat
```

 4. Instale o Django no ambiente virtualizado:
  ```bash
pip install django
```

 5. Crie um projeto chamado config:
  ```bash
django-admin startproject config .
```

 6. Na pasta config, altere no arquivo settings.py o idioma e o horário:
  ```python
LANGUAGE_CODE = 'pt-br'
TIME_ZONE = 'America/Sao_Paulo'
```
 7. No terminal, rode o comando abaixo para criar a pasta que contém os arquivos models, views, templates, etc.:
 ```bash
 python manage.py startapp escola
 ```

## Avisos
 - Para criar um super usuário, digite o seguinte comando e siga os passos:
 ```bash
 python manage.py createsuperuser
 ```
 - Quando fizer novos models ou quando trocar de banco de dados, deve se rodar os comandos abaixo:
 ```bash
 python manage.py makemigrations # Django cria o banco de dados e as migrations, mas não realmente aplica as alterações no banco de dados.
 python manage.py migration # Aplica as alterações no banco de dados.
 ```
 - Para utilizar seu próprio banco de dados, altere as configurações do arquivo settings.py, de acordo com a documentação [Django Databases](https://docs.djangoproject.com/en/4.2/ref/databases/):
 ```python
 DATABASES = {
    "default": {
        "ENGINE": "django.db.backends.postgresql",
        "NAME": "postgres",
        "USER": "postgres",
        "PASSWORD": "postgres",
        "HOST": "localhost",
        "PORT": "5432",
    }
}
 ```

