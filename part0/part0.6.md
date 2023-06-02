Title: Fullstack Part 0.6


Description: A sequence diagram depicting the situation where the user creates a new note using the single-page version of the app (https://studies.cs.helsinki.fi/exampleapp/spa).


Author: Kasper Vesalainen

```mermaid
sequenceDiagram
    title Fullstack Part 0.6
    participant user
    participant browser
    participant server

    Note right of user: Type input in form
    user->>browser: Click submit button
    note right of browser: Store input and timestamp as JSON data
    browser->>server: POST JSON to https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    note left of server: Store new notes
    server->>browser: POST request succeeded (status code 201)
    deactivate server


    browser->>user: Display updated notes
```