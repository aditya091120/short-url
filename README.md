# 🔗 Short URL Service

A simple and efficient URL shortener built with **Node.js, Express, and MongoDB**. This project allows users to convert long URLs into short, shareable links and track basic analytics.

---

## 🚀 Features

* 🔗 Generate short URLs
* 📊 Track number of clicks (analytics)
* ⚡ Fast redirection
* 🗄️ MongoDB database storage
* 🛠️ REST API support

---

## 🏗️ Tech Stack

* **Backend:** Node.js, Express.js
* **Database:** MongoDB (Mongoose)
* **Utilities:** shortid / nanoid

---

## 📁 Project Structure

```
short-url/
│
├── controllers/
│   └── url.js
├── models/
│   └── url.js
├── routes/
│   └── url.js
├── index.js
├── package.json
└── README.md
```

---

## ⚙️ Installation & Setup

### 1. Clone the repository

```
git clone https://github.com/your-username/short-url.git
cd short-url
```

### 2. Install dependencies

```
npm install
```

### 3. Setup environment variables

Create a `.env` file in the root:

```
PORT=8000
MONGO_URI=your_mongodb_connection_string
```

### 4. Run the server

```
npm start
```

Server will run on:

```
http://localhost:8000
```

---

## 📌 API Endpoints

### 🔹 Create Short URL

**POST** `/url`

**Request Body:**

```
{
  "url": "https://example.com"
}
```

**Response:**

```
{
  "shortId": "abc123"
}
```

---

### 🔹 Redirect to Original URL

**GET** `/:shortId`

Redirects user to the original URL.

---

### 🔹 Get Analytics

**GET** `/url/:shortId`

**Response:**

```
{
  "totalClicks": 10,
  "analytics": [...]
}
```

---

## 🧠 How It Works

1. User sends a long URL
2. Server generates a unique short ID
3. URL + ID stored in MongoDB
4. Short link is shared
5. On visiting, user is redirected and click is tracked

---

## 🧪 Example

**Input URL:**

```
https://www.google.com
```

**Short URL:**

```
http://localhost:8000/abc123
```

---

## 🛡️ Future Improvements

* User authentication
* Custom short URLs
* Expiration links
* QR code generation
* Rate limiting

---

## 🤝 Contributing

Contributions are welcome! Feel free to fork this repo and submit a pull request.

---

## 📄 License

This project is licensed under the MIT License.

---

## 👨‍💻 Author

**Aditya Raj**

---

⭐ If you like this project, don't forget to star the repository!
