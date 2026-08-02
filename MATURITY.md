# Richardson Maturity Model Evaluation

## Student Details
- Name: Bhavika Patel
- Roll No: 24IT062

## API Evaluation

| Level | Criterion | Satisfy? | Evidence |
|-------|-----------|----------|----------|
| Level 0 | Single endpoint | No | API uses multiple endpoints. |
| Level 1 | Separate resources | Yes | `/tasks` and `/tasks/:id` are separate resources. |
| Level 2 | Correct HTTP methods and status codes | Yes | Uses GET, POST, PUT, DELETE with 200, 201, 400, 404, 500 status codes. |
| Level 3 | HATEOAS | No | HATEOAS is not implemented. |

---

## Endpoint Evaluation

### GET /tasks
- Method: GET
- Status: 200 OK
- Used to get all tasks.

### POST /tasks
- Method: POST
- Status: 201 Created
- Used to create a new task.

### PUT /tasks/:id
- Method: PUT
- Status: 200 OK
- Used to update a task.

### DELETE /tasks/:id
- Method: DELETE
- Status: 200 OK
- Used to delete a task.

---

## Level 2 Improvements

My API already satisfies Level 2 because:
- Uses proper HTTP methods.
- Returns correct HTTP status codes.
- Uses separate resource URLs.

No major changes were required.

---

## HATEOAS Example (Level 3)

```json
{
  "id": 1,
  "title": "Task A",
  "_links": {
    "self": "/tasks/1",
    "delete": "/tasks/1"
  }
}
```

---

## Why do most APIs stop at Level 2?

Most production APIs stop at Level 2 because it is simple, easy to maintain, and supports proper REST principles using resources, HTTP methods, and status codes. HATEOAS adds extra complexity and is not commonly used in modern applications.

---

## Conclusion

The Task Management API satisfies **Richardson Maturity Model Level 2** because it:
- Uses separate resource URLs.
- Uses GET, POST, PUT and DELETE methods.
- Returns appropriate HTTP status codes.
- Does not implement HATEOAS, so it does not reach Level 3.
