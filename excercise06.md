

  sequenceDiagram
    participant JS File
    participant server

    note over JS File: document.getElementById('notes_form')
    note over JS File: obtains the form element of the page
    note over JS File: e.preventDefault()
    note over JS File: prevents the default management of the forms sends
    note over JS File: notes.push(note)
    note over JS File: The JS file creates a new note
    note over JS File: redraw()
    note over JS File: redraws the notes list in the browser

    JS File->>server: POST https://studies.cs.helsinki.fi/exagit git mpleapp/new_note
    activate server
    server-->>JS File: HTTP 201
    deactivate server
    
    