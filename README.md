# OpenAI GPT-3 Chatbot

This project is a simple chatbot that uses OpenAI's GPT-3 to generate responses to user input.

## Setup

1. **Clone the repository**:

    ```bash
    git clone https://github.com/your-username/openai-gpt3-chatbot.git
    cd openai-gpt3-chatbot
    ```

2. **Create and activate a virtual environment (optional but recommended)**:

    ```bash
    python -m venv venv
    source venv/bin/activate # On Windows use `venv\Scripts\activate`
    ```

3. **Install the required packages**:

    ```bash
    pip install openai
    ```

4. **Set up your OpenAI API key**:
   
   Create a `.env` file in the root directory of the project and add your OpenAI API key:

    ```plaintext
    OPENAI_API_KEY=your-api-key-here
    ```

5. **Load environment variables**:

    Install `python-dotenv` package to load environment variables from the `.env` file:

    ```bash
    pip install python-dotenv
    ```

    Add the following lines to the beginning of your script to load the API key:

    ```python
    from dotenv import load_dotenv

    load_dotenv()
    ```

## Usage

To run the chatbot, execute the following command:

```bash
python chatbot.py
```

## Example

```plaintext
You: Hello, how are you?
Bot: I'm doing great, thank you! How can I help you today?
```

## Customization

You can customize the behavior of the chatbot by modifying the parameters of the `openai.Completion.create` function call. Here are a few key parameters you can adjust:

- `engine`: The GPT-3 model to use. Options include `davinci`, `curie`, `babbage`, and `ada`.
- `temperature`: Controls the creativity of the responses. Lower values make the output more deterministic.
- `max_tokens`: The maximum number of tokens to generate in the response.
- `top_p`: Controls diversity via nucleus sampling.
- `frequency_penalty`: Penalizes new tokens based on their existing frequency in the text so far.
- `presence_penalty`: Penalizes new tokens based on whether they appear in the text so far.
