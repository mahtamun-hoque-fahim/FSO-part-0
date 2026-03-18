# FSO
## 0.6: New note in Single Page App

```mermaid
sequenceDiagram
    participant browser
    participant server

    Note right of browser: User writes a note and clicks Save

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    Note left of server: Server saves note, responds with 201
    server-->>browser: {"message": "note created"}
    deactivate server

    Note right of browser: JavaScript updates the note list without reloading
```