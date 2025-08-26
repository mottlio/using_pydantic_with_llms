# Using the Pydantic package to validate data in applications relying on LLM APIs

I've been experimenting with validating LLM input and output data with the Pydantic Python package. Several applications I'm working on require data validation at different stages. 

Data that can be obtained from user input (comments, issues, reviews, addresses, emails) and passed on to other parts of the application needs to be checked. Calling LLM APIs also creates a need to validate the output data, especially when it will be used to make other API calls. I've found that simply requesting a certain output format (like JSON) in the LLM prompt is not 100% reliable and the LLM response often contains some additional 'fluff' or misses key fields.  

There are several ways in which the Pydantic package can be used for data validation. It can be used to validate data coming from the user or an LLM response. It can also be included directly in the LLM prompt. I'll compare these two methods.


