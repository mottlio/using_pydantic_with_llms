# Using the Pydantic package to validate data in applications relying on LLM APIs

I've been experimenting with validating LLM input and output data with the [Pydantic](https://ai.pydantic.dev/) Python package. Several applications I'm working on require data validation at different stages: when accepting user input, when receiving responses from LLM APIs, when using that data to call other functions.

User input data can be messy and needs to be validated before being passed to other parts of the application. When using LLM APIs, I've found that simply requesting a certain output format (like JSON) in the LLM prompt is not 100% reliable and the LLM response often contains some additional 'fluff' or misses key fields.  

There are several ways in which the Pydantic package can be used to help with this. It can be used to validate data coming from the user or an LLM response. 

When using [Instructor](https://python.useinstructor.com/), another useful Python library helping to bring structure to LLM outputs, a Pydantic model schema (in JSON format) can also be included directly in the LLM API call. 

I'll experiment with these methods. I'll use the OpenAI, Anthropic and Gemini LLMs in the process. 


