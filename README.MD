# Example Project

A minimal Python sample that calls an Azure OpenAI chat completion endpoint using the `openai` SDK.

## Quickstart

### Prerequisites

- Python 3.9 or later

### 1. Clone the repository

```bash
git clone <your-repo-url>
cd example-hackathon-python
```

### 2. Create and activate a virtual environment

On Windows (PowerShell):

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

On macOS/Linux:

```bash
python -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure credentials

Open [main.py](main.py) and update the following values with your own:

- `subscription_key` — your API Key
- `deployment` — the name of your model deployment
- `model_name` — the underlying model name
- `api_version` — the API version to target

> **Tip:** For real projects, load these values from environment variables (e.g. via `os.environ` or `python-dotenv`) instead of hard-coding them.

### 5. Run the sample

```bash
python main.py
```

You should see the assistant's response printed to the terminal.

## Troubleshooting

- **`AuthenticationError`** — verify your `subscription_key` and `endpoint` are correct.
- **`DeploymentNotFound`** — make sure the `deployment` name matches a deployment in your Azure OpenAI resource.
- **SSL or network errors** — check that your machine can reach the Azure endpoint and that any corporate proxy is configured.
