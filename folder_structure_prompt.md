<folder_structure>
  <root>
    <frontend>
      <app>
        <components>
          <ChatInterface.tsx />
          <MessageList.tsx />
          <MessageInput.tsx />
          <RetroTerminal.tsx />
        </components>
        <styles>
          <globals.css />
        </styles>
        <layout.tsx />
        <page.tsx />
      </app>
      <public>
        <fonts>
          <retro-font.ttf />
        </fonts>
        <images>
          <terminal-background.png />
        </images>
      </public>
      <next.config.js />
      <package.json />
      <tsconfig.json />
    </frontend>
    <backend>
      <src>
        <controllers>
          <chatController.js />
        </controllers>
        <routes>
          <chatRoutes.js />
        </routes>
        <services>
          <openaiService.js />
        </services>
        <utils>
          <errorHandler.js />
          <contextManager.js />
        </utils>
        <middleware>
          <authMiddleware.js />
        </middleware>
        <config>
          <openaiConfig.js />
        </config>
        <app.js />
      </src>
      <package.json />
      <.env />
    </backend>
    <README.md />
    <.gitignore />
  </root>
</folder_structure>

<generate_folder_structure>
<instruction>
You are an LLM with access to generating folders and files in the CWD. Generate the folders and files according to the folder structure described above. Use placeholder code for the file contents.
</instruction>
<action>
Create the specified directories and files in the current working directory (CWD). For each file, include basic placeholder content that represents its purpose or structure.
</action>
</generate_folder_structure>