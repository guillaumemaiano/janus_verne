# Architecture

```mermaid
flowchart TD

    USER[Human Authors]
    KOBOLD[KoboldCpp<br/>Inference Engine]
    MODEL[Qwen GGUF<br/>Language Model]
    JANUS[Janus Verne<br/>Identity, Prompts, Conventions]
    WORLD[World Repository<br/>Canon, References, Memory]

    USER --> KOBOLD
    KOBOLD --> MODEL

    JANUS --> KOBOLD
    WORLD --> KOBOLD

    MODEL --> USER
```

## Components

| Component        | Responsibility                                    |
| ---------------- | ------------------------------------------------- |
| KoboldCpp        | Executes the model and manages context            |
| Language Model   | Provides reasoning and prose                      |
| Janus Verne      | Provides identity, prompts, methodology and tests |
| World Repository | Provides canon and memory                         |
| Human Authors    | Provide purpose and judgment                      |
