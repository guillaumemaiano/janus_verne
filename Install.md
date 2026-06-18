# Install

This document explains how to set up Janus Verne with a local language model.

For an overview of the system, see [Architecture.md](Architecture.md).

## Requirements

* A local inference engine such as KoboldCpp.
* A GGUF language model.
* A clone of the `janus_verne` repository.
* A world repository (for example `beaumont_world`).

## Conceptual Overview

### Install KoboldCpp

Download or build KoboldCpp.

Launch the server and ensure the Web UI is accessible.

### Install a Language Model

Download a compatible GGUF model.

Load the model in KoboldCpp and verify that text generation works.

The language model provides reasoning and prose. Janus Verne itself contains no intelligence.

### Install Janus and world repositories

This implies cloning two or more repositories using GIT.

World repositories contain canon, references, and memory.

### Verify the Setup

At this point, you should have:

```text
KoboldCpp
    ↓
GGUF Model

janus_verne
    ↓
world repository
```
## Detailed overview

### Install KoboldCpp

Janus Verne currently recommends KoboldCpp.

Official repository:

https://github.com/LostRuins/koboldcpp

Download a release appropriate for your platform and verify that the Web UI launches successfully.

### Install a Language Model

Janus Verne currently recommends a Qwen 3 GGUF model.

Official repository:

https://huggingface.co/Qwen

GGUF conversions:

https://huggingface.co/unsloth

Recommended starting point:

Qwen3-30B-A3B-Instruct-2507-GGUF

Select a quantization appropriate for your hardware.

Verify that the model loads correctly in KoboldCpp and that text generation functions normally.

The language model provides reasoning and prose. Janus Verne itself contains no intelligence.

### Clone Janus Verne

Clone this repository:

```bash
git clone https://github.com/guillaumemaiano/janus_verne.git
```

Janus Verne provides identity, methodology, prompts, and conventions.

### Clone a World Repository

Clone the appropriate world repository:

```bash
git clone <world_repository>
```

Examples:

* `beaumont_world`
* `dover_world`

## Next steps

You are now ready to use Janus Verne.

See [Getting_Started.md](Getting_Started.md) for first steps.
