
# Simple Todo API

This is a simple Todo API built with Node.js and Express. It allows you to perform basic CRUD operations (Create, Read, Update, Delete) on a collection of todos stored in a JSON file.

## Installation

1. Clone the repository:
```bash
  npm install my-project
  cd my-project
```
2. Install dependencies:
Navigate into the project directory and run:
```bash
npm install
```
3.Run the server:

```bash
node server.js
```


## API Reference

#### Get all items

```http
  GET /todos
```
Retrieves all todos from the JSON file.


``` http
    POST /todos
```
Creates a new todo with the provided title and description. A unique random id is generated for each todo.



``` http 
    DELETE/todos/:id
```
Deletes the todo with the specified id.





## Usage/Examples
GET /todos
```bash
curl http://localhost:3000/todos
```
POST /todos

```bash
curl -X POST -H "Content-Type: application/json" -d '{"title":"Example Todo", "description":"This is an example todo."}' http://localhost:3000/todos
```

DELETE /todos/:id
Replace :id with the id of the todo you want to delete. For example:
```bash
curl -X DELETE http://localhost:3000/todos/12345
```

## NOTES
    1.Todos are stored in a JSON file named todos.json.
    2.Each todo has a unique random id generated when created.
    3.Error handling is minimal in this example for brevity. In a production environment, you should implement more robust error handling and validation.
    4.Feel free to customize and extend this API according to your needs!



