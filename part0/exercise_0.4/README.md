# Exercise 0.4

## Description
This exercise involves creating a simple diagram to illustrate the series of HTTP requests and responses when a user writes a note in https://studies.cs.helsinki.fi/exampleapp/notes 

## Diagram
```mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
    activate server
    server-->>browser: HTML document
    deactivate server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp
    activate server
    server-->>browser: HTML document
    deactivate server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    activate server
    server-->>browser: the CSS file
    deactivate server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    activate server
    server-->>browser: the JavaScript file
    deactivate server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate server
    server-->>browser: [{ "content": "I love you ana", "date": "2024-05-19T03:33:51.888Z" }, ... ]
    deactivate server
```

## Solution

### Step-by-Step Instructions
1. **Inspect the Website**
   - Right-click anywhere on the web page and select "Inspect" from the context menu.
   - This will open the Chrome browser's Developer Tools.

2. **Open the Network Tab**
   - In the Developer Tools, click on the "Network" tab.
   - This tab will show all the network requests made by the browser.

3. **Write a Note**
   - Wrote down "I love you ana"

4. **Click the Save Button**
   - Performed a click in the "Save" button on the website.

5. **Examine the Responses**
   - Look at the network requests that appear in the Network tab.
   - Note down the names and details of the responses, such as their URLs and the payloads.