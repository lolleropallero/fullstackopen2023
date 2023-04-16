sequenceDiagram
    participant browser
    participant server

    Note right of browser: The browser renders note list with the new note. Then browser sends a new note data as payload to server.

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: {"message":"note created"}
    deactivate server