# Backend Service Implementation

This directory is for the implementation of a RESTful API to manage a resource of your choice (e.g., "Tasks", "Notes", or "Products").

## Instructions

- **API Endpoints:** Implement the following endpoints:
  - **GET `/items`**: Retrieve a list of items.
  - **GET `/items/{id}`**: Retrieve a specific item by its unique ID.
  - **POST `/items`**: Create a new item.
  - **PUT `/items/{id}`**: Update an existing item.
  - **DELETE `/items/{id}`**: Delete an item.

- **Database Integration:** Connect your service to a database. You may use an in-memory database (like SQLite for Python) or a file-based database. Seed the database with a few initial records.

- **Data Validation & Error Handling:** Validate incoming data and return appropriate HTTP status codes (e.g., 400 Bad Request, 404 Not Found).

- **Language Choice:** Use **Python** or **C#**—choose the language you’re most comfortable with (The Java/Spring Boot exercise is in the `backend-java/` directory).

## Starter Code (Python Example)

If you're using Python, you might consider starting with a basic Flask app:

```python
from flask import Flask, request, jsonify

app = Flask(__name__)

# Sample in-memory data store
items = [
    {'id': 1, 'name': 'Item 1'},
    {'id': 2, 'name': 'Item 2'},
]

@app.route('/items', methods=['GET'])
def get_items():
    return jsonify(items)

@app.route('/items/<int:item_id>', methods=['GET'])
def get_item(item_id):
    item = next((item for item in items if item['id'] == item_id), None)
    if item is None:
        return jsonify({'error': 'Item not found'}), 404
    return jsonify(item)

# TODO: Implement POST, PUT, and DELETE endpoints

if __name__ == '__main__':
    app.run(debug=True)
