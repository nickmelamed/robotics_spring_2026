# Multi-Turn Conversation: Asking More than One Question 

## What is Multi-Turn? 

A turn in an LLM conversation refers to a single sequence of an input (your prompt) followed by an output (the model response). A multi-turn conversation is more than one of these sequences. 

## Why does this difference matter? 

In a single turn conversation, the only context the LLM is handling is your original prompt, and its original output. However, if you ask follow-up questions, its context now includes those questions and corresponding outputs. LLMs have the tendency to "get lost" and "forget" the previous sequences when generating their new outputs. 

However, strong prompting can help mitigate this problem and allow you to get more out of the longer conversations. 

## Prompting for Multi-Turn 

