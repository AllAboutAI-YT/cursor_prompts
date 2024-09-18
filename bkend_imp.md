<prompt><nodejs_express_setup>
  <instructions>
    <title>How to Set Up a Node.js Backend for a Next.js Application</title>
    <prerequisites>
      <item>Ensure you have Node.js and npm installed on your system.</item>
      <item>Basic knowledge of JavaScript and command-line operations.</item>
    </prerequisites>
    <steps>
      <step>
        <number>1</number>
        <description>Create a New Directory for the Backend</description>
        <action>
          <command><![CDATA[
mkdir backend
cd backend
          ]]></command>
        </action>
      </step>
      <step>
        <number>2</number>
        <description>Initialize a New Node.js Project</description>
        <action>
          <command><![CDATA[
npm init -y
          ]]></command>
        </action>
      </step>
      <step>
        <number>3</number>
        <description>Install Required Dependencies</description>
        <action>
          <command><![CDATA[
npm install express cors dotenv
npm install --save-dev nodemon
          ]]></command>
        </action>
      </step>
      <step>
        <number>4</number>
        <description>Update <code>package.json</code> Scripts</description>
        <code_file>
          <name>package.json</name>
          <content><![CDATA[
{
  "scripts": {
    "start": "node index.js",
    "dev": "nodemon index.js"
  }
}
          ]]></content>
        </code_file>
      </step>
      <step>
        <number>5</number>
        <description>Create a Basic Express Server with Environment Variables</description>
        <code_file>
          <name>index.js</name>
          <content><![CDATA[
require('dotenv').config();
const express = require('express');
const cors = require('cors');

const app = express();
const PORT = process.env.PORT || 4000;

// Middleware to parse JSON requests
app.use(express.json());

// Middleware to handle CORS (allow requests from your frontend)
const corsOptions = {
  origin: 'http://localhost:3000', // Next.js default port
  optionsSuccessStatus: 200
};
app.use(cors(corsOptions));

// Example route
app.get('/', (req, res) => {
  res.send('Hello from the backend server!');
});

// API Endpoint example
app.post('/api/data', (req, res) => {
  // Handle data sent from frontend
  res.json({ message: 'Data received', data: req.body });
});

// Error-handling middleware
app.use((err, req, res, next) => {
  console.error(err.stack);
  res.status(500).send('Something broke!');
});

// Start the server
app.listen(PORT, () => {
  console.log(`Server is running on http://localhost:${PORT}`);
});
          ]]></content>
        </code_file>
      </step>
      <step>
        <number>6</number>
        <description>Create a <code>.env</code> File for Environment Variables</description>
        <code_file>
          <name>.env</name>
          <content><![CDATA[
PORT=4000
          ]]></content>
        </code_file>
      </step>
      <step>
        <number>7</number>
        <description>Set Up Project Structure for Scalability</description>
        <action>
          <command><![CDATA[
mkdir routes controllers models
          ]]></command>
        </action>
        <note>Organize your code by separating routes, controllers, and models into their respective directories.</note>
      </step>
      <step>
        <number>8</number>
        <description>Start the Backend Server in Development Mode</description>
        <action>
          <command><![CDATA[
npm run dev
          ]]></command>
        </action>
      </step>
      <step>
        <number>9</number>
        <description>Connect Your Next.js Frontend to the Backend</description>
        <note>
          In your Next.js application, you can make API calls to the backend using the Fetch API or Axios. Ensure that the backend server is running, and use the correct port in your requests (e.g., <code>http://localhost:4000/api/data</code>).
        </note>
      </step>
      <step>
        <number>10</number>
        <description>Set Up <code>.gitignore</code> File</description>
        <code_file>
          <name>.gitignore</name>
          <content><![CDATA[
node_modules/
.env
          ]]></content>
        </code_file>
      </step>
    </steps>
  </instructions>
</nodejs_express_setup></prompt>

<execution>
  <action>Execute the prompt above please, use a MODULAR APPROACH with codeblocks I Run Please:</action>
</execution>
