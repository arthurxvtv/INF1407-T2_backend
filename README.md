# INF1407-T2 Backend

Este é o backend do projeto INF1407-T2, desenvolvido utilizando Django e Django REST Framework. O projeto consiste em uma aplicação de revisão de jogos, onde os usuários podem se registrar, autenticar, postar revisões e alterar suas senhas.

## Estrutura do Projeto

```
requirements.txt
src/
    db.sqlite3
    manage.py
    ReviewApp/
        __init__.py
        __pycache__/
        admin.py
        apps.py
        forms.py
        migrations/
            __init__.py
            __pycache__/
            0001_initial.py
        models.py
        serializer.py
        static/
        tests.py
        views.py
    Reviews/
        __init__.py
        __pycache__/
        asgi.py
        settings.py
        urls.py
        wsgi.py
```

## Aplicações e Arquivos Principais

- `manage.py`: Utilitário de linha de comando do Django para tarefas administrativas.
- `ReviewApp/`: Aplicação principal contendo modelos, views, serializers e formulários.
    - `models.py`: Define o modelo `Review`.
    - `views.py`: Contém as views `Autenticar`, `Registrar`, `AlterarSenha`, `Reviews` e `Logout`.
    - `serializer.py`: Define o serializer `ReviewSerializer`.
    - `forms.py`: Define o formulário `ReviewForm`.
    - `admin.py`: Registro de modelos no admin do Django.
    - `tests.py`: Arquivo para testes.
    - `migrations/`: Contém as migrações do banco de dados.
- `Reviews/`: Configurações do projeto Django.
    - `settings.py`: Configurações do projeto.
    - `urls.py`: Define as rotas da aplicação.
    - `wsgi.py`: Configuração WSGI para deploy.
    - `asgi.py`: Configuração ASGI para deploy.

## Endpoints da API

- `POST /login/`: Autenticação de usuário.
- `POST /logout/`: Logout de usuário.
- `POST /register/`: Registro de novo usuário.
- `POST /alterar-senha/`: Alteração de senha do usuário.
- `GET /reviews/`: Listagem de reviews do usuário autenticado.
- `POST /reviews/`: Criação de nova review.
- `GET /reviews/<int:pk>/`: Detalhes de uma review específica.
- `PATCH /reviews/<int:pk>/`: Atualização parcial de uma review.
- `DELETE /reviews/<int:pk>/`: Exclusão de uma review.

# O que faltou:

# Recuperação de senha por e-mail

Não foi possível implementar o o cadastro do e-mail do usuário, tampouco a recuperação de senha via e-mail.

# Documentação Swagger

Não foi possível implementar a documentação Swagger das APIs.
