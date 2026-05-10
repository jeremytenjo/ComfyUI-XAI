# ComfyUI-XAI

Custom ComfyUI node that uses xAI Grok Vision to analyze an image and generate a prompt.

## What It Does

- Analyzes input images with Grok Vision
- Outputs a detailed prompt for image generation workflows
- Supports custom system/user prompts
- Supports API key via env var or node input

## Install

For ComfyUI on RunPod (or similar):

```bash
cd /workspace/ComfyUI/custom_nodes
git clone https://github.com/jeremytenjo/ComfyUI-XAI.git
cd ComfyUI-XAI
pip install -r requirements.txt
```

If you need to locate your `custom_nodes` folder:

```bash
find / -maxdepth 4 -type d -name "custom_nodes" 2>/dev/null
```

Restart ComfyUI after install.

## Setup

Set your API key (recommended):

```bash
export XAI_API_KEY="your-api-key-here"
```

Or paste it directly into the node `api_key` input.

Optional custom endpoint:

```bash
export XAI_BASE_URL="https://custom-api.example.com/v1"
```

## Node Properties

Node name in ComfyUI: `ComfyUI-XAI` (`ComfyUIXAI`)

Required inputs:
- `image` (`IMAGE`): Input image tensor
- `api_key` (`STRING`): xAI API key. If empty, uses `XAI_API_KEY` env var
- `model` (`STRING` enum): `grok-4-1-fast-non-reasoning`

Optional inputs:
- `system_prompt` (`STRING`, multiline): Custom instruction for prompt generation

Output:
- `prompt` (`STRING`): Generated image prompt text

Node metadata:
- `FUNCTION`: `analyze_image`
- `CATEGORY`: `image/analysis`
- `OUTPUT_NODE`: `True`

## Update

```bash
cd /workspace/ComfyUI/custom_nodes/ComfyUI-XAI
git pull
pip install -r requirements.txt
```

Restart ComfyUI after updating.

## Links

- [xAI API Docs](https://api.x.ai/documentation)
- [ComfyUI](https://github.com/comfyanonymous/ComfyUI)

## Contributing

Open an issue or PR.
