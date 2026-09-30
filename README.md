# 📝 Blog Platform with Commenting System

A RESTful Blog Platform that allows users to create and manage blog posts, organize content using categories and tags, and interact through a nested commenting system. The platform provides role-based access for Authors and Readers along with search, filtering, and pagination features.

## ✨ Features

* **Authentication:** User registration, login, logout, and authenticated access
* **Role-Based Access Control:** Author and Reader roles with different permissions
* **Post Management:** Create, view, update, and delete blog posts
* **Category Management:** Organize blog posts using categories
* **Tag Management:** Add and manage tags for blog content
* **Commenting System:** Add and manage comments with nested comment support
* **Search:** Search blog posts by title, category, or author
* **Filtering:** Filter posts by tags and publication date
* **Pagination:** Paginated responses for posts and comments
* **API Documentation:** Interactive API documentation using Swagger UI and ReDoc
* **API Testing:** REST APIs tested using Postman

## 🛠 Tech Stack

* Python
* Django
* Django REST Framework
* PostgreSQL
* Git & GitHub
* Postman

## 👥 User Roles

| Role       | Permissions                                                                  |
| ---------- | ---------------------------------------------------------------------------- |
| **Author** | Create, manage, update, and delete own blog posts and interact with comments |
| **Reader** | View blog posts, search and filter content, and participate in comments      |

## 📂 Project Structure

```text
blog-platform/
├── blog_app/
├── my_project/
├── users/
├── .gitignore
├── manage.py
└── requirements.txt
```

## 🗄 Database Design

The project consists of the following main entities:

* User
* Post
* Category
* Tag
* PostTag
* Comment

### Relationships

* One User can create multiple blog posts.
* One Category can contain multiple blog posts.
* One Post can have multiple tags.
* One Tag can be associated with multiple posts.
* One Post can have multiple comments.
* Comments can have nested replies.
* Users can create comments on blog posts.

## 📋 Prerequisites

Make sure the following are installed on your system:

* Python 3.10+
* PostgreSQL
* Git
* pip (Python Package Manager)

## ⚙️ Installation

### Clone the Repository

```bash
git clone https://github.com/jilani-code182/blog-platform.git
```

### Navigate to the Project Directory

```bash
cd blog-platform
```

### Create a Virtual Environment

```bash
python -m venv venv
```

### Activate the Virtual Environment

**Windows:**

```bash
venv\Scripts\activate
```

**Git Bash:**

```bash
source venv/Scripts/activate
```

**Linux/macOS:**

```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Apply Database Migrations

```bash
python manage.py migrate
```

### Create a Superuser

```bash
python manage.py createsuperuser
```

### Run the Development Server

```bash
python manage.py runserver
```

The application will be available at:

```text
http://127.0.0.1:8000/
```

## 📄 API Endpoints

### Authentication

| Method | Endpoint          | Description         |
| ------ | ----------------- | ------------------- |
| POST   | `/auth/register/` | Register a new user |
| POST   | `/auth/login/`    | User login          |
| POST   | `/auth/logout/`   | User logout         |

### Blog APIs

| Method | Endpoint            | Description              |
| ------ | ------------------- | ------------------------ |
| CRUD   | `/api/v1/post/`     | Blog post management     |
| CRUD   | `/api/v1/category/` | Blog category management |
| CRUD   | `/api/v1/tag/`      | Tag management           |
| CRUD   | `/api/v1/comment/`  | Comment management       |
| CRUD   | `/api/v1/user/`     | User management          |

> **Note:** Update the endpoint paths above if your current URL configuration uses different routes.

### API Documentation

| Endpoint                  | Description              |
| ------------------------- | ------------------------ |
| `/api/schema/`            | OpenAPI Schema           |
| `/api/schema/swagger-ui/` | Swagger UI Documentation |
| `/api/schema/redoc/`      | ReDoc Documentation      |

## 🔐 Authentication & Authorization

The application uses authentication and role-based permissions to control access to resources.

* Authors can manage their own blog posts.
* Readers can access published blog content and interact with comments.
* Protected endpoints require authenticated access.
* Permissions are applied according to the user's assigned role.

## 🧪 Testing

The APIs were tested using **Postman** to verify:

* Authentication
* Authorization
* Post Management
* Category Management
* Tag Management
* Comment Management
* Search
* Filtering
* Pagination
* Error Handling

## 💡 Future Improvements

* JWT Authentication
* Post likes and bookmarks
* Image upload for blog posts
* Blog analytics

## 👨‍💻 Author

**Jilani Nadaf**

Backend Developer

* [GitHub](https://github.com/jilani-code182/)
* [Email](mailto:nadafjilani182@gmail.com)
* [LinkedIn](https://www.linkedin.com/in/jilani-nadaf)

## 📄 License

This project was developed for practice and to strengthen backend development skills.
