[![Python Web Development Roadmap](https://img.shields.io/badge/Python-Web%20Development-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Contributions Welcome](https://img.shields.io/badge/Contributions-Welcome-blue.svg)](https://github.com/anomalyco/opencode/issues)

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/c/c3/Python-logo-notext.svg" width="120" alt="Python Logo">
</p>

<h1 align="center">🐍 Python Web Development Roadmap</h1>

<p align="center">
  A comprehensive guide to becoming a Python Web Developer in 2026
</p>

---

## 📌 Table of Contents

1. [What is Python & Why Use It for Web Development?](#-what-is-python--why-use-it-for-web-development)
2. [Getting Started - Installation](#-getting-started---installation)
3. [Virtual Environments & Package Management](#-virtual-environments--package-management)
4. [Development Tools](#-development-tools)
5. [Web Frameworks Overview](#-web-frameworks-overview)
6. [REST APIs & FastAPI](#-rest-apis--fastapi)
7. [Flask: Micro-Framework](#-flask-micro-framework)
8. [Django: Full-Stack Framework](#-django-full-stack-framework)
9. [Databases & SQLite](#-databases--sqlite)
10. [Frontend Integration](#-frontend-integration)
11. [Authentication & Security](#-authentication--security)
12. [Testing](#-testing)
13. [Deployment](#-deployment)
14. [Learning Path](#-learning-path)
15. [Roadmap Diagram](#-roadmap-diagram)
16. [Resources](#-resources)

---

## 🐍 What is Python & Why Use It for Web Development?

**Python** is a high-level, interpreted programming language known for its readability and versatility. Created by Guido van Rossum in 1991.

### Why Python for Web Dev?

```
┌─────────────────────────────────────────────────────────────┐
│                    WHY PYTHON?                              │
├─────────────────────────────────────────────────────────────┤
│  ✓ Easy to Learn      → Simple syntax, great for beginners │
│  ✓ Fast Development   → Rich libraries & frameworks        │
│  ✓ Scalable           → Used by Instagram, Spotify, Netflix│
│  ✓ Large Community    → 50M+ developers worldwide           │
│  ✓ Career Opportunities → High demand, great salaries      │
└─────────────────────────────────────────────────────────────┘
```

### What Can You Build with Python Web?

| Category | Examples |
|----------|----------|
| 🌐 **Web Apps** | Social networks, e-commerce sites, blogs |
| API | REST APIs, GraphQL APIs |
| 🤖 **Automation** | Web scrapers, bots, task schedulers |
| 📊 **Data Dashboards** | Analytics tools, admin panels |
| 🏢 **Enterprise Apps** | CRMs, ERPs, internal tools |

---

## 💻 Getting Started - Installation

### Installing Python

#### Windows
```powershell
# Download from https://www.python.org/downloads/
# OR using winget
winget install Python.Python.3.12

# Verify installation
python --version
```

#### macOS
```bash
# Using Homebrew
brew install python

# OR using pyenv (recommended)
brew install pyenv
pyenv install 3.12.0

# Verify installation
python3 --version
```

#### Linux (Ubuntu/Debian)
```bash
# Update package list
sudo apt update

# Install Python
sudo apt install python3 python3-pip python3-venv

# Verify installation
python3 --version
```

### Installing pip (Package Installer)

```bash
# Linux/macOS
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
python3 get-pip.py

# Windows (if not included)
python -m ensurepip --upgrade

# Upgrade pip
pip install --upgrade pip
```

### Checking Your Installation

```bash
# Check Python version
python --version       # Output: Python 3.12.0

# Check pip version
pip --version          # Output: pip 24.0

# Check installed packages
pip list
```

---

## 🐍 Virtual Environments & Package Management

### Why Use Virtual Environments?

```
┌─────────────────────────────────────────────────────────────┐
│              WHY VIRTUAL ENVIRONMENTS?                     │
├─────────────────────────────────────────────────────────────┤
│  • Isolated dependencies per project                        │
│  • Avoid version conflicts between projects                │
│  • Clean project structure                                 │
│  • Easy to reproduce & share                               │
│  • Required for deployment                                 │
└─────────────────────────────────────────────────────────────┘
```

### Creating Virtual Environments

#### Using venv (Built-in)

```bash
# Create virtual environment
python -m venv myenv

# Activate (Windows)
myenv\Scripts\activate

# Activate (Linux/macOS)
source myenv/bin/activate

# Install packages
pip install flask fastapi

# Deactivate
deactivate
```

#### Using virtualenv

```bash
# Install virtualenv
pip install virtualenv

# Create environment
virtualenv myenv

# Activate
source myenv/bin/activate  # Linux/macOS
myenv\Scripts\activate    # Windows
```

### pip Commands

```bash
# Install package
pip install flask

# Install specific version
pip install flask==3.0.0

# Install from requirements.txt
pip install -r requirements.txt

# Create requirements.txt
pip freeze > requirements.txt

# Upgrade package
pip install --upgrade flask

# Uninstall package
pip uninstall flask

# List installed packages
pip list

# Show package info
pip show flask
```

### requirements.txt Example

```
# requirements.txt
flask==3.0.0
fastapi==0.109.0
uvicorn==0.27.0
sqlalchemy==2.0.25
pydantic==2.5.3
python-jose[cryptography]==3.3.0
passlib[bcrypt]==1.7.4
python-multipart==0.0.6
flask-cors==4.0.0
psycopg2-binary==2.9.9
redis==5.0.1
```

---

## 🛠️ Development Tools

### Code Editors & IDEs

| Tool | Type | Best For |
|------|------|----------|
| [VS Code](https://code.visualstudio.com/) | Free Editor | All-around, great extensions |
| [PyCharm](https://www.jetbrains.com/pycharm/) | IDE (Free/Paid) | Large projects, Django |
| [Sublime Text](https://www.sublimetext.com/) | Editor | Lightweight |
| [Vim/Neovim](https://neovim.io/) | Editor | Advanced users |

### Essential VS Code Extensions

```
┌─────────────────────────────────────────────────────────────┐
│              RECOMMENDED VS CODE EXTENSIONS                 │
├─────────────────────────────────────────────────────────────┤
│  • Python                     → Official Microsoft        │
│  • Pylance                    → Type checking              │
│  • Python Debugger             → Debugging                  │
│  • GitHub Copilot             → AI code completion         │
│  • Flake8                     → Linting                     │
│  • Black Formatter            → Code formatting            │
│  • autoDocstring              → Docstring generation       │
│  • REST Client                → API testing                │
└─────────────────────────────────────────────────────────────┘
```

### VS Code Settings (settings.json)

```json
{
    "python.defaultInterpreterPath": "/usr/bin/python3",
    "python.linting.enabled": true,
    "python.linting.pylintEnabled": true,
    "python.formatting.provider": "black",
    "python.testing.pytestEnabled": true,
    "python.testing.unittestEnabled": false,
    "editor.formatOnSave": true,
    "files.autoSave": "afterDelay"
}
```

### Terminal Tools

```bash
# Windows
# PowerShell or Windows Terminal (recommended)

# macOS
# iTerm2 (recommended) or Terminal

# Linux
# GNOME Terminal, Konsole, or Alacritty

# Oh My Zsh (recommended shell)
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### Browser Extensions

- **Postman** - API testing
- **JSON Viewer** - Format JSON responses
- **Vue DevTools** / **React DevTools** - Frontend debugging
- **Wappalyzer** - Identify web technologies

---

## 🌐 Web Frameworks Overview

```
┌────────────────────────────────────────────────────────────────────────┐
│                    PYTHON WEB FRAMEWORKS                               │
├────────────────────────────────────────────────────────────────────────┤
│                                                                        │
│   ┌─────────────┐      ┌─────────────┐      ┌─────────────┐          │
│   │   FLASK     │      │   DJANGO    │      │  FASTAPI    │          │
│   │  (Micro)    │      │  (Full-Stack│      │  (Modern)   │          │
│   └──────┬──────┘      └──────┬──────┘      └──────┬──────┘          │
│          │                    │                    │                  │
│          ▼                    ▼                    ▼                  │
│   • Lightweight         • All-in-one          • Async Native         │
│   • Flexible            • Batteries-included   • Auto Docs (Swagger)  │
│   • Full control        • Built-in Admin      • Type Validation       │
│   • Small projects      • Large projects       • High Performance     │
│                                                                        │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 🔗 REST APIs & FastAPI

### What is a REST API?

**REST (Representational State Transfer)** is an architectural style for building web services. It uses HTTP requests to perform CRUD operations.

```
┌─────────────────────────────────────────────────────────────────┐
│                      REST API CONCEPTS                          │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│   HTTP Methods:                                                  │
│   ┌────────┬──────────────┬────────────────────────────────┐   │
│   │ METHOD │    ACTION    │            EXAMPLE             │   │
│   ├────────┼──────────────┼────────────────────────────────┤   │
│   │  GET   │  Read data   │  GET /users                    │   │
│   │  POST  │  Create data │  POST /users                   │   │
│   │  PUT   │  Update data │  PUT /users/1                  │   │
│   │ DELETE │  Delete data │  DELETE /users/1               │   │
│   └────────┴──────────────┴────────────────────────────────┘   │
│                                                                 │
│   Key Principles:                                               │
│   • Stateless (each request is independent)                    │
│   • Client-Server architecture                                  │
│   • JSON responses                                              │
│   • Standard HTTP methods                                       │
│                                                                 │
│   HTTP Status Codes:                                            │
│   ┌──────┬─────────────────────────────────────────────────┐   │
│   │ 200  │ OK - Successful request                         │   │
│   │ 201  │ Created - Resource successfully created         │   │
│   │ 400  │ Bad Request - Invalid input                     │   │
│   │ 401  │ Unauthorized - Missing/invalid token             │   │
│   │ 404  │ Not Found - Resource doesn't exist              │   │
│   │ 500  │ Server Error - Internal server error            │   │
│   └──────┴─────────────────────────────────────────────────┘   │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### REST API Best Practices

```
┌─────────────────────────────────────────────────────────────────┐
│              REST API DESIGN BEST PRACTICES                     │
├─────────────────────────────────────────────────────────────────┤
│  ✓ Use nouns for endpoints (/users, /articles)                 │
│  ✓ Use HTTP methods correctly (GET/POST/PUT/DELETE)            │
│  ✓ Return proper status codes                                  │
│  ✓ Use plural nouns for collections (/users not /user)         │
│  ✓ Use versioning (/api/v1/users)                              │
│  ✓ Implement pagination for large datasets                     │
│  ✓ Use filtering and sorting query parameters                  │
│  ✓ Implement proper error responses with details              │
│  ✓ Use JSON for request/response bodies                       │
│  ✓ Implement HATEOAS (optional)                               │
└─────────────────────────────────────────────────────────────────┘
```

### REST API URL Design

```python
# Good REST API URLs
GET    /api/users           # Get all users
GET    /api/users/123       # Get single user
POST   /api/users           # Create new user
PUT    /api/users/123       # Update user (full)
PATCH  /api/users/123       # Partial update
DELETE /api/users/123      # Delete user

# Nested resources
GET    /api/users/123/posts           # Get user's posts
POST   /api/users/123/posts           # Create post for user

# Filtering
GET    /api/users?age=25              # Filter by age
GET    /api/users?status=active      # Filter by status
GET    /api/users?sort=name          # Sort by name
GET    /api/users?page=1&limit=10   # Pagination

# Search
GET    /api/users/search?q=john      # Search users
```

### GraphQL (Alternative to REST)

```bash
pip install graphene graphene-django
```

```python
# schema.py
import graphene
from graphene_django import DjangoObjectType
from .models import User

class UserType(DjangoObjectType):
    class Meta:
        model = User
        fields = ["id", "name", "email"]

class Query(graphene.ObjectType):
    all_users = graphene.List(UserType)
    user = graphene.Field(UserType, id=graphene.Int())

    def resolve_all_users(self, info):
        return User.objects.all()

    def resolve_user(self, info, id):
        return User.objects.get(id=id)

class CreateUser(graphene.Mutation):
    class Arguments:
        name = graphene.String(required=True)
        email = graphene.String(required=True)

    user = graphene.Field(UserType)

    def mutate(self, info, name, email):
        user = User.objects.create(name=name, email=email)
        return CreateUser(user=user)

class Mutation(graphene.ObjectType):
    create_user = CreateUser.Field()

schema = graphene.Schema(query=Query, mutation=Mutation)
```

```javascript
// GraphQL Query
query {
  allUsers {
    id
    name
    email
  }
}

// With parameters
query {
  user(id: 1) {
    name
    posts {
      title
    }
  }
}

// Mutation
mutation {
  createUser(name: "John", email: "john@example.com") {
    user {
      id
      name
    }
  }
}
```

### REST vs GraphQL

| Feature | REST | GraphQL |
|---------|------|---------|
| **Data Fetching** | Multiple endpoints | Single endpoint |
| **Over-fetching** | Can return extra data | Get exactly what you need |
| **Under-fetching** | Need multiple requests | Single request |
| **Caching** | HTTP caching | Custom caching |
| **Learning Curve** | Lower | Higher |
| **Performance** | Good for simple APIs | Better for complex data |

### API Testing with Postman

```bash
# Install Postman from https://www.postman.com/downloads/
```

```
Postman Collection Example:

Collection: My API

├── GET /api/users
│   └── Get all users
├── GET /api/users/:id
│   └── Get user by ID
├── POST /api/users
│   └── Create new user
│   Body: { "name": "John", "email": "john@example.com" }
├── PUT /api/users/:id
│   └── Update user
├── DELETE /api/users/:id
│   └── Delete user

Variables:
{{base_url}} = http://localhost:8000
{{token}} = <JWT token>
```

### HTTP Headers

```python
# Request headers (FastAPI)
from fastapi import Header

@app.get("/users")
def get_users(authorization: str = Header(None)):
    token = authorization.replace("Bearer ", "")
    return {"token": token}

# Response headers
from fastapi import Response
import json

@app.get("/download")
def download_file(response: Response):
    response.headers["Content-Disposition"] = "attachment; filename=data.json"
    return {"data": "content"}
```

### API Versioning

```python
# URL-based versioning (recommended)
@app.get("/api/v1/users")
def get_users_v1():
    return {"version": "v1"}

@app.get("/api/v2/users")
def get_users_v2():
    return {"version": "v2"}

# Header-based versioning
from fastapi import Header

@app.get("/users")
def get_users(x_api_version: str = Header("v1")):
    if x_api_version == "v2":
        return {"users": [], "new_fields": True}
    return {"users": []}
```

### Rate Limiting

```python
# FastAPI with slowapi
pip install slowapi

from fastapi import FastAPI, Request
from slowapi import Limiter
from slowapi.util import get_remote_address

limiter = Limiter(key_func=get_remote_address)
app = FastAPI()

@app.get("/api/data")
@limiter.limit("10/minute")
async def get_data(request: Request):
    return {"data": "limited"}
```

### API Documentation

```python
# FastAPI auto-generates OpenAPI docs
# Visit: /docs (Swagger UI)
# Visit: /redoc (ReDoc)

@app.get("/users", summary="Get all users", description="Returns a list of users")
def get_users():
    """This is a docstring that appears in docs"""
    return []

# Add examples
from pydantic import BaseModel, Field, examples

class User(BaseModel):
    name: str = Field(..., example="John Doe")
    email: str = Field(..., example="john@example.com")
```

### Webhooks

```python
# Webhook receiver (Flask)
from flask import Flask, request, jsonify

app = Flask(__name__)

@app.route("/webhook", methods=["POST"])
def handle_webhook():
    payload = request.get_json()
    event_type = request.headers.get("X-Webhook-Event")
    
    if event_type == "user.created":
        print(f"New user: {payload['user']['email']}")
    elif event_type == "payment.succeeded":
        print(f"Payment: {payload['amount']}")
    
    return jsonify({"status": "received"}), 200
```

### API Keys

```python
# FastAPI API Key authentication
from fastapi import FastAPI, Depends, HTTPException
from fastapi.security import APIKeyHeader

app = FastAPI()
API_KEY_HEADER = APIKeyHeader(name="X-API-Key")

async def verify_api_key(api_key: str = Depends(API_KEY_HEADER)):
    if api_key != "your-api-key":
        raise HTTPException(status_code=403, detail="Invalid API key")
    return api_key

@app.get("/protected")
async def protected_endpoint(api_key: str = Depends(verify_api_key)):
    return {"message": "Access granted"}
```

### What is FastAPI?

**FastAPI** is a modern, high-performance Python web framework for building APIs (introduced in 2018).

### Installing FastAPI

```bash
# Create virtual environment
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows

# Install FastAPI and uvicorn
pip install fastapi uvicorn
```

### FastAPI Hello World

```python
# main.py
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def read_root():
    return {"message": "Hello, World!"}

@app.get("/users/{user_id}")
def read_user(user_id: int):
    return {"user_id": user_id, "name": "John Doe"}
```

### Running FastAPI

```bash
# Development server (auto-reload)
uvicorn main:app --reload

# Custom host/port
uvicorn main:app --host 0.0.0.0 --port 8000

# With workers
uvicorn main:app --workers 4
```

### FastAPI HTTP Methods

```python
from fastapi import FastAPI, HTTPException, status
from pydantic import BaseModel
from typing import Optional, List

app = FastAPI()

# Pydantic models for validation
class User(BaseModel):
    name: str
    email: str
    age: Optional[int] = None

class UserCreate(User):
    pass

class UserResponse(User):
    id: int

# In-memory database
users_db = []

@app.get("/users", response_model=List[UserResponse])
def get_users():
    return users_db

@app.post("/users", response_model=UserResponse, status_code=status.HTTP_201_CREATED)
def create_user(user: UserCreate):
    new_user = UserResponse(id=len(users_db) + 1, **user.dict())
    users_db.append(new_user)
    return new_user

@app.get("/users/{user_id}", response_model=UserResponse)
def get_user(user_id: int):
    for user in users_db:
        if user.id == user_id:
            return user
    raise HTTPException(status_code=404, detail="User not found")

@app.put("/users/{user_id}", response_model=UserResponse)
def update_user(user_id: int, user: UserCreate):
    for i, u in enumerate(users_db):
        if u.id == user_id:
            users_db[i] = UserResponse(id=user_id, **user.dict())
            return users_db[i]
    raise HTTPException(status_code=404, detail="User not found")

@app.delete("/users/{user_id}")
def delete_user(user_id: int):
    for i, u in enumerate(users_db):
        if u.id == user_id:
            users_db.pop(i)
            return {"message": "User deleted"}
    raise HTTPException(status_code=404, detail="User not found")
```

### FastAPI Query Parameters

```python
from fastapi import FastAPI, Query
from typing import Optional

app = FastAPI()

@app.get("/search")
def search(
    q: str = Query(..., min_length=3, description="Search query"),
    limit: int = Query(10, ge=1, le=100),
    offset: int = 0
):
    return {"query": q, "limit": limit, "offset": offset}

@app.get("/users")
def get_users(
    skip: int = 0,
    limit: int = 10,
    active: Optional[bool] = None
):
    return {"skip": skip, "limit": limit, "active": active}
```

### FastAPI Path Parameters & Validation

```python
from fastapi import FastAPI, Path
from enum import Enum

app = FastAPI()

class ModelName(str, Enum):
    alexnet = "alexnet"
    resnet = "resnet"
    lenet = "lenet"

@app.get("/models/{model_name}")
def get_model(model_name: ModelName):
    return {"model_name": model_name}

@app.get("/files/{file_path:path}")
def read_file(file_path: str = Path(..., description="File path")):
    return {"file_path": file_path}

@app.get("/items/{item_id}")
def get_item(
    item_id: int = Path(..., gt=0, le=1000, description="Item ID")
):
    return {"item_id": item_id}
```

### FastAPI Request Body

```python
from fastapi import FastAPI, Body
from pydantic import BaseModel

app = FastAPI()

class Item(BaseModel):
    name: str
    description: str | None = None
    price: float
    tax: float | None = None

@app.post("/items")
def create_item(item: Item):
    return item

# With additional body data
@app.post("/items-extra")
def create_item_extra(
    item: Item,
    importance: int = Body(..., ge=0)
):
    return {"item": item, "importance": importance}
```

### FastAPI Response Models

```python
from fastapi import FastAPI
from pydantic import BaseModel, EmailStr
from typing import Optional, List

app = FastAPI()

class UserOut(BaseModel):
    name: str
    email: EmailStr
    id: int

class UserIn(BaseModel):
    name: str
    email: EmailStr
    password: str

# FastAPI automatically converts UserIn to UserOut
@app.post("/users", response_model=UserOut)
def create_user(user: UserIn):
    # In real app, hash password before saving
    return UserOut(id=1, name=user.name, email=user.email)
```

### FastAPI Dependencies & Injection

```python
from fastapi import FastAPI, Depends
from typing import Optional

app = FastAPI()

# Simple dependency
def get_db():
    db = "database_connection"
    try:
        yield db
    finally:
        print("Close connection")

@app.get("/users")
def get_users(db: str = Depends(get_db)):
    return {"db": db}

# Dependency with parameters
def get_current_user(x_token: str = Depends(lambda: "user")):
    return {"user": "admin"}

@app.get("/protected")
def protected(user: dict = Depends(get_current_user)):
    return user
```

### FastAPI Authentication

```python
from fastapi import FastAPI, Depends, HTTPException, status
from fastapi.security import OAuth2PasswordBearer, OAuth2PasswordRequestForm
from pydantic import BaseModel
from datetime import datetime, timedelta
import jwt

app = FastAPI()
SECRET_KEY = "your-secret-key"
ALGORITHM = "HS256"

oauth2_scheme = OAuth2PasswordBearer(tokenUrl="token")

class Token(BaseModel):
    access_token: str
    token_type: str

class User(BaseModel):
    username: str

def create_access_token(data: dict, expires_delta: timedelta = None):
    to_encode = data.copy()
    expire = datetime.utcnow() + (expires_delta or timedelta(minutes=15))
    to_encode.update({"exp": expire})
    return jwt.encode(to_encode, SECRET_KEY, algorithm=ALGORITHM)

@app.post("/token", response_model=Token)
async def login(form_data: OAuth2PasswordRequestForm = Depends()):
    if form_data.username == "admin" and form_data.password == "secret":
        token = create_access_token(data={"sub": form_data.username})
        return {"access_token": token, "token_type": "bearer"}
    raise HTTPException(
        status_code=status.HTTP_401_UNAUTHORIZED,
        detail="Incorrect username or password"
    )

@app.get("/users/me")
async def read_users_me(token: str = Depends(oauth2_scheme)):
    return {"token": token}
```

### FastAPI Middleware

```python
from fastapi import FastAPI, Request
from fastapi.middleware.cors import CORSMiddleware
from fastapi.middleware.trustedhost import TrustedHostMiddleware
import time

app = FastAPI()

# CORS middleware
app.add_middleware(
    CORSMiddleware,
    allow_origins=["http://localhost:3000"],
    allow_credentials=True,
    allow_methods=["*"],
    allow_headers=["*"],
)

# Custom middleware
@app.middleware("http")
async def add_process_time_header(request: Request, call_next):
    start_time = time.time()
    response = await call_next(request)
    process_time = time.time() - start_time
    response.headers["X-Process-Time"] = str(process_time)
    return response
```

### FastAPI Error Handling

```python
from fastapi import FastAPI, HTTPException, Request
from fastapi.responses import JSONResponse

app = FastAPI()

@app.exception_handler(HTTPException)
async def http_exception_handler(request: Request, exc: HTTPException):
    return JSONResponse(
        status_code=exc.status_code,
        content={"detail": exc.detail}
    )

@app.exception_handler(Exception)
async def general_exception_handler(request: Request, exc: Exception):
    return JSONResponse(
        status_code=500,
        content={"detail": "Internal server error"}
    )

@app.get("/error")
def trigger_error():
    raise HTTPException(status_code=400, detail="Custom error")
```

### FastAPI File Upload/Download

```python
from fastapi import FastAPI, UploadFile, File, HTTPException
from fastapi.responses import FileResponse
import aiofiles
import os

app = FastAPI()

UPLOAD_DIR = "uploads"
os.makedirs(UPLOAD_DIR, exist_ok=True)

@app.post("/upload")
async def upload_file(file: UploadFile = File(...)):
    file_path = os.path.join(UPLOAD_DIR, file.filename)
    async with aiofiles.open(file_path, "wb") as f:
        content = await file.read()
        await f.write(content)
    return {"filename": file.filename, "size": len(content)}

@app.get("/download/{filename}")
async def download_file(filename: str):
    file_path = os.path.join(UPLOAD_DIR, filename)
    if not os.path.exists(file_path):
        raise HTTPException(status_code=404, detail="File not found")
    return FileResponse(file_path, filename=filename)
```

### FastAPI WebSocket

```python
from fastapi import FastAPI, WebSocket, WebSocketDisconnect

app = FastAPI()

class ConnectionManager:
    def __init__(self):
        self.active_connections: list[WebSocket] = []

    async def connect(self, websocket: WebSocket):
        await websocket.accept()
        self.active_connections.append(websocket)

    def disconnect(self, websocket: WebSocket):
        self.active_connections.remove(websocket)

    async def send_personal_message(self, message: str, websocket: WebSocket):
        await websocket.send_text(message)

    async def broadcast(self, message: str):
        for connection in self.active_connections:
            await connection.send_text(message)

manager = ConnectionManager()

@app.websocket("/ws")
async def websocket_endpoint(websocket: WebSocket):
    await manager.connect(websocket)
    try:
        while True:
            data = await websocket.receive_text()
            await manager.broadcast(f"Message: {data}")
    except WebSocketDisconnect:
        manager.disconnect(websocket)
```

### FastAPI Background Tasks

```python
from fastapi import FastAPI, BackgroundTasks

app = FastAPI()

def write_log(message: str):
    with open("log.txt", "a") as f:
        f.write(f"{message}\n")

@app.post("/send-notification/{email}")
async def send_notification(email: str, background_tasks: BackgroundTasks):
    background_tasks.add_task(write_log, f"Notification sent to {email}")
    return {"message": "Notification scheduled"}
```

### FastAPI Dependency Override

```python
from fastapi import FastAPI, Depends
from typing import Optional

app = FastAPI()

async def get_database():
    return "real_database"

# Override for testing
def override_get_database():
    return "test_database"

@app.get("/items")
def get_items(db: str = Depends(get_database)):
    return {"db": db}

# In tests, override the dependency
app.dependency_overrides[get_database] = override_get_database
```

### FastAPI Async/Await

```python
from fastapi import FastAPI
import asyncio
import aiohttp

app = FastAPI()

@app.get("/sync")
def sync_endpoint():
    # Synchronous function
    return {"message": "Sync"}

@app.get("/async")
async def async_endpoint():
    # Asynchronous function
    await asyncio.sleep(1)
    return {"message": "Async"}

@app.get("/external")
async def external_api():
    async with aiohttp.ClientSession() as session:
        async with session.get("https://api.example.com/data") as response:
            data = await response.json()
    return data
```

### FastAPI Project Structure

```
my_fastapi_app/
├── app/
│   ├── __init__.py
│   ├── main.py
│   ├── routers/
│   │   ├── __init__.py
│   │   ├── users.py
│   │   └── items.py
│   ├── models/
│   │   ├── __init__.py
│   │   └── user.py
│   ├── schemas/
│   │   ├── __init__.py
│   │   └── user.py
│   ├── crud/
│   │   └── user.py
│   ├── database.py
│   └── dependencies.py
├── venv/
├── requirements.txt
└── .env
```

### FastAPI with SQLAlchemy

```bash
pip install sqlalchemy asyncpg aiomysql
```

```python
# database.py
from sqlalchemy.ext.asyncio import create_async_engine, AsyncSession
from sqlalchemy.orm import sessionmaker, declarative_base

DATABASE_URL = "sqlite+aiosqlite:///app.db"

engine = create_async_engine(DATABASE_URL, echo=True)
async_session = sessionmaker(engine, class_=AsyncSession, expire_on_commit=False)
Base = declarative_base()

async def get_db():
    async with async_session() as session:
        yield session

# models.py
from sqlalchemy import Column, Integer, String
from database import Base

class User(Base):
    __tablename__ = "users"
    id = Column(Integer, primary_key=True, index=True)
    name = Column(String)
    email = Column(String, unique=True)

# main.py
from fastapi import FastAPI, Depends
from sqlalchemy.ext.asyncio import AsyncSession
from database import get_db, Base, engine
from models import User

app = FastAPI()

@app.on_event("startup")
async def startup():
    async with engine.begin() as conn:
        await conn.run_sync(Base.metadata.create_all)

@app.get("/users")
async def get_users(db: AsyncSession = Depends(get_db)):
    result = await db.execute("SELECT * FROM users")
    return result.scalars().all()
```

### FastAPI OpenAPI Documentation

```python
from fastapi import FastAPI
from pydantic import BaseModel, Field

app = FastAPI(
    title="My API",
    description="API documentation with FastAPI",
    version="1.0.0",
    docs_url="/docs",
    redoc_url="/redoc"
)

class Item(BaseModel):
    name: str = Field(..., example="Item name")
    price: float = Field(..., example=9.99)

@app.post("/items")
def create_item(item: Item):
    return item
```

### FastAPI Best Practices

```
┌─────────────────────────────────────────────────────────────────┐
│                 FASTAPI BEST PRACTICES                          │
├─────────────────────────────────────────────────────────────────┤
│  ✓ Use Pydantic models for all data validation                  │
│  ✓ Use async/await for I/O operations                          │
│  ✓ Implement proper error handling                             │
│  ✓ Use dependency injection for shared logic                    │
│  ✓ Configure CORS properly for production                       │
│  ✓ Use background tasks for slow operations                    │
│  ✓ Add response_model to all endpoints                         │
│  ✓ Document with docstrings for OpenAPI                        │
└─────────────────────────────────────────────────────────────────┘
```

### Why FastAPI?

```
┌─────────────────────────────────────────────────────────────┐
│                  WHY CHOOSE FASTAPI?                        │
├─────────────────────────────────────────────────────────────┤
│  ⚡ High Performance    → On par with Node.js & Go          │
│  📚 Auto Documentation  → Built-in Swagger UI               │
│  🔒 Auto Type Safety    → Pydantic validation               │
│  ⭐ Async Support       → Handle thousands of requests      │
│  📦 Minimal Code       → Less boilerplate                  │
└─────────────────────────────────────────────────────────────┘
```

---

## 🍶 Flask: Micro-Framework

**Flask** is a lightweight WSGI web application framework (created in 2010). It's called "micro" because it keeps things simple but extensible.

### Installing Flask

```bash
# Create virtual environment
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows

# Install Flask
pip install flask
```

### Flask Hello World

```python
# app.py
from flask import Flask, jsonify, request, render_template

app = Flask(__name__)

@app.route("/")
def home():
    return jsonify({"message": "Hello, World!"})

@app.route("/api/users")
def get_users():
    return jsonify({"users": ["Alice", "Bob", "Charlie"]})

if __name__ == "__main__":
    app.run(debug=True)
```

### Running Flask

```bash
# Development
flask run

# Or
python app.py

# With custom host/port
flask run --host=0.0.0.0 --port=5000
```

### Flask Routes & Methods

```python
@app.route("/api/users", methods=["GET"])
def get_users():
    return jsonify({"users": [{"id": 1, "name": "John"}]})

@app.route("/api/users", methods=["POST"])
def create_user():
    data = request.get_json()
    return jsonify({"id": 1, "name": data["name"]}), 201

@app.route("/api/users/<int:user_id>", methods=["PUT"])
def update_user(user_id):
    data = request.get_json()
    return jsonify({"id": user_id, "name": data["name"]})

@app.route("/api/users/<int:user_id>", methods=["DELETE"])
def delete_user(user_id):
    return jsonify({"message": f"User {user_id} deleted"}), 204
```

### Flask with SQLite Database

```python
from flask import Flask, jsonify, request
import sqlite3

app = Flask(__name__)

def get_db():
    conn = sqlite3.connect("app.db")
    conn.row_factory = sqlite3.Row
    return conn

@app.route("/api/users", methods=["GET"])
def get_users():
    conn = get_db()
    users = conn.execute("SELECT * FROM users").fetchall()
    conn.close()
    return jsonify([dict(uid) for uid in users])

@app.route("/api/users", methods=["POST"])
def create_user():
    data = request.get_json()
    conn = get_db()
    cursor = conn.execute(
        "INSERT INTO users (name, email) VALUES (?, ?)",
        (data["name"], data["email"])
    )
    conn.commit()
    conn.close()
    return jsonify({"id": cursor.lastrowid}), 201

if __name__ == "__main__":
    # Initialize database
    conn = get_db()
    conn.execute("""
        CREATE TABLE IF NOT EXISTS users (
            id INTEGER PRIMARY KEY AUTOINCREMENT,
            name TEXT NOT NULL,
            email TEXT UNIQUE
        )
    """)
    conn.commit()
    conn.close()
    
    app.run(debug=True)
```

### Flask Blueprints (Modular Apps)

```python
# api/routes.py
from flask import Blueprint

api = Blueprint("api", __name__, url_prefix="/api")

@api.route("/users")
def get_users():
    return {"users": []}

@api.route("/posts")
def get_posts():
    return {"posts": []}

# main.py
from flask import Flask
from api.routes import api

app = Flask(__name__)
app.register_blueprint(api)

if __name__ == "__main__":
    app.run(debug=True)
```

### Flask with SQLAlchemy

```bash
pip install flask-sqlalchemy
```

```python
from flask import Flask
from flask_sqlalchemy import SQLAlchemy

app = Flask(__name__)
app.config["SQLALCHEMY_DATABASE_URI"] = "sqlite:///app.db"
app.config["SQLALCHEMY_TRACK_MODIFICATIONS"] = False

db = SQLAlchemy(app)

class User(db.Model):
    id = db.Column(db.Integer, primary_key=True)
    name = db.Column(db.String(100), nullable=False)
    email = db.Column(db.String(100), unique=True)

    def to_dict(self):
        return {"id": self.id, "name": self.name, "email": self.email}

# Create tables
with app.app_context():
    db.create_all()

@app.route("/api/users", methods=["GET"])
def get_users():
    users = User.query.all()
    return jsonify([u.to_dict() for u in users])

@app.route("/api/users", methods=["POST"])
def create_user():
    data = request.get_json()
    user = User(name=data["name"], email=data["email"])
    db.session.add(user)
    db.session.commit()
    return jsonify(user.to_dict()), 201
```

### Flask Session & Authentication

```python
from flask import Flask, request, jsonify, session
from functools import wraps

app = Flask(__name__)
app.secret_key = "your-secret-key"

def login_required(f):
    @wraps(f)
    def decorated(*args, **kwargs):
        if "user_id" not in session:
            return jsonify({"error": "Unauthorized"}), 401
        return f(*args, **kwargs)
    return decorated

@app.route("/login", methods=["POST"])
def login():
    data = request.get_json()
    if data["username"] == "admin" and data["password"] == "secret":
        session["user_id"] = 1
        return jsonify({"message": "Logged in"})
    return jsonify({"error": "Invalid credentials"}), 401

@app.route("/logout", methods=["POST"])
def logout():
    session.pop("user_id", None)
    return jsonify({"message": "Logged out"})

@app.route("/protected")
@login_required
def protected():
    return jsonify({"message": "Protected content"})
```

### Flask Error Handling

```python
@app.errorhandler(404)
def not_found(e):
    return jsonify({"error": "Not found"}), 404

@app.errorhandler(500)
def server_error(e):
    return jsonify({"error": "Server error"}), 500

# Custom error
@app.route("/api/users/<int:user_id>")
def get_user(user_id):
    user = User.query.get(user_id)
    if not user:
        return jsonify({"error": "User not found"}), 404
    return jsonify(user.to_dict())
```

### Flask WebSocket (Real-time)

```bash
pip install flask-socketio eventlet
```

```python
from flask import Flask, render_template
from flask_socketio import SocketIO, emit

app = Flask(__name__)
app.config["SECRET_KEY"] = "secret"
socketio = SocketIO(app)

@app.route("/")
def index():
    return render_template("index.html")

@socketio.on("message")
def handle_message(data):
    print(f"Received: {data}")
    emit("message", data, broadcast=True)

if __name__ == "__main__":
    socketio.run(app, debug=True)
```

### Flask Forms & Validation

```bash
pip install flask-wtf wtforms email_validator
```

```python
from flask import Flask, render_template, request, flash
from flask_wtf import FlaskForm
from wtforms import StringField, PasswordField, SubmitField
from wtforms.validators import DataRequired, Email, Length

app = Flask(__name__)
app.config["SECRET_KEY"] = "secret"

class LoginForm(FlaskForm):
    username = StringField("Username", validators=[DataRequired()])
    password = PasswordField("Password", validators=[DataRequired(), Length(min=6)])
    submit = SubmitField("Login")

@app.route("/login", methods=["GET", "POST"])
def login():
    form = LoginForm()
    if form.validate_on_submit():
        flash(f"Welcome, {form.username.data}!")
        return redirect("/dashboard")
    return render_template("login.html", form=form)
```

### Flask Logging

```python
import logging

app = Flask(__name__)

# Configure logging
logging.basicConfig(level=logging.INFO)
logger = logging.getLogger(__name__)

@app.route("/api/data")
def get_data():
    logger.info("Fetching data")
    return jsonify({"data": "example"})

@app.errorhandler(Exception)
def handle_exception(e):
    logger.error(f"Error: {str(e)}")
    return jsonify({"error": "Internal server error"}), 500
```

### Flask Configuration

```python
app.config["DEBUG"] = True
app.config["SECRET_KEY"] = "your-secret-key"
app.config["SQLALCHEMY_DATABASE_URI"] = "sqlite:///app.db"
app.config["JSON_SORT_KEYS"] = False
app.config["MAX_CONTENT_LENGTH"] = 16 * 1024 * 1024  # 16MB max

# Environment-based config
app.config.from_object("config.DevelopmentConfig")
# or
app.config.from_envvar("APP_CONFIG")
```

### Flask RESTful API

```bash
pip install flask-restful
```

```python
from flask import Flask
from flask_restful import Resource, Api, reqparse

app = Flask(__name__)
api = Api(app)

class HelloWorld(Resource):
    def get(self):
        return {"message": "Hello World"}
    
    def post(self):
        return {"message": "Created"}, 201

api.add_resource(HelloWorld, "/api/helloworld")

if __name__ == "__main__":
    app.run(debug=True)
```

### Flask CORS

```bash
pip install flask-cors
```

```python
from flask_cors import CORS

app = Flask(__name__)
CORS(app, resources={r"/api/*": {"origins": "http://localhost:3000"}})
```

### Flask File Upload

```python
from flask import Flask, request, send_from_directory
import os

app = Flask(__name__)
app.config["UPLOAD_FOLDER"] = "uploads"
os.makedirs(app.config["UPLOAD_FOLDER"], exist_ok=True)

@app.route("/upload", methods=["POST"])
def upload_file():
    if "file" not in request.files:
        return {"error": "No file"}, 400
    file = request.files["file"]
    file.save(os.path.join(app.config["UPLOAD_FOLDER"], file.filename))
    return {"message": "File uploaded"}

@app.route("/uploads/<filename>")
def uploaded_file(filename):
    return send_from_directory(app.config["UPLOAD_FOLDER"], filename)
```

### Flask Project Structure

```
my_flask_app/
├── app/
│   ├── __init__.py
│   ├── routes/
│   │   ├── __init__.py
│   │   ├── main.py
│   │   └── api.py
│   ├── models/
│   │   ├── __init__.py
│   │   └── user.py
│   ├── templates/
│   │   ├── base.html
│   │   └── index.html
│   └── static/
│       ├── css/
│       └── js/
├── venv/
├── requirements.txt
└── run.py
```

### Flask Best Practices

```
┌─────────────────────────────────────────────────────────────────┐
│                 FLASK BEST PRACTICES                             │
├─────────────────────────────────────────────────────────────────┤
│  ✓ Use Blueprints for modular code                              │
│  ✓ Use environment variables for secrets                        │
│  ✓ Enable debug mode only in development                        │
│  ✓ Use SQLAlchemy instead of raw SQL                            │
│  ✓ Implement proper error handling                              │
│  ✓ Use Flask CLI for commands                                    │
│  ✓ Use factories for app creation                               │
└─────────────────────────────────────────────────────────────────┘
```

### Flask Ecosystem

```
┌─────────────────────────────────────────────────────────────┐
│                    FLASK ECOSYSTEM                          │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│   Core:                  Extensions:                        │
│   ┌──────────────┐      ┌──────────────┐                   │
│   │ Flask-SQLAlchemy │  │ Flask-Login  │                   │
│   │ Flask-Migrate   │  │ Flask-WTF    │                   │
│   │ Flask-RESTful  │  │ Flask-CORS   │                   │
│   │ Flask-SocketIO │  │ Flask-Mail   │                   │
│   └──────────────┘      └──────────────┘                   │
│                                                             │
│   Perfect for:  → REST APIs, Microservices, Prototypes      │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

## 🐅 Django: Full-Stack Framework

**Django** is a high-level, batteries-included framework (released in 2005). Used by Instagram, Pinterest, Spotify.

### Installing Django

```bash
# Create virtual environment
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows

# Install Django
pip install django

# Create Django project
django-admin startproject myproject

# Start development server
cd myproject
python manage.py runserver
```

### Django Project Structure

```
myproject/
├── manage.py
├── myproject/
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   └── asgi.py
├── app/
│   ├── migrations/
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── tests.py
│   └── views.py
└── templates/
```

### Django Models

```python
# models.py
from django.db import models
from django.contrib.auth.models import User

class Article(models.Model):
    title = models.CharField(max_length=200)
    slug = models.SlugField(unique=True)
    content = models.TextField()
    author = models.ForeignKey(User, on_delete=models.CASCADE)
    created_at = models.DateTimeField(auto_now_add=True)
    updated_at = models.DateTimeField(auto_now=True)
    published = models.BooleanField(default=False)
    tags = models.ManyToManyField("Tag", blank=True)

    def __str__(self):
        return self.title

    class Meta:
        ordering = ["-created_at"]

class Tag(models.Model):
    name = models.CharField(max_length=50)

    def __str__(self):
        return self.name
```

### Django Model Fields

```python
from django.db import models

class ExampleModel(models.Model):
    # Text fields
    char_field = models.CharField(max_length=100)
    text_field = models.TextField()
    slug_field = models.SlugField()
    
    # Numeric fields
    integer_field = models.IntegerField()
    positive_integer = models.PositiveIntegerField()
    float_field = models.FloatField()
    decimal_field = models.DecimalField(max_digits=10, decimal_places=2)
    
    # Date/Time
    date_field = models.DateField()
    datetime_field = models.DateTimeField()
    time_field = models.TimeField()
    
    # Boolean
    boolean_field = models.BooleanField()
    null_boolean = models.NullBooleanField()
    
    # File
    file_field = models.FileField(upload_to="uploads/")
    image_field = models.ImageField(upload_to="images/")
    
    # Email & URL
    email_field = models.EmailField()
    url_field = models.URLField()
    
    # Choice field
    STATUS_CHOICES = [
        ("draft", "Draft"),
        ("published", "Published"),
    ]
    status = models.CharField(max_length=10, choices=STATUS_CHOICES)
    
    # Relationships
    foreign_key = models.ForeignKey("OtherModel", on_delete=models.CASCADE)
    many_to_many = models.ManyToManyField("TagModel")
    one_to_one = models.OneToOneField("Profile", on_delete=models.CASCADE)
```

### Django Views

```python
# views.py
from django.shortcuts import render, redirect, get_object_or_404
from django.http import JsonResponse
from django.views import View
from django.views.generic import ListView, DetailView, CreateView, UpdateView, DeleteView
from django.contrib.auth.mixins import LoginRequiredMixin
from .models import Article
from .forms import ArticleForm

# Function-based view
def article_list(request):
    articles = Article.objects.filter(published=True)
    return render(request, "app/article_list.html", {"articles": articles})

def article_detail(request, slug):
    article = get_object_or_404(Article, slug=slug)
    return render(request, "app/article_detail.html", {"article": article})

@login_required
def article_create(request):
    if request.method == "POST":
        form = ArticleForm(request.POST)
        if form.is_valid():
            article = form.save(commit=False)
            article.author = request.user
            article.save()
            return redirect("article_detail", slug=article.slug)
    else:
        form = ArticleForm()
    return render(request, "app/article_form.html", {"form": form})

# Class-based view
class ArticleListView(ListView):
    model = Article
    template_name = "app/article_list.html"
    context_object_name = "articles"
    paginate_by = 10

    def get_queryset(self):
        return Article.objects.filter(published=True)

class ArticleDetailView(DetailView):
    model = Article
    template_name = "app/article_detail.html"
    context_object_name = "article"

# API View (DRF)
from rest_framework.views import APIView
from rest_framework.response import Response
from rest_framework import status

class ArticleAPIView(APIView):
    def get(self, request):
        articles = Article.objects.all()
        # Serialize here or use DRF serializer
        return Response(ArticleSerializer(articles, many=True).data)

    def post(self, request):
        serializer = ArticleSerializer(data=request.data)
        if serializer.is_valid():
            serializer.save()
            return Response(serializer.data, status=status.HTTP_201_CREATED)
        return Response(serializer.errors, status=status.HTTP_400_BAD_REQUEST)
```

### Django URLs

```python
# urls.py (project)
from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path("admin/", admin.site.urls),
    path("api/", include("api.urls")),
    path("", include("app.urls")),
]

# urls.py (app)
from django.urls import path
from . import views

urlpatterns = [
    path("", views.article_list, name="article_list"),
    path("article/<slug:slug>/", views.article_detail, name="article_detail"),
    path("create/", views.article_create, name="article_create"),
]
```

### Django Forms

```python
# forms.py
from django import forms
from .models import Article

class ArticleForm(forms.ModelForm):
    class Meta:
        model = Article
        fields = ["title", "content", "published", "tags"]
        widgets = {
            "content": forms.Textarea(attrs={"rows": 10, "class": "form-control"}),
            "title": forms.TextInput(attrs={"class": "form-control"}),
        }

# Custom validation
class ArticleForm(forms.ModelForm):
    class Meta:
        model = Article
        fields = ["title", "content"]

    def clean_title(self):
        title = self.cleaned_data["title"]
        if len(title) < 10:
            raise forms.ValidationError("Title must be at least 10 characters")
        return title
```

### Django Admin

```python
# admin.py
from django.contrib import admin
from .models import Article, Tag

@admin.register(Article)
class ArticleAdmin(admin.ModelAdmin):
    list_display = ["title", "author", "status", "created_at"]
    list_filter = ["status", "created_at", "author"]
    search_fields = ["title", "content"]
    prepopulated_fields = {"slug": ("title",)}
    date_hierarchy = "created_at"
    ordering = ["-created_at"]
    
    fieldsets = (
        ("Basic Info", {
            "fields": ("title", "slug", "content")
        }),
        ("Publishing", {
            "fields": ("status", "published", "author")
        }),
    )

@admin.register(Tag)
class TagAdmin(admin.ModelAdmin):
    list_display = ["name"]
```

### Django ORM Queries

```python
# Create
article = Article.objects.create(
    title="My Article",
    content="Content here",
    author=user
)

# Read
all_articles = Article.objects.all()
published = Article.objects.filter(published=True)
single = Article.objects.get(id=1)

# Update
article = Article.objects.get(id=1)
article.title = "New Title"
article.save()

# Delete
article.delete()

# Related objects
user.articles.all()
article.tags.all()

# Complex queries
from django.db.models import Q

# OR condition
Article.objects.filter(Q(title__icontains="python") | Q(content__icontains="python"))

# AND condition
Article.objects.filter(published=True, author=user)

# Exclude
Article.objects.exclude(author=user)

# Ordering
Article.objects.order_by("-created_at")

# Limit
Article.objects.all()[:10]

# Count
Article.objects.count()

# Exists
Article.objects.filter(id=1).exists()
```

### Django Templates

```html
<!-- base.html -->
<!DOCTYPE html>
<html>
<head>
    <title>{% block title %}My Blog{% endblock %}</title>
    <link rel="stylesheet" href="{% static 'css/style.css' %}">
</head>
<body>
    <nav>
        <a href="{% url 'article_list' %}">Home</a>
        {% if user.is_authenticated %}
            <a href="{% url 'article_create' %}">New Article</a>
            <form action="{% url 'logout' %}" method="post">
                {% csrf_token %}
                <button type="submit">Logout</button>
            </form>
        {% else %}
            <a href="{% url 'login' %}">Login</a>
        {% endif %}
    </nav>
    
    {% block content %}{% endblock %}
</body>
</html>

<!-- article_list.html -->
{% extends 'base.html' %}

{% block title %}Articles{% endblock %}

{% block content %}
<h1>Articles</h1>

{% for article in articles %}
    <article>
        <h2><a href="{% url 'article_detail' article.slug %}">{{ article.title }}</a></h2>
        <p>By {{ article.author.username }} on {{ article.created_at }}</p>
        <p>{{ article.content|truncatewords:50 }}</p>
    </article>
{% empty %}
    <p>No articles yet.</p>
{% endfor %}

{% if is_paginated %}
    <div class="pagination">
        {% if page_obj.has_previous %}
            <a href="?page=1">First</a>
            <a href="?page={{ page_obj.previous_page_number }}">Previous</a>
        {% endif %}
        
        Page {{ page_obj.number }} of {{ page_obj.paginator.num_pages }}
        
        {% if page_obj.has_next %}
            <a href="?page={{ page_obj.next_page_number }}">Next</a>
            <a href="?page={{ page_obj.paginator.num_pages }}">Last</a>
        {% endif %}
    </div>
{% endif %}
{% endblock %}
```

### Django REST Framework

```bash
pip install djangorestframework
```

```python
# serializers.py
from rest_framework import serializers
from .models import Article

class ArticleSerializer(serializers.ModelSerializer):
    author_username = serializers.CharField(source="author.username", read_only=True)
    
    class Meta:
        model = Article
        fields = ["id", "title", "slug", "content", "author", "author_username", "created_at", "tags"]
        read_only_fields = ["author", "created_at"]

# views.py
from rest_framework import viewsets
from rest_framework.permissions import IsAuthenticatedOrReadOnly

class ArticleViewSet(viewsets.ModelViewSet):
    queryset = Article.objects.all()
    serializer_class = ArticleSerializer
    permission_classes = [IsAuthenticatedOrReadOnly]
    lookup_field = "slug"

    def perform_create(self, serializer):
        serializer.save(author=self.request.user)

# urls.py
from rest_framework.routers import DefaultRouter
from .views import ArticleViewSet

router = DefaultRouter()
router.register(r"articles", ArticleViewSet)

urlpatterns = router.urls
```

### Django Authentication

```bash
# settings.py
INSTALLED_APPS = [
    ...
    "django.contrib.auth",
    "django.contrib.sessions",
]

# urls.py
from django.contrib.auth import views as auth_views

urlpatterns = [
    path("login/", auth_views.LoginView.as_view(), name="login"),
    path("logout/", auth_views.LogoutView.as_view(), name="logout"),
    path("password_change/", auth_views.PasswordChangeView.as_view(), name="password_change"),
    path("password_reset/", auth_views.PasswordResetView.as_view(), name="password_reset"),
]
```

### Django Settings

```python
# settings.py - Important settings
SECRET_KEY = "your-secret-key-here"
DEBUG = True  # False in production
ALLOWED_HOSTS = ["localhost", "yourdomain.com"]

INSTALLED_APPS = [
    "django.contrib.admin",
    "django.contrib.auth",
    "django.contrib.contenttypes",
    "django.contrib.sessions",
    "django.contrib.messages",
    "django.contrib.staticfiles",
    "rest_framework",
    "app",
]

DATABASES = {
    "default": {
        "ENGINE": "django.db.backends.sqlite3",
        "NAME": BASE_DIR / "db.sqlite3",
    }
}

# For PostgreSQL
DATABASES = {
    "default": {
        "ENGINE": "django.db.backends.postgresql",
        "NAME": "mydb",
        "USER": "user",
        "PASSWORD": "password",
        "HOST": "localhost",
        "PORT": "5432",
    }
}

# Static & Media files
STATIC_URL = "/static/"
STATIC_ROOT = BASE_DIR / "staticfiles"

MEDIA_URL = "/media/"
MEDIA_ROOT = BASE_DIR / "media"

# Authentication
LOGIN_REDIRECT_URL = "home"
LOGOUT_REDIRECT_URL = "home"

# REST Framework
REST_FRAMEWORK = {
    "DEFAULT_AUTHENTICATION_CLASSES": [
        "rest_framework.authentication.SessionAuthentication",
    ],
    "DEFAULT_PERMISSION_CLASSES": [
        "rest_framework.permissions.IsAuthenticatedOrReadOnly",
    ],
}
```

### Django Migrations

```bash
# Create migrations
python manage.py makemigrations

# Apply migrations
python manage.py migrate

# Show migrations
python manage.py showmigrations

# SQL for migrations
python manage.py sqlmigrate app 0001

# Rollback
python manage.py migrate app 0002  # Go back to specific migration
python manage.py migrate app zero   # Undo all migrations
```

### Django Middleware

```python
# middleware.py
def my_middleware(get_response):
    def middleware(request):
        # Before view
        response = get_response(request)
        # After view
        return response
    return middleware

# settings.py
MIDDLEWARE = [
    "django.middleware.security.SecurityMiddleware",
    "django.contrib.sessions.middleware.SessionMiddleware",
    "django.middleware.common.CommonMiddleware",
    "django.middleware.csrf.CsrfViewMiddleware",
    "django.contrib.auth.middleware.AuthenticationMiddleware",
    "django.contrib.messages.middleware.MessageMiddleware",
    "myapp.middleware.my_middleware",
]
```

### Django Signals

```python
from django.db.models.signals import post_save, pre_delete
from django.dispatch import receiver
from .models import Article

@receiver(post_save, sender=Article)
def article_created(sender, instance, created, **kwargs):
    if created:
        # Send notification
        print(f"New article created: {instance.title}")

@receiver(pre_delete, sender=Article)
def article_deleted(sender, instance, **kwargs):
    # Clean up
    print(f"Article deleted: {instance.title}")
```

### Django Testing

```bash
# Create test
python manage.py test

# Run specific app
python manage.py test myapp

# With coverage
pip install coverage
coverage run --manage.py test
coverage report
```

```python
# tests.py
from django.test import TestCase, Client
from django.contrib.auth.models import User
from .models import Article

class ArticleTestCase(TestCase):
    def setUp(self):
        self.user = User.objects.create_user("testuser", "test@example.com", "password")
        
    def test_article_list(self):
        response = self.client.get("/")
        self.assertEqual(response.status_code, 200)
        
    def test_article_create(self):
        self.client.login(username="testuser", password="password")
        response = self.client.post("/create/", {
            "title": "Test Article",
            "content": "Test content",
        })
        self.assertEqual(response.status_code, 302)
        self.assertTrue(Article.objects.filter(title="Test Article").exists())
```

### Django Deployment

```bash
# Collect static files
python manage.py collectstatic

# Gunicorn
pip install gunicorn

# Run with gunicorn
gunicorn myproject.wsgi --bind 0.0.0.0:8000 --workers 4
```

```python
# Procfile (for Heroku/Render)
web: gunicorn myproject.wsgi --bind 0.0.0.0:$PORT
```

### Django Project Structure (Large Apps)

```
myproject/
├── manage.py
├── myproject/
│   ├── __init__.py
│   ├── settings/
│   │   ├── __init__.py
│   │   ├── base.py
│   │   ├── development.py
│   │   └── production.py
│   ├── urls.py
│   └── wsgi.py
├── apps/
│   ├── users/
│   │   ├── migrations/
│   │   ├── __init__.py
│   │   ├── admin.py
│   │   ├── apps.py
│   │   ├── models.py
│   │   ├── views.py
│   │   ├── serializers.py
│   │   ├── urls.py
│   │   └── tests.py
│   └── blog/
│       ├── migrations/
│       ├── __init__.py
│       └── ...
├── templates/
├── static/
├── media/
├── requirements.txt
└── .env
```

### Django Best Practices

```
┌─────────────────────────────────────────────────────────────────┐
│                 DJANGO BEST PRACTICES                           │
├─────────────────────────────────────────────────────────────────┤
│  ✓ Use virtual environments                                     │
│  ✓ Keep settings modular (dev/prod)                           │
│  ✓ Use Django ORM, avoid raw SQL                               │
│  ✓ Implement proper model indexes                              │
│  ✓ Use class-based views for complex views                    │
│  ✓ Write tests for critical paths                             │
│  ✓ Use migrations for all DB changes                          │
│  ✓ Implement proper error logging                             │
│  ✓ Use Django signals for decoupled logic                     │
│  ✓ Secure your SECRET_KEY in production                        │
└─────────────────────────────────────────────────────────────────┘
```

### Django's "Batteries Included" Philosophy

```
┌─────────────────────────────────────────────────────────────────┐
│                  DJANGO BUILT-IN FEATURES                       │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│   ┌──────────────┐  ┌──────────────┐  ┌──────────────┐        │
│   │   Admin UI   │  │   ORM        │  │  Forms       │        │
│   │  (Built-in)  │  │  (Database)  │  │  (Handling)  │        │
│   └──────────────┘  └──────────────┘  └──────────────┘        │
│                                                                 │
│   ┌──────────────┐  ┌──────────────┐  ┌──────────────┐        │
│   │  Authentication│ │  URL Routing │  │  Template    │        │
│   │   System      │  │  (Built-in)  │  │  Engine      │        │
│   └──────────────┘  └──────────────┘  └──────────────┘        │
│                                                                 │
│   Perfect for:  → Large apps, CMS, E-commerce, Social networks │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### Flask vs Django vs FastAPI

| Feature | Flask | Django | FastAPI |
|---------|-------|--------|---------|
| **Type** | Micro | Full-Stack | API Framework |
| **Learning Curve** | Low | Medium | Low |
| **Built-in Admin** | ❌ | ✅ | ❌ |
| **Async Support** | ⚠️ Extensions | ❌ | ✅ Native |
| **Best For** | APIs, Small Apps | Large Apps | Modern APIs |
| **Database ORM** | SQLAlchemy (choice) | Django ORM | SQLModel |

---

## 💾 Databases & SQLite

### What is SQLite?

**SQLite** is a lightweight, file-based database that requires no server setup. Perfect for learning and small projects.

### Installing SQLite

```bash
# SQLite comes pre-installed with Python
# No installation needed!

# Verify
python -c "import sqlite3; print(sqlite3.sqlite_version)"
```

### SQLite Basic Operations

```python
import sqlite3
from contextlib import contextmanager

@contextmanager
def get_db(db_name="app.db"):
    conn = sqlite3.connect(db_name)
    conn.row_factory = sqlite3.Row
    try:
        yield conn
    finally:
        conn.close()

# Create table
with get_db() as conn:
    conn.execute("""
        CREATE TABLE IF NOT EXISTS users (
            id INTEGER PRIMARY KEY AUTOINCREMENT,
            name TEXT NOT NULL,
            email TEXT UNIQUE,
            created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
        )
    """)
    conn.commit()

# Insert data
with get_db() as conn:
    conn.execute(
        "INSERT INTO users (name, email) VALUES (?, ?)",
        ("John", "john@example.com")
    )
    conn.commit()

# Read data
with get_db() as conn:
    cursor = conn.execute("SELECT * FROM users WHERE id = ?", (1,))
    user = cursor.fetchone()
    print(dict(user))  # {'id': 1, 'name': 'John', 'email': 'john@example.com', ...}

# Update data
with get_db() as conn:
    conn.execute(
        "UPDATE users SET name = ? WHERE id = ?",
        ("Jane", 1)
    )
    conn.commit()

# Delete data
with get_db() as conn:
    conn.execute("DELETE FROM users WHERE id = ?", (1,))
    conn.commit()

# Query with filters
with get_db() as conn:
    cursor = conn.execute(
        "SELECT * FROM users WHERE name LIKE ? ORDER BY created_at DESC",
        ("%John%",)
    )
    users = cursor.fetchall()
```

### SQL Basics

```sql
-- CREATE TABLE
CREATE TABLE users (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL,
    age INTEGER,
    is_active BOOLEAN DEFAULT 1,
    created_at DATETIME DEFAULT CURRENT_TIMESTAMP
);

-- INSERT
INSERT INTO users (name, email, age) VALUES ('John', 'john@example.com', 25);
INSERT INTO users (name, email) VALUES ('Jane', 'jane@example.com');

-- SELECT
SELECT * FROM users;
SELECT name, email FROM users;
SELECT * FROM users WHERE age > 18;
SELECT * FROM users WHERE name LIKE 'J%';
SELECT * FROM users ORDER BY created_at DESC;
SELECT * FROM users LIMIT 10 OFFSET 0;

-- UPDATE
UPDATE users SET age = 26 WHERE name = 'John';

-- DELETE
DELETE FROM users WHERE id = 1;

-- Aggregate functions
SELECT COUNT(*) FROM users;
SELECT AVG(age) FROM users;
SELECT MAX(age), MIN(age) FROM users;

-- JOINs
SELECT users.name, orders.total FROM users
INNER JOIN orders ON users.id = orders.user_id;

-- GROUP BY
SELECT COUNT(*), age FROM users GROUP BY age;

-- ALTER TABLE
ALTER TABLE users ADD COLUMN phone VARCHAR(20);
ALTER TABLE users DROP COLUMN phone;
```

### SQLite with Flask

```bash
pip install flask-sqlalchemy
```

```python
from flask import Flask
from flask_sqlalchemy import SQLAlchemy

app = Flask(__name__)
app.config["SQLALCHEMY_DATABASE_URI"] = "sqlite:///app.db"
app.config["SQLALCHEMY_TRACK_MODIFICATIONS"] = False

db = SQLAlchemy(app)

class User(db.Model):
    id = db.Column(db.Integer, primary_key=True)
    name = db.Column(db.String(100), nullable=False)
    email = db.Column(db.String(100), unique=True, nullable=False)
    age = db.Column(db.Integer)

    def to_dict(self):
        return {"id": self.id, "name": self.name, "email": self.email}

# Create all tables
with app.app_context():
    db.create_all()

@app.route("/users", methods=["GET"])
def get_users():
    users = User.query.all()
    return {"users": [u.to_dict() for u in users]}

@app.route("/users", methods=["POST"])
def create_user():
    data = request.get_json()
    user = User(name=data["name"], email=data["email"])
    db.session.add(user)
    db.session.commit()
    return user.to_dict(), 201
```

### PostgreSQL

#### Installing PostgreSQL

```bash
# Windows - Download from https://www.postgresql.org/download/windows/
# macOS
brew install postgresql
brew services start postgresql

# Linux (Ubuntu)
sudo apt install postgresql postgresql-contrib
sudo systemctl start postgresql
sudo systemctl enable postgresql
```

#### PostgreSQL with Python

```bash
pip install psycopg2-binary
```

```python
import psycopg2
from psycopg2.extras import RealDictCursor

# Connect to PostgreSQL
conn = psycopg2.connect(
    host="localhost",
    database="mydb",
    user="postgres",
    password="password"
)
conn.set_session(cursor_factory=RealDictCursor)

# Create table
with conn.cursor() as cursor:
    cursor.execute("""
        CREATE TABLE IF NOT EXISTS users (
            id SERIAL PRIMARY KEY,
            name VARCHAR(100) NOT NULL,
            email VARCHAR(100) UNIQUE NOT NULL,
            created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
        )
    """)
    conn.commit()

# Insert with returning
with conn.cursor() as cursor:
    cursor.execute(
        "INSERT INTO users (name, email) VALUES (%s, %s) RETURNING id, name, email",
        ("John", "john@example.com")
    )
    user = cursor.fetchone()
    conn.commit()
    print(user)  # {'id': 1, 'name': 'John', 'email': 'john@example.com'}
```

#### PostgreSQL with SQLAlchemy

```python
from sqlalchemy import create_engine
from sqlalchemy.orm import sessionmaker
from sqlalchemy.ext.declarative import declarative_base

DATABASE_URL = "postgresql://user:password@localhost/mydb"

engine = create_engine(DATABASE_URL)
Session = sessionmaker(bind=engine)
Base = declarative_base()

class User(Base):
    __tablename__ = "users"
    id = db.Column(db.Integer, primary_key=True)
    name = db.Column(db.String(100))
    email = db.Column(db.String(100), unique=True)

# Create tables
Base.metadata.create_all(engine)

# Use session
session = Session()
user = User(name="John", email="john@example.com")
session.add(user)
session.commit()
```

### MySQL

```bash
pip install mysql-connector-python
# or
pip install pymysql
```

```python
import mysql.connector

conn = mysql.connector.connect(
    host="localhost",
    database="mydb",
    user="root",
    password="password"
)

with conn.cursor() as cursor:
    cursor.execute("SELECT * FROM users")
    users = cursor.fetchall()
```

### MongoDB (NoSQL)

```bash
pip install pymongo
```

```python
from pymongo import MongoClient

# Connect to MongoDB
client = MongoClient("mongodb://localhost:27017/")
db = client["mydb"]
collection = db["users"]

# Insert document
user = {"name": "John", "email": "john@example.com", "age": 25}
result = collection.insert_one(user)
print(result.inserted_id)

# Insert multiple
users = [
    {"name": "Jane", "email": "jane@example.com"},
    {"name": "Bob", "email": "bob@example.com"}
]
result = collection.insert_many(users)

# Find one
user = collection.find_one({"name": "John"})

# Find all
for user in collection.find({"age": {"$gt": 20}}):
    print(user)

# Update
collection.update_one(
    {"name": "John"},
    {"$set": {"age": 26}}
)

# Delete
collection.delete_one({"name": "John"})
```

### MongoDB with Flask

```bash
pip install flask-pymongo
```

```python
from flask import Flask, jsonify, request
from flask_pymongo import PyMongo

app = Flask(__name__)
app.config["MONGO_URI"] = "mongodb://localhost:27017/mydb"
mongo = PyMongo(app)

@app.route("/users", methods=["GET"])
def get_users():
    users = list(mongo.db.users.find())
    for user in users:
        user["_id"] = str(user["_id"])
    return jsonify(users)

@app.route("/users", methods=["POST"])
def create_user():
    data = request.get_json()
    user_id = mongo.db.users.insert_one(data).inserted_id
    return jsonify({"id": str(user_id)}), 201
```

### Redis (Cache & Sessions)

```bash
pip install redis
```

```python
import redis
from datetime import timedelta

# Connect to Redis
r = redis.Redis(host="localhost", port=6379, db=0)

# String operations
r.set("name", "John")
r.get("name")  # b'John'

# With expiration
r.setex("temp_token", timedelta(hours=1), "token_value")

# List operations
r.push("queue", "task1")
r.pop("queue")

# Hash operations
r.hset("user:1", "name", "John")
r.hget("user:1", "name")

# Check if key exists
r.exists("name")

# Delete
r.delete("name")

# Get all keys
r.keys("*")
```

### Redis with FastAPI

```bash
pip install fastapi-cache2
```

```python
from fastapi import FastAPI
from fastapi_cache import FastAPICache
from fastapi_cache.backends.redis import RedisBackend

app = FastAPI()

@app.on_event("startup")
async def startup():
    FastAPICache.init(RedisBackend(redis_url="redis://localhost"), prefix="fastapi-cache")

@app.get("/cached")
@cache(expire=60)
async def cached_endpoint():
    return {"data": "expensive computation"}
```

### Database Types for Python Web

```
┌─────────────────────────────────────────────────────────────────┐
│                    DATABASE OPTIONS                             │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│   SQLite  →  Small apps, learning, prototypes                  │
│   ──────────────────────────────────────────────────────────    │
│   PostgreSQL  →  Production apps, complex data                 │
│   ──────────────────────────────────────────────────────────    │
│   MySQL      →  Traditional web apps                           │
│   ──────────────────────────────────────────────────────────    │
│   MongoDB    →  NoSQL, flexible schemas                        │
│   ──────────────────────────────────────────────────────────    │
│   Redis      →  Caching, sessions, real-time                   │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### ORM (Object-Relational Mapping)

```
┌─────────────────────────────────────────────────────────────────┐
│                    ORM CONCEPT                                  │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│   Without ORM:              With ORM:                          │
│   ┌─────────────┐            ┌─────────────┐                  │
│   │ SQL Query   │            │ Python Code │                  │
│   │ ─────────── │            │ ─────────── │                  │
│   │ SELECT *   │            │ User.objects│                  │
│   │ FROM users │     =>     │  .all()     │                  │
│   │ WHERE...   │            │             │                  │
│   └─────────────┘            └─────────────┘                  │
│                                                                 │
│   Popular ORMs:  SQLAlchemy, Django ORM, Peewee, SQLModel      │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### SQLAlchemy (ORM)

```bash
pip install sqlalchemy
```

```python
from sqlalchemy import create_engine, Column, Integer, String
from sqlalchemy.orm import sessionmaker, declarative_base

Base = declarative_base()

class User(Base):
    __tablename__ = "users"
    id = Column(Integer, primary_key=True)
    name = Column(String(100), nullable=False)
    email = Column(String(100), unique=True)

# Create engine
engine = create_engine("sqlite:///app.db")
Base.metadata.create_all(engine)

# Create session
Session = sessionmaker(bind=engine)
session = Session()

# Create
user = User(name="John", email="john@example.com")
session.add(user)
session.commit()

# Read
users = session.query(User).all()
user = session.query(User).filter_by(name="John").first()

# Update
user.name = "Jane"
session.commit()

# Delete
session.delete(user)
session.commit()
```

### SQLModel (FastAPI ORM)

```bash
pip install sqlmodel
```

```python
from sqlmodel import SQLModel, Field, Session, create_engine
from typing import Optional

class User(SQLModel, table=True):
    id: Optional[int] = Field(default=None, primary_key=True)
    name: str
    email: str = Field(unique=True)

# Create engine
engine = create_engine("sqlite:///app.db")
SQLModel.metadata.create_all(engine)

# Create user
with Session(engine) as session:
    user = User(name="John", email="john@example.com")
    session.add(user)
    session.commit()
```

### Database Best Practices

```
┌─────────────────────────────────────────────────────────────────┐
│              DATABASE BEST PRACTICES                           │
├─────────────────────────────────────────────────────────────┤
│  ✓ Use connection pooling in production                       │
│  ✓ Implement proper database indexing                         │
│  ✓ Use parameterized queries (prevent SQL injection)         │
│  ✓ Use migrations for schema changes                         │
│  ✓ Implement proper backup strategy                           │
│  ✓ Use transactions for atomic operations                    │
│  ✓ Monitor query performance                                  │
│  ✓ Use environment variables for credentials                  │
│  ✓ Implement proper error handling                           │
│  ✓ Separate read/write operations when needed                │
└─────────────────────────────────────────────────────────────────┘
```

---

## 🎨 Frontend Integration

### How Python Web Talks to Frontend

```
┌─────────────────────────────────────────────────────────────────┐
│               FRONTEND-BACKEND COMMUNICATION                    │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│   Browser (Frontend)          Server (Backend)                  │
│   ┌─────────────┐            ┌─────────────┐                  │
│   │   React     │ ◄────────► │  FastAPI    │                  │
│   │   Vue       │   HTTP/    │  Flask      │                  │
│   │   Angular   │   REST     │  Django     │                  │
│   │   Vanilla   │            │             │                  │
│   └─────────────┘            └─────────────┘                  │
│        │                            │                          │
│        │        JSON Data            │                          │
│        └────────────────────────────┘                          │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### Returning HTML (Server-Side Rendering)

#### Flask with Jinja2
```python
from flask import render_template

@app.route("/")
def home():
    return render_template("index.html", name="John")

# templates/index.html
# <h1>Hello, {{ name }}!</h1>
```

#### Django Templates
```python
# views.py
from django.shortcuts import render

def home(request):
    return render(request, "index.html", {"name": "John"})

# templates/index.html
# <h1>Hello, {{ name }}!</h1>
```

### Returning JSON (REST API)

#### FastAPI
```python
from fastapi import FastAPI
from pydantic import BaseModel

app = FastAPI()

class User(BaseModel):
    name: str
    email: str

@app.get("/api/users")
def get_users():
    return [{"name": "John", "email": "john@example.com"}]

@app.post("/api/users")
def create_user(user: User):
    return {"name": user.name, "email": user.user_email}
```

#### Flask
```python
from flask import jsonify

@app.route("/api/users", methods=["GET"])
def get_users():
    return jsonify([
        {"name": "John", "email": "john@example.com"}
    ])
```

### AJAX/Fetch from Frontend

```javascript
// JavaScript Fetch API
async function getUsers() {
    const response = await fetch("/api/users");
    const data = await response.json();
    console.log(data);
}

fetch("/api/users", {
    method: "POST",
    headers: { "Content-Type": "application/json" },
    body: JSON.stringify({ name: "John", email: "john@example.com" })
});
```

### CORS (Cross-Origin Resource Sharing)

```python
# Flask
from flask_cors import CORS
CORS(app)

# FastAPI (built-in)
from fastapi import FastAPI
from fastapi.middleware.cors import CORSMiddleware

app = FastAPI()
app.add_middleware(
    CORSMiddleware,
    allow_origins=["http://localhost:3000"],
    allow_credentials=True,
    allow_methods=["*"],
    allow_headers=["*"],
)
```

---

## 🔐 Authentication & Security

### JWT (JSON Web Tokens)

```
┌─────────────────────────────────────────────────────────────────┐
│                      JWT FLOW                                  │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│   1. Client sends credentials                                   │
│           │                                                     │
│           ▼                                                     │
│   2. Server validates & returns JWT                            │
│           │                                                     │
│           ▼                                                     │
│   3. Client stores JWT (localStorage/cookie)                    │
│           │                                                     │
│           ▼                                                     │
│   4. Client sends JWT with each request                        │
│           │                                                     │
│           ▼                                                     │
│   5. Server verifies JWT before allowing access               │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### JWT Implementation with FastAPI

```python
from fastapi import FastAPI, Depends, HTTPException, status
from fastapi.security import OAuth2PasswordBearer, OAuth2PasswordRequestForm
from pydantic import BaseModel
from datetime import datetime, timedelta
import jwt

app = FastAPI()
SECRET_KEY = "your-secret-key"
ALGORITHM = "HS256"

oauth2_scheme = OAuth2PasswordBearer(tokenUrl="token")

def create_access_token(data: dict, expires_delta: timedelta = None):
    to_encode = data.copy()
    expire = datetime.utcnow() + (expires_delta or timedelta(minutes=15))
    to_encode.update({"exp": expire})
    return jwt.encode(to_encode, SECRET_KEY, algorithm=ALGORITHM)

@app.post("/token")
async def login(form_data: OAuth2PasswordRequestForm = Depends()):
    if form_data.username == "admin" and form_data.password == "secret":
        token = create_access_token(data={"sub": form_data.username})
        return {"access_token": token, "token_type": "bearer"}
    raise HTTPException(status_code=400, detail="Incorrect credentials")

@app.get("/protected")
async def read_protected(token: str = Depends(oauth2_scheme)):
    return {"token": token}
```

### JWT with Flask

```python
import jwt
from flask import Flask, request, jsonify
from functools import wraps

app = Flask(__name__)
SECRET_KEY = "your-secret-key"

def token_required(f):
    @wraps(f)
    def decorated(*args, **kwargs):
        token = request.headers.get("x-access-token")
        if not token:
            return jsonify({"message": "Token is missing"}), 401
        try:
            jwt.decode(token, SECRET_KEY, algorithms=["HS256"])
        except:
            return jsonify({"message": "Token is invalid"}), 401
        return f(*args, **kwargs)
    return decorated

@app.route("/protected", methods=["GET"])
@token_required
def protected():
    return jsonify({"message": "Protected data"})

@app.route("/login", methods=["POST"])
def login():
    # Verify credentials
    token = jwt.encode({"user": "admin"}, SECRET_KEY, algorithm="HS256")
    return jsonify({"token": token})
```

### Password Hashing

```python
from passlib.hash import bcrypt

# Hash password
def hash_password(password):
    return bcrypt.hash(password)

# Verify password
def verify_password(password, hashed):
    return bcrypt.verify(password, hashed)

# Usage
hashed = hash_password("mypassword")
verify_password("mypassword", hashed)  # True
```

### OAuth 2.0 (Social Login)

```python
# Using FastAPI with Google OAuth
from fastapi import FastAPI
from fastapi.security import OAuth2PasswordBearer
from authlib.integrations.starlette_client import OAuth

app = FastAPI()
oauth = OAuth(app)
google = oauth.register(
    name="google",
    client_id="YOUR_CLIENT_ID",
    client_secret="YOUR_CLIENT_SECRET",
    server_metadata_url="https://accounts.google.com/.well-known/openid-configuration",
    client_kwargs={"scope": "openid email profile"},
)

@app.get("/login/google")
async def login_google():
    return await google.authorize_redirect(redirect_uri="http://localhost:8000/auth")
```

### Security Best Practices

```
┌─────────────────────────────────────────────────────────────────┐
│                 SECURITY BEST PRACTICES                         │
├─────────────────────────────────────────────────────────────────┤
│  ✓ Use HTTPS in production                                      │
│  ✓ Hash passwords with bcrypt                                   │
│  ✓ Use JWT with expiration                                     │
│  ✓ Implement rate limiting                                     │
│  ✓ Validate & sanitize all inputs                              │
│  ✓ Use environment variables for secrets                      │
│  ✓ Enable CORS only for trusted origins                        │
│  ✓ Keep dependencies updated                                  │
└─────────────────────────────────────────────────────────────────┘
```

---

## 🧪 Testing

### Why Testing Matters

```
┌─────────────────────────────────────────────────────────────────┐
│                      TESTING PYRAMID                            │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│                        ▲                                        │
│                       / \       E2E Tests                       │
│                      /   \      (Selenium, Playwright)          │
│                     /─────\                                      │
│                    /       \    Integration Tests               │
│                   /─────────\                                   │
│                  /           \   Unit Tests                     │
│                 /─────────────\ (pytest, unittest)             │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### Installing Test Tools

```bash
pip install pytest pytest-cov pytest-asyncio httpx
```

### Unit Tests with pytest

```python
# test_calculator.py
def add(a, b):
    return a + b

def test_add():
    assert add(2, 3) == 5
    assert add(-1, 1) == 0
    assert add(0, 0) == 0

def test_add_strings():
    with pytest.raises(TypeError):
        add("2", "3")
```

### Testing FastAPI

```python
# test_main.py
from fastapi.testclient import TestClient
from main import app

client = TestClient(app)

def test_read_main():
    response = client.get("/")
    assert response.status_code == 200
    assert response.json() == {"message": "Hello World"}

def test_create_user():
    response = client.post("/users", json={"name": "Alice", "email": "alice@example.com"})
    assert response.status_code == 201
    assert response.json()["name"] == "Alice"
```

### Testing Flask

```python
# test_main.py
import pytest
from app import app

@pytest.fixture
def client():
    app.config["TESTING"] = True
    with app.test_client() as client:
        yield client

def test_home(client):
    response = client.get("/")
    assert response.status_code == 200
    assert b"Hello" in response.data
```

### Test Coverage

```bash
# Run tests with coverage
pytest --cov=app --cov-report=html

# View coverage report
# Open htmlcov/index.html in browser
```

### Mocking

```python
# test_with_mock.py
from unittest.mock import patch, MagicMock

@patch("app.database.fetch_users")
def test_get_users(mock_fetch):
    mock_fetch.return_value = [{"name": "John"}]
    result = get_users()
    assert result == [{"name": "John"}]
```

---

## 🚀 Deployment

### Deployment Options

```
┌─────────────────────────────────────────────────────────────────┐
│                 DEPLOYMENT PLATFORMS                            │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│   🟢 Free Tier Available:                                       │
│   • Render         → Easy, good for Python                     │
│   • Railway        → Modern, developer-friendly                │
│   • Vercel         → Serverless functions                      │
│   • Fly.io         → Docker-based, global                     │
│   • Cyclic         → Free for small projects                   │
│                                                                 │
│   💰 Paid/Enterprise:                                           │
│   • AWS (EC2, Lambda, ECS)                                      │
│   • Google Cloud (Cloud Run, App Engine)                       │
│   • Azure (App Service, Container Apps)                         │
│   • DigitalOcean (Droplets, App Platform)                      │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### Using Gunicorn (Production Server)

```bash
# Install gunicorn
pip install gunicorn

# Run with gunicorn
gunicorn -w 4 -b 0.0.0.0:8000 main:app

# w = workers, b = bind address
```

### Using Uvicorn (ASGI Server)

```bash
# Install uvicorn
pip install uvicorn

# Run development
uvicorn main:app --reload

# Run production
uvicorn main:app --host 0.0.0.0 --port 8000 --workers 4
```

### Docker Deployment

#### Dockerfile for FastAPI/Flask

```dockerfile
# Dockerfile
FROM python:3.12-slim

WORKDIR /app

# Copy requirements first for caching
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy application code
COPY . .

# Expose port
EXPOSE 8000

# Run the application
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
```

#### docker-compose.yml

```yaml
version: '3.8'

services:
  web:
    build: .
    ports:
      - "8000:8000"
    environment:
      - DATABASE_URL=postgres://user:pass@db:5432/mydb
    depends_on:
      - db

  db:
    image: postgres:15
    environment:
      POSTGRES_USER: user
      POSTGRES_PASSWORD: pass
      POSTGRES_DB: mydb
    volumes:
      - postgres_data:/data/db

volumes:
  postgres_data:
```

### Deploy to Render (Step by Step)

```bash
# 1. Create requirements.txt
pip freeze > requirements.txt

# 2. Create runtime.txt
echo "python-3.12.0" > runtime.txt

# 3. Create Procfile
echo "web: uvicorn main:app --host 0.0.0.0 --port $PORT" > Procfile

# 4. Push to GitHub

# 5. Go to render.com, create new Web Service
# 6. Connect GitHub repository
# 7. Deploy!
```

### Environment Variables

```python
# config.py
import os
from dotenv import load_dotenv

load_dotenv()  # Load .env file

DATABASE_URL = os.getenv("DATABASE_URL")
SECRET_KEY = os.getenv("SECRET_KEY")
DEBUG = os.getenv("DEBUG", "False") == "True"
```

#### .env file (local)

```
DATABASE_URL=postgres://user:pass@localhost/mydb
SECRET_KEY=my-super-secret-key
DEBUG=True
```

### Deployment Checklist

```
┌─────────────────────────────────────────────────────────────────┐
│               DEPLOYMENT CHECKLIST                              │
├─────────────────────────────────────────────────────────────┤
│  ☐ Set DEBUG=False                                             │
│  ☐ Configure environment variables                             │
│  ☐ Use strong SECRET_KEY                                        │
│  ☐ Set up proper CORS origins                                   │
│  ☐ Configure logging                                           │
│  ☐ Set up database migrations                                   │
│  ☐ Configure static files (WhiteNoise)                         │
│  ☐ Enable HTTPS                                                 │
│  ☐ Set up monitoring & error tracking                           │
│  ☐ Configure backup strategy                                    │
└─────────────────────────────────────────────────────────────────┘
```

---

## 📚 Learning Path

```
┌──────────────────────────────────────────────────────────────────────────────┐
│                       COMPLETE LEARNING PATH                                │
├──────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│   PHASE 1: Python Fundamentals (Weeks 1-4)                                  │
│   ┌────────────────────────────────────────────────────────────────┐         │
│   │ • Variables, Data Types, Operators                             │         │
│   │ • Control Flow (if/else, loops)                                │         │
│   │ • Functions & Modules                                          │         │
│   │ • OOP Basics (Classes, Objects)                               │         │
│   │ • File Handling & Exception Handling                          │         │
│   └────────────────────────────────────────────────────────────────┘         │
│                                    ▼                                        │
│   PHASE 2: Web Basics (Weeks 5-8)                                          │
│   ┌────────────────────────────────────────────────────────────────┐         │
│   │ • HTML/CSS Fundamentals                                        │         │
│   │ • HTTP Protocol & REST APIs                                    │         │
│   │ • JSON & Data Serialization                                    │         │
│   │ • API Concepts (GET, POST, PUT, DELETE)                        │         │
│   └────────────────────────────────────────────────────────────────┘         │
│                                    ▼                                        │
│   PHASE 3: Database & SQL (Weeks 9-12)                                      │
│   ┌────────────────────────────────────────────────────────────────┐         │
│   │ • SQL Basics (SELECT, INSERT, UPDATE, DELETE)                 │         │
│   │ • Database Design & Normalization                              │         │
│   │ • SQLite Practical Exercises                                   │         │
│   │ • ORM Concepts                                                 │         │
│   └────────────────────────────────────────────────────────────────┘         │
│                                    ▼                                        │
│   PHASE 4: Choose Your Framework (Weeks 13-20)                             │
│   ┌────────────────────────────────────────────────────────────────┐         │
│   │ Option A: Flask → Build REST APIs, small projects              │         │
│   │ Option B: Django → Full-stack apps, learn Django ORM           │         │
│   │ Option C: FastAPI → Modern APIs, async programming             │         │
│   └────────────────────────────────────────────────────────────────┘         │
│                                    ▼                                        │
│   PHASE 5: Advanced & Deployment (Weeks 21-24)                             │
│   ┌────────────────────────────────────────────────────────────────┐         │
│   │ • Authentication & Authorization (JWT, OAuth)                  │         │
│   │ • Docker & Containerization                                    │         │
│   │ • Deployment (Railway, Render, Vercel)                        │         │
│   │ • Testing & CI/CD                                              │         │
│   └────────────────────────────────────────────────────────────────┘         │
│                                                                              │
└──────────────────────────────────────────────────────────────────────────────┘
```

---

## 🗺️ Roadmap Diagram

```
╔══════════════════════════════════════════════════════════════════════════════╗
║                     PYTHON WEB DEVELOPMENT ROADMAP                          ║
╠══════════════════════════════════════════════════════════════════════════════╣
║                                                                              ║
║                         ┌─────────────────┐                                  ║
║                         │   PYTHON BASICS │                                  ║
║                         │  • Syntax       │                                  ║
║                         │  • Functions    │                                  ║
║                         │  • OOP          │                                  ║
║                         └────────┬────────┘                                  ║
║                                  │                                           ║
║                                  ▼                                           ║
║                    ┌────────────────────────────┐                            ║
║                    │       INTERMEDIATE         │                            ║
║                    │  • Database & SQL         │                            ║
║                    │  • HTTP & REST APIs       │                            ║
║                    │  • JSON & AJAX            │                            ║
║                    └─────────────┬─────────────┘                            ║
║                                  │                                           ║
║                                  ▼                                           ║
║         ┌────────────────────────┼────────────────────────┐                  ║
║         │                        │                        │                  ║
║         ▼                        ▼                        ▼                  ║
║  ┌─────────────┐         ┌─────────────┐         ┌─────────────┐          ║
║  │   FLASK     │         │   DJANGO     │         │  FASTAPI    │          ║
║  │  ─────────  │         │  ─────────   │         │  ─────────  │          ║
║  │ • Blueprints│         │ • MVT Pattern│         │ • Path Ops  │          ║
║  │ • Jinja2    │         │ • Django ORM │         │ • Pydantic  │          ║
║  │ • SQLAlchemy│         │ • Admin UI   │         │ • Async/Await│         ║
║  └──────┬──────┘         └──────┬──────┘         └──────┬──────┘          ║
║         │                      │                       │                   ║
║         │                      │                       │                   ║
║         ▼                      ▼                       ▼                   ║
║  ┌─────────────┐         ┌─────────────┐         ┌─────────────┐          ║
║  │  REST APIs  │         │Full-Stack   │         │  Modern APIs│          ║
║  │  Microserv. │         │Web Apps     │         │  Real-time  │          ║
║  └──────┬──────┘         └──────┬──────┘         └──────┬──────┘          ║
║         │                      │                       │                   ║
║         └──────────────────────┼───────────────────────┘                  ║
║                                  │                                           ║
║                                  ▼                                           ║
║                    ┌────────────────────────────┐                            ║
║                    │        PROJECTS            │                            ║
║                    │  • Portfolio Website        │                            ║
║                    │  • REST API                 │                            ║
║                    │  • Blog with CMS             │                            ║
║                    │  • E-commerce                │                            ║
║                    └─────────────┬─────────────┘                            ║
║                                  │                                           ║
║                                  ▼                                           ║
║                    ┌────────────────────────────┐                            ║
║                    │       DEPLOYMENT            │                            ║
║                    │  • Docker                   │                            ║
║                    │  • Cloud (AWS/GCP/Azure)    │                            ║
║                    │  • CI/CD                    │                            ║
║                    └────────────────────────────┘                            ║
║                                                                              ║
╚══════════════════════════════════════════════════════════════════════════════╝
```

---

## 🎯 Recommended Projects by Level

```
┌─────────────────────────────────────────────────────────────────┐
│                  PROJECT IDEAS BY LEVEL                         │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│   BEGINNER:                                                     │
│   ┌─────────────────────────────────────────────────────────┐ │
│   │ 📝 Todo List App (Flask/FastAPI)                        │ │
│   │ 🔗 URL Shortener                                        │ │
│   │ 📊 Simple Calculator Web App                            │ │
│   └─────────────────────────────────────────────────────────┘ │
│                                                                 │
│   INTERMEDIATE:                                                │
│   ┌─────────────────────────────────────────────────────────┐ │
│   │ 📝 Blog with Authentication                             │ │
│   │ 🛒 REST API for E-commerce                              │ │
│   │ 👥 User Management System                               │ │
│   └─────────────────────────────────────────────────────────┘ │
│                                                                 │
│   ADVANCED:                                                    │
│   ┌─────────────────────────────────────────────────────────┐ │
│   │ 🌐 Social Media Platform (Django)                      │ │
│   │ 📱 Real-time Chat App (FastAPI + WebSocket)            │ │
│   │ 📊 Analytics Dashboard with Charts                     │ │
│   └─────────────────────────────────────────────────────────┘ │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

---

## 📖 Resources

### Official Documentation
- [Python.org](https://www.python.org/) - Official Python website
- [FastAPI Docs](https://fastapi.tiangolo.com/) - FastAPI documentation
- [Flask Docs](https://flask.palletsprojects.com/) - Flask documentation
- [Django Docs](https://docs.djangoproject.com/) - Django documentation

### Learning Platforms
- [FreeCodeCamp](https://www.freecodecamp.org/) - Free coding curriculum
- [Real Python](https://realpython.com/) - Python tutorials
- [Python Docs](https://docs.python.org/3/) - Official Python documentation

### Books
| Book | Level | Description |
|------|-------|-------------|
| Python Crash Course | Beginner | Hands-on projects |
| Flask Web Development | Intermediate | Flask deep dive |
| Two Scoops of Django | Advanced | Django best practices |

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&text=Happy%20Coding!&height=100&animation=twinkin" width="100%">
</p>

<p align="center">
  Made with ❤️ for Python Web Developers
</p>
