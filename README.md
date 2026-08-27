# Memory API 🧠

Backend API for a memory card game.

This project handles users, cards, game results and rankings.

It is built with **Laravel 11**, **PostgreSQL** and **JWT authentication**.

## Frontend

The frontend of the project is here:

[Memory Frontend](https://github.com/AzucarGlas/Memory)

---

## Features

- User register and login
- JWT authentication
- Memory cards management
- Save game results
- User game history
- TOP 5 ranking
- Admin routes
- User management
- Card CRUD

---

## Technologies

- PHP 8.2
- Laravel 11
- PostgreSQL
- Eloquent ORM
- JWT
- Docker
- Redis
- GitHub Codespaces

---

## Main API Routes

### Authentication

| Method | Route | Description |
|---|---|---|
| POST | `/api/register` | Register user |
| POST | `/api/login` | Login |
| POST | `/api/logout` | Logout |
| GET | `/api/me` | Get logged user |

### Cards

| Method | Route | Description |
|---|---|---|
| GET | `/api/targeta` | Get all cards |
| GET | `/api/targeta/{id}` | Get one card |
| POST | `/api/targeta` | Create card |
| PUT | `/api/targeta/{id}` | Update card |
| PATCH | `/api/targeta/{id}` | Update part of a card |
| DELETE | `/api/targeta/{id}` | Delete card |

### Games

| Method | Route | Description |
|---|---|---|
| GET | `/api/partidas` | Get user games |
| POST | `/api/partidas` | Save a game |
| DELETE | `/api/partidas/{id}` | Delete a game |
| GET | `/api/ranking` | Get TOP 5 ranking |

### Admin

| Method | Route | Description |
|---|---|---|
| GET | `/api/usuarios` | Get users |
| PUT | `/api/usuarios/{id}` | Update user |
| DELETE | `/api/usuarios/{id}` | Delete user |
| GET | `/api/partidasAdmin` | Get all games |

---

## Authentication

Protected routes use JWT.

After login, the token must be sent in the request:

```http
Authorization: Bearer YOUR_TOKEN
```

---

## Local Installation

Clone the repository:

```bash
git clone https://github.com/AzucarGlas/memory-api.git
cd memory-api
```

Install dependencies:

```bash
composer install
```

Create the environment file:

```bash
cp .env.example .env
```

Generate Laravel key:

```bash
php artisan key:generate
```

Generate JWT secret:

```bash
php artisan jwt:secret
```

Run the database:

```bash
php artisan migrate --seed
```

---

## Database

The project uses PostgreSQL.

Main data:

- Users
- Cards
- Categories
- Games

Game results are connected to users and are used for the ranking.

---

## Development

The project includes a Docker development environment with:

- PHP / Apache
- PostgreSQL
- Redis
- MailHog

It can also be used with GitHub Codespaces.

---

## Useful Commands

Show API routes:

```bash
php artisan route:list
```

Reset the database:

```bash
php artisan migrate:fresh --seed
```

Test the cards endpoint:

```bash
curl http://localhost/api/targeta
```

---

## About the Project

Memory is a full-stack memory card game.

Users can register, play games, save their results and check the ranking.

The frontend and backend are stored in separate repositories.

- [Memory Frontend](https://github.com/AzucarGlas/Memory)
- [Memory API](https://github.com/AzucarGlas/memory-api)
