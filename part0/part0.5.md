Title: Fullstack Part 0.5
Description: A sequence diagram depicting the situation where the user goes to the single-page app version of the notes app at https://studies.cs.helsinki.fi/exampleapp/spa.
Author: Kasper Vesalainen

```mermaid
sequenceDiagram
    title Fullstack Part 0.5
    participant user
    participant browser
    participant server

    user->>browser: Enter website

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa
    activate server
    server->>browser: HTML document (includes main.css and spa.js)
    deactivate server

    Note right of browser: Execute spa.js

    browser->>server: GET data.json (AJAX)
    activate server
    server->>browser: data.json
    deactivate server

    browser->>user: Display page
```