# Introduction to Node.js

- Node.js was conceived in 2009 by Ryan Dahl as a JavaScript runtime built on Chrome's V8 engine.
- npm 1.0, released in 2011, was a significant milestone as it introduced the node package manager, enabling easy sharing of open-source node libraries.
- The establishment of the Node.js Foundation in 2015 marked a turning point amidst community disputes. Major entities like IBM, Microsoft, and PayPal joined hands to guide the project's growth and evolution under the Linux Foundation.
- Node.js has become a major player in the ecosystem, widely used across various industries, with a flourishing community and numerous international conferences and events.
- JavaScript is commonly associated with front-end development for web applications, but its capabilities extend beyond that.
- Node.js, introduced in 2009, allows leveraging JavaScript for a wider range of tasks including building command line tools, servers, and interacting with the file system.
- Major companies like PayPal, Netflix, and Microsoft have adopted Node.js for constructing scalable event-driven applications.
- The course will cover fundamental aspects of Node core including standard input and output, the module system, and the file system, with practical examples applicable in real-world scenarios.
- In modern web development, front-end functionalities are commonly authored in JavaScript due to its ubiquity in web browsers.
- Using a uniform language for both front-end and back-end development eliminates concerns about syntactical disparities and streamlines the development process.
- Code and data structures can be seamlessly shared between the front-end and back-end, enhancing maintainability and efficiency.
- Notable libraries like Underscore can be leveraged uniformly on both fronts, providing encryption or utility functions.
- Sharing code ensures consistency, such as in user authentication systems or web games where identical algorithms are crucial for preventing cheating.
- Maintaining data models in a single language reduces redundancy and increases efficiency compared to managing them in multiple languages.
- Embracing code sharing and unifying front-end and back-end development in a common language leads to substantial benefits in terms of maintainability and overall development efficiency.

- # Pros of Javascript

   JavaScript offers the advantage of utilizing the same language for both front-end and back-end development with Node.js, enabling seamless code sharing across components.
- Its dynamic nature, where type is determined by value, showcases loose typing compared to strong typing, offering flexibility in coding.
- JavaScript integrates seamlessly with JSON (JavaScript Object Notation), a format well-suited for web applications on both front and back ends, simplifying data transfer without complex conversions.
- While JavaScript has numerous advantages, some may perceive its dynamic nature as a drawback in certain situations. However, the ability to share it between front end and back end significantly enhances web app development.

- # Callbacks and Asynchronous

- Synchronous tasks require waiting for each task to complete before moving on, causing blocking, while asynchronous tasks allow proceeding to the next task without waiting.
- Synchronous processing can lead to a grayed-out screen in applications, hindering user interface responsiveness until background processes complete.
- Asynchronous tasks are crucial for tasks like networking and file system access in web applications, where lengthy waits are common.
- Node.js efficiently handles asynchronous tasks, contributing to its effectiveness in web applications.
- Asynchronous code commonly employs callbacks, where tasks register a callback function to be executed upon completion, allowing execution to continue without waiting.

- # Node Globals

- In Node.js, modules are akin to JavaScript libraries, comprising a set of functions that can be included in applications. These modules can be built-in or external, providing various functionalities. Built-in modules in Node.js can be utilized without any additional installation. To include a module in a Node.js application, the `require()` function is used, specifying the name of the module. For example, `var http = require('http')` imports the built-in HTTP module, allowing access to its functions within the application.

  # NPM (Node Package Manager)

-NPM (Node Package Manager) is a tool for managing Node.js packages, also known as modules. It hosts thousands of free packages on www.npmjs.com. When you install Node.js, NPM is automatically installed on your computer and ready to use.

-A package in Node.js contains all the files needed for a module, which are JavaScript libraries you can include in your project. Downloading a package is straightforward using the command line interface with the `npm install` command followed by the package name. For example, `npm install upper-case` downloads the "upper-case" package.

-NPM creates a folder named "node_modules" in your project directory where the installed package is placed. All future packages you install will also be placed in this folder.

-Once a package is installed, it can be included in your project using the `require()` function like any other module. For instance, `var uc = require('upper-case')` includes the "upper-case" package. Then, you can use the functions provided by the package in your code. For example, `uc.upperCase("Hello World!")` converts the string "Hello World!" to uppercase letters.

# Package.json files

