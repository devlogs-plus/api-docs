# Devlogs+ Dev Workspace

This workspace contains the API collection and environment configuration for the **Devlogs+** project — a platform for creating and managing developer project logs (devlogs).

---

## Overview

Devlogs+ allows users to register, manage projects, and publish devlogs tied to those projects. This workspace is used for development and testing of the backend API.

---

## Collection

### Devlogs Plus

The main collection is organized into three folders:

#### Auth
Handles user authentication and identity.

| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/auth/register` | Register a new user |
| `POST` | `/auth/login` | Log in and receive a session |
| `POST` | `/auth/logout` | Log out the current user |
| `GET` | `/auth/me` | Get the currently authenticated user |
| `GET` | `/auth/get/:id` | Get user info by ID |

#### Projects
Manage developer projects.

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/projects` | View all projects |
| `POST` | `/projects` | Create a new project |
| `GET` | `/projects/:id` | View a project by ID |
| `PATCH` | `/projects/:id` | Update a project |
| `DELETE` | `/projects/:id` | Delete a project |

#### Devlogs
Create and manage devlogs within a project.

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/projects/:id/devlogs` | View all devlogs for a project |
| `POST` | `/projects/:id/devlogs` | Create a new devlog |
| `GET` | `/projects/:id/devlogs/:id` | View a specific devlog |
| `PATCH` | `/projects/:id/devlogs/:id` | Edit a devlog |
| `POST` | `/projects/:id/devlogs/:id/publish` | Publish a devlog |
| `POST` | `/projects/:id/devlogs/:id/unpublish` | Unpublish a devlog |

---

## Environment

### Dev Env
The active environment for this workspace. It includes the following variable:

- `URL` — The base URL for the API (e.g. `http://localhost:3000`)

Make sure this is set before sending requests.

---

## Getting Started

1. Select the **Dev Env** environment from the environment dropdown.
2. Set the `URL` variable to your local or dev server address.
3. Start with the **Auth** folder — register or log in to get a valid session.
4. Use the **Projects** folder to create a project.
5. Use the **Devlogs** folder to create and publish devlogs under that project.
