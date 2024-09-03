OpenAI API Docs =

Node.js:

import OpenAI from "openai";
const openai = new OpenAI();

const completion = await openai.chat.completions.create({
    model: "gpt-4o-mini",
    messages: [
        { role: "system", content: "Your System Instructions" },
        {
            role: "user",
            content: "Your Prompt",
        },
    ],
});

console.log(completion.choices[0].message);

# Ensure you have your OpenAI API key in the .env file
# Example: OPENAI_API_KEY=your_api_key_here