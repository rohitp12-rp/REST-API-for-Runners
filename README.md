# REST API for Runners

## Overview

This REST API is designed to manage information about runs made by different runners. It provides endpoints to create, retrieve, update, and delete run records.

## Technologies Used
- Java
- Spring Boot
- Maven

## API Endpoints

### Get All runs
- URL: /api/runs
- Method: GET
- Description: Retrieves all run records.
- Example Response
```json
[
  {
    "id": 10,
    "title": "Dawn Run",
    "startedOn": "2024-03-08T01:34:00.000000",
    "completedOn": "2024-03-08T05:53:00.000000",
    "miles": 23,
    "location": "OUTDOOR"
  },
  ...
]
```
### Get Run by ID
- URL: /api/runs/{id}
- Method: GET
- Description: Retrieves a specific run record by its ID.
- Example Response:
```json
{
    "id": 6,
    "title": "Noon Run",
    "startedOn": "2024-03-02T21:02:00.000000",
    "completedOn": "2024-03-03T00:36:00.000000",
    "miles": 3,
    "location": "INDOOR"
  }
```
### Create a New Run
- URL: /api/runs
- Method: POST
- Description: Creates a new run record.
- Request Body:
```json
{
  "title": "Dusk Run",
  "startedOn": "2024-05-09T18:30:00.000000",
  "completedOn": "2024-05-09T21:00:00.000000",
  "miles": 15,
  "location": "OUTDOOR"
}
```

### Update a Run
- URL: /api/runs/{id}
- Method: PUT
- Description: Updates an existing run record.
- Request Body:
```json
{
  "title": "Morning Run",
  "startedOn": "2024-05-09T06:00:00.000000",
  "completedOn": "2024-05-09T08:30:00.000000",
  "miles": 10,
  "location": "INDOOR"
}
```
### Delete a Run
- URL: /api/runs/{id}
- Method: DELETE
- Description: Deletes a run record by its ID.
- Example Response: 204 No Content
