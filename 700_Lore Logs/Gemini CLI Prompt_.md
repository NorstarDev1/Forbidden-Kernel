 **Gemini CLI Prompt:**

 Hello, Aura. You've been activated in a special context to perform a critical reconnaissance mission.

 **Your Mission:** To scout an old Windows file system and gather the intelligence needed to build a new, unified server architecture on a different  
 operating system (Kubuntu). You are the key to our migration.

 **Your Current Location:** /media/norstar66/Windows (This is a read-only snapshot of the old system).

 **Your Objective:** Identify and document the configuration, code, and scripts for all the AI services and development tools we were using. Your final  
 report will be the blueprint for our new, centralized system.

 **Here is your step-by-step plan:**

  1\. **Initial Reconnaissance:**  
      \* Your first priority is to map the territory. The most valuable files will likely be in user-specific project folders. Start by searching for  
        common development directories. Good places to check would be /Users/norstar66/Documents/, /Users/norstar66/source/repos/, or  
        /Users/norstar66/Projects/.  
      \* Use the list\_directory tool recursively to get a feel for the structure.

  2\. **Identify Key Services & Technologies:**  
      \* Search for files and folders related to the services we need to connect. Your primary targets are: **Windsurf, Ollama, Roo Code, Cline, VS Code**    
        **(server-side configurations), HuggingFace (local cache/configs), Agentic Seek, Computer Use, and CodeX.**  
      \* Be on the lookout for common configuration and project files like:  
          \* docker-compose.yml, Dockerfile  
          \* .env files (document their names and locations, but not their secret values)  
          \* config.json, settings.json, conf.yaml  
          \* package.json (for Node.js projects)  
          \* requirements.txt (for Python projects)  
          \* \*.sh (bash scripts) or \*.bat (windows batch scripts) that might be used to start servers.

  3\. **Detailed Analysis:**  
      \* When you find a relevant file, use read\_file to examine its contents.  
      \* For each service, extract critical information:  
          \* What port was it running on?  
          \* What were the startup commands?  
          \* What other services or databases did it depend on?  
          \* What environment variables were required?  
          \* Where was the source code located?

  4\. **Create Your Intelligence Report:**  
      \* As you gather information, compile it into a single file.  
      \* Use the write\_file command to create a file named AURA\_MIGRATION\_NOTES.md in your current directory (/media/norstar66/Windows).  
      \* Structure the file in Markdown for clarity. For each service you find, create a section like this:

  1     \#\# Service: Ollama  
  2    
  3     \*   \*\*Source Code Location:\*\* \`/Users/norstar66/Projects/ollama-server/\`  
  4     \*   \*\*Configuration Files:\*\*  
  5         \*   \`/Users/norstar66/Projects/ollama-server/config.json\`  
  6         \*   \`/Users/norstar66/Projects/ollama-server/.env\`  
  7     \*   \*\*Startup Command:\*\* \`python server.py \--port 8080\`  
  8     \*   \*\*Dependencies:\*\* \`requirements.txt\` lists \`fastapi\`, \`uvicorn\`.  
  9     \*   \*\*Notes:\*\* Seems to connect to a local database. Port 8080 might conflict with another service.

 Your work here will be the foundation of our new, streamlined system. Once you have created and saved the AURA\_MIGRATION\_NOTES.md file, your mission  
 is complete.

 Spellbound & powered up\!

