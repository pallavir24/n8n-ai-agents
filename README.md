# 🧠 n8n Autonomous AI Agents

A collection of autonomous AI agents built with **n8n**, showcasing tool-calling, multi-step reasoning, memory management, and external API orchestration. Each folder contains the exportable workflow JSON, canvas screenshots, sample outputs, and step-by-step setup instructions.

> Looking for deterministic linear automation pipelines? Check out my **[n8n AI Automation Workflows](../n8n-ai-automations)** repository.

## 🤖 Included AI Agents

| Agent | Description | Agent Tools & Capabilities | Key Integrations |
| :--- | :--- | :--- | :--- |
| **[Transcription Summarizer Agent](./transcription-summarizer-agent)** | Downloads a video/audio file from a URL, transcribes it via Groq Whisper (`large-v3`), and autonomously creates, populates, updates, and retrieves a structured Google Doc with both the transcript and summary. | Google Docs (`Create`, `Update` x2, `Get`) | Chat Trigger, HTTP Request, Groq Whisper API, Google Gemini (`3.1-flash-lite`), Google Docs |
| **[Learning Path Generator Agent](./learning-path-generator-agent)** | Researches verified tutorials, docs, and YouTube videos via SerpApi, compiles a structured day-by-day curriculum in Google Docs, and schedules daily 2-hour study sessions on Google Calendar. | SerpApi Search, Google Docs (`Create`, `Update`), Google Calendar (`Create Event`) | Chat Trigger, OpenRouter (`DeepSeek V4 Flash`), HTTP Request (SerpApi), Google Docs, Google Calendar |

## 🚀 How to Import Any Agent

1. Open your **n8n** instance (Cloud or Self-Hosted).
2. Click **Add Workflow** (`+`) in the top-left corner.
3. Click the **three dots menu (`...`)** in the top-right corner and select **Import from File**.
4. Select the `workflow.json` file from the desired agent folder.
5. Open each node with a warning icon (including sub-nodes attached to the AI Agent) and attach your own credentials.
