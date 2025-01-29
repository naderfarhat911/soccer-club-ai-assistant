# 🚀 Soccer Club AI Assistant 🤖

[![CI/CD Status](https://github.com/<user>/soccer-club-ai-assistant/actions/workflows/ci-cd.yml/badge.svg)](https://github.com/<user>/soccer-club-ai-assistant/actions)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Docker Pulls](https://img.shields.io/docker/pulls/<user>/soccer-ai-backend)](https://hub.docker.com/r/<user>/soccer-ai-backend)

## 📚 Table des Matières
- [Architecture Technique](#-architecture-technique)
- [Prérequis](#-prérequis)
- [Installation](#-installation)
- [Développement Local](#-développement-local)
- [API Documentation](#-api-documentation)
- [Contributing](#-contributing)

## 🛠 Architecture Technique
```mermaid
graph TD
    A[Frontend React] -->|HTTPS| B[Backend FastAPI]
    B -->|gRPC| C[LLM Service]
    B -->|Vector Search| D[(ChromaDB)]
    B -->|Cache| E[(Redis)]
    C -->|API| F{OpenAI/Azure}
    D -->|Embeddings| G[HuggingFace]
