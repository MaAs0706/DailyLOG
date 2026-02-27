# DailyLOG

A daily log of my learning journey — tracking goals, concepts, and hands-on experiments as I build toward advanced backend and AI development.

---

## 21st Feb 2026

### Goal
Start FastAPI to build a foundation for advanced backend and AI work.

### What I Did Today
- Set up this GitHub repo for daily logging
- Chose FastAPI as the starting point for backend development
- Setting up the Virtual Environment
  
Creating virtual environment 
```bash
python3 -m venv .venv
```

Activating the Virtual Environment

```bash

source .venv/bin/activate

```
---

## 22nd Feb 2026

### Goal
Learn FastAPI fundamentals through the official documentation and a freeCodeCamp course.

### What I Learned Today
##### What is FastAPI 
FastAPI is a basically a high-performance web framework for building API's using Python. It offers speed comparabale to node.js and go . 

#### Basic Endpoint Creation

```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def read_root():
    return {"Hello": "World"}

@app.get("/items/{item_id}")
def read_item(item_id: int, q: str | None = None):
    return {"item_id": item_id, "q": q}
```

We import `FastAPI`, create an `app` instance, and define two endpoints:

- `GET /` — responds to the root URL and returns a simple JSON message.
- `GET /items/{item_id}` — takes an `item_id` from the URL path (must be an integer) and an optional query parameter `q`, then returns both in the response.

---

#### Pydantic & the PUT Method

```python
from fastapi import FastAPI
from pydantic import BaseModel

app = FastAPI()

class Item(BaseModel):
    name: str
    description: str | None = None
    price: float
    tax: float | None = None

@app.get("/")
def read_root():
    return {"Hello": "World"}

@app.get("/items/{item_id}")
def read_item(item_id: int, q: str | None = None):
    return {"item_id": item_id, "q": q}

@app.put("/items/{item_id}")
def update_item(item_id: int, item: Item):
    return {"item_name": item.name, "item_id": item_id}
```

The `PUT` method is used to update existing data. We use **Pydantic** to define the shape and types of that data via a `BaseModel` class.

Think of Pydantic as a bouncer at a club , you define what valid data looks like, and Pydantic checks every request at the door:

- Data matches your rules → it passes through to your function.
- Data is wrong (e.g. `price` is a string instead of a number) → it's rejected with a clear error message before your function even runs.

### What I Tried & Tested
- Visited `http://localhost:8000/docs` and explored the auto-generated interactive API docs
- Tested the `PUT` endpoint using the Swagger UI
- Deliberately sent wrong data types to trigger Pydantic validation errors

---
## 23rd Feb 2026

### Notes
Didn't get to study today. Picking back up tomorrow.

---
## 24th Feb 2026
https://medium.com/@aswanthmadhav07/virtual-environment-725706aae0bd

Here is a blog on virtual Environment.
---

## 25th Feb 2026

### Goal
Learn about instances 

### What I learned Today

#### What is a Class?
Think of a class as a blueprint. For example, a blueprint for a house defines what a house should have  rooms, doors, windows etc.
FastAPI is a class ,it's a blueprint that defines everything an API app should be able to do.

#### What is an Instance
Instance any real object made from the class , like if you make an actual house from the blueprint that would be the instance.

```python
app = FastAPI()

```

Here FastAPI() creates an actual, real API application from the FastAPI blueprint. That real application is stored in the variable app. So app is the instance.

---
## 26th Feb 2026

### Goal 
Learn about path and parameters

### What I learned Today 

"Path" here refers to the last part of the URL starting from the first /.

```
https://example.com/items/this
```
here the path is 
/items/this

---

### 27th Feb 2026

