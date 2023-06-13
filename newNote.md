```mermaid
sequenceDiagram
	participant browser
	participant server

	broswer->>server: Get https://studies.cs.helsinki.fi/exampleapp/notes
	activate server
	server-->>browser: HTML document
```

When a user creataes a new note on the page and clicks submit.

- Post https://fullstack-exampleapp.herokuapp.com/new_note
- gets response 302
  Which is a redirect to `/notes`.
- Get /notes
-

```mermaid
sequenceDiagram
	participant browser
	participant server
```
