# 🌑 Web Development Library Guide

<div align="center">

### *Dark • Minimal • Developer Friendly*

**Created by: Arun VK**

![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=flat-square&logo=python&logoColor=white)
![Web Dev](https://img.shields.io/badge/Web-Development-ff69b4?style=flat-square)
![Status](https://img.shields.io/badge/Status-Active-success?style=flat-square)

</div>

---

## 🖤 Overview

Python has evolved into a powerhouse for web development, offering frameworks and tools that range from minimal microservices to enterprise-grade applications. Whether you're building RESTful APIs, dynamic web apps, or full-stack solutions, Python's ecosystem provides everything you need for modern web development.

This guide curates essential libraries for **web development** — covering backend frameworks, templating engines, database management, authentication systems, and API integration. Build fast, secure, and scalable web applications with confidence.

Dark-themed. Minimal. Web-ready.

---

## 📚 Web Development Libraries

### 1️⃣ Backend Frameworks

| Library | Description | Install |
|---------|-------------|---------|
| **Django** | Full-scale web framework | `pip install django` |
| **Flask** | Minimal micro-framework | `pip install flask` |
| **FastAPI** | Modern async backend | `pip install fastapi uvicorn` |

---

### 2️⃣ Templating Engines

| Library | Description | Install |
|---------|-------------|---------|
| **Jinja2** | HTML templating | `pip install jinja2` |
| **Mako** | Fast templating | `pip install mako` |

---

### 3️⃣ Databases & ORM

| Library | Description | Install |
|---------|-------------|---------|
| **SQLAlchemy** | ORM for SQL databases | `pip install sqlalchemy` |
| **Django ORM** | Built-in ORM | (comes with Django) |
| **Psycopg2** | PostgreSQL driver | `pip install psycopg2` |

---

### 4️⃣ Authentication & Security

| Library | Description | Install |
|---------|-------------|---------|
| **Authlib** | OAuth & JWT | `pip install authlib` |
| **Passlib** | Password hashing | `pip install passlib` |

---

### 5️⃣ Frontend + APIs

| Library | Description | Install |
|---------|-------------|---------|
| **Requests** | API calls | `pip install requests` |
| **httpx** | Async HTTP | `pip install httpx` |

---

## 🚀 Install All at Once

```bash
pip install django flask fastapi uvicorn jinja2 mako sqlalchemy psycopg2 authlib passlib requests httpx
```

---

## 💡 Quick Start Examples

### Flask Web App
```python
from flask import Flask, render_template

app = Flask(__name__)

@app.route('/')
def home():
    return render_template('index.html')

@app.route('/api/data')
def api_data():
    return {'status': 'success', 'data': [1, 2, 3]}

if __name__ == '__main__':
    app.run(debug=True)
```

### Django Project Setup
```bash
django-admin startproject myproject
cd myproject
python manage.py runserver
```

### FastAPI Backend
```python
from fastapi import FastAPI
from pydantic import BaseModel

app = FastAPI()

class User(BaseModel):
    name: str
    email: str

@app.post("/users/")
async def create_user(user: User):
    return {"message": f"User {user.name} created"}

# Run: uvicorn main:app --reload
```

### SQLAlchemy ORM
```python
from sqlalchemy import create_engine, Column, Integer, String
from sqlalchemy.ext.declarative import declarative_base
from sqlalchemy.orm import sessionmaker

Base = declarative_base()

class User(Base):
    __tablename__ = 'users'
    id = Column(Integer, primary_key=True)
    name = Column(String)
    email = Column(String)

engine = create_engine('sqlite:///app.db')
Base.metadata.create_all(engine)
```

---

## 🎯 Framework Comparison

| Feature | Django | Flask | FastAPI |
|---------|--------|-------|---------|
| **Size** | Full-stack | Micro | Micro |
| **Speed** | 🔷 Good | 🔷 Good | ⚡ Excellent |
| **Async** | ⚠️ Limited | ❌ No | ✅ Native |
| **Learning Curve** | 🟡 Steep | 🟢 Easy | 🟢 Easy |
| **Best For** | Enterprise apps | Prototypes | Modern APIs |
| **ORM** | ✅ Built-in | ❌ Separate | ❌ Separate |

---

## 🛠️ Essential Extensions

**Flask Extensions:**
```bash
pip install flask-sqlalchemy flask-login flask-wtf
```

**Django Packages:**
```bash
pip install djangorestframework django-cors-headers
```

**Database Drivers:**
```bash
pip install pymongo redis mysql-connector-python
```

**Testing Tools:**
```bash
pip install pytest pytest-flask pytest-django
```

---

## 📋 Best Practices

- Use **virtual environments** (`venv` or `virtualenv`) for project isolation
- Choose **Django** for full-featured apps with admin panels
- Pick **Flask** for lightweight, flexible applications
- Select **FastAPI** for high-performance APIs with async support
- Implement **SQLAlchemy** for database abstraction and portability
- Use **Authlib** for secure OAuth and JWT authentication
- Always hash passwords with **Passlib** or similar libraries
- Enable **CORS** properly for API endpoints
- Use environment variables for sensitive configuration

---

## 🔗 Resources

- [Django Documentation](https://docs.djangoproject.com/)
- [Flask Official Guide](https://flask.palletsprojects.com/)
- [FastAPI Docs](https://fastapi.tiangolo.com/)
- [SQLAlchemy Tutorial](https://docs.sqlalchemy.org/)
- [Real Python Web Dev](https://realpython.com/tutorials/web-dev/)

---

## 📄 License

MIT License - Build the web, your way.

---

<div align="center">

**Made with 🖤 by Arun VK**

*"Clean code. Clean design."*

---

🌑 **Dark theme. Fast builds. Better web.**

</div>