# 🎙️ Multilanguage Voice Assistant — Whisper + ChatGPT + gTTS

> **DIO Bootcamp challenge:** Building a voice-powered conversational AI assistant that understands spoken questions in multiple languages and responds with synthesized speech — combining OpenAI Whisper, ChatGPT, and Google Text-to-Speech.

---

## Overview

This project was developed as part of a **DIO Bootcamp challenge** and demonstrates the integration of three powerful AI tools into a single, cohesive voice assistant pipeline:

1. **OpenAI Whisper** — transcribes and translates spoken audio input across multiple languages
2. **ChatGPT (OpenAI API)** — processes the transcribed text and generates accurate, contextual responses
3. **Google Text-to-Speech (gTTS)** — converts ChatGPT's text response back into spoken audio

The result is an end-to-end **voice-to-voice AI assistant** capable of understanding and responding to questions spoken in different languages — no typing required.

---

## How It Works

```
🎤 User speaks a question (any language)
        │
        ▼
┌───────────────────────┐
│   OpenAI Whisper       │  ← Speech-to-Text + Translation
│   Audio transcription  │
└───────────┬───────────┘
            │  Transcribed text
            ▼
┌───────────────────────┐
│   ChatGPT API          │  ← Natural Language Understanding
│   Response generation  │     + Contextual answer
└───────────┬───────────┘
            │  Text response
            ▼
┌───────────────────────┐
│   Google TTS (gTTS)    │  ← Text-to-Speech synthesis
│   Audio output         │
└───────────┬───────────┘
            │
            ▼
🔊 Assistant speaks the answer
```

---

## Tech Stack

| Component | Technology | Role |
|---|---|---|
| **Speech-to-Text** | OpenAI Whisper | Transcribes and translates spoken audio |
| **Language Model** | OpenAI ChatGPT API | Understands questions and generates responses |
| **Text-to-Speech** | Google gTTS | Converts text responses into spoken audio |
| **Language** | Python | Pipeline orchestration and API integration |

---

## Features

- 🎤 **Voice input** — captures spoken questions from the microphone
- 🌍 **Multilanguage support** — Whisper understands and translates across multiple languages
- 🤖 **AI-powered responses** — ChatGPT generates accurate, contextual answers
- 🔊 **Voice output** — gTTS brings responses to life as synthesized speech
- ⚡ **End-to-end pipeline** — fully automated voice-to-voice interaction

---

## Key Concepts Demonstrated

**Speech-to-Text with Whisper**
OpenAI's Whisper model is one of the most robust transcription tools available, capable of handling accents, background noise, and multiple languages with high accuracy. In this project it serves as the entry point — converting the user's voice into processable text.

**Prompt Engineering with ChatGPT**
The transcribed text is sent to the ChatGPT API with a structured prompt that instructs the model to respond concisely and in the appropriate language — demonstrating practical prompt design for voice-first interactions.

**Text-to-Speech with gTTS**
Google's Text-to-Speech library converts ChatGPT's text response into an audio file that is played back to the user, closing the voice-to-voice loop without requiring any manual reading.

**API Integration**
The project connects three separate AI APIs (OpenAI Whisper, OpenAI ChatGPT, Google gTTS) in a single Python pipeline — a pattern directly applicable to production-grade AI assistant architectures.

---

## Installation

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/bootcamp-multilanguage-voice-assistant-whisper-chatgpt.git
cd bootcamp-multilanguage-voice-assistant-whisper-chatgpt

# Install dependencies
pip install -r requirements.txt
```

**Required packages:**
```
openai
openai-whisper
gtts
pygame
sounddevice
scipy
```

---

## Configuration

Create a `.env` file in the root directory with your OpenAI API key:

```env
OPENAI_API_KEY=your_api_key_here
```

> ⚠️ Never commit your `.env` file. Make sure it is listed in `.gitignore`.

---

## How to Run

```bash
python main.py
```

Speak your question when prompted. The assistant will transcribe, process, and respond by voice.

---

## Repository Structure

```
bootcamp-multilanguage-voice-assistant-whisper-chatgpt/
├── main.py                  # Main pipeline — record → transcribe → respond → speak
├── requirements.txt         # Python dependencies
├── .env.example             # Environment variable template
├── .gitignore               # Excludes .env and audio temp files
└── README.md
```

---

## What I Learned

- How to integrate **OpenAI Whisper** for multilanguage Speech-to-Text transcription
- How to use the **ChatGPT API** to generate contextual responses from voice input
- How to implement **gTTS** for Text-to-Speech audio synthesis in Python
- How to chain **multiple AI APIs** into a cohesive, real-time voice pipeline
- The architecture behind modern **voice assistant systems**

---

# 🎙️ Assistente de Voz Multilíngue — Whisper + ChatGPT + gTTS

> **Desafio de Bootcamp DIO:** Construção de um assistente de IA conversacional por voz que entende perguntas faladas em múltiplos idiomas e responde com voz sintetizada — combinando OpenAI Whisper, ChatGPT e Google Text-to-Speech.

---

## Visão Geral

Este projeto foi desenvolvido como um **desafio do Bootcamp da DIO** e demonstra a integração de três poderosas ferramentas de IA em um único pipeline de assistente de voz:

1. **OpenAI Whisper** — transcreve e traduz áudio de entrada falado em múltiplos idiomas
2. **ChatGPT (OpenAI API)** — processa o texto transcrito e gera respostas precisas e contextuais
3. **Google Text-to-Speech (gTTS)** — converte a resposta textual do ChatGPT em áudio falado

O resultado é um **assistente de IA voz-a-voz** capaz de entender e responder perguntas faladas em diferentes idiomas — sem necessidade de digitação.

---

## Como Funciona

```
🎤 Usuário faz uma pergunta por voz (qualquer idioma)
        │
        ▼
