
# Debug reactJS on chrome  

Open *launch.json* inside */.vscode* (if not present, create the file). Copy (or append to the configuration array) the following: 

```json
{
    // Use IntelliSense to learn about possible attributes.
    // Hover to view descriptions of existing attributes.
    // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Launch Chrome",
            "request": "launch",
            "type": "chrome",
            "url": "http://localhost:3000",
            "webRoot": "${workspaceFolder}"
        },
        {
            "name": "Attach to Chrome",
            "port": 9222,
            "request": "attach",
            "type": "chrome",
            "urlFilter": "http://localhost:3000/*", // use urlFilter instead of url!
            "webRoot": "${workspaceFolder}"
        }
    ]
}
```

## Running debugger

Run react project as usual with the following command: 

```json
npm start
```

Goto Run>Start Debugging. If prompted, select ***Launch Chrome.*** The debugger will be launched in a separate chrome window. 

**Note**: The debugger will be attached to the window that launches with the debugger.
