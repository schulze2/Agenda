# Agenda

Aplicacao web de agenda de contatos feita com Django, desenvolvido no curso do Luiz Otávio Miranda.

## Funcionalidades

- Listagem de contatos com paginacao
- Cadastro, edicao e exclusao de contatos
- Categorias de contato
- Upload de imagem (foto do contato)
- Autenticacao de usuarios

## Tecnologias

- Python
- Django 4.2.4
- SQLite
- Pillow (suporte a ImageField)

## Estrutura principal

- `project/`: configuracoes do projeto Django
- `contact/`: app principal com models, views, forms e templates
- `base_templates/`: templates base e parciais globais
- `base_static/`: arquivos estaticos globais
- `utils/create_contacts.py`: script para gerar contatos ficticios

## Como executar o projeto

### 1) Criar e ativar ambiente virtual

Windows (PowerShell):

```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
```

Linux/macOS:

```bash
python -m venv venv
source venv/bin/activate
```

### 2) Instalar dependencias

```bash
python -m pip install django pillow faker
```

### 3) Aplicar migrations

```bash
python manage.py migrate
```

### 4) Iniciar servidor

```bash
python manage.py runserver
```

Abra no navegador:

- http://127.0.0.1:8000/

## Comandos uteis

Criar superusuario:

```bash
python manage.py createsuperuser
```

Popular o banco com contatos de exemplo:

```bash
python utils/create_contacts.py
```

Checar configuracao do projeto:

```bash
python manage.py check
```

## Midias e arquivos estaticos

- Midias de upload ficam em `media/`
- Arquivos estaticos globais ficam em `base_static/`

## Observacoes

- O projeto usa SQLite (`db.sqlite3`) no ambiente de desenvolvimento.
- Para upload de imagens funcionar, a dependencia Pillow precisa estar instalada.
