# Project Map

Mermaid diagrams mapping [sachinsshetty](https://github.com/sachinsshetty) projects and how they connect.

## High-level: Vision → Organizations → Projects

```mermaid
flowchart TB
    subgraph Vision["🎯 Vision: Guide to Mars"]
        V1[Accessible Open Source AI]
        V2[Humanoid Robots]
        V3[Healthcare for ALL]
    end

    subgraph Orgs["Organizations"]
        subgraph dwani["dwani-ai · Knowledge from Curiosity"]
            subgraph platform["🌟 Platform"]
                P1[dwani.ai]
                P2[dwani-ai.github.io]
            end
            subgraph llm["🔬 LLM & Experiments"]
                L1[llm-recipes]
            end
            subgraph indic["🗣️ Indic Language Services"]
                I1[asr-indic-server]
                I2[tts-indic-server]
                I3[indic-translate-server]
                I4[docs-indic-server]
            end
            subgraph mobile["📱 Mobile & Discovery"]
                M1[dwani-android]
                M2[discovery]
                M3[workshop]
            end
        end
        subgraph slab["slabstech · Building Sustainable Robots"]
            subgraph infra["🛠️ Infrastructure"]
                S1[action-deploy-container]
                S2[action-cuda-compiler]
                S3[docker]
            end
        end
    end

    subgraph personal["sachinsshetty · Personal"]
        subgraph robotics["🤖 Robotics & Agents"]
            R1[biryani_bot]
            R2[agent-olympics-school]
            R3[agent-beats-dwani-discovery]
        end
        subgraph health["🏥 Healthcare"]
            H1[Sanjeevini]
            H2[care_scribe]
        end
    end

    Vision --> Orgs
    Vision --> personal
    P1 --> I1 & I2 & I3
    L1 --> R1
    S1 & S2 & S3 --> dwani
```

## By category (mindmap style)

```mermaid
mindmap
  root((building dwani.ai))
    dwani-ai
      Platform
        dwani.ai
        dwani-ai.github.io
      LLM Recipes
        llm-recipes
      Indic Services
        asr-indic-server
        tts-indic-server
        indic-translate-server
        docs-indic-server
      Mobile & Discovery
        dwani-android
        discovery
        workshop
    slabstech
      Infrastructure
        action-deploy-container
        action-cuda-compiler
        docker
    Personal
      Robotics
        biryani_bot
        agent-olympics-school
        agent-beats-dwani-discovery
      Healthcare
        Sanjeevini
        care_scribe
```

## Dependency / flow view

```mermaid
flowchart LR
    subgraph inputs["Inputs & infra"]
        docker[docker]
        cuda[action-cuda-compiler]
        deploy[action-deploy-container]
    end

    subgraph indic["Indic language stack"]
        asr[asr-indic-server]
        tts[tts-indic-server]
        trans[indic-translate-server]
        docs[docs-indic-server]
    end

    subgraph platform["Platform & apps"]
        dwani[dwani.ai]
        android[dwani-android]
        discovery[discovery]
        workshop[workshop]
    end

    subgraph experiments["Experiments & robotics"]
        llm[llm-recipes]
        biryani[biryani_bot]
        agents[agent-olympics-school]
    end

    subgraph health["Healthcare"]
        sanjeevini[Sanjeevini]
        care[care_scribe]
    end

    inputs --> indic
    inputs --> platform
    indic --> platform
    llm --> biryani
    platform --> android
```

## Priority projects (top 4)

```mermaid
flowchart LR
    P1[dwani.ai]
    P2[LLM Recipes]
    P3[Sanjeevini]
    P4[Biryani bot]

    P1 --> Platform["Main platform"]
    P2 --> Robots["Tools for Robots"]
    P3 --> Healthcare["AI Healthcare"]
    P4 --> Robotics["Robot cooking"]
```
