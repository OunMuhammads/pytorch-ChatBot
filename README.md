# pytorch-ChatBot
I have built a chatbot that uses a neural network to understand and respond to user input. The chatbot is based on a set of intents and responses that are defined in a JSON file. These intents describe different topics that the chatbot can help with, such as greeting the user, providing information about a product, or answering a question.
I am using a bag-of-words approach to represent the user's input as a vector of word counts. This vector is then fed into a neural network, which has three layers: an input layer, a hidden layer, and an output layer. The input and hidden layers use the ReLU activation function, while the output layer does not use any activation function. 
When the chatbot receives user input, it tokenizing the input and converts it into a bag-of-words representation using the same vocabulary as the training data. The bag-of-words vector is then fed into the neural network to produce a probability distribution over the different intents. The chatbot selects the intent with the highest probability and uses the associated response to generate a message back to the user.
Here is an example of tokenization:
Input: "What is the weather like today?"
Tokens: "What", "is", "the", "weather", "like", "today", "?"
In this example, the input sentence has been broken down into individual tokens, each representing a separate word or punctuation mark.

Tokenization can also involve additional steps such as stemming, which involves reducing words to their base form (e.g., "running" to "run"), and lemmatization, which involves reducing words to their canonical form (e.g., "ran" to "run").
Overall, my chatbot is a simple but effective example of how natural language processing techniques can be used to build conversational agents. With further improvements and additions, it could potentially be expanded into a more sophisticated chatbot capable of handling a wider range of user queries and providing more informative responses.
I have divided into 4 modules:
Created train data
PyTorch model and training
Save/load model and training
Implement the Chat
The "train.py" script reads this file, preprocesses the data, and trains a neural network model using the PyTorch library. The trained model is then saved to a file named "data.pth".
The "model.py" script defines the architecture of the neural network used by the chatbot. It consists of an input layer, two hidden layers with ReLU activation, and an output layer.
The "nltk_utils.py" script provides utility functions for tokenizing and stemming words in the input text.
The "chat.py" script loads the pre-trained model from the "data.pth" file and uses it to generate responses to user input. The input is first preprocessed and converted into a bag-of-words representation. The model then predicts the intent based on the bag-of-words representation and generates a response based on the predicted intent.

Resource: 
 "Contextual Chatbots with Tensorflow": https://chatbotsmagazine.com/contextual-chat-bots-with-tensorflow-4391749d0077


Here are some key points about the project:

Area: Natural Language Processing, Conversational AI
Description: The project trains a sequence-to-sequence neural network model to have conversations. The model is trained on conversational dialog data to generate human-like responses to user input queries and statements.
The model architecture uses an encoder-decoder LSTM structure commonly used in NLP tasks. The encoder encodes the input sequence to a vector representation, and the decoder generates the output sequence token-by-token.
The training data is the Cornell Movie Dialog dataset which contains over 200k conversational exchanges from movie scripts. This provides a diverse range of conversational dialog for the model to learn from.
TorchText is used for text preprocessing of the training data, like building the vocabulary. Spacy is used for tokenization and lemmatization.
The model is trained end-to-end on this dataset to minimize the cross-entropy loss and optimize the sequence generation.
Keras and PyTorch libraries provide the deep learning model building components like RNN cells, optimization functions etc.
So in summary, this is an NLP focused conversational chatbot project leveraging deep learning and sequence-to-sequence models to create an artificial agent that can have natural conversations with humans. The core areas are conversational AI, NLP, and deep learning.
