# SpeakEasy

SpeakEasy is a Flask-based web application that uses OpenAI's GPT-3.5-turbo model to create an interactive chatbot with memory capabilities. The bot can also play music on YouTube based on user requests.

## Features

- Interactive chatbot powered by OpenAI's GPT-3.5-turbo model.
- Chat memory to retain conversation context.
- Ability to play songs on YouTube by detecting specific keywords in the chat.
- Save and clear chat history.
- Responsive web interface.

## Getting Started

### Prerequisites

- Python 3.7+
- Flask
- Flask-CORS
- python-dotenv
- openai
- langchain
- pywhatkit

### Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/speakeasy.git
    cd speakeasy
    ```

2. Create a virtual environment and activate it:

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the required packages:

    ```bash
    pip install -r requirements.txt
    ```

4. Create a `.env` file in the root directory of the project and add your OpenAI API key:

    ```
    OPENAI_API_KEY=your_openai_api_key
    ```

### Running the Application

1. Start the Flask application:

    ```bash
    python app.py
    ```

2. Open your web browser and go to `http://localhost:5000`.

### Project Structure

- `app.py`: Main application file containing the Flask routes and logic.
- `templates/index.html`: HTML file for the web interface.
- `requirements.txt`: List of Python packages required for the project.

### API Endpoints

- `/`: Renders the main chat interface.
- `/data`: POST endpoint to handle user messages and return chatbot responses.
- `/history`: GET endpoint to retrieve chat history.
- `/clear`: POST endpoint to clear chat history.
- `/save`: POST endpoint to save chat history to a file.

### Usage

- Type your message in the chat box and press Enter or click the send button.
- The chatbot will respond based on the context of the conversation.
- If you mention words like "song", "music", "track", "play", "listen", or "sing", the bot will attempt to play the mentioned song on YouTube.
- Use the "Clear Chat" button to clear the chat history.

### Saving and Clearing Chat History

- The chat history can be saved by sending a POST request to the `/save` endpoint.
- The chat history can be cleared by sending a POST request to the `/clear` endpoint.

### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### Acknowledgments

- OpenAI for the GPT-3.5-turbo model.
- The contributors of Flask, Flask-CORS, and other libraries used in this project.
