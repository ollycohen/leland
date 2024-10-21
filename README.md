# Books API

[Click me!](https://replit.com/@ollycohen/Books-API?s=app)

## Implementation Details

This project contains the backend functionality for a hypothetical books API.
The methods and some unit tests are all written in one python file.   
Next steps could involve setting up a local environment to run REST requests that call these functions. 

## How to Run

To run the API functions and unit tests, open the [repl.it](https://replit.com/@ollycohen/Books-API?s=app) and click run.

To play with the API yourself, you can make a new tab in Repl.it, click "Shell", and type `python -i main.py`. 
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

`update_author(name: str, bio: str)`

`delete_author(name: str)`

`create_book(title: str, description: str, author: str,
                published_date: datetime.date)`

`get_all_books() -> list`

`get_book_by_id(book_id: int) -> str`

`update_book(title: str, description: str, author: str,
                published_date: datetime.date)`

`delete_book(title)`

Testing

Tools Used