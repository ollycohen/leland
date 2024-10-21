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
Creates an author with corresponding bio. Returns status code 201 on success. 

`get_all_authors() -> list`
Returns list of authors by name. TODO return HTTP status code also.

`get_author_by_id(author_id: int)` 
Gets author by index. Returns author object and status code 200 if author exists. If author does not exist, returns status code 404.

`update_author(name: str, bio: str)` 
Updates author if exists and returns code 200. If author does not exist, returns 404.

`delete_author(name: str)` 
Deletes author if exists and returns code 200. Else returns 404.

`create_book(title: str, description: str, author: str,
                published_date: datetime.date)`
Creates book with `published_date` as datetime object. for example, `datetime.datetime(2020, 5, 17)`. Returns code 201 on success.

`get_all_books() -> list` 
Returns list of books by titles. TODO return HTTP status also.

`get_book_by_id(book_id: int) -> str`
Gets book by index. Returns book object and 200 if exists. Else, code 404.

`update_book(title: str, description: str, author: str,
                published_date: datetime.date)`
Returns code 200 if book exists. Else code 404.


`delete_book(title)`
Returns code 200 if book exists. Else code 404.

## Testing

Most methods have corresponding tests in the main python file. Given more time, I would finish writing unit tests for all methods.
You can test the methods yourself by starting an interactive session with the python file in Repl.it's shell `python -i main.py`

## Tools Used

This entire project was completed on Repl.it's iOS mobile app free version (I do not have access to my computer at the moment). 
Repl.it mobile has AI code completion, which was a little buggy but mostly worked great. It definitely saved me time. 
Repl.it free version also has limited use of an internal AI helper to help debug problems. I used that to help me with syntax a couple times until running out of uses.
I used ChatGPT one time at the end to ask the easiest way to test individual functions from my python file within Repl.it.
