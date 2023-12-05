# Adventure-Game-OpenAI

The necessary dependencies have been listed in the `Requirements.txt` file ...just create a virtual environment and install all the dependencies and then follow along.
To install all the dependencies from `Requirements.txt`....activate your virtual environment..and then run the following command in the terminal
`pip install -r \Requirements.txt`
<br>
To create the `Requirements.txt` file ..run the command in the terminall `pip freeze > Requirements.txt`


### LangChain -  https://astra.datastax.com/org/f86072ff-9b0c-4f97-bcea-b3224186edd2/integrations/LangChain


The method we are using here is called as RAG(Retrieval Augmented Generation) ....Traditional Language Models generate Text from 
Scratch, whereas RAG model first retrieve relevant information and then generate responses based on that retrieved context....so
in this way RAG models are designed to provide more accuracte responses...

    So what basically happening in this project is - we define a template(adventure) based on which our game revolves...then 
    user can respond with literally anything....and this all chat between AI and User is saved in Cassandra's database...
    now whatever user replies...i want my AI model to give a next prompt based on the user reply and the prompt should not 
    break the template we are using...that's why we again pass the whole template...in which chat_history will keep on updating
    as well as human_input...these two will decide what will be the next Prompt...now a particular session is stored at max for
    60 mins....after which it automatically gets deleted....now ...when the game ends..we are also instructed our LLM to 
    include "The End." at the last....so we know when to stop the game...




# For connection with Cassandra's Astra DB ....do the following Steps - 
1. Go to the following Link - https://www.datastax.com/lp/astra-registration?utm_medium=youtube_video&utm_source=datastax&utm_campaign=yt_influencers&utm_content=vector_search_tim_ruscica
2. SignUp your account
3. Click on create database & create a vector database
<img width="562" alt="image" src="https://github.com/AmmanChhetri/Adventure-Game-OpenAI/assets/121025542/321182f8-a5eb-4cc7-9a0b-bcd6e6c6689b">

<hr>

4. Now go to `Connect` section and then generate token and save it in the same directory
<img width="482" alt="image" src="https://github.com/AmmanChhetri/Adventure-Game-OpenAI/assets/121025542/d31d7d04-1a95-4545-82d9-90e6b214d153">

<hr>

5. Now download the bundle and save it in the same directory as well
<img width="272" alt="image" src="https://github.com/AmmanChhetri/Adventure-Game-OpenAI/assets/121025542/541e0f9d-52ac-40f4-9bca-c2f6abe7d497">

<hr>

6. After this follow along the code file `main.py` in the repository.



# To get the OpenAI API key -
NOTE - OpenAI API is not free....So once you get the key you can run this game
1. Visit the website - https://platform.openai.com/api-keys
2. Click on generate secret key and get your key


# To Run the Game ..while your virtual environment is activated...type the command `python .\main.py` in the terminal.
