# RESTful APIs

> You must understand the REST spec

## What is REST?
REST stands for Representational State Transfer. It's a spec that defines what methods and URLs can be used to access a resource.

Given a resource and knowing that it's RESTful, you should be able to predict every single URL to manage that resource.

REST works like this: with Methods and URLs.

Here's a table that explains that spec simply

```
--------------------------------------------------------------------------------
| METHOD | URL            | What it does                                       |
|--------|----------------|-----------------------------------------------------
| GET    | /resources/    | Shows all resources in the database                |
|--------|----------------|----------------------------------------------------|
| GET    | /resources/:id | Shows the details of a single resource (1 DB row)  |
|--------|----------------|----------------------------------------------------|
| POST   | /resources/    | Creates a new single resource                      |
|--------|----------------|----------------------------------------------------|
| PATCH  | /resources/:id | Updates an existing resource in the database       |
|--------|----------------|----------------------------------------------------|
| DELETE | /resources/:id | Deletes a single resource in the database          |
|--------|----------------|----------------------------------------------------|
```

REST's rules are this: if I give you a base domain, a resource name, and tell you that the API is RESTful then you should be able to guess the HTTP method and URL to guess how to manipulate the resoureces
