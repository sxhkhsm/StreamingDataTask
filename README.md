# StreamingDataTask
This is a simple WebSocket server built with Node.js and the ws package. The server listens for incoming WebSocket connections and sends pre-defined questions and answers to the clients. The questions and answers are stored in a JavaScript object array.

# Installation

    Install Node.js on your system if you haven't done so already.
    Clone this repository.
    Run npm install to install the ws package.
    
# Usage

    Run node index.js to start the WebSocket server.
    Connect to the server using a WebSocket client. For example, you can use wscat by running wscat -c ws://localhost:8765.

    Once connected, the server will send a greeting message and the first question to the client.
    To answer the question, send a message to the server in the format {"id": <question_id>, "answer": "<your_answer>"}. For example, {"id": 1, "answer": "SICP is a book about programming."}.
    The server will check your answer and respond with the correct answer and the next question.
    Repeat steps 4-5 until all questions are answered.
    To end the connection, send a message to the server in the format {"id": -1}.