- When distributing a project or placing it in a git repository, including all dependencies is impractical due to space and time constraints.
- To simplify dependency management for other developers, a package.json file can be created to maintain a list of project dependencies.
- The package.json file can be generated by running `npm init` in the terminal, which prompts for project details or uses defaults. It also scans the node_modules folder to add existing dependencies to the list.
- Alternatively, to quickly create a package.json file with defaults, `npm init --yes` can be used.
- The package.json file includes project details and a list of dependencies, making it easier for other developers to install all necessary packages with the `npm install` command.

  # Node modules

  - In Node.js, heavy input/output operations often involve network and disk access.
- To work with files, the 'fs' (file system) module in Node.js is required, which provides functions for file-related operations.
- To demonstrate file reading, a temporary JSON file named 'data.json' is created, containing an object with a 'name' property.
- The 'readFile' function from the 'fs' module is used to read the contents of the JSON file asynchronously. It requires the file location as the first parameter and a callback function as the second parameter.
- Initially, unexpected output with a buffer at the start is encountered due to the absence of a specified file format. To rectify this, 'UTF-8' encoding is added as a string parameter.
- Alternatively, the JSON file can be accessed using 'require' directly, creating a 'data' variable set to 'require' with the path to 'data.json'.
- Differences between objects obtained through 'require' and 'readFile' are observed, with the latter being a string. To convert the string to JSON, 'JSON.parse(data)' is used within the 'readFile' callback, enabling access to properties like 'data.name'.

  # Direectory Access

- Directory reading in Node.js involves accessing the file system using the 'fs' module and the 'readdir' function.
- The 'readdir' function requires the directory location as its initial parameter to specify the directory to be read.
- A callback function is established to handle the error and data parameters returned by 'readdir'.
- When executed, the callback logs the data, showcasing all directories within the specified directory. In this case, it demonstrates all directories within Drive C.
- Utilizing tools like nodemon can simplify the execution of the demonstration file and facilitate observing the output.
- This process illustrates the straightforward approach to reading directories in Node.js.
- Next, we will explore the topic of writing files.

  # Writing files

- File writing in Node.js involves using the 'fs' module and the 'writeFile' function.
- To write a file, the 'writeFile' function is called with the file name as the first parameter and the data to be written as the second parameter.
- Data can be specified directly or stored in a variable, such as a JSON object.
- When using a JSON object, it needs to be converted to a string format using `JSON.stringify()` to align with the expected parameter type of the 'writeFile' function.
- A callback function can be provided as the third parameter to handle errors and provide feedback upon completion of the writing process.
- Implementing the callback function helps eliminate deprecation warnings and provides confirmation of successful file writing.
- This process concludes the exploration of file system operations, paving the way for exploring popular web frameworks for Node.js.

  # Node frameworks

- A framework in software development serves as a foundational structure that provides essential components and structure for building applications.
- In web development, especially for creating large APIs or HTTP servers, leveraging web frameworks is crucial as they offer structured foundations and necessary components.
- Web frameworks for Node.js facilitate tasks such as serving static files for traditional websites or constructing web APIs for interaction in web applications.
- A web API enables the retrieval and storage of data to and from the server or backend, managing functionalities like user creation and retrieval.
- Popular web frameworks for Node.js include Express, Sails, and Koa.
- Express is a traditional and extensively tested framework known for its simplicity, providing a straightforward and reliable option for developers.
- Sails goes beyond a singular framework and includes sub-frameworks like an Object Relational Mapper (ORM), facilitating database access and offering additional functionalities.
- Koa is the most modern among the discussed frameworks, offering a contemporary approach to web development and innovative features.
- In the upcoming sections, we will explore each framework - Express, Sails, and Koa - in detail to understand their features and capabilities better.

# Express Node Manager

- Express.js, the initial web framework designed for Node.js, supports both web applications and web APIs.
- The term "web application" encompasses functionalities on both the front end and back end, distributed across the entire application.
- While web apps may be associated with functionalities running in browsers or on mobile devices, they often need to communicate with a server for tasks like user authentication or retrieving data for display.
- Express.js specifically addresses the back end within Node.js, contributing significantly to the overall app by facilitating communication with the back end.
- Despite its back-end nature, Express.js has extensive community support and online documentation, thanks to its longstanding presence in the development community.

- # Socket.io

- Socket.io facilitates real-time, two-way, event-driven communication, addressing a limitation in Express where only the client can initiate requests to the server. With Socket.io, bidirectional communication is achieved, allowing the server to push notifications and data to the client when specific events occur.

-The mechanism involves two parts: a client-side library for browsers and a server-side library for Node.js. Both feature nearly identical APIs and function in an event-driven manner, similar to Node.js. In the forthcoming demonstration application, we'll explore how this functionality operates.

