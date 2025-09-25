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

<div class="columns">
<div>

- [Introduction to JupyterLite](#4)
- [Chat with remote models](#5)
- [Agent mode](#6)
- [Remote MCP servers](#9)
- [AI workflows (voice, image)](#10)

</div>
<div>

- [Transformers.js demo](#11)
- [Built-in AI](#12)
- [The case of privacy](#13)
- [What's next?](#14)

</div>
</div>

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

---

TODO: screencast

---

# Agent Mode

-

---

# Accept / Reject Diffs

`jupyterlab-cell-diff` provides a command to display diffs under input cells:

TODO: screenshot

---

TODO: screencast for showing diffs

---

# Execute JupyterLab Commands

- Expose arbitrary JupyterLab commands as `tools` to the agent.
- `discover_commands` to find available commands
- `execute_command` to execute a command

---

# MCP

- What is MCP?

---

# Remote MCP Servers

---

# In-Browser AI

- Run models directly in browser
- No server dependencies
- Privacy-preserving AI

---

# Transformers.js Demo

---

# Beyond Code

- Transcription
- Image recognition

---

# Built-in AI Future

- ChromeAI

---

# The Case of Privacy

- Data stays in browser
- No server round-trips
- Enhanced privacy protection

---

# What's Next?

- Enhanced AI integration
- More model support

---

# Thanks!

- Presentation: https://github.com/jtpio/pydata-paris-2025
- Live version: https://jtpio.github.io/pydata-paris-2025/files/index.html
