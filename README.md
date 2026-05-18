# CHATBOT
# 📄 ChatbotV2 — PDF Question Answering com Groq

Chatbot de linha de comando que lê um PDF e responde perguntas sobre o conteúdo usando LLaMA 3.3 via Groq API.

## Demo

```
Chatbot pronto. Digite 'x' para sair.

Você: Quem foi Alan Turing?
Processando...

IA: Alan Turing foi um matemático e cientista da computação britânico...
```

## Requisitos

- Python 3.8+
- Conta e chave de API no [Groq Console](https://console.groq.com)

## Instalação

```bash
pip install langchain-core langchain-groq PyPDF2
```

## Configuração

Substitua `"your_key"` pela sua chave no código, ou use variável de ambiente:

```bash
export GROQ_API_KEY="sua_chave_aqui"
```

## Uso

1. Coloque o PDF na mesma pasta do script
2. Altere a variável `nome_do_arquivo` se necessário (padrão: `Alan_Turing.pdf`)
3. Execute:

```bash
python chatbot_v2.py
```

Digite suas perguntas e `x` para sair.

## Limitações

- O contexto é limitado a 10.000 caracteres do PDF para evitar estouro de tokens
- Não há memória de conversa — cada pergunta é independente
- Responde **apenas** com base no conteúdo do PDF carregado

## Stack

| Lib | Função |
|---|---|
| `PyPDF2` | Extração de texto do PDF |
| `LangChain` | Orquestração do prompt |
| `Groq` | Inferência via LLaMA 3.3 70B |

## Licença

MIT
