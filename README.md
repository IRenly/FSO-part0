# FSO-part0
Entregables tareas Full Stack Open Parte#0


```mermaid
sequenceDiagram
    participant User
    participant Browser
    participant Server

    User ->> Browser: ingresa a la página

    Browser ->> Server: HTTP GET /exampleapp/notes
    Server -->> Browser: HTML code

    Browser ->> Server: HTTP GET /exampleapp/main.css
    Server -->> Browser: main.css

    Browser ->> Server: HTTP GET /exampleapp/main.js
    Server -->> Browser: main.js

    Browser ->> Server: HTTP GET /exampleapp/data.json
    Server -->> Browser: data.json {}

    User ->> Browser: escribe la nota en el formulario
    User ->> Browser: da clic en el botón Save

    Browser ->> Server: HTTP POST /exampleapp/new_note
    Server -->> Browser: HTTP STATUS CODE 302

    Note right of Browser:  <- Se recarga la pagina

    Browser ->> Server: HTTP GET /exampleapp/main.css
    Server -->> Browser: main.css

    Browser ->> Server: HTTP GET /exampleapp/main.js
    Server -->> Browser: main.js

    Browser ->> Server: HTTP GET /exampleapp/data.json
    Server -->> Browser: data.json {}

    Browser -->> User: observa su nota entre la lista de notas
