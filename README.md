# Gemini AI Assistant

A single-file Python assistant powered by the Google Gemini API. The project includes persistent local memory, voice interaction, file and system utilities, optional desktop automation, and a terminal interface.

## Features

- Google Gemini API integration with configurable model fallbacks
- Local conversation history and persistent memory under `~/.vesper/`
- Optional speech input/output and desktop interaction
- File indexing and selected system utilities
- Rich terminal interface

## Requirements

- Python 3.10 or newer
- A Google Gemini API key
- `rich` (required)

Install the required package:

```bash
python -m pip install -r requirements.txt
```

Optional capabilities may require `edge-tts`, `SpeechRecognition`, `PyAutoGUI`, `cryptography`, `pypdf`, `PyPDF2`, `Pillow`, and `pytesseract`. Some features may also require platform-specific tools and permissions.

## Configure and run

Set the API key in your environment (recommended):

```bash
export GEMINI_API_KEY="your-api-key"
python gemini_ai_assistant.py
```

On Windows PowerShell:

```powershell
$env:GEMINI_API_KEY = "your-api-key"
python .\gemini_ai_assistant.py
```

The application can also prompt for a key and save it locally under `~/.vesper/api_key`. Do not commit API keys, personal data, or runtime memory files to GitHub.

## Security notice

This is an experimental personal assistant, not a hardened sandbox. It can invoke local shell commands and perform system/file operations; model-generated or user-provided actions can have side effects. Review the code before running it, use it only in an environment you control, and do not run it with elevated privileges or on sensitive systems. Desktop automation and optional modules may require broad device permissions.

## Platform notes

The script contains Termux-oriented paths and behavior as well as cross-platform branches. Compatibility depends on the installed optional packages and available operating-system tools. Test in a disposable environment before relying on it.

## License

No license has been added. All rights remain with the copyright holder unless a license is explicitly provided.
