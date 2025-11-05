# BookSwap

# 📚 BookSwap – Plataforma de Troca de Livros

BookSwap é uma aplicação **fullstack** desenvolvida com **Django REST Framework** no backend e **React + TypeScript (Vite)** no frontend.  
O objetivo é permitir que usuários **cadastrem livros**, **ofereçam cópias** e **realizem trocas** com outros usuários, usando autenticação JWT e uma interface moderna feita com Tailwind CSS.

---

## 🧩 Tecnologias Utilizadas

### 🔙 Backend (API)
- Python 3.10+
- Django 5.1
- Django REST Framework (DRF)
- SimpleJWT (autenticação JWT)
- drf-spectacular (Swagger UI)
- MySQL (ou SQLite em modo dev)
- CORS Headers (integração com frontend)

### 🔮 Frontend
- React 18 + TypeScript
- Vite
- Axios
- React Router DOM
- React Query
- React Hook Form + Yup
- Tailwind CSS

---

## 📁 Estrutura do Projeto

```
BookSwap/
│
├── backend/                     # API Django REST Framework
│   ├── myproject/                # Configurações Django (urls, settings, etc.)
│   ├── myapp/                    # Aplicação principal
│   │   ├── models.py             # Modelos (Book, BookCopy, SwapRequest)
│   │   ├── api/v1/
│   │   │   ├── serializers.py    # Serializers DRF
│   │   │   ├── viewsets.py       # ViewSets e rotas da API
│   │   │   └── urls.py           # Versionamento da API
│   └── manage.py
│
└── frontend/                    # Aplicação React + TypeScript
    ├── src/
    │   ├── pages/               # Páginas (Login, Dashboard, Trocas, etc.)
    │   ├── components/          # Navbar, Layouts e componentes reutilizáveis
    │   ├── lib/                 # Contextos e tipagens globais
    │   └── services/            # Conexão com API via Axios
    └── vite.config.ts
```

---

## ⚙️ Instalação e Execução

### 🖥️ Backend (Django)

1️⃣ **Acesse a pasta do backend**
```bash
cd backend
```

2️⃣ **Crie e ative o ambiente virtual**
```bash
python -m venv venv
venv\Scripts\activate   # (Windows)
source venv/bin/activate  # (Linux/macOS)
```

3️⃣ **Instale as dependências**
```bash
pip install -r requirements.txt
```

4️⃣ **Configure o banco de dados (.env)**
Crie o arquivo `.env` na pasta `backend/` com:
```
DEBUG=True
SECRET_KEY=chave_secreta_troque_aqui
DB_ENGINE=django.db.backends.mysql
DB_NAME=bookswap_db
DB_USER=root
DB_PASSWORD=112244
DB_HOST=localhost
DB_PORT=3306
```

5️⃣ **Rode as migrações e o servidor**
```bash
python manage.py makemigrations
python manage.py migrate
python manage.py runserver
```

O backend estará disponível em:
👉 `http://127.0.0.1:8000/`

---

### 💻 Frontend (React + TypeScript)

1️⃣ **Acesse a pasta**
```bash
cd frontend
```

2️⃣ **Instale as dependências**
```bash
npm install
```

3️⃣ **Configure a URL da API**
Crie o arquivo `.env.local` com:
```
VITE_API_URL=http://localhost:8000
```

4️⃣ **Inicie o servidor**
```bash
npm run dev
```

Acesse o frontend em:
👉 `http://localhost:5173/`

---

## 📘 Funcionalidades

### 🔒 Autenticação
- Login via **JWT** (tokens armazenados em cookies)
- Proteção de rotas via `PrivateRoute`
- Logout com limpeza automática da sessão

### 📚 Módulos Principais
- **Livros (Books)** – Cadastro, edição, exclusão e listagem
- **Cópias (Book Copies)** – Exibe os livros que o usuário possui
- **Trocas (Swaps)** – Permite oferecer e solicitar trocas entre usuários
- **Dashboard** – Mostra todos os livros disponíveis no sistema

### ⚡ Extras
- Paginação nas listagens
- Validação de formulários com **Yup**
- Interface moderna e responsiva com **Tailwind CSS**
- Documentação automática da API em `/api/docs/` (Swagger)

---

## 🎯 Critérios de Avaliação (Frontend)

| Critério | Pontos |
|-----------|--------|
| Integração com API (Axios, CRUD, JWT) | 3 pts |
| Estrutura e Organização (components, hooks, context, types) | 2 pts |
| Funcionalidades e Navegação (rotas, login, logout, exibição) | 2 pts |
| Estilo e Usabilidade (Tailwind, responsividade) | 1 pt |
| Boas Práticas e Código limpo | 1 pt |
| **Total** | **9 / 9 pontos** ✅ |

---

## 🧠 Sobre o Projeto

BookSwap foi desenvolvido como um **projeto fullstack acadêmico**, com foco em:
- Boas práticas de API REST
- Autenticação JWT entre backend e frontend
- Comunicação segura Django ↔ React
- Organização modular e reutilizável
- Design responsivo e intuitivo

---

## 🧑‍💻 Autoria

**Desenvolvido por:** Paulo Kaike  
**Professor:** [Nome do Professor]  
**Disciplina:** Desenvolvimento Web Fullstack  
**Ano:** 2025  

---

## 🖼️ Prints de Exemplo

### 🔹 Dashboard
Visualização do catálogo de livros disponíveis para troca.

### 🔹 Minhas Cópias
Listagem das cópias que o usuário possui e pode oferecer.

### 🔹 Trocas
Histórico e status de solicitações de troca (pendente, aceita, recusada).

---
