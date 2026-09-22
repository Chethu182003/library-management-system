# 📚 Library Management System

A full-stack web application to manage library operations — book inventory, member registrations, and borrowing records — built with Django and React.js.

---

## 🚀 Live Demo

> _Add your deployed link here (e.g., Render, Railway, Vercel)_

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Backend | Python, Django, Django REST Framework |
| Frontend | React.js, JavaScript |
| Database | PostgreSQL / MySQL |
| Version Control | Git & GitHub |

---

## ✨ Features

- **Book Management** — Add, update, search, and delete books from the inventory
- **Member Management** — Register and manage library members
- **Borrow & Return Tracking** — Issue books to members and track return deadlines
- **Search & Filter** — Find books by title, author, or genre
- **Admin Dashboard** — Overview of stock levels, active borrows, and overdue books
- **REST API** — Clean API endpoints for all core operations

---

## 📂 Project Structure

```
library-management-system/
├── backend/
│   ├── library/          # Django app
│   │   ├── models.py     # Book, Member, BorrowRecord models
│   │   ├── views.py      # API views
│   │   ├── serializers.py
│   │   └── urls.py
│   ├── manage.py
│   └── requirements.txt
├── frontend/
│   ├── src/
│   │   ├── components/   # React components
│   │   ├── pages/        # Page views
│   │   └── App.js
│   └── package.json
└── README.md
```

---

## ⚙️ Getting Started

### Prerequisites

- Python 3.9+
- Node.js 16+
- PostgreSQL or MySQL

### Backend Setup

```bash
# Clone the repository
git clone https://github.com/Chethu182003/library-management-system.git
cd library-management-system/backend

# Create a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Apply migrations
python manage.py migrate

# Run the development server
python manage.py runserver
```

### Frontend Setup

```bash
cd frontend
npm install
npm start
```

The app will be running at `http://localhost:3000`

---

## 📡 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/books/` | List all books |
| POST | `/api/books/` | Add a new book |
| GET | `/api/books/<id>/` | Get book details |
| PUT | `/api/books/<id>/` | Update book |
| DELETE | `/api/books/<id>/` | Delete book |
| GET | `/api/members/` | List all members |
| POST | `/api/borrow/` | Issue a book |
| POST | `/api/return/<id>/` | Return a book |

---

## 📸 Screenshots

> _Add screenshots of your UI here_

---

## 🧠 What I Learned

- Designing relational data models (Books ↔ Members ↔ BorrowRecords)
- Building REST APIs with Django REST Framework
- Connecting a React.js frontend to a Django backend
- Managing database migrations and schema changes

---

## 🔮 Future Improvements

- [ ] Email/SMS notifications for overdue books
- [ ] Fine calculation for late returns
- [ ] User authentication with JWT tokens
- [ ] Export reports as PDF/CSV

---

## 👤 Author

**Chethan** — B.E. Electronics & Communication Engineering  
📍 Bengaluru, India  
🔗 [GitHub](https://github.com/Chethu182003) | [LinkedIn](https://linkedin.com/in/your-profile)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
