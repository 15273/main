from typing import Optional

from fastapi import FastAPI
from pydantic import BaseModel

# uvicorn main:app --reload
from typing import Optional

from fastapi import FastAPI
from pydantic import BaseModel

app = FastAPI()

list_of_usernams = list()


@app.get("/home/{user_name}")
def write_home(user_name: str, query):
    return {"name": user_name,
            "age": 20,
            "query": query}


@app.put("/username/{user_name}")
def put_data(user_name: str):
    print("user_name")
    list_of_usernams.append(user_name)
    return {"user_name": user_name}


@app.post("/post_data")
def post_data(user_name: str):
    list_of_usernams.append(user_name)
    return {"usernams": list_of_usernams}


@app.delete("/delete_data{user_name}")
def delete_data(user_name: str):
    list_of_usernams.remove(user_name)
    return {"list of users": list_of_usernams}


@app.api_route("/home", methods=["post", "get", "delete", "put"])
def handel_data(user_name: str):
    print("user names")
    return {
        "user name": user_name
    }
