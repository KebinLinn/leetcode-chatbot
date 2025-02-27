# Coding Chatbot - VS Code Extension
![VSCode Extension Demo](https://github.com/KebinLinn/leetcode-chatbot/raw/main/demo.gif)

A Visual Studio Code extension that provides an AI-powered coding assistant to help with LeetCode problems and general programming questions. The extension integrates with multiple AI models including Deepseek Coder, OpenAI GPT-4, and custom models through Groq or Ollama.

## Features

- **Multiple AI Model Support**: 
  - Deepseek Coder (6.7b)
  - Deepseek R1
  - OpenAI GPT-4
  - Custom LLM via Groq
  - Custom Ollama models

- **Dual Mode Operation**:
  - LeetCode Help: Specialized assistance for LeetCode problems
  - General Coding: Help with any programming questions

- **Smart Context Awareness**:
  - Automatically captures current file content
  - Provides context-aware suggestions
  - Maintains conversation history

- **User Interface**:
  - Integrated chat panel
  - Code formatting support
  - Easy model switching
  - New chat creation
  - Conversation history management

## Installation

1. **Install the Extension**:
   - Install from VS Code Marketplace [link](https://marketplace.visualstudio.com/items?itemName=kebinLin.leetcode-chatbot)
   - Or clone the Github repository and run it locally.

2. **Install Required Python Packages**:
   ```bash
   pip install Flask==3.1.0 Flask-Cors==5.0.0 requests==2.32.3 black==25.1.0 openai==1.63.0 typing-extensions==4.12.2
   ```

3. **Configure AI Models** (Optional):
   - For OpenAI GPT-4: Set your API key using the "Update OpenAI API Key" command
   - For Groq: Set your API key and model using the respective commands
   - For Ollama: Install Ollama locally and set up your preferred model

4. **Extension Activation**:
   - After installation, you may need to reload VS Code for the extension to fully activate

## Usage

### Starting the Extension

1. Open VS Code
2. Click the LeetCode Chatbot icon in the sidebar
3. The chat panel will open, ready to assist

### Available Commands

Access these commands through the Command Palette (`Ctrl+Shift+P` / `Cmd+Shift+P`):

- `LeetCode Chatbot: Analyze Code`
- `LeetCode Chatbot: Update OpenAI API Key`
- `LeetCode Chatbot: Update Groq API Key`
- `LeetCode Chatbot: Set Custom Model`
- `LeetCode Chatbot: Set Ollama Model`

### Features Guide

1. **Model Selection**:
   - Choose your preferred AI model from the dropdown
   - Models include Deepseek Coder, OpenAI GPT-4, and custom options

2. **Mode Toggle**:
   - Switch between "LeetCode Help" and "General Coding" modes
   - LeetCode mode provides problem-specific assistance
   - General mode offers broader programming help

3. **Chat Interface**:
   - Type questions in the input box
   - View conversation history
   - Start new conversations with the "New Chat" button
   - Copy code snippets with one click

## Configuration

### API Keys

1. **OpenAI GPT-4**:
   ```
   Command: LeetCode Chatbot: Update OpenAI API Key
   ```

2. **Groq Custom Model**:
   ```
   Commands:
   - LeetCode Chatbot: Update Groq API Key
   - LeetCode Chatbot: Set Custom Model
   ```

3. **Ollama Custom Model**:
   ```
   Command: LeetCode Chatbot: Set Ollama Model
   ```

## Requirements

- Visual Studio Code 1.84.0 or higher
- Python 3.8 or higher
- The Python packages listed in the installation section

## Known Issues

Please report any issues on the [GitHub repository](https://github.com/KebinLinn/leetcode-chatbot/issues).

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

---

**Note**: This extension is not affiliated with LeetCode. It's an independent tool designed to assist with programming tasks.
