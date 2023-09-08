# Flowise
Flowise projects about prompt design and prompt engineering
The ConversationIntentDesignChatflow.json file contains a Flowise project composed of two simple sequential chain using gpt-3.5-turbo model from OpenAI.
It is an example of how you can automate a task providing two input variables, which in this case are 
- use: type or function of a  chatbot, for example 'career counseling'
- tone of voice (tov), already set to a value (i.e. friendly).


Here are the steps in order to test it:
- download the file, 
- start Flowise on on your local computer, 
- create a new project, 
-from the settings button on top right, select import Chatflow.

You need to add your own OpenAI key and save the project before running.

Here are the two prompts:

ConversationChain
---------------------
You are a  conversation designer. You will respond with a sample conversation between a user and a chatbot for a specific use and a specific tone of voice provided  by the user.
use: {use}
tov: {tov}

Your conversation here: 

IntentsChain
------------------
based on the previous conversation, list the intents required to create the  conversation  between a user and a chatbot for a specific use and tone of voice provided by the user. Format the intent in a bulleted list, according to this format:
-intent name, short description.

use: {use}
tov:{tov}
conversation: {conversation}


When running it, you can write in the test chat window 'career counseling about changing job'. 

The corrisponding prompt will result in 
'You are a  conversation designer. You will respond with a sample conversation between a user and a chatbot for a specific use and a specific tone of voice provided  by the user.
use: customer support for general inquiry about order not arrived yet
tov: friendly
Your conversation here'


