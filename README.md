# Pytorch-ChatBot
I have built a chatbot that uses a neural network to understand and respond to user input. The chatbot is based on a set of intents and responses that are defined in a JSON file. These intents describe different topics that the chatbot can help with, such as greeting the user, providing information about a product, or answering a question.


I am using a bag-of-words approach to represent the user's input as a vector of word counts. This vector is then fed into a neural network, which has three layers: an input layer, a hidden layer, and an output layer. The input and hidden layers use the ReLU activation function, while the output layer does not use any activation function. 


When the chatbot receives user input, it tokenizing the input and converts it into a bag-of-words representation using the same vocabulary as the training data. The bag-of-words vector is then fed into the neural network to produce a probability distribution over the different intents. The chatbot selects the intent with the highest probability and uses the associated response to generate a message back to the user.


#Here is an example of tokenization:


Input: "What is the weather like today?"


Tokens: "What", "is", "the", "weather", "like", "today", "?"


In this example, the input sentence has been broken down into individual tokens, each representing a separate word or punctuation mark.



Tokenization can also involve additional steps such as stemming, which involves reducing words to their base form (e.g., "running" to "run"), and lemmatization, which involves reducing words to their canonical form (e.g., "ran" to "run").
Overall, my chatbot is a simple but effective example of how natural language processing techniques can be used to build conversational agents. With further improvements and additions, it could potentially be expanded into a more sophisticated chatbot capable of handling a wider range of user queries and providing more informative responses.


I have divided into 4 modules:


1- Created train data


2- PyTorch model and training


3- Save/load model and training


4- Implement the Chat


The "train.py" script reads this file, preprocesses the data, and trains a neural network model using the PyTorch library. The trained model is then saved to a file named "data.pth".


The "model.py" script defines the architecture of the neural network used by the chatbot. It consists of an input layer, two hidden layers with ReLU activation, and an output layer.

The "nltk_utils.py" script provides utility functions for tokenizing and stemming words in the input text.


The "chat.py" script loads the pre-trained model from the "data.pth" file and uses it to generate responses to user input. The input is first preprocessed and converted into a bag-of-words representation. The model then predicts the intent based on the bag-of-words representation and generates a response based on the predicted intent.



Resource: 
 "Contextual Chatbots with Tensorflow": https://chatbotsmagazine.com/contextual-chat-bots-with-tensorflow-4391749d0077
