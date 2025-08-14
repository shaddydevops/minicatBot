
````markdown
# MiniCatBot – Web-based Chatbot with Flask & Hugging Face

This project is a simple **web-based chatbot** powered by a **Hugging Face Transformer model** and served using **Flask**.  
It supports conversational memory and a clean front-end interface for interacting with the chatbot directly from a browser.

---

## 📌 Features
- **Flask backend** to host the chatbot and serve the web interface.
- **Hugging Face BlenderBot model** (`facebook/blenderbot-400M-distill`) for text generation.
- **Conversation memory** to maintain context between messages.
- **Web interface** (HTML/CSS/JS) for interactive chatting.
- **CORS enabled** for cross-origin requests.
- Easily deployable locally or on cloud platforms.

---

## 🛠 Prerequisites
Make sure you have:
- Python **3.10+**
- `pip` package manager
- Git installed
- Virtual environment (recommended)

---

## 📦 Installation

### 1️⃣ Clone the repository
```bash
git clone https://github.com/ibm-developer-skills-network/LLM_application_chatbot
cd LLM_application_chatbot
````

### 2️⃣ Set up a virtual environment

```bash
python3 -m venv my_env
source my_env/bin/activate
```

### 3️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

---

## 🚀 Running the Application

### 1️⃣ Start the Flask backend

```bash
export FLASK_APP=app.py
flask run
```

The backend will run at:

```
http://127.0.0.1:5000/
```

### 2️⃣ Access the chatbot in your browser

Open:

```
http://127.0.0.1:5000/
```

---

## 📂 Project Structure

```
LLM_application_chatbot/
│── app.py               # Flask backend application
│── requirements.txt     # Python dependencies
│── static/              # Static assets (CSS, JS, images)
│   └── script.js        # Frontend JavaScript for chat
│── templates/
│   └── index.html       # Chatbot UI template
```

---

## 🔧 Configuration

* **Backend route for chatbot:** `/chatbot`
* **Frontend JS file:** `/static/script.js`
  Update the `endpoint` variable in `script.js` to match your backend URL:

```javascript
const endpoint = "http://127.0.0.1:5000/chatbot";
```

---

## 🧠 How It Works

1. User sends a message from the web interface.
2. `script.js` sends a POST request to `/chatbot` with the message.
3. Flask backend processes the request:

   * Appends the message to conversation history.
   * Generates a response using Hugging Face’s BlenderBot model.
4. Response is returned to the frontend and displayed in the chat.

---

## ⚠ Troubleshooting

* **`ModuleNotFoundError: No module named 'flask_cors'`**
  Make sure you have activated your virtual environment and installed dependencies:

  ```bash
  source my_env/bin/activate
  pip install flask-cors
  ```
* **Model load takes too long:** The first run will download the BlenderBot model from Hugging Face; this may take several minutes depending on your internet speed.

---

## 📜 License

MIT License © 2025
Adapted from IBM Developer Skills Network Guided Project.

---

## 👤 Author

**Your Name**
Based on work by [Sina Nazeri (Ph.D.)](https://www.linkedin.com/in/sinanz) – IBM

```

---

