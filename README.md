Cursor & AI Tools Portfolio Project

This project is part of a hiring assessment to demonstrate my ability to set up development environments, research solutions, troubleshoot issues, and utilize AI tools.

Tools I Installed
- **Git**: Version 2.50.1 (macOS Apple Git-155)
- **Cursor IDE**: Downloaded from cursor.com
- **Claude Code CLI**: Version 2.1.165
- **Claude Code Extension**: Unable to add on Cursor
- **Codex Extension**: Unable to add on Cursor
- **uv**: Version 0.11.19 (Python package manager)
- **LiteLLM**: Version 1.87.1 (Proxy server for translating API formats)
- **Ollama**: Local LLM runner (running qwen2.5-coder:7b model locally)

## Steps I Completed
1. Verified Git installation and configured global user name/email.
2. Downloaded and installed Cursor IDE on macOS.
3. Created a GitHub repository.
4. Installed the Claude Code CLI via terminal.
5. Attempted to set up Claude Code and Codex to Cursor
6. Attempted to use Claude Code, but hit paywalls (no paid subscriptions).
7. Used an AI assistant (GLM/Claude) to find a workaround to run Claude Code for free.
8. Installed `uv` package manager and LiteLLM proxy.
9. Attempted to use Google Gemini API, but hit a billing wall (Google required a credit card).
10. Downloaded Ollama and pulled the `qwen2.5-coder:7b` model to run AI locally on my Mac Mini.
11. Configured LiteLLM and Claude Code to route requests to Ollama.
12. Used the GitHub Web UI to upload this README.

## Issues I Ran Into and How I Solved Them

### 1. `claude: command not found` after CLI installation
- **Issue**: The Claude Code CLI installed successfully, but my terminal could not find the command.
- **Solution**: I used an AI assistant, which explained my Mac was defaulting to bash instead of zsh and the PATH wasn't updated. I switched to zsh and manually added the path to my `~/.zshrc` file.

### 2. `uv` installer URL failing to resolve
- **Issue**: The URL I found for installing `uv` (`https://get.uv.tools`) returned a `Could not resolve host` error.
- **Solution**: I asked an AI assistant for the correct official domain (`astral.sh`), which installed successfully.

### 3. LiteLLM Python Compatibility Error
- **Issue**: Upon installing LiteLLM, it threw a `TypeError` related to `_TypedDictMeta`. I did not understand this error.
- **Solution**: I pasted the error into an AI assistant, which explained LiteLLM was using my Mac's older Python 3.9, but required Python 3.10+. I used `uv` to install Python 3.12 and forced LiteLLM to use it, fixing the issue.

### 4. Claude Code Login Paywalls
- **Issue**: Both the Claude Code and Codex extensions required paid subscriptions/API keys to log in.
- **Solution**: I consulted an AI assistant for a workaround and decided to set up a local proxy to bypass the Anthropic API entirely.

### 5. Google Gemini API Billing Wall
- **Issue**: My initial workaround was to use the free Google Gemini API. However, Google required me to set up a billing account/credit card first, which defeated the purpose of a "free" setup.
- **Solution**: I asked my AI assistant for an alternative, and it recommended using Ollama to run a model entirely locally.

### 6. Cursor UI & Extensions Mismatch
- **Issue**: Instructions to add extensionsfound online were not working in Cursor, and the extensions UI seemed different than expected.
- **Solution**: Attempted to connect Claude Code through terminal with Cursor.

### 7. Git Push Authentication Failure via Terminal
- **Issue**: When trying to push the code to GitHub via the Terminal, the command failed. I did not have the required SSH keys or Personal Access Token (PAT) configured on my Mac to authenticate.
- **Solution**: I bypassed the terminal and used the GitHub web interface to upload files directly.

### 8. LiteLLM Proxy Parameter Mismatch
- **Issue**: When routing Claude Code through LiteLLM to Ollama, I received a `litellm.UnsupportedParamsError` stating Ollama does not support `context_management`.
- **Solution**: This is a known compatibility gap between the parameters Claude Code sends and what local models can understand. I documented the error, but ultimately could not get the proxy to execute commands cleanly.

### 9. Local LLM (Ollama) Hallucinating Tool Calls
- **Issue**: When I launched Claude Code directly via Ollama (`ollama launch claude`), the local model (`qwen2.5-coder`) could not actually read or write files. Instead, it "hallucinated" dummy JSON code pretending to write a file, rather than executing the action.
- **Solution**: I realized that while local models can generate text, smaller models like 7B often struggle with the complex "agentic" tool-calling required by Claude Code. I could not get the local AI to write this file for me, so I used a cloud AI assistant to help me draft this README instead.

### 10. Using AI as a Troubleshooting Tool
- **Issue**: I did not inherently know how to configure API proxies, translate between API formats, or debug Python environments.
- **Solution**: I heavily utilized an AI assistant as a pair programmer. I shared my terminal errors, explained my goals, and followed the step-by-step guidance provided. This allowed me to attempt a complex, multi-tool local AI setup. Even when the local AI setup failed to fully function, the process of troubleshooting it demonstrated my ability to research, adapt, and find workarounds.

