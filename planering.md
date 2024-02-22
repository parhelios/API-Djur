# Planering för DjurApi

## Endpoints

### Pets

| Path       | Method | Request     | Response | ResponseCodes |
| ---------- | ------ | ----------- | -------- | ------------- |
| "/pets"    | GET    | NONE        | Pet[]    | 200           |
| "/pets{id} | GET    | int id      | Pet      | 200, 404      |
| "/pets     | GET    | string Type | Pet[]    | 200, 404      |
| "/pets     | POST   | Pet         | NONE     | 200, 400      |

### Owners

| Path         | Method | Request | Response | ResponseCodes |
| ------------ | ------ | ------- | -------- | ------------- |
| "/people"    | GET    | NONE    | Person[] | 200           |
| "/people{id} | GET    | int id  | Pet      | 200, 404      |
| "/people"    | POST   | Person  | NONE     | 200, 400      |

## Data

### Pet

| Property Name | Data Type | Description          |
| ------------- | --------- | -------------------- |
| Name          | string    | Name of the pet      |
| Date of birth | Date      | To calculate the age |
| Type          | string    | Type of the animal   |

### Person

| Property Name | Data Type | Description           |
| ------------- | --------- | --------------------- |
| Name          | string    | Name of the person    |
| Phone         | string    | Person's phone number |
| Pets          | Pet[]     | List of pets          |
