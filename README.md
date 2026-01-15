# ShaderCells

This project provides files to create a custom AI assistant, a program that can answer questions or give advice for working with ReShadeFX. ReShadeFX enhances how games look by modifying visual effects. The ShaderCells project offers a specialized AI assistant for creating ReShadeFX shaders, which are scripts that control these visual changes. It uses a specialized collection of information (its "knowledge base") and a technique called Retrieval-Augmented Generation (RAG) to ensure the AI uses accurate information.

## What is "RAG"?

Imagine an AI that seems knowledgeable but sometimes makes up facts or gives outdated information. RAG, which stands for Retrieval-Augmented Generation, helps address this. With RAG, the AI first looks up information from a trusted source and then uses it to create its response. This method makes the AI's answers more accurate and specific to your question.

ShaderCells uses RAG by following the instructions in Source/Instructions.md. These instructions tell the AI to treat the files in the Source/Knowledge folder as its main source of truth. When you ask the AI a question about a shader:

1. **It retrieves**: The AI searches `REFERENCE.md`, `windows-win32-direct3dhlsl.pdf`, `ReShade.txt`, and `Examples.txt` to find the most relevant information.
2. **It augments**: The AI uses the information it finds to build its response. This ensures shader code, explanations, or debugging advice are correct and follow ReShadeFX's best practices.

This RAG approach makes ShaderCells a specialized and dependable expert for ReShadeFX shader development.

## Installation for Google Gemini

Use this guide to prepare your ShaderCells files for Google's Gemini platform and create a specialized AI assistant.

### Step 1: Download the Files

1. Go to the official project page: https://papadanku.github.io/ShaderCells/
2. Click **`Download .zip`** to get the files.
3. Unzip to a location on your computer that you will remember.

### Step 2: Create Your Gemini Gem

1. Open Google Gemini (https://gemini.google.com/app) and log in.
2. Find and click the **`Gems`** button on the right side of the screen.
3. Click the **`New Gem`** button on the left side of the screen.
4. Give your new Gem a name, like "ShaderCells Assistant."

### Step 3: Configure Your Gem

1. Copy `Source/Description.txt` into the Gem's Description box.
2. Copy `Source/Instructions.md` into the **`Instructions`** box.
3. Add all `Source/Knowledge` files into the Gem's **`Knowledge`** box.

## Installation for Mistral AI's Le Chat

Use this guide to set up ShaderCells files with Mistral AI's Le Chat to create your own ReShadeFX expert.

### Step 1: Download the Files

1. Go to the project's website: https://papadanku.github.io/ShaderCells/
2. Click **`Download .zip`** to get the files.
3. Unzip the files to a location on your computer that you will remember.

### Step 2: Create Your Agent

1. Open Le Chat (https://chat.mistral.ai/chat) and log in.
2. Click **`Agents`** on the left, then select Create an agent.
3. Click the **`New Agent`** box and give it a name, like "Shader Assistant."

### Step 3: Configure Your Agent

1. Copy `Source/Description.txt` into the **`Purpose of this agent`**.
2. Copy `Source/Instructions.md` into the **`Instructions`** box.
3. Click **`Knowledge`** on the Agent customization page.
4. Click the arrow by **`Search libraries`**, then select **`New Library`**.
5. In the **`New Library`** box, name the library something like "Shader Knowledge."
6. Add all `Source/Knowledge` files to the library.
7. Select your new library in the agent customization page.

## Installation for AnythingLLM

Use AnythingLLM to run your AI assistant locally and offline. Follow this guide to set it up with ShaderCells's ReShadeFX knowledge.

### Step 1: Install the Application

1. Download **AnythingLLM** from https://anythingllm.com/desktop.
2. Follow the on-screen prompts to install. For help, see the official documentation.
3. Install your preferred Large Language Model (LLM). LLMs are AI programs designed to understand and generate human language from a prompt.

### Step 2: Create a Workspace

1. In **AnythingLLM**, click the box in the top-left corner to start a new workspace.
2. Name your workspace "ReShadeFX Workspace" and press Save.

### Step 3: Add Knowledge Files

1. In your workspace, click the **upload icon** next to the workspace name.
2. Add all `Source/Knowledge` files to the upload area.
3. Click the **`Move to Workspace`** button to embed the files. This adds them permanently to your workspace so the AI can use them as a reference.
4. Close the window after the embedding completes.

### Step 4: Configure the System Prompt

1. Click the **gear icon** to open chat settings.
2. In **`Chat Settings`**, select **`System Prompt`**.
3. Copy `Source/Instructions.md` into the **`System Prompt`** box.

## Installation for GPT4All

Use GPT4All to run your AI assistant locally without an internet connection. Follow this guide to set up ShaderCells's ReShadeFX capabilities.

Step 1: Prepare the Application

1. Download **GPT4All** from https://www.nomic.ai/gpt4all.
2. Open **GPT4All**.
3. Go to **`Settings > LocalDocs > LocalDocs Setting > Indexing`**.
4. In the **`Allowed File Extensions`** box, add the following file types: `docx,txt,pdf,md,rst,fxh,csx`.

Step 2: Add Knowledge Files

1. Go to **`Settings > LocalDocs > LocalDocs Setting`**.
2. Add `Source/Knowledge` to folders for indexing.
3. Start the indexing process.
4. Go to **`Settings > Model > Model Settings`**.
5. Pick a GPT4All model and click **`Clone`**.
6. Copy `Source/Instructions.md` into **`System Message`**.
