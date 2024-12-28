# Getting Started with OpenAssistant in React Project

The repository [simple_react_app](https://github.com/openassistant/simple_react_app) is a minimal example of how to use OpenAssistant in a React project.

The basic structure is as follows:

```
src/
├── App.js
├── index.js
public/
├── index.html
├── package.json
```

## Instructions

1. Install dependencies:

To use OpenAssistant in your React project, you need to install the following packages:

```bash
yarn add @openassistant/ui @openassistant/core 
```

2. Add chat component to your app:

```jsx
import { Assistant } from '@openassistant/ui';
// for project not using tailwind, you need to import the css file
import '@openassistant/ui/dist/index.css';

function App() {
  return (
    <div style={{ width: '400px', height: '800px', margin: '20px' }}>
      <Assistant
        name="My Assistant"
        apiKey=""
        version="v1"
        modelProvider="ollama"
        model="llama3.1"
          baseUrl="http://127.0.0.1:11434"
          welcomeMessage="Hello, how can I help you today?"
        instructions="You are a helpful assistant."
        functions={[]}
      />
    </div>
  );
}
```

You can see the UI interface in browser if you run `yarn start`.

<img width="300" alt="" src="https://github.com/user-attachments/assets/394a9bb6-6022-477d-a98d-f85db043ce71" />

3. Set up the local ollama server

Download the Ollama desktop app from [https://ollama.com/download](https://ollama.com/download) and run it.



4. Run the project

```bash
yarn start
```
