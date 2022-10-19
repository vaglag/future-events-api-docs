# Future Event's API Documentation

This repository contains the documentation for the Future Event's API.

## 1. Overview

An API that has JSON for events. Authentication coming soon. ;)

All requests endpoints begin at `localhost:3000/events`


## 2. Getting Started

### 2.1 Install server for usage
Install the project by running:
- `npm install`

#### Noteworthy Dependencies
- `express`: Backend web framework
- `cors`: Prevents the "Cross-Origin Request Blocked: The Same Origin Policy disallows reading the remote resource at $somesite" error, by allowing some cross-origin requests.

### 2.2 Run the server
- Launch the server by running `npm run start`.
- **Note:** We will be assuming from this point forward you are running the server at port 3000 to interact with this service.

## 3. Resources
Restful API service

### 3.1 Events

#### Getting all the Events data
```
GET https://localhost:3000/events
```

Example request

```
GET /events/ HTTP/1.1
Host: localhost:3000/events
Content-Type: application/json
Accept: application/json
Accept-Charset: utf-8

```
The response is an Event object.

Example response:

```
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

{
  "data": {
    "id": "1",
    "name": "Spooky Booky Ball",
    "description": "",
    "venue": "",
    "date": "",
    "start-time": "",
    "end-time": "",
    "ticket-price": "",
    "ticket availability": "",
    "ticket-holders": "[]"
    "url": "localhost:3000/events"
  }
}
```

Event Object:
|Field|Type|Description|
|---|---|---|
|id|String|Unique identifier of an event object|
|name|String|Name of the event|
|description|String|A description of th event|
|venue|String|The venue the event will take place at|
|date|String|The date that the event will take place on|
|start|String||

Possible errors:

|Error Code|Description|
|---|---|
|404| Event not found|

#### Getting all the User data

```
GET https://localhost:3000/users
```

Example request

```
GET /users/ HTTP/1.1
Host: localhost:3000/users
Content-Type: application/json
Accept: application/json
Accept-Charset: utf-8

```
The response is an User object.

Example response:

```
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

{
  "data": {
    "id": "1",
    "name": "Spooky Booky Ball",
    "url": "localhost:3000/users"
  }
}
```

User Object:
|Field|Type|Description|
|---|---|---|
|id|String|Unique identifier of a user object|
|name|String|Name of user|

Possible errors:

|Error Code|Description|
|---|---|
|404| User not found|


#### Getting all the Ticket data
