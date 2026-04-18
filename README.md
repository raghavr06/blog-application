# 📝 MERN Blog Application

A simple full-stack blog app built with **MongoDB, Express, React, and Node.js**.

---

## 📁 Project Structure

```
BLOG APPLICATION/
├── backend/
│   ├── models/
│   │   └── Post.js          # Mongoose schema
│   ├── routes/
│   │   └── posts.js         # REST API routes
│   ├── server.js            # Express server entry point
│   ├── .env                 # MongoDB connection string (you must fill this)
│   └── package.json
└── frontend/
    ├── src/
    │   ├── App.js            # All React logic (form + post list)
    │   └── App.css           # Basic styles
    └── package.json
```

---

## ⚙️ Setup & Run Locally

### Step 1: Configure MongoDB

Open `backend/.env` and replace the placeholder with your real MongoDB Atlas URI:

```
MONGO_URI=mongodb+srv://<username>:<password>@cluster0.xxxxx.mongodb.net/blogdb?retryWrites=true&w=majority
PORT=5000
```

> Get your URI from: [MongoDB Atlas](https://cloud.mongodb.com) → your cluster → **Connect** → **Drivers**  
> Make sure to **whitelist your IP** in Atlas Network Access.

---

### Step 2: Start the Backend

```bash
cd backend
npm install       # (already done if you followed setup)
npm start
```

Server runs at: `http://localhost:5000`

---

### Step 3: Start the Frontend

Open a **new terminal**:

```bash
cd frontend
npm start
```

React app runs at: `http://localhost:3000`

---

## 🚀 API Endpoints

| Method | Route         | Description         |
|--------|---------------|---------------------|
| GET    | /posts        | Get all blog posts  |
| POST   | /posts        | Create a new post   |
| DELETE | /posts/:id    | Delete a post by ID |

**POST /posts body (JSON):**
```json
{
  "title": "My First Post",
  "content": "Hello World!"
}
```

---

## 📦 Push to GitHub

```bash
# From the root "BLOG APPLICATION" folder:
git init
git add .
git commit -m "Initial commit - MERN Blog App"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```

> ⚠️ Make sure `backend/.env` is in `backend/.gitignore` so your MongoDB URI is never pushed to GitHub.

---

## 🧰 Tech Stack

- **Frontend**: React (Create React App)
- **Backend**: Node.js + Express
- **Database**: MongoDB Atlas (via Mongoose)
- **CORS**: Enabled for cross-origin requests
