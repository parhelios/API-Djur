# Planering för DjurApi

## Endpoints

### Pets

| Path               | Method | Request     | Response | ResponseCodes |
| ------------------ | ------ | ----------- | -------- | ------------- |
| "/pets"            | GET    | NONE        | Pet[]    | 200           |
| "/pets/{id}        | GET    | int Id      | Pet      | 200, 404      |
| "/pets/{type}"     | GET    | string Type | Pet[]    | 200, 404      |
| "/pets/{age}"      | GET    | int Age     | Pet[]    | 200           |
| "/pets/people/{id} | GET    | int Id      | Person[] | 200           |
| "/pets"            | POST   | Pet         | NONE     | 200, 400      |

### Owners

| Path                  | Method | Request                 | Response | ResponseCodes |
| --------------------- | ------ | ----------------------- | -------- | ------------- |
| "/people"             | GET    | NONE                    | Person[] | 200           |
| "/people/{id}"        | GET    | int id                  | Person   | 200, 404      |
| "/people/pets/{id}"   | GET    | int id                  | Pet[]    | 200, 404      |
| "/people/pets/{type}" | GET    | string Type             | Person[] | 200, 404      |
| "/people"             | POST   | Person                  | NONE     | 200, 400      |
| "/people/{personid}"  | POST   | int personId, Pet pet   | NONE     | 200, 404      |
| "/people/{personid}"  | PUT    | int personId, int petId | NONE     | 200, 404      |
| "/people/{personid}"  | DELETE | int personId, int petId | NONE     | 200, 404      |

## Data

### Pet

| Property Name | Data Type  | Description          |
| ------------- | ---------- | -------------------- |
| Id            | int        | Id for database      |
| Name          | string     | Name of the pet      |
| Date of birth | Date       | To calculate the age |
| Type          | AnimalType | Type of the animal   |

### AnimalType

| Property Name | Data Type | Description                   |
| ------------- | --------- | ----------------------------- |
| Id            | int       | Id for database               |
| Name          | string    | Name of the Type (e.g. "Cat") |

### Person

| Property Name | Data Type | Description           |
| ------------- | --------- | --------------------- |
| Id            | int       | Id for database       |
| Name          | string    | Name of the person    |
| Phone         | string    | Person's phone number |
| Pets          | Pet[]     | List of pets          |
