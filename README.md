Running the Application
Start the server:

node server.js
The server will start running on http://localhost:3000.

API Endpoints
Create a Task
URL: /tasks
Method: POST
Headers:
Content-Type: application/json
Body:

{
  "title": "Task Title",
  "description": "Task Description",
  "status": "pending"
}
Response:

{
  "message": "Task created successfully",
  "task": {
    "_id": "60d21b4667d0d8992e610c85",
    "title": "Task Title",
    "description": "Task Description",
    "status": "pending",
    "__v": 0
  }
}
Update a Task
URL: /tasks/:id
Method: PUT
Headers:
Content-Type: application/json
Body:

{
  "title": "Updated Task Title",
  "description": "Updated Task Description",
  "status": "completed"
}
Response:

{
  "message": "Task updated successfully",
  "task": {
    "_id": "60d21b4667d0d8992e610c85",
    "title": "Updated Task Title",
    "description": "Updated Task Description",
    "status": "completed",
    "__v": 0
  }
}
Delete a Task
URL: /tasks/:id
Method: DELETE
Response:

{
  "message": "Task deleted successfully"
}
Using Postman
Create a Task:

Open Postman.
Select POST method.
Enter http://localhost:3000/tasks in the URL field.
Go to the Body tab, select raw and choose JSON from the dropdown.
Enter the task details in JSON format:

{
  "title": "Task Title",
  "description": "Task Description",
  "status": "pending"
}
Click Send.
Update a Task:

Select PUT method.
Enter http://localhost:3000/tasks/<task_id> in the URL field (replace <task_id> with the actual ID of the task to update).
Go to the Body tab, select raw and choose JSON from the dropdown.
Enter the updated task details in JSON format:

{
  "title": "Updated Task Title",
  "description": "Updated Task Description",
  "status": "completed"
}
Click Send.
Delete a Task:

Select DELETE method.
Enter http://localhost:3000/tasks/<task_id> in the URL field (replace <task_id> with the actual ID of the task to delete).
Click Send.
