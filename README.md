# URL Shortener API

The main purpose of this API is to receive a full target URL and return a shortened URL.

## Development

- FastAPI
- SQLite

**install dependencies**

```terminal
pipenv install sync && pipenv install sync -d
```

**api docs**  
http://localhost:8000/docs

**run application**

```terminal
uvicorn shortener_app.main:app --reload
```

## API Endpoints

| Endpoint            | HTTP Verb | Request Body    | Action                                                                     |
| ------------------- | --------- | --------------- | -------------------------------------------------------------------------- |
| /                   | GET       |                 | Returns a `Hello, World!` string                                           |
| /url                | POST      | Your target URL | Shows the created `url_key` with additional info, including a `secret_key` |
| /{url_key}          | GET       |                 | Forwards to your target URL                                                |
| /admin/{secret_key} | GET       |                 | Shows administrative info about your shortened URL                         |
| /admin/{secret_key} | DELETE    | Your secret key | Deletes your shortened URL                                                 |

---
