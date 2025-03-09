# Django com Docker - Guia de Configuração e Uso

O projeto possui um ambiente para a imagem Django separados em dois serviços:
- **webapp**: O servidor Django é a aplicação web.
- **db**: O banco de dados PostgreSQL.


## Configuração do projeto

### 1. Criar um Projeto Django
Criado o projeto com:
```sh
django-admin startproject django_project .
```

### 2. Arquivo `requirements.txt`
Dependências do projeto.
```
django
psycopg2-binary
```

### 3. Dockerfile
O Dockerfile define a imagem do contêiner do Django

### 4. Criar o docker-compose.yml
Definição dos serviços do sistema

### 5. Foi adicionado ao `settings.py` para conectar-se ao banco:
```python
import os
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': os.getenv('DB_NAME'),
        'USER': os.getenv('DB_USER'),
        'PASSWORD': os.getenv('DB_PASSWORD'),
        'HOST': os.getenv('DB_HOST'),
        'PORT': '5432',
    }
}
```

### 6. Rodando no docker
```sh
docker-compose up -d --build
```
Isso irá:
- Criar e iniciar os contêineres `webapp` e `db`
- Instalar as dependências do Django
- Rodar o servidor Django em `http://localhost:8000/`

### 7. Migrações e criação do Superusuário
Para configurar o banco de dados, execute:
```sh
python manage.py migrate
```
Para criar um superusuário para acessar o admin do Django:
```sh
python manage.py createsuperuser
```

### 8. Acessar o Painel de Admin
Acesse `http://localhost:8000/admin/` e entre com o superusuário criado.

