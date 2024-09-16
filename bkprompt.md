<nodejs_express_setup>
  <instructions>
    <title>How to Set Up a Basic Node.js Backend in a Backend Folder</title>
    <steps>
      <step>
        <number>1</number>
        <description>Create a New Directory for the Backend</description>
        <action>
          <command>mkdir backend</command>
          <command>cd backend</command>
        </action>
      </step>
      <step>
        <number>2</number>
        <description>Initialize a New Node.js Project</description>
        <action>
          <command>npm init -y</command>
        </action>
      </step>
      <step>
        <number>3</number>
        <description>Install Required Dependencies</description>
        <action>
          <command>npm install express</command>
          <command>npm install cors</command>
        </action>
      </step>
      <step>
        <number>4</number>
        <description>Create a Basic Express Server</description>
        <code_file>
          <name>index.js</name>
          <content>
            <![CDATA[
const express = require('express');
const cors = require('cors');

const app = express();
const PORT = 4000; // You can choose any port that's not in use

// Middleware to parse JSON requests
app.use(express.json());

// Middleware to handle CORS (allow requests from your frontend)
app.use(cors());

// Example route
app.get('/', (req, res) => {
  res.send('Hello from the backend server!');
});

// Start the server
app.listen(PORT, () => {
  console.log(`Server is running on http://localhost:${PORT}`);
});
            ]]>
          </content>
        </code_file>
      </step>
      <step>
        <number>5</number>
        <description>Start the Backend Server</description>
        <action>
          <command>node index.js</command>
        </action>
      </step>
    </steps>
  </instructions>
  
  <execution>
    <prompt>Execute this please, use a MODULAR APPROACH with codeblocks I Run Please:</prompt>
  </execution>
</nodejs_express_setup>
