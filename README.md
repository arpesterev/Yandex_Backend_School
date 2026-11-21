# Backend school REST exercise

A Python/Flask exercise implementing part of a courier and order management API. It stores data through Flask-SQLAlchemy and contains route handlers for creating couriers and orders, assigning orders and marking deliveries complete.

## Routes in the source

| Method | Path | Action |
| --- | --- | --- |
| `POST` | `/couriers` | Submit courier records |
| `GET`, `PATCH` | `/couriers/<id>` | Read or update a courier |
| `POST` | `/orders` | Submit order records |
| `POST` | `/orders/assign` | Attempt order assignment |
| `POST` | `/orders/complete` | Mark delivery completion |

The routes are defined in [`app/routes.py`](app/routes.py). Supporting data and logic live in `app/components.py` and `app/functions.py`.

## Local setup outline

The source imports Flask, Flask-SQLAlchemy and Flask-Migrate. There is no pinned requirements file, so set up a compatible Python environment and install those packages before attempting to launch:

```sh
python yandex.py
```

`config.py` uses a local SQLite database by default and accepts `DATABASE_URL` for an alternative connection.

## Limitations

This is a historical exercise, not a maintained production API. Some references in the source are inconsistent, dependencies are not pinned and the repository does not contain an automated test suite. The launch command and endpoints were read from source, not verified through a running server.
