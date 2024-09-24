# TalkingHealthcare_Chatbot

This project implements a voice-enabled healthcare chatbot that assists users in identifying potential health issues based on their symptoms. The chatbot processes voice input, predicts the user’s intent using a trained neural network model, and provides a response both via text and voice.

#### Key Features:
- **Voice Input and Output**: The chatbot listens to the user's symptoms via a microphone using the `SpeechRecognition` library, converts speech to text, and responds using `pyttsx3` for text-to-speech functionality.
- **Intent Classification**: User input is processed using a pre-trained model built with TensorFlow. The model classifies the user's intent by matching symptoms to a predefined set of health conditions in `intents.json`.
- **NLP with NLTK**: The chatbot tokenizes, lemmatizes, and processes the input text using NLTK to ensure accurate intent recognition.
- **Model Training**: The chatbot is trained using a deep learning model (Sequential model in Keras) with dense layers, dropout for regularization, and softmax activation for multi-class classification.
- **Voice Customization**: Users can choose between male and female voices for the chatbot’s responses.
- **Interactive Conversation**: The bot provides ongoing interaction, asking if the user wants to continue or exit after each interaction.

#### How it Works:
1. **Data Preprocessing**: The chatbot uses tokenization and lemmatization to process the user’s text input.
2. **Prediction**: A bag-of-words model is created, and the chatbot predicts the user's intent using the trained neural network model.
3. **Response Generation**: Based on the predicted intent, the chatbot retrieves an appropriate response from the predefined set in `intents.json`.
4. **Voice Interaction**: The response is read out to the user via text-to-speech (TTS) using `pyttsx3`.

#### Libraries and Tools:
- **TensorFlow/Keras**: For building and training the neural network.
- **NLTK**: For natural language processing (lemmatization and tokenization).
- **SpeechRecognition**: To capture and convert voice input to text.
- **Pyttsx3**: To generate voice output from the chatbot’s response.
- **Pickle**: For saving and loading processed data and models.
- **JSON**: For storing intents and responses.

#### Setup:
1. Install the required libraries using `pip install -r requirements.txt`.
2. Run the `healthcare_bot.py` script to start the chatbot.
3. The chatbot will guide you through the conversation via voice commands, taking your symptoms as input and providing health-related responses.

