LangChain Runnable Examples
This repository contains Python scripts demonstrating various use cases of LangChain's Runnable components, including RunnableSequence, RunnableParallel, RunnablePassthrough, RunnableBranch, and RunnableLambda. Each script showcases a different way to chain language model operations using the LangChain framework with OpenAI's Chat model.
Prerequisites

Python 3.8+
Install required dependencies:pip install langchain langchain-openai python-dotenv


Set up an OpenAI API key in a .env file:OPENAI_API_KEY=your_api_key_here



Files and Descriptions

runnable_sequence.py

Demonstrates a RunnableSequence to create a chain that generates a joke about a given topic and then explains the joke.
Input: A topic (e.g., 'AI').
Output: The joke followed by its explanation.


runnable_parallel.py

Uses RunnableParallel to generate a tweet and a LinkedIn post about a given topic simultaneously.
Input: A topic (e.g., 'AI').
Output: A dictionary containing the tweet and LinkedIn post.


runnable_passthrough.py

Combines RunnableSequence and RunnableParallel with RunnablePassthrough to generate a joke and explain it in parallel.
Input: A topic (e.g., 'cricket').
Output: A dictionary with the joke and its explanation.


runnable_branch.py

Implements RunnableBranch to conditionally summarize a detailed report if it exceeds 300 words.
Input: A topic (e.g., 'Russia vs Ukraine').
Output: Either the full report or a summarized version, depending on word count.


runnable_lambda.py

Uses RunnableLambda to compute the word count of a generated joke alongside the joke itself.
Input: A topic (e.g., 'AI').
Output: The joke and its word count, formatted as a string.



How to Run

Ensure the .env file is configured with your OpenAI API key.
Run any script using Python:python <script_name>.py

Replace <script_name> with the desired file (e.g., runnable_sequence.py).
Each script takes a topic as input and prints the result to the console.

Notes

The scripts use the ChatOpenAI model from LangChain, requiring an active OpenAI API key.
Ensure a stable internet connection for API calls.
Modify the input topics in the invoke method of each script to experiment with different outputs.
