# GeminiFX

This project provides special files to help you create a custom AI assistants for working with ReShadeFX, a tool used to change how games look.

## Install Instructions (Google Gemini)

This guide helps you get your GeminiFX files ready for use with Google's Gemini platform to create your own specialized AI assistant.

### Step 1: Get the Files

1. Go to the official project page here: **`https://papadanku.github.io/GeminiFX/`**
2. Click the **`Download .zip`** button (it's usually in the middle at the top of the page) to download all the project files.
3. **Unzip** the downloaded file to a place on your computer where you can easily find it.

### Step 2: Make Your Custom AI Assistant

1. Open **Google Gemini** in your web browser (make sure you're logged in).
2. Look for an option to "Create a Gemini Gem" or something similar to start building a new custom AI.
3. **Give Your AI a Name**: Choose a clear name for your new AI, like "GeminiFX Assistant."

### Step 3: Give Your AI Its Instructions and Knowledge

Now you'll copy and paste important information into your new AI assistant's settings.

#### A. Description (What Your AI Does)

1. Find the **`Description.txt`** file inside the `Source` folder you unzipped.
2. **Copy** everything in that file.
3. **Paste** the copied text into the "Description" box in your AI's settings. This tells users what your AI assistant is good at.

#### B. Instructions (How Your AI Should Behave)

1. Find the **`Instructions.md`** file inside the `Source` folder.
2. **Copy** everything in that file.
3. **Paste** the copied text into the "Instructions" box in your AI's settings. This text tells your AI assistant how to act and what rules to follow.

#### C. Knowledge Files (What Your AI Knows)

1. Find the **`Knowledge`** folder inside the `Source` folder. This folder has important `.fx` files (shader code) and a `REFERENCE.md` file (documentation).
2. **Drag and drop** all the files from the **`Knowledge`** folder directly into your AI's "Knowledge" box. These files give your AI assistant all the technical information it needs to help you.

## Install Instructions (AnythingLLM)

Use AnythingLLM to run your AI assistant locally and offline. This guide helps you set it up to use GeminiFX's ReShadeFX expertise.

### Step 1: Install AnythingLLM

1. **Download AnythingLLM**: Get the desktop application from https://anythingllm.com/desktop.
2. **Follow Installation Steps**: Run the installer. AnythingLLM guides you through the process. If you encounter issues, refer to their official documentation at https://docs.anythingllm.com/installation-desktop/overview.
3. **Choose Your LLM**: The AnythingLLM app will prompt you to install your preferred Large Language Model (LLM). Follow its instructions. For more help, see https://docs.anythingllm.com/setup/llm-configuration/overview.

### Step 2: Create Your Workspace

Once AnythingLLM is running:

1. **Start a New Workspace**: Click the white box in the top-left corner. A prompt appears, asking for a new workspace name.
2. **Name Your Workspace**: Type "ReShadeFX Workspace" (or your preferred name) into the prompt.
3. **Save**: Press "Save" to create the workspace.

### Step 3: Add GeminiFX Knowledge to AnythingLLM

Now, add the GeminiFX knowledge files to your "ReShadeFX Workspace":

1. **Upload Files**: In your workspace, locate and click the upload icon. It's next to the workspace name ("ReShadeFX Workspace") and the gear icon.
2. **Drag and Drop**: Drag all files from your GeminiFX project's `Source/Knowledge` folder into the upload area.
3. **Select Files**: Confirm the selected files within the upload box.
4. **Move to Workspace**: Click the white "Move to Workspace" button at the bottom of the box.
5. **Embed Files**: AnythingLLM will now embed these files using its chosen embedding engine. This may take some time.
6. **Close Window**: Once embedding finishes, close the upload window.

### Step 4: Configure Your System Prompt

Finally, instruct AnythingLLM on how to use the GeminiFX knowledge:

1. **Open Chat Settings**: Click the gear icon to the right of your workspace name and the upload icon.
2. **Access System Prompt**: Go to `Chat Settings`, then select `System Prompt`. You will see a default prompt.
3. **Copy Instructions**: Navigate to your GeminiFX project folder and open `Source/Instructions.md`. Copy all its content.
4. **Paste Instructions**: Paste the copied text into AnythingLLM's `System Prompt` box, replacing any existing content.

## Install Instructions (GPT4All)

If you prefer to use your AI assistant without an internet connection, you can set it up locally using **GPT4All**, a free desktop AI tool. This lets you use the ReShadeFX expert AI and its knowledge on your own computer.

### Step 1: Prepare GPT4All for Documents

1. Open **GPT4All**.
2. Go to **Settings > LocalDocs > LocalDocs Setting > Indexing**.
3. In the `Allowed File Extensions` box, make sure these file types are listed: `docx,txt,pdf,md,rst,fxh,csx`. This tells GPT4All to read and understand these types of files, including your shader code and documents.

### Step 2: Add Knowledge Files to GPT4All

1. In GPT4All, go to **Settings > LocalDocs > LocalDocs Setting**.
2. Add the `Source/Knowledge` folder (from where you unzipped the GeminiFX project) to the list of folders GPT4All should look at. This will allow GPT4All to read `Examples.txt`, `REFERENCE.md`, `ReShade.fxh`, and `windows-win32-direct3dhlsl.pdf`.
3. Start the "indexing" process in GPT4All. This makes the files searchable by the AI.

### Step 3: Configure Your GPT4All AI Model

1. Go to **Settings > Model > Model Settings**.
2. Choose the GPT4All AI model you want to use.
3. Click the `Clone` button to make a copy of the model's settings that you can change.
4. In the `System Message` box, copy and paste the entire content of the `Source/Instructions.md` file. This will teach your local GPT4All model to act like the GeminiFX expert, just like the online version.

## How GeminiFX Uses Its Knowledge and "RAG"

The GeminiFX project aims to be a specialised AI assistant for creating ReShadeFX shaders. It does this by using a special collection of information (its "knowledge base") and a technique called Retrieval Augmented Generation (RAG).

### What `Source/Instructions.md` Does

The `Source/Instructions.md` file is like the AI's main rulebook. It tells the AI:

- **Who it is (Persona)**: It makes the AI act like a "ReShadeFX shader author." This means it will always be precise, use correct code, and explain things technically.
- **What to do (Task)**: It lists the AI's main jobs, such as writing shader code, fixing your code, explaining shader concepts, showing off ReShadeFX features, and turning your ideas into working shader logic.
- **What to know (Context)**: Most importantly, it points the AI to the files in the `Source/Knowledge` folder and tells it that *only* the information in those files is true and correct. This is a key part of how RAG works.

### What the `Source/Knowledge` Folder Contains

This folder holds all the specific documents and examples that make up the AI's expertise in ReShadeFX. These include:

- **`REFERENCE.md`**: This is the main guide for the ReShadeFX language. It explains its unique code rules, special commands (macros), how to use textures and samplers, variables, and built-in functions.
- **`windows-win32-direct3dhlsl.pdf`**: This PDF teaches the basics of High-Level Shading Language (HLSL), which ReShadeFX is built upon. It covers general code structure and how different parts of a shader work.
- **`ReShade.fxh`**: This is an important file with helpful functions and settings, especially for accessing and configuring the "depth buffer" (which helps shaders understand how far away objects are).
- **`Examples.txt`**: This file contains real, complete examples of ReShadeFX shaders. These examples show you how to create different visual effects and follow good coding practices.

### What is Retrieval Augmented Generation (RAG)?

Imagine an AI that knows a lot, but sometimes makes things up or gives old information. RAG helps fix this. It's a method where an AI first **looks up** information from a trusted source (like a library) and then uses that information to **create** its answer. This makes the AI's responses much more accurate, less likely to invent facts, and very specific to the topic.

### How GeminiFX Uses RAG for Shader Help

GeminiFX uses RAG by telling the AI (through `Source/Instructions.md`) to treat the files in the `Source/Knowledge` folder as a primary source of information. When you ask the AI a question or for help with a shader:

1. **It Looks Up (Retrieves)**: The AI searches through `REFERENCE.md`, `windows-win32-direct3dhlsl.pdf`, `ReShade.fxh`, and `Examples.txt` to find the most relevant information for your request.
2. **It Creates an Answer (Augments)**: Then, it uses this found information to build its response. This ensures that any shader code it generates, explanations it gives, or debugging advice it offers is correct, follows the rules of ReShadeFX, and is based on solid facts.

This RAG approach makes GeminiFX a highly specialized and dependable expert for ReShadeFX shader development, always relying on verified documents instead of just general knowledge.
