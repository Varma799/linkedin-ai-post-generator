# LinkedIn Post Generator using LLM
This project generates LinkedIn posts automatically using Groq LLM models and Streamlit. Users can select a topic, post length, and language, and the system generates a post using few shot prompting based on example LinkedIn posts.

<img src="resources/tool.jpg"/>

Let's say Mohan is a LinkedIn influencer and he needs help in writing his future posts. He can feed his past LinkedIn posts to this tool and it will extract key topics. Then he can select the topic, length, language etc. and use Generate button to create a new post that will match his writing style. 

## Tech Stack
- Python
- Streamlit
- LangChain
- Groq LLM API
- Prompt Engineering

## Technical Architecture
<img src="resources/architecture.jpg"/>

1. Stage 1: Collect LinkedIn posts and extract Topic, Language, Length etc. from it.
1. Stage 2: Now use topic, language and length to generate a new post. Some of the past posts related to that specific topic, language and length will be used for few shot learning to guide the LLM about the writing style etc.

## Features
- Generates LinkedIn posts using Groq LLM
- Supports topic, length, and language selection
- Uses few shot prompting based on past LinkedIn posts
- Simple Streamlit interface 

## Set-up
1. To get started we first need to get an API_KEY from here: https://console.groq.com/keys. Inside `.env` update the value of `GROQ_API_KEY` with the API_KEY you created. 
2. To get started, first install the dependencies using:
    ```commandline
     pip install -r requirements.txt
    ```
3. Run the streamlit app:
   ```commandline
   streamlit run main.py
   ```
