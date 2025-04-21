
  sequenceDiagram
    participant browser
    participant server

    note over browser: Rellenar el formulario save con la nueva nota
    note over browser: presionar el boton save del formulario

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
    activate server
    browser-->>server: {content ,type}
    server-->>browser: HTTP 201 CREATED
    deactivate server
    
   

   
    Note over browser,server: The browser doesnt send more HTTP requests