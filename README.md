# 🐝 Bee Deep Researcher reproduction

This is a reproduction of the original [Ollama Deep Researcher](https://github.com/langchain-ai/ollama-deep-researcher/blob/main/README.md) from Langchain, built using the [BeeAI Framework](https://i-am-bee.github.io/bee-agent-framework#/). All credits go to the Langchain team for the original work 🙏👏.

### Workflow

```mermaid
flowchart TB
    Start --> GenerateQuery[Generate Query]
    GenerateQuery --> WebResearch[Web Research]
    WebResearch --> SummarizeSources[Summarize Sources]
    
    SummarizeSources -->|No Pages Left| ReflectOnSummary[Reflect on Summary]
    
    ReflectOnSummary -->|Loop Count <= Max| WebResearch
    ReflectOnSummary -->|Loop Count > Max| FinalizeSummary[Finalize Summary]
    
    FinalizeSummary --> End
    
    subgraph Search Loop
        WebResearch
        SummarizeSources
        ReflectOnSummary
    end
```

## Run

`npm start <<< "How does the PPO RL algorithm work?"`

## Recording


https://github.com/user-attachments/assets/32cd06f3-0739-48ca-8d79-c3233068fca6

