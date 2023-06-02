title Fullstack Part 0.4

participant user
participant browser
participant server

Note right of user: Type input in form
user->>browser: Click submit button

browser->>server: POST user input to address new_note
activate server
server->>browser: URL redirect (status code 302)
deactivate server

browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/notes
Note right of browser: Reload /notes page
note right of browser: Fetch data from server by 3 GET requests
browser->>server: GET main.css
browser->>server: GET main.js
browser->>server: GET data.json
activate server
server->>browser: Send fetched files
deactivate server

browser->>user: Display page