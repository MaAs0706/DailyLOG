# DailyLOG
## 21st Feb 2026

## Goal
Starting FastAPI to build foundation for advanced backend and AI work.

## What I Did Today
- Set up GitHub repo for daily logging


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

THe frist endpoint whne you 
