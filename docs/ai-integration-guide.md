# AI Integration Guide

## Overview

Rosetta DBT Studio includes built-in AI assistance to help you generate dbt™ models, write SQL queries, and automate data transformations. To use the AI features you need to connect at least one AI provider.

---

## Supported AI Providers

| Provider | API Key |
|----------|---------|
| **Google Gemini** | [aistudio.google.com](https://aistudio.google.com) |
| **OpenAI** | [platform.openai.com](https://platform.openai.com) |
| **Anthropic** | [console.anthropic.com](https://console.anthropic.com) |
| **Ollama** | No API key required |
| **OpenAI Compatible** | Optional — depends on the service |
| **LM Studio** | No API key required |

---

## Setup

### Step 1 — Open AI Settings

1. Click **Settings** at the bottom of the left sidebar
2. Click **AI Settings**

![AI Settings empty](images/ai-settings-empty.png)

---

### Step 2 — Add a Provider

1. Click **Add Your First Provider**
2. Fill in the fields:
   - **Provider Name** — a label for your reference
   - **Provider Type** — select your provider from the dropdown
   - **API Key** — paste your key here
3. Click **Test Connection** to verify your key works

![Add AI Provider](images/ai-add-provider.png)

4. Click **Create Provider**

---

### Step 3 — Select a Model and Set Active

1. Click **Edit** on your provider card
2. Open the **Default Model** dropdown and select a model
3. Save your changes
4. Click **Set Active**

![AI model selected](images/ai-model-selected.png)

Your provider is now active and ready to use:

![AI provider active](images/ai-provider-active.png)

---

## Ollama Setup

Ollama runs entirely on your computer with no API key required.

1. Download and install Ollama from [ollama.com](https://ollama.com)
2. Open your terminal and pull a model:
```bash
ollama pull llama3
```
3. In Rosetta DBT Studio go to **Settings** → **AI Settings**
4. Click **Add Provider** and select **Ollama**
5. Set the Base URL to `http://localhost:11434`
6. Click **Test Connection**
7. Select your model and click **Set Active**

---

## OpenAI Compatible Setup

Use this provider to connect any AI service that supports the OpenAI API format. Instead of choosing a built-in provider, you supply the service's address yourself — which lets you connect services like Groq, Together, or OpenRouter, or a model hosted inside your own company.

1. Get the **Base URL** (and an API key, if the service requires one) from your AI service
2. In Rosetta DBT Studio go to **Settings** → **AI Settings**
3. Click **Add Provider** and select **OpenAI Compatible**
4. Fill in the fields:
   - **Provider Name** — a label for your reference
   - **Base URL** — the service's API endpoint (usually ends in `/v1`)
   - **API Key** — optional; enter one only if your service requires it
5. Click **Test Connection**
6. Select your model and click **Set Active**

---

## LM Studio Setup

LM Studio runs open-source models on your own computer, with no API key required. It works the same way as Ollama.

1. Download and install LM Studio from [lmstudio.ai](https://lmstudio.ai)
2. In LM Studio, download a model from the **Discover** tab
3. Open the **Local Server** tab, select your model, and click **Start Server** (it runs on port `1234` by default)
4. In Rosetta DBT Studio go to **Settings** → **AI Settings**
5. Click **Add Provider** and select **LM Studio**
6. Leave **Base URL** empty to use the default local server — only fill it in if you changed the port or are using a cloud-hosted deployment
7. Click **Test Connection**
8. Select your model and click **Set Active**

> **Note:** For a cloud-hosted LM Studio deployment, set the remote **Base URL** and add an **API Key** (optional field).

---

## Accessing AI Features

Once your provider is active, AI features are available in the DBT Studio editor. Open any SQL model file and click the **AI** button at the top right of the editor.

![AI button dropdown](images/ai-button-dropdown.png)

For full details on using AI features see [AI Assistant](features/ai-assistant.md).

---

## Common Issues

**AI features are greyed out**
→ No provider is configured or set as active. Follow the setup steps above.

**Connection test failed**
→ Check your API key was copied correctly with no extra spaces.

**Invalid API key error**
→ Your key may have expired. Generate a new one from your provider's website.

**Ollama not connecting**
→ Make sure the Ollama app is running before testing the connection.

**OpenAI Compatible or LM Studio not connecting**
→ Make sure the service (or LM Studio's local server) is running, and that the Base URL is correct — leave it empty to use LM Studio's default, or include the `/v1` path if your service requires it.