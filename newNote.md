When a user creates a new note on the page and clicks submit.

- Post https://fullstack-exampleapp.herokuapp.com/new_note
- gets response 302
  Which is a redirect to `/notes`.
- Get /notes
-

```mermaid
sequenceDiagram
	participant browser
	participant server

	browser->>server: POST https://fullstack-exampleapp.herokuapp.com/new_note
	activate server
	server-->>browser: 302 `/notes`
	deactivate server

	browser->>server: GET https://fullstack-exampleapp.herokuapp.com/notes
    activate server
    server-->>browser: HTML document
    deactivate server

    browser->>server: GET https://fullstack-example.herokuapp.com/main.css
    activate server
    server-->>browser: the css file
    deactivate server

    browser->>server: GET https://fullstack-example.herokuapp.com/main.js
    activate server
    server-->>browser: the JavaScript file
    deactivate server

    browser->>server: GET https://fullstack-example.herokuapp.com/data.json
    activate server
    server-->>browser: [{ "content": "HTML is easy", "date": "2023-1-1" }, ... ]
    deactivate server
```
