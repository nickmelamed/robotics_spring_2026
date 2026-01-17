# Context is Key

Context is the information you give the model to get an answer. You give the model context in the form of prompts, which are simply the text you give the model in the form of a question (usually). 

Since models cannot read your mind (at least not yet, anyway), the answer you get from them will only be as good as the context you give them. 

For example, say we create a function to calculate someone's age based on their birthday. However, we haven't taken into account the day/month, just the year, so some ages might be wrong.

Below is a poor way to prompt (or ask) the AI to fix this issue: 

```text
Fix my code
```
```python
def calculate_age(birth_date):
    today = datetime.date.today()
    age = today.year - birth_date.year
    return age
```
The model has no idea what to fix here! 

Instead, you should point out the error in the function, and 