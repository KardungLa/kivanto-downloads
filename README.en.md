<img src="assets/kivanto-mark.png" width="72" alt="Kivanto">

# Kivanto Free Local

**Your files, knowledge and tasks – together on your computer.**

Organize documents into projects, ask your AI questions about your files, and manage contacts and tasks. Explore connections between your content in the knowledge graph.

**[Download Kivanto →](https://github.com/KardungLa/kivanto-downloads/releases)** · [Deutsch](README.md)

## What you can do

- **Work with your documents:** Upload files or connect local folders, search their contents and ask questions.
- **Explore connections:** Browse entities and relationships in the knowledge graph and export to TTL, CSV, Excel or Markdown.
- **Manage contacts and tasks:** Use the built-in CRM directly or through chat. Review and approve the agent's proposed CRM changes in the conversation.
- **Choose your AI:** Use Ollama, LM Studio, OpenAI, Mistral, OpenRouter or your own compatible provider.
- **Connect other assistants:** Use Kivanto with Claude Desktop, Claude Code or Codex.

## 1. Choose your download

Open the [download page](https://github.com/KardungLa/kivanto-downloads/releases), choose a version and expand **Assets**.

| Your computer | File to choose |
| --- | --- |
| Mac with an Apple chip, such as M1, M2, M3 or M4 | Filename contains **`macos-arm64`** and ends in **`.dmg`** |
| Mac with an Intel processor | Filename contains **`macos-x64`** and ends in **`.dmg`** |
| 64-bit Windows PC with an Intel or AMD processor | Filename contains **`windows-x64`** and ends in **`-en.exe`** |
| 64-bit Linux PC with an Intel or AMD processor | **`linux-x64`**: **`.deb`** for Ubuntu/Debian or **`.tar.gz`** to extract |

On a Mac, check ** → About This Mac** to find your chip. Choose **`-de.exe`** for a German Windows installer. The application supports both English and German.

**Choose the installer for your operating system.** You do not need the “Source code” downloads or the `.jar` file for a normal desktop installation. Java and the local database are included.

Versions marked **Pre-release** are preview builds for trying out new changes. Packages marked **`unsigned`** do not yet have a digitally verified publisher, so your operating system may display a security message. Read the notes for your chosen version.

If there is no matching installer under **Assets**, a download for that platform is not yet available.

## 2. Install Kivanto

### macOS

1. Open the downloaded `.dmg` file.
2. Drag **Kivanto** into **Applications**.
3. Start Kivanto from **Applications**.

### Windows

1. Open the downloaded `.exe` file.
2. Follow the installation wizard.
3. Start **Kivanto** from the Start menu or desktop shortcut.

### Linux

**Ubuntu/Debian:** Open the downloaded `.deb` file with your software manager and install Kivanto. Alternatively, run this in the download folder:

```sh
sudo apt install ./Kivanto-Free-Local-*-linux-x64-unsigned.deb
```

Start **Kivanto** from the application menu, using your normal user account.

**Portable version:** Extract the `.tar.gz` file into a folder you own and start `Kivanto/bin/Kivanto` inside it. Java is included. You need a Linux x64 desktop with glibc 2.35 or newer, X11 or XWayland, and `xdg-utils`. Ubuntu 22.04 and newer desktop installations normally include the basic desktop libraries.

The suggested data folder is `~/.local/share/Kivanto/instance/`. If you set a custom `XDG_DATA_HOME`, it is located there under `Kivanto/instance/` instead. The portable and installed apps use the same data folder.

On first launch, the setup assistant guides you through choosing a language, reading and accepting the terms, and selecting a data folder. You can start with the suggested settings.

Kivanto then opens in your browser. The desktop app continues running in the background.

## 3. Set up your AI

In **Set up AI model**, choose your provider and model. Use **Load models** to see available models and **Test connection** to check your settings.

- **Local AI:** Start Ollama or LM Studio and load a model there. In LM Studio, also start the local server.
- **Cloud AI:** Enter your provider's API key. A chat subscription does not replace an API key; API usage may be billed separately.

You can skip this step and return to it later from the Kivanto status icon. AI answers and automatic extraction of relationships require a configured, reachable AI provider.

## 4. Create your first project

1. Open **Projects → New project** and create a project.
2. Open **Files** and upload your documents. You can select several files at once.
3. Wait for Kivanto to process the documents. Check progress in the project.
4. Open **Chat** and ask a question, such as “Summarize the key points in these documents.”

You can also add an existing folder. Using it as a **project folder** lets Kivanto work directly with the original files. Adding it as a **read-only source** imports copies and leaves the originals unchanged. Use **Synchronize** to import later changes from a source.

You can ask general questions without uploading documents. Answers about your own files require those files to be processed first. Semantic search also requires an embedding model, configured separately from the chat model.

## Everyday use

Find the Kivanto icon in the Mac menu bar or the Windows notification area. On Windows, it may be among the hidden icons. On Linux, icon support depends on your desktop environment. If no tray icon is supported, use the status window; closing it then quits the app.

| Status | Meaning |
| --- | --- |
| Green | Kivanto is running. Choose **Open in browser** to open the interface. |
| Yellow | Kivanto is starting or stopping. |
| Gray | Kivanto is stopped. |
| Red | Something needs attention. Open the status window. |

To close the application completely, choose **Quit Kivanto** from the icon's menu. Closing your browser does not stop the app.

## Your data and costs

Kivanto stores your projects and settings locally. When you connect a cloud AI provider or another external service, the content needed for a request is sent to that service. You choose which AI provider to use.

**Free Local is free for one person on their personally used computer, for personal or professional use.** A shared installation for several people requires the Kivanto Server edition. The terms included with the download apply. Charges from your AI provider or other connected services are separate.

## Updates and backups

Quit Kivanto before installing a new version. Your data is stored separately from the application. If setup asks for a data folder, select the folder you used previously.

For a backup, quit Kivanto and copy the **entire data folder selected during setup**, including `kivanto.env`. Back up any original folders used directly as projects as well.

## Troubleshooting

- **The interface does not open:** Check the status icon and choose **Open in browser**.
- **The AI does not respond:** Open the AI setup, check the selected model and test the connection. For local AI, Ollama or the LM Studio server must be running.
- **An answer misses your documents:** Check the selected project, uploaded files and processing status. Use **Synchronize** to update connected sources when needed.
- **Report a problem:** Open an [issue](https://github.com/KardungLa/kivanto-downloads/issues) with your operating system, Kivanto version and steps to reproduce it. Remove personal content and credentials from screenshots or logs before uploading them.
