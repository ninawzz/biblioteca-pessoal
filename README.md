# 📚 Biblioteca Pessoal - Django

Um sistema simples de gerenciamento de livros e categorias, desenvolvido em **Django**.  
Permite buscar livros, adicionar à sua coleção, organizar por categorias e gerenciar cada item.

---

## 🚀 Funcionalidades

- 🔎 **Pesquisar livros** e adicionar à biblioteca.
- 📖 **Gerenciar livros** (listar, visualizar detalhes, excluir, alterar categoria).
- 🏷️ **Categorias personalizadas** (adicionar, editar, deletar, ver livros da categoria).
- 🎨 **Interface estilizada** com HTML + CSS customizado.

---

## 🛠️ Tecnologias utilizadas

- [Python 3.13.7](https://www.python.org/)
- [Django 5.2.6](https://www.djangoproject.com/)
- HTML5, CSS3
- SQLite

---

## 📂 Estrutura do projeto
```
Project/
│── biblioteca/ # App principal
│ ├── templates/ # Templates HTML
│ │ ├── base.html
│ │ ├── livros/
│ │ └── categoria/
│ ├── static/ # Arquivos CSS / imagens
│ ├── views.py
│ ├── urls.py
│ └── models.py
│
├── Project/ # Configurações principais do Django
│ ├── settings.py
│ ├── urls.py
│
├── db.sqlite3 # Banco de dados
├── manage.py
└── README.md
```
---

## ⚙️ Como rodar o projeto

### 1. Clonar o repositório
```
git clone https://github.com/ninawz/biblioteca-django.git
cd biblioteca-django
```
### 2. Criar ambiente virtual
```
python -m venv venv
source venv/bin/activate    # Linux / Mac
venv\Scripts\activate       # Windows
```
### 3. Instalar dependências
```
pip install -r requirements.txt
```

### 4. Rodar as migrações
```
python manage.py migrate
```
### 5. Rodar servidor local
```
python manage.py runserver
```
➡️ Acesse em: http://127.0.0.1:8000/

## 📡 Endpoints:

  📚 Livros
| Método   | URL                               | Descrição                         |
| -------- | --------------------------------- | --------------------------------- |
| **GET**  | `/livros/`                        | Lista todos os livros cadastrados |
| **GET**  | `/livros/<id>/`                   | Detalhes de um livro específico   |
| **POST** | `/livros/adicionar/`              | Adiciona um novo livro            |
| **POST** | `/livros/<id>/editar/`            | Edita informações de um livro     |
| **POST** | `/livros/<id>/deletar/`           | Deleta um livro                   |
| **POST** | `/livros/<id>/alterar-categoria/` | Alterar categoria de um livro     |

# # 🏷️ Categorias

| Método   | URL                         | Descrição                              |
| -------- | --------------------------- | -------------------------------------- |
| **GET**  | `/categorias/`              | Lista todas as categorias              |
| **GET**  | `/categorias/<id>/`         | Lista todos os livros de uma categoria |
| **POST** | `/categorias/adicionar/`    | Cria uma nova categoria                |
| **POST** | `/categorias/<id>/editar/`  | Edita o nome de uma categoria          |
| **POST** | `/categorias/<id>/deletar/` | Deleta uma categoria                   |

# # 🔎 Outros
| Método  | URL           | Descrição                                       |
| ------- | ------------- | ----------------------------------------------- |
| **GET** | `/pesquisar/` | Página de pesquisa de livros (por título/autor) |