┌───────────────────────┐
│   OpenAI Whisper       │  ← Speech-to-Text + Tradução
│   Transcrição de áudio │
└───────────┬───────────┘
            │  Texto transcrito
            ▼
┌───────────────────────┐
│   ChatGPT API          │  ← Compreensão de linguagem natural
│   Geração de resposta  │     + Resposta contextual
└───────────┬───────────┘
            │  Resposta em texto
            ▼
┌───────────────────────┐
│   Google TTS (gTTS)    │  ← Síntese Text-to-Speech
│   Saída de áudio       │
└───────────┬───────────┘
            │
            ▼
🔊 Assistente fala a resposta
```

---

## Stack

| Componente | Tecnologia | Função |
|---|---|---|
| **Speech-to-Text** | OpenAI Whisper | Transcreve e traduz áudio falado |
| **Modelo de Linguagem** | OpenAI ChatGPT API | Entende perguntas e gera respostas |
| **Text-to-Speech** | Google gTTS | Converte respostas em áudio sintetizado |
| **Linguagem** | Python | Orquestração do pipeline e integração de APIs |

---

## Funcionalidades

- 🎤 **Entrada por voz** — captura perguntas faladas pelo microfone
- 🌍 **Suporte multilíngue** — Whisper entende e traduz múltiplos idiomas
- 🤖 **Respostas com IA** — ChatGPT gera respostas precisas e contextuais
- 🔊 **Saída por voz** — gTTS traz as respostas à vida como fala sintetizada
- ⚡ **Pipeline completo** — interação voz-a-voz totalmente automatizada

---

## Conceitos Demonstrados

**Speech-to-Text com Whisper**
O modelo Whisper da OpenAI é uma das ferramentas de transcrição mais robustas disponíveis, capaz de lidar com sotaques, ruído de fundo e múltiplos idiomas com alta precisão. Neste projeto serve como ponto de entrada — convertendo a voz do usuário em texto processável.

**Engenharia de Prompt com ChatGPT**
O texto transcrito é enviado à API do ChatGPT com um prompt estruturado que instrui o modelo a responder de forma concisa e no idioma apropriado — demonstrando design prático de prompts para interações voice-first.

**Text-to-Speech com gTTS**
A biblioteca Google Text-to-Speech converte a resposta textual do ChatGPT em um arquivo de áudio reproduzido ao usuário, fechando o ciclo voz-a-voz sem exigir leitura manual.

**Integração de APIs**
O projeto conecta três APIs de IA distintas (OpenAI Whisper, OpenAI ChatGPT, Google gTTS) em um único pipeline Python — um padrão diretamente aplicável a arquiteturas de assistentes de IA em produção.

---

## Instalação

```bash
# Clonar o repositório
git clone https://github.com/YOUR_USERNAME/bootcamp-multilanguage-voice-assistant-whisper-chatgpt.git
cd bootcamp-multilanguage-voice-assistant-whisper-chatgpt

# Instalar dependências
pip install -r requirements.txt
```

**Pacotes necessários:**
```
openai
openai-whisper
gtts
pygame
sounddevice
scipy
```

---

## Configuração

Crie um arquivo `.env` na raiz do projeto com sua chave da API OpenAI:

```env
OPENAI_API_KEY=sua_chave_aqui
```

> ⚠️ Nunca faça commit do arquivo `.env`. Certifique-se de que está listado no `.gitignore`.

---

## Como Executar

```bash
python main.py
```

Fale sua pergunta quando solicitado. O assistente vai transcrever, processar e responder por voz.

---

## Estrutura do Repositório

```
bootcamp-multilanguage-voice-assistant-whisper-chatgpt/
├── main.py                  # Pipeline principal — gravar → transcrever → responder → falar
├── requirements.txt         # Dependências Python
├── .env.example             # Template de variáveis de ambiente
├── .gitignore               # Exclui .env e arquivos de áudio temporários
└── README.md
```

---

## O que Aprendi

- Como integrar o **OpenAI Whisper** para transcrição Speech-to-Text multilíngue
- Como usar a **API do ChatGPT** para gerar respostas contextuais a partir de entrada de voz
- Como implementar **gTTS** para síntese de áudio Text-to-Speech em Python
- Como encadear **múltiplas APIs de IA** em um pipeline de voz coeso e em tempo real
- A arquitetura por trás de sistemas modernos de **assistentes de voz**
