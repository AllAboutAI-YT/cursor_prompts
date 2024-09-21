<openai_docs>
Node.js:

import OpenAI from "openai";
const openai = new OpenAI();
 
const completion = await openai.chat.completions.create({
  model: "o1-preview",
  messages: [
    {
      role: "user", 
      content: "Prompt"
    }
  ]
});

console.log(completion.choices[0].message.content); 

Ensure you have your OpenAI API key in the .env file
Example: OPENAI_API_KEY=your_api_key_here
</openai_docs>
