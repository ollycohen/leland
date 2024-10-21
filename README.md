# Books API

[Click me!](https://replit.com/@ollycohen/Books-API?s=app)

## Implementation Details

This project contains the backend functionality for a hypothetical books API.
The methods and some unit tests are all written in one python file.   
Next steps could involve setting up a local environment to run REST requests that call these functions. 

## How to Run

To run the API functions and unit tests, open the [repl.it](https://replit.com/@ollycohen/Books-API?s=app) and click run.

To play with the API functions yourself, you can make a new tab in Repl.it, click "Shell", and type `python -i main.py`. 
From that point you can test the API methods from the command line. For example, 
```
>>> create_author("Olly Cohen", "Olly writes a blog.")
<HTTPStatus.CREATED: 201>
>>> get_all_authors()
['Olly Cohen']
>>> get_author_by_id(0)
'{"status": 200, "data": ["Olly Cohen", "Olly writes a blog."]}'
```

## API Documentation
`create_author(name: str, bio: str)` 
Creates an author with corresponding bio. Returns HTTP status 200 on success. 

`get_all_authors() -> list`
Returns list of authors by name.

`get_author_by_id(author_id: int)` 
Gets author by index in authors object. Returns author object.

**/* TODO Finish API Documentation **

`update_author(name: str, bio: str)` 

`delete_author(name: str)`

`create_book(title: str, description: str, author: str,
                published_date: datetime.date)`

`get_all_books() -> list`

`get_book_by_id(book_id: int) -> str`

`update_book(title: str, description: str, author: str,
                published_date: datetime.date)`

`delete_book(title)`

## Testing

Most methods have corresponding tests in the main python file. Given more time, I would finish writing unit tests for all methods.
You can test the methods yourself by starting an interactive session with the python file in Repl.it's shell `python -i main.py`

## Tools Used

This entire project was completed on Repl.it's iOS mobile app free version (I do not have access to my computer at the moment). 
Repl.it mobile has AI code completion, which was a little buggy but mostly worked great. It definitely saved me time. 
Repl.it free version also has limited use of an internal AI helper to help debug problems. I used that to help me with syntax a couple times until running out of uses.
I used ChatGPT one time at the end to ask the easiest way to test individual functions from my python file within Repl.it.
