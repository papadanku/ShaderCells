# ShaderCell

This project gives you the files to create a custom AI assistant for working with ReShadeFX, a tool that changes how games look. The ShaderCell project provides a specialized AI assistant for creating ReShadeFX shaders. It uses a special collection of information (its "knowledge base") and a technique called Retrieval-Augmented Generation (RAG).

## What is "RAG"?

Imagine an AI that knows a lot but sometimes invents facts or gives you old information. RAG helps fix this. It is a method where an AI first **retrieves** information from a trusted source and then uses that information to **generate** its answer. This makes the AI's responses more accurate and specific to the topic.

ShaderCell uses RAG by following the instructions in `Source/Instructions.md`. These instructions tell the AI to treat the files in the `Source/Knowledge` folder as its primary source of truth. When you ask the AI a question about a shader:

1. **It Retrieves**: The AI searches `REFERENCE.md`, `windows-win32-direct3dhlsl.pdf`, `ReShade.txt`, and `Examples.txt` to find the most relevant information.
2. **It Augments**: The AI uses the information it finds to build its response. This ensures that any shader code, explanation, or debugging advice is correct and follows ReShadeFX best practices.

This RAG approach makes ShaderCell a highly specialized and dependable expert for ReShadeFX shader development.

## Installation for Google Gemini

This guide helps you prepare your ShaderCell files for Google's Gemini platform to create your own specialized AI assistant.

### Step 1: Download the Files

1. Go to the official project page: **`https://papadanku.github.io/ShaderCell/`**
2. Click the **`Download .zip`** button to download the project files.
3. Unzip the downloaded file to a memorable location on your computer.

### Step 2: Create Your Gemini Gem

1. Open **Google Gemini** in your web browser and log in.
2. Find and click the option to **`Create a Gemini Gem`**.
3. Give your new Gem a name, like "ShaderCell Assistant."

### Step 3: Configure Your Gem

1. Open `Source/Description.txt`, copy its contents, and paste them into the **`Description`** box in your Gem's settings.
2. Open `Source/Instructions.md`, copy its contents, and paste them into the **`Instructions`** box.
3. Drag and drop all files from the `Source/Knowledge` folder into your Gem's **`Knowledge`** box.

## Installation for Mistral AI's Le Chat

This guide shows you how to use the ShaderCell files with Mistral AI's Le Chat to create your own ReShadeFX expert.

### Step 1: Download the Files

1. Go to the project's website: **`https://papadanku.github.io/ShaderCell/`**
2. Click the **`Download .zip`** button to save the files to your computer.
3. Unzip the downloaded folder to a memorable location.

### Step 2: Create Your Agent

1. Open **Le Chat** in your web browser and log in.
2. On the left side of the screen, click the **`Agents`** button, then click **`Create an agent`**.
3. Click the **`New agent`** box and give it a name, like "Shader Assistant."

### Step 3: Configure Your Agent

1. Open `Source/Description.txt`, copy its contents, and paste them into the **`Purpose of this agent`** box.
2. Open `Source/Instructions.md`, copy its contents, and paste them into the **`Instructions`** box.
3. In the agent customization page, click the **`Knowledge`** button.
4. Click the arrow next to the **`Search libraries`** button, then click **`New Library`**.
5. In the **`New Library`** box, name the library something like "Shader Knowledge."
6. Drag and drop all files from the `Source/Knowledge` folder into the library box.
7. Return to the agent customization page, click the **`Knowledge`** button again, and select the library you just created.

## Installation for AnythingLLM

Use AnythingLLM to run your AI assistant locally and offline. This guide helps you set it up with ShaderCell's ReShadeFX expertise.

### Step 1: Install the Application

1. Download **AnythingLLM** from https://anythingllm.com/desktop.
2. Run the installer and follow the on-screen prompts. For help, refer to the official documentation.
3. Install your preferred Large Language Model (LLM) when prompted.

### Step 2: Create a Workspace

1. In **AnythingLLM**, click the box in the top-left corner to start a new workspace.
2. Name your workspace "ReShadeFX Workspace" and press **`Save`**.

### Step 3: Add Knowledge Files

1. In your workspace, click the **upload icon** next to the workspace name.
2. Drag all files from the `Source/Knowledge` folder into the upload area.
3. Click the **`Move to Workspace`** button to embed the files.
4. Close the window after the embedding process finishes.

### Step 4: Configure the System Prompt

1. Click the **gear icon** to open chat settings.
2. Go to **`Chat Settings`** and select **`System Prompt`**.
3. Open `Source/Instructions.md`, copy its contents, and paste them into the **`System Prompt`** box, replacing the default text.

## Installation for GPT4All

Use GPT4All to run your AI assistant locally without an internet connection.

### Step 1: Prepare the Application

1. Open **GPT4All**.
2. Go to **`Settings > LocalDocs > LocalDocs Setting > Indexing`**.
3. In the **`Allowed File Extensions`** box, add the following file types: `docx,txt,pdf,md,rst,fxh,csx`.

### Step 2: Add Knowledge Files

1. In **GPT4All**, go to **`Settings > LocalDocs > LocalDocs Setting`**.
2. Add the `Source/Knowledge` folder to the list of folders for GPT4All to index.
3. Start the indexing process.

### Step 3: Configure the AI Model

1. Go to **`Settings > Model > Model Settings`**.
2. Choose your desired GPT4All AI model and click the **`Clone`** button.
3. Open `Source/Instructions.md`, copy its contents, and paste them into the **`System Message`** box.
