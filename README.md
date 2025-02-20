# Python Code Assistant API
![image](https://github.com/user-attachments/assets/ca86969c-a342-4687-a2ea-144218beba9b)

This is a Flask-based API that integrates with the **Ollama AI Model** (`deepseek-coder:6.7b`) to assist developers with Python code analysis, suggestions, debugging, and answering coding-related questions.

## Features

- **Get Code Suggestions**: Analyze provided Python code and receive structured suggestions for improvement.
- **Ask Questions**: Ask Python-related questions and receive AI-generated responses.
- **Format Code with Black**: Automatically formats Python code blocks for readability.
- **Conversation Context**: Maintains conversation history for each user.
- **Retrieve & Clear History**: Fetch or reset conversation history.

---

## Installation

1. **Clone the Repository**  
   ```sh
   git clone https://github.com/your-repo/python-code-assistant.git
   cd python-code-assistant
   ```

2. **Install Dependencies**  
   ```sh
   pip install -r requirements.txt
   ```

3. **Start the Flask Server**  
   ```sh
   python app.py
   ```

---

## API Endpoints

### 1⃣ Get Code Suggestions  
**Endpoint**: `POST /get_suggestions`  
**Description**: Analyzes Python code and provides suggestions.  
**Request Body (JSON)**:
```json
{
  "code": "def add(a, b): return a+b",
  "user_id": "user123",
  "file_name": "script.py"
}
```
**Response Example**:
```json
{
  "suggestion": "- Use type hints: def add(a: int, b: int) -> int\n...",
  "status": "success"
}
```

---

### 2⃣ Ask a Coding Question  
**Endpoint**: `POST /ask_question`  
**Description**: Answers Python-related questions.  
**Request Body (JSON)**:
```json
{
  "question": "How do I optimize this function?",
  "user_id": "user123",
  "file_name": "script.py",
  "code": "def add(a, b): return a+b"
}
```
**Response Example**:
```json
{
  "answer": "- Consider using numpy for performance...",
  "status": "success"
}
```

---

### 3⃣ Retrieve Conversation History  
**Endpoint**: `GET /conversation_history`  
**Description**: Fetches the conversation history of a user.  
**Query Parameters**:
```
user_id (optional) - Default: "default_user"
```
**Response Example**:
```json
{
  "history": [
    {"role": "user", "message": "How to optimize this?"},
    {"role": "assistant", "message": "- Use a list comprehension..."}
  ]
}
```

---

### 4⃣ Clear Conversation History  
**Endpoint**: `POST /clear_conversation`  
**Description**: Clears the conversation history of a user.  
**Request Body (JSON)**:
```json
{
  "user_id": "user123"
}
```
**Response Example**:
```json
{
  "status": "success",
  "message": "Conversation history cleared"
}
```

---

## Configuration

- **Ollama API URL**: The service assumes Ollama is running locally at `http://localhost:11434/api/generate`. Update `OLLAMA_API_URL` if needed.
- **Port**: The Flask server runs on `0.0.0.0:5000` (can be modified in `app.py`).
- **Logging**: Debug logs are enabled for troubleshooting.

---

## Dependencies

- **Flask** - API framework
- **Flask-CORS** - Handles cross-origin requests
- **Requests** - API calls to Ollama
- **Black** - Python code formatting
- **Logging** - For debugging

Install with:
```sh
pip install flask flask-cors requests black
```

---

## License

This project is open-source under the **MIT License**.

---

