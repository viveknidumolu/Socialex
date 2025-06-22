### 📁 `docs/API.md` — SocialeX API Documentation

````markdown
# 📘 SocialeX API Documentation

This document provides an overview of the RESTful API endpoints available in the **SocialeX** backend (`/server`). All endpoints follow JSON request/response standards.

---

## 🔐 Authentication

### POST `/register`
Register a new user.

**Request Body:**
```json
{
  "username": "john_doe",
  "email": "john@example.com",
  "password": "123456",
  "profilePic": "https://example.com/avatar.jpg"
}
````

**Response:**

```json
{
  "token": "jwt_token_here",
  "user": {
    "_id": "userId",
    "username": "john_doe",
    "email": "john@example.com",
    ...
  }
}
```

---

### POST `/login`

Authenticate an existing user.

**Request Body:**

```json
{
  "email": "john@example.com",
  "password": "123456"
}
```

**Response:**

```json
{
  "token": "jwt_token_here",
  "user": {
    "_id": "userId",
    "username": "john_doe",
    ...
  }
}
```

---

## 📝 Posts

### POST `/createPost`

Create a new post.

**Request Body:**

```json
{
  "userId": "userId123",
  "description": "My new post",
  "imageUrl": "https://firebase.com/image123.jpg"
}
```

**Response:**

```json
{
  "message": "Post created successfully",
  "post": {
    "_id": "postId",
    ...
  }
}
```

---

### GET `/fetchAllPosts`

Fetch all user posts (feed).

**Response:**

```json
[
  {
    "_id": "postId",
    "userId": "userId123",
    "description": "My new post",
    "imageUrl": "...",
    ...
  },
  ...
]
```

---

## 📖 Stories

### GET `/fetchAllStories`

Fetch active stories from all users.

**Response:**

```json
[
  {
    "_id": "storyId",
    "userId": "userId123",
    "storyImage": "https://firebase.com/story123.jpg",
    ...
  }
]
```

---

## 👤 User Info

### GET `/fetchUserName?userId=...`

Returns username based on ID.

### GET `/fetchUserImg?userId=...`

Returns profile picture URL.

---
