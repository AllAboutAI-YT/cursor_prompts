<Instructions>
How to Set Up a Basic Next.js ShadCN App in a frontend Folder
Create a New Next.js ShadCN Project in a Folder Named frontend

1. Create a New Next.js Project
bash
npx create-next-app@latest frontend

This command will:

Create a new directory named frontend.
Install the latest version of Next.js and its dependencies.
Set up a basic project structure with some initial files in the frontend directory.

2. Navigate to Your Project Directory
bash
cd frontend

3. Install ShadCN CLI
bash
npm install -D @shadcn/ui

4. Initialize ShadCN
bash
npx shadcn@latest init

5. Configure components.json
You will be asked a few questions to configure components.json:

Which style would you like to use? › New York
Which color would you like to use as base color? › Zinc
Do you want to use CSS variables for colors? › yes

6. App structure
Here's how to structure my Next.js apps:

.
├── app
│   ├── layout.tsx
│   └── page.tsx
├── components
│   ├── ui
├── lib
│   └── utils.ts
├── styles
│   └── globals.css
├── next.config.js
├── package.json
├── postcss.config.js
├── tailwind.config.ts
└── tsconfig.json

I place the UI components in the components/ui folder.
The lib folder contains all the utility functions. I have a utils.ts where I define the cn helper.
The styles folder contains the global CSS.

7. Start the Development Server
To start the development server, run:

bash
npm run dev
</Instructions>

<Prompt>
Execute this please, use a MODULAR APPROACH with codeblocks I Run Please:
</Promt>