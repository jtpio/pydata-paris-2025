---
marp: true
paginate: true
style: |
  .columns {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 1rem;
  }
  .center {
    text-align: center;
  }
---

<style>
section::after {
  content: attr(data-marpit-pagination) '/' attr(data-marpit-pagination-total);
}
img[alt~="center"] {
  display: block;
  margin: 0 auto;
}
iframe {
  border: none;
}
.prompt-box {
  background: #f5f5f5;
  border: 1px solid #ddd;
  border-radius: 4px;
  padding: 12px;
  margin: 10px 0;
  position: relative;
  font-family: monospace;
  font-size: 14px;
  color: #333;
}
.copy-btn {
  position: absolute;
  top: 8px;
  right: 8px;
  background: #007acc;
  color: white;
  border: none;
  border-radius: 3px;
  padding: 4px 8px;
  cursor: pointer;
  font-size: 12px;
}
.copy-btn:hover {
  background: #005a9e;
}
</style>

<div class="center">

# Browser-based AI workflows in Jupyter

## PyData Paris 2025

### 2025-09-30

Jeremy Tuloup
Nicolas Brichet

</div>

---

# About

- Jeremy Tuloup
- Nicolas Brichet
- QuantStack

---

# Agenda

TODO

---

# What is JupyterLite?

![bg fit right:33%](https://raw.githubusercontent.com/jupyterlite/jupyterlite/main/docs/_static/icon.svg)

> JupyterLite is a JupyterLab distribution that runs entirely in the web browser, backed by in-browser language kernels.

---

# Introduction to JupyterLite

---

# Chat with Remote Models

Connect to AI providers, directly from your browser:

- Anthropic
- OpenAI
- Mistral
- Ollama

---

<div class="prompt-box">
  Give suggestions to make the plot look nicer
  <button class="copy-btn" onclick="navigator.clipboard.writeText(this.parentElement.firstChild.textContent.trim())">
    Copy
  </button>
</div>

---

TODO: screencast

---

# Code completion

- Configure a different model for code completion

---

TODO: screencast

---

# Agent Mode

- Tool calling
- Approve or reject tool calls
- Add context

---

TODO: screencast

---

# Accept / Reject Diffs

`jupyterlab-cell-diff` provides a command to display diffs under input cells:

![a screenshot showing the diff view](images/diffs.png)

---

<div class="prompt-box">
  Replace the use of `pandas` with `polars` in this cell
  <button class="copy-btn" onclick="navigator.clipboard.writeText(this.parentElement.firstChild.textContent.trim())">
    Copy
  </button>
</div>

---

TODO: screencast for showing diffs

---

# Execute JupyterLab Commands

- Expose JupyterLab commands as `tools` to the agent.
- `discover_commands` to find available commands
- `execute_command` to execute a command

---

# Model Context Protocol (MCP)

- open-source standard for connecting AI applications to external systems:
  - Tools
  - Resources
  - Prompts

---

# Remote MCP Servers

- The server is hosted somewhere else
- Available from any MCP client with an internet connection
- Ideal for web-based AI applications

---

TODO: screencast with DeepWiki

---

# In-Browser AI

- Run models directly in browser
- No server dependencies
- Privacy-preserving AI

---

# In-Browser AI libraries

- [Transformers.js](https://huggingface.github.io/transformers.js/)
- [WebLLM](https://webllm.mlc.ai/)

---

# WebLLM Demo

TODO: screencast

---

# Built-in AI

- Chrome: Gemini Nano
- Edge: Phi mini

---

# Not just about code

ChromeAI Multimodal capabilities:

- Generate alt text for images
- Transcribe audio to text

---

# The Case of Privacy

- Data stays in browser
- No server round-trips
- Enhanced privacy protection

---

# Limitations of In-Browser AI

- Model size
- The model must be downloaded before use
- Performance
- Browser and hardware compatibility
- Secret management

---

# Building blocks for AI in Jupyter

- Towards modular and extensible components
- Extension authors can provide more functionalities via JupyterLab commands
- Hybrid workflows (server + browser)

---

# What's Next?

- Support for more models and providers
- CLI tools via `jupyterlite-terminal`

---

# References

- Presentation: https://github.com/jtpio/pydata-paris-2025
- Live version: https://jtpio.github.io/pydata-paris-2025/files/index.html
