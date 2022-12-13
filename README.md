<h2 align="center">Vue Chrome Extension Boilerplate </h2>

<p>A vueJs boilerplate to create a chrome extension</p>

<h3> Main scripts <h3>
  
 ```bash
  $ npm run dev
  $ npm run build
 ```
  
  <h3> Configure your manifest </h3>
  <p>
    To configure extension manifest edit the file extension.config.js. <a target=”_blank” href="https://developer.chrome.com/docs/extensions/mv3/manifest/">see more.</a>
  </p>
  <p>Example:</p>
  
  ```javascript
  ...
    manifest: {
      name: 'Extension Name',
      description: 'Extension description here',
      version: '1.0',
      manifest_version: 3,
      background: {
        service_worker: 'background.js'
      },
      content_scripts: [],
      permissions: [],
      action: {
        default_popup: 'index.html'
      },
    }
  ...
  ```
  
  <p>
    To configure your source files edit the entry parameter on extension.config.js
  </p>
  <p>Example</p>
  
  ```javascript
  ...
    entry: {
      main: './src/main.js',
      background: './src/background.js',
      content: './src/handle-dom.js'
    }
  ...
  ```
  