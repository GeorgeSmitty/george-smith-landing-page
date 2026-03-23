# Generating a Project README with an LLM
**BAIS:3300 Provide Your Project Context
You have two options for giving the LLM information about your
project. Use whichever fits your situation.
### Option A Share a Link to Your GitHub Repository
If your repository is **public**, you can paste the URL directly
into the chat:
`Here is my GitHub repository:
https://github.com/your-username/your-repo-name. Please let me
know if you can read the files.`
If the LLM can read your files it can use them to write accurate,
specific content for each section.
### Option C Prompt to create the README.md
Read and edit the prompt below. Copy the prompt and paste it into
the AI.
---
### The Prompt
````
I need you to generate a professional README.md file for my
project repository.
I have [shared my GitHub repository link / uploaded my project
files] above.
Review the project and generate a complete README.md file using
the following
sections. Write the content in Markdown format so it can be
displayed in GitHub.
Use the actual details of my project 4 sentences describing what
the project does, why it exists, and who it is for.
4. FEATURES
A bullet list of 45 bullet points describing features or
improvements for a hypothetical
future version of this project.
12. CONTRIBUTING
A short paragraph and numbered steps explaining how someone
could fork the
repo, make changes, and submit a pull request.
13. LICENSE
A one-line statement that the project is licensed under the
MIT License,
with a markdown link to a LICENSE file.
14. AUTHOR
My name, institution, and course name.
15. CONTACT
A link to my GitHub profile.
16. ACKNOWLEDGEMENTS
A bullet list crediting any tutorials, tools, documentation,
or AI assistants
used in building the project. If AI tools were used, include a
brief
description of how they were used (e.g., "Initial code
structure generated
with Claude and reviewed/modified by the author"). If the
"vibe coded" badge was used, include this acknowledgement: Icon:
[vibe coding](https://thenounproject.com) by iqonica from [Noun
Project](https://thenounproject.com) (CC BY 3.0)
---
Format requirements:
- Output only the Markdown content Review and Customize
After the LLM generates the README, do the following before
committing it to your repo:
1. **Read every section** the LLM may leave placeholders if it
couldn't find certain details
3. **Update the Author and Contact sections** with your actual
information
4. **Check the badges** go to your GitHub repo, click _Add file_,
and choose _Create new file_. Name it `LICENSE`, then click
_Choose a license template_ and select MIT.
---
### Tips for Better Results
- The more context you provide, the better the output. A public
GitHub link is ideal.
- If the LLM gets something wrong, just say: _"The tech stack is
actually HTML, CSS, and vanilla JavaScript you can reuse it.