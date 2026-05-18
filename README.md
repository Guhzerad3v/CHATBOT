# 📄 Chatbot — PDF Question Answering com Groq

Chatbot em linha de comando projetado para extrair o conteúdo de arquivos PDF e responder perguntas contextuais utilizando o modelo **LLaMA 3.3 (70B)** através da API do Groq.

---

## 🚀 Funcionalidades

* 📄 **Extração Direta:** Lê e processa arquivos PDF localmente usando `PyPDF2`.
* ⚡ **Inferência Ultra-rápida:** Integração com a infraestrutura do Groq utilizando o modelo `llama-3.3-70b-versatile`.
* 🧩 **Orquestração Moderna:** Construído utilizando a sintaxe baseada em LCEL (*LangChain Expression Language*).
* 🛠️ **Tratamento de Contexto:** Proteção nativa contra estouro de tokens, limitando o texto processado a 10.000 caracteres.

---

## 🛠️ Stack Tecnológica

| Biblioteca | Função |
| :--- | :--- |
| **PyPDF2** | Extração e leitura de texto do arquivo PDF. |
| **LangChain (Core)** | Orquestração do prompt dinâmico e gerenciamento do fluxo. |
| **LangChain Groq** | Integração do modelo de linguagem via API do Groq. |
| **LLaMA 3.3 70B** | Modelo de linguagem (LLM) utilizado para a inferência. |

---

## 📋 Pré-requisitos

* Python 3.8 ou superior instalado.
* Uma conta e chave de API criadas no [Groq Console](https://console.groq.com/).

---

## 🔧 Instalação e Configuração

1. **Clone o repositório ou baixe o arquivo do script:**
   ```bash
   python chatbot_v2.py
Instale as dependências necessárias:

# Bash
pip install langchain-core langchain-groq PyPDF2



# ⚠️ Nota de Segurança: Evite deixar sua chave explicitamente hardcoded na variável os.environ["GROQ_API_KEY"] dentro do código se pretender subir o projeto para um repositório público (como o GitHub).

# 🎯 Como Usar
Coloque o arquivo PDF que deseja analisar na mesma pasta do script.

# Certifique-se de que o nome do arquivo no código corresponde ao seu PDF (o padrão configurado é Alan_Turing.pdf):

# Python
nome_do_arquivo = "Seu_Arquivo.pdf"
your_key = A sua chave groq que você pegou anteriormente.
Execute o chatbot.

# Bash
python chatbot_v2.py
Interaja pelo terminal. Para encerrar a sessão, digite x.

# Exemplo de Uso
Plaintext
Leitura concluída com sucesso!

Chatbot pronto. Digite 'x' para sair.

Você: Quem foi Alan Turing?
Processando...

IA: Alan Turing foi um matemático, cientista da computação e criptoanalista britânico, amplamente considerado o pai da ciência da computação teórica e da inteligência artificial...
# ⚠️ Limitações Conhecidas
Tamanho do Texto: O contexto enviado à API é truncado nos primeiros 10.000 caracteres para evitar erros de limite de processamento (Erro 413).

Sem Memória: O chatbot funciona no modelo stateless — cada pergunta é tratada de forma independente, sem histórico das interações anteriores.

Escopo Fechado: As respostas são geradas com base estrita no conteúdo extraído do PDF fornecido.

# 📄 Licença
Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.
