# Yatube API

Yatube API provides access to social media functionalities for managing posts, comments, and groups. The API is designed to allow authenticated users to interact with Yatube's core models through a RESTful interface.

## Features

- Token-based authentication for secure access.
- CRUD operations for posts, comments, and group retrieval.
- Permissions to ensure only authors can edit or delete their content.
- Read-only access for non-authenticated users.

## API Endpoints

Base URL: `/api/v1/`

- **Authentication**
  - `POST /api/v1/api-token-auth/`: Obtain an authentication token by passing login credentials.

- **Posts**
  - `GET /posts/`: Retrieve all posts.
  - `POST /posts/`: Create a new post (authenticated users only).
  - `GET /posts/{post_id}/`: Retrieve a specific post.
  - `PUT /posts/{post_id}/`: Update a post (author only).
  - `PATCH /posts/{post_id}/`: Partially update a post (author only).
  - `DELETE /posts/{post_id}/`: Delete a post (author only).

- **Comments**
  - `GET /posts/{post_id}/comments/`: Retrieve all comments for a specific post.
  - `POST /posts/{post_id}/comments/`: Add a new comment to a post.
  - `GET /posts/{post_id}/comments/{comment_id}/`: Retrieve a specific comment.
  - `PUT /posts/{post_id}/comments/{comment_id}/`: Update a comment (author only).
  - `PATCH /posts/{post_id}/comments/{comment_id}/`: Partially update a comment (author only).
  - `DELETE /posts/{post_id}/comments/{comment_id}/`: Delete a comment (author only).

- **Groups**
  - `GET /groups/`: Retrieve all groups.
  - `GET /groups/{group_id}/`: Retrieve details of a specific group.

## Quick Start

1. **Clone the repository**:
   ```bash
   git clone https://github.com/srv328/api_yatube.git
   cd yatube_api
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```
3. **Apply migrations**
   ```bash
   pip install -r requirements.txt
   ```
4. **Run the server**
   ```bash
   python manage.py runserver
   ```
