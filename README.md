# Customer Service Chat Bot Using RASA Framework

## Introduction
A Chatbot is an automated computer program that simulates human conversation.
Chatbots are generally used by the organisations to engage with their customers.
Some examples are Virtual Assistants(Google Assistant, Apple Siri, etc.), chatbots used by WhatsApp, Telegram, etc..

In terms of the technical complexity, the chatbots can be broadly categorized in to three types. 
1) Simple chatbots
2) Smart chatbots 
3) Hybrid chatbots 

### Our Objectives are
1)  Collect Intents and responses for training the chatbot 
2) Create the basic RASA framework and train the chatbot 
3) Conduct unit testing on different “stories” (Conversational flows) 
4) Rectify general errors and errors raised from testing 

## System Analysis
RASA is an open source framework used to perform various jobs.
We can split the Chatbot's tasks into two categories: 
1. Understand the user's inquiry and the response he is anticipating.  
2. Maintain the flow of the discussion by responding to him based on the question/query and conversing further.

Rasa NLU and Rasa Core are two important components for handling these tasks individually. While NLU focuses on classifying the intents, extract any entities and get the response, the Core focuses on dialogue management.

### Intents and Responses

Intents: Intent are tags that are attributed to the sentences of the conversation, based on the context of user’s message.

Responses: Responses are the action which are executed by the chatbot for specific intent. 

### Stories
Responses: 
Responses are the action which are executed by the chatbot for specific intent.
Stories are used to construct the conversational flow inside a chatbot.

Multiple types of inputs constitute a Story, some of which are- 
1) User Messages
2) Actions
3) Events
4) Checkpoints and OR Statements

## Model Architecture
The chatbot works on two primary components main Natural Language Processing (NLU) and dialogue management. 
We write all the intents (basically questions) in the data/nlu file and the responses of these intents(questions) is provided in the domain file.
The predicted flow of the chatbot is provided under the stories file.

The NLU part of the RASA classification handles mostly things like classification of intents, creating a bag of words, providing certain confidence levels for intents and their responses, entity extraction and response retrieval.
RASA core decides the next action in a conversation based on the intents and entities received.

## Results and Observations
The initial training of the chatbot model achieved an accuracy of 97.6%.
But this accuracy may not ensure that correct intent is inferred from a user’s sentence.

Conducting a unit test on the existing conversational flows, led to some conflicts and errors. Some intents were divided into separate intents, some responses were changed and some new intents were added. Existing intents were added with some more phrases.  

This resulted in an improved chatbot with near perfect simulation of human conversation.

With commands like RASA shell, we can run our bot in the command prompt and with RASA interactive where we can build and test out chatbot and see the functioning of the backend pipeline and visually see the flow of the chatbot using a flow chart. 
With the help of socket.io and BotFront we can also give our bot a frontend looks for the website where it can be deployed.

## Conclusion
RASA provides a wonderful playground for developing, creating, testing and also deploying high end functioning chatbots. 

With a complex Natural language understanding unit to power up intent-based AI through text, RASA is a dynamic framework.  RASA is also open source. NLU training models, project guidance and prototypes, all supported by a healthy and active developers’ community. 

In conclusion RASA is a very reliable framework for building communication chatbot and deploying it wherever necessary.
