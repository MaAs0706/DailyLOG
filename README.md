# DailyLOG
</br>

## 21st Feb 2026

## Goal
Starting FastAPI to build foundation for advanced backend and AI work.

## What I Did Today
- Set up GitHub repo for daily logging


</br>

## 22nd Feb 2026

## Goal 
Learning ALong the documentation of FastAPI and freecodecamp course of FastAPI

## What I am learning today 

```
from fastapi import FastAPI
app = FastAPI()

@app.get("/")
def read_root():
    return {"Hello": "World"}

@app.get("/items/{item_id}")
def read_item(item_id: int , q : str| None = None):
    return {"item_id": item_id,"q":q}

```

This is a basic endpoint creation , First we import FastAPI and then create an app .
Then we can see that there are two endpoints.

The first endpoint (@app.get("/")) responds to the root URL and 
returns a simple JSON message. Which in this case is Hello World

The second endpoint (@app.get("/items/{item_id}")) takes an item_id 
from the URL path (must be an integer) and an optional query 
parameter q, then returns both in the response.
