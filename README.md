# 🎟️ Eventory

**Eventory** is a modern full-stack event booking platform built with Django REST Framework and React.js. It features real-time seat management, role-based access control, AWS S3 media integration, and a clean, responsive interface — perfect for managing and attending events.

---

## 🌐 Live Demo

Access the deployed platform here:  
👉 [https://eventory.allem.pro/](https://eventory.allem.pro/)

---

## 🚀 Key Features

- 🔐 Token-based authentication with custom `Dusty` prefix
- 📅 Admin dashboard to manage events, users, and bookings
- 🎫 Real-time event booking with auto seat decrement/increment
- 🧑‍💼 User profiles with booking and attendance history
- ⚙️ Settings page for updating user information
- 🌗 Light/Dark mode synced via `localStorage`
- ☁️ AWS S3 storage for user profile images
- ❌ Custom `NotFound` component for unauthorized or broken routes
- 🛡️ Role-based permissions and API protection
- 🧾 Full event details via `EventDetails` component

---

## 🛠 Tech Stack

- **Backend:** Django, Django REST Framework, PostgreSQL
- **Frontend:** React.js, Tailwind CSS, Framer Motion
- **Authentication:** Custom Token Auth (`Dusty`)
- **Media Storage:** AWS S3
- **Styling & Animation:** Tailwind CSS, Framer Motion

---

## 📁 Project Structure

```
.
├── backend/                  # Django backend
│   ├── manage.py
│   ├── requirements.txt
│   └── ...
├── frontend/                 # React frontend
│   ├── package.json
│   ├── src/
│   └── ...
├── .env                      # Add your environment variables here
└── README.md
```

---

## ⚙️ Environment Setup

### ✅ Prerequisites

- Python 3.8+
- Node.js 16+ and npm
- PostgreSQL
- AWS S3 account

### 🔐 Configuration

Fill out the `.env` file at the root level with the following keys:

```env
# AWS S3 Credentials
AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
AWS_STORAGE_BUCKET_NAME=
AWS_S3_REGION_NAME=eu-north-1
AWS_S3_ADDRESSING_STYLE=virtual

# PostgreSQL Database Config
DB_NAME=
DB_USER=
DB_PASSWORD=
DB_HOST=localhost
DB_PORT=5432
```

---

## ▶️ Getting Started

### 1. Backend Setup

```bash
cd backend
python -m venv venv

source venv/bin/activate  

# On Windows:
venv\Scripts\activate

pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

### 2. Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

---

## 👤 User Roles & Permissions

| Role         | Capabilities                                                                 |
|--------------|-------------------------------------------------------------------------------|
| **User**     | Book/cancel events, view event details, update profile                       |
| **Admin**    | Create/update/delete events, manage **user** bookings, promote users         |
| **Superuser**| Full access — including promoting/demoting **admins** and editing their data |

> ❗ **Admins cannot modify other admins' data or roles.** Only a superuser can manage admin-level accounts.

---

## 📂 Core Components

- **`EventDetails`** — Full event info and booking actions  
- **`Profile`** — Lists user's bookings and attended events  
- **`Settings`** — Update personal info and profile image  
- **`AdminPanel`** — Admin tools to manage events and users  
- **`NotFound`** — Handles broken or unauthorized routes

---

## 🤝 Contributing

Pull requests are welcome. For large changes, please open an issue first to discuss your ideas and goals.

---

## 📄 License

This project is licensed under the MIT License.

---

## 📬 Contact

Developed by **Allem**  
📧 Email: [allemhamed98@gmail.com](mailto:allemhamed98@gmail.com)  
🔗 GitHub: [https://github.com/C4ll-0f-Du5ty](https://github.com/C4ll-0f-Du5ty)  
💼 Portfolio: [https://allem.pro/](https://allem.dev/)
