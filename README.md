# ComfyUI-XAI - ComfyUI Custom Node

A ComfyUI custom node that analyzes images using XAI's Grok vision model and generates detailed prompts suitable for image generation models.

## Features

- 🖼️ Analyzes images using Grok's vision capabilities
- 🎨 Generates detailed, structured prompts for image generation
- ⚙️ Configurable system and user prompts
- 🔒 Secure API key handling (supports environment variables)
- 🚀 Fast inference with non-reasoning Grok model

## Installation

Use this when ComfyUI is running inside a RunPod template/container.

1. Open your pod terminal (or SSH into the pod).
2. Go to ComfyUI custom nodes directory (common path shown below):

```bash
cd /workspace/ComfyUI/custom_nodes
```

3. import node:

```bash
git clone https://github.com/jeremytenjo/ComfyUI-XAI.git &&
cd ComfyUI-XAI &&
pip install -r requirements.txt
```

4. Restart ComfyUi

Go to comfyui - click Manager - click Restart

```bash
find / -maxdepth 4 -type d -name "custom_nodes" 2>/dev/null
```

## Setup

### 1. Get Your API Key

- Sign up at [x.ai](https://x.ai) (formerly XAI)
- Get your API key from the dashboard
- Keep it secure!

### 2. Configure API Key

You can provide the API key in two ways:

**Option A: Environment Variable (Recommended)**

```bash
export XAI_API_KEY="your-api-key-here"
```

**Option B: Node Input**
Simply paste your API key directly into the node's `api_key` input field in ComfyUI.

### 3. Optional: Configure Base URL

If using a custom API endpoint, set:

```bash
export XAI_BASE_URL="https://custom-api.example.com/v1"
```

## Update Node

1. Pull updates

```bash
cd /workspace/ComfyUI/custom_nodes/ComfyUI-XAI && git pull && pip install -r requirements.txt
```

2. Restart ComfyUi

Go to comfyui - click Manager - click Restart

## Related Resources

- [XAI Documentation](https://api.x.ai/documentation)
- [ComfyUI Documentation](https://github.com/comfyanonymous/ComfyUI)
- [Grok Vision Capabilities](https://x.ai/api/docs#vision)

## License

Same license as the parent project.

## Contributing

Found an issue or have a feature request? Please submit an issue in the repository.
