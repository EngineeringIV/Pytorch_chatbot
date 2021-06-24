# Pytorch_chatbot
A Pytorch-based chatbot with a GUI built with Tkinter
 
 ## Motivation
We interact with chatbot everyday. As a member of the Lenovo eServices team, we have a chatbot called [Lena](https://lena.lenovo.com/) that helps customer answer questions
about their machines and warranties. I'd like to build a simple chatbot myself while experiment with PyTorch, a popular deep learning package. 

## Techniques and Steps to Run
For the training data, I defined some intents with tags, patterns, and responses in a JSON file. 

The NLP (Natural Language Processing) pipeline is consist of tokenization, stemming, removing punctuations, and creating a bag of words

I designed a feed forward neural network. The structure is as follows:
- Input layer (# of neurons  = # of patterns, relu activation)
- Hidden layer 1 (8 neurons, relu activation)
- Hidden layer 2 (8 neurons, relu activation)
- Output layer
- Loss: Crossentropy loss
- Optimizer: Adam, with learning rate 0.001

I designed the GUI with Tkinter


## File Structure
- Python files
  - app.py: chatbot with Tkinter GUI
  - chat.py: normal chatbot
  - model.py: PyTorch feed forward neural network model
  - nltk_utils.py: NLTK utility functions such as tokenize, stem, and creating bag of words
  - train.py: script to train and save the neural network

- Other files
  - intens.json: JSON file
  - data.pth: trained neural network


## Credit and Acknowledgement
This project follows the wonderful [tutorial](https://www.youtube.com/playlist?list=PLqnslRFeH2UrFW4AUgn-eY37qOAWQpJyg) by [Patrick Leober](https://www.youtube.com/channel/UCbXgNpp0jedKWcQiULLbDTA). 
It also got inspirations from this [tutorial](https://chatbotsmagazine.com/contextual-chat-bots-with-tensorflow-4391749d0077) on contextual chatbot


