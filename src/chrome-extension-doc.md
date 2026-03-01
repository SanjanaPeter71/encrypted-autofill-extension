Chrome Extension:

Main Elements:
1. Manifest file: (manifest.json)It is the configuration file, we define the extension's name, version, required permissions etc.
2. Service Worker: This is the background script or we can say it's the event handler. It listens for browser events like "tab closed" or "extension installed".
3. Content Scripts: These are the scripts injected directly into web pages one visit. It has access to the page's DOM (the html) and can modify what one see.
4. Popup UI: This is the interface the user see or appears when user clicks the extension icon in the toolbar.
   

Step-by-step Development Cycle of Extension :
1. A dedicated folder for our chrome extension project
2. Define the manifest.json file.
3. Logic: 
   1. Content.js - to interact with websites
   2. popup.html and popup.js for the user interface
   3. Create background.js for background tasks
   

How does the communication happend between the files?
1. These files uses Message Passing to talk to each other.
2. We use chrome.runtime.sendMessage() to send a message and quick response.
3. For data persistence, we use chrome.storage 