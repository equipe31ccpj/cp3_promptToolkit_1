# cp3_promptToolkit_1
# Prompt Toolkit — Veículos Elétricos

Toolkit de Prompt Engineering desenvolvido em Python para comparar técnicas de prompting utilizando modelos LLM locais via Ollama.

O projeto implementa e compara:

- Zero-Shot Prompting
- Few-Shot Prompting
- Chain-of-Thought (CoT)
- Role Prompting

O domínio escolhido foi análise de feedbacks e suporte para infraestrutura de recarga de veículos elétricos.

---

# Objetivo

O objetivo do toolkit é identificar qual técnica de prompting apresenta melhor desempenho para tarefas de NLP relacionadas ao atendimento e análise de feedbacks de usuários de veículos elétricos.

O sistema compara:

- acurácia
- consistência
- tempo de resposta
- quantidade de tokens utilizados

---

# Estrutura do Projeto

```text
prompt-toolkit/
│
├── README.md
├── requirements.txt
├── .env.example
├── main.py
│
├── src/
│   ├── __init__.py
│   ├── llm_client.py
│   ├── prompt_builder.py
│   ├── techniques.py
│   ├── tasks.py
│   ├── evaluator.py
│   └── report.py
│
├── data/
│   ├── inputs.json
│   └── examples.json
│
├── prompts
│   ├── system_prompts.json
│   └── templates.json
│
├── output/
│   ├── resultados.csv
│   └── graficos/
│
└── docs/
    └── CP02_Grupo.pdf/
---
## Tecnologias Utilizadas
Python 3.10+
Ollama
gpt-oss:120b
pandas
matplotlib
tiktoken
requests
--
## Técnicas Implementadas
* Zero-Shot

Executa a tarefa sem exemplos prévios.

* Few-Shot

Executa a tarefa utilizando exemplos no prompt.

* Chain-of-Thought (CoT)

Utiliza raciocínio passo a passo para resolver tarefas mais complexas.

* Role Prompting

Utiliza personas específicas para especializar o comportamento do modelo.

##  Tarefas Implementadas
* Classificação de Sentimento

Classifica feedbacks como:

POSITIVO
NEGATIVO
NEUTRO
MISTO

* Extração de Problemas

Extrai:

local
problema
modelo do veículo
tempo de espera
Sumarização

* Cria resumos executivos de feedbacks dos usuários.
---
## Como Instalar
1. Clone o projeto
git clone https://github.com/seu-repositorio/prompt-toolkit.git
2. Instale as dependências
pip install -r requirements.txt
Como Instalar o Ollama

Baixe e instale:

https://ollama.com/

## Como Baixar o Modelo
ollama run gpt-oss:120b
Como Executar

Com o Ollama rodando:

python main.py
---
## Funcionamento do Sistema

O fluxo do sistema é:

inputs.json
↓
techniques.py
↓
prompt_builder.py
↓
llm_client.py
↓
evaluator.py
↓
report.py
↓
output/
---
## Métricas Avaliadas

O sistema mede:

acurácia
tokens utilizados
tempo de resposta
consistência entre respostas

## Resultados Gerados

Após a execução, o sistema gera:

* CSV
output/resultados.csv
Gráficos
output/graficos/

Exemplos:

acuracia.png
custo.png

- Exemplo de Uso

Entrada:

"O carregador estava quebrado e demorou muito."

Saída esperada:

NEGATIVO
---
## Bibliotecas Utilizadas

* pandas

Geração de tabelas e CSV.

* matplotlib

Criação de gráficos comparativos.

* tiktoken

Contagem de tokens.

* equests

Comunicação com API local do Ollama.
---
##Guia Rápido — Quando usar cada técnica
| Técnica        | Melhor Uso               |
| -------------- | ------------------------ |
| Zero-Shot      | tarefas simples          |
| Few-Shot       | classificação e padrões  |
| CoT            | raciocínio complexo      |
| Role Prompting | respostas especializadas |

## Resultados Esperados
O projeto permite analisar:

qual técnica possui maior precisão
qual técnica consome menos tokens
qual técnica é mais rápida
qual técnica funciona melhor para cada tipo de tarefa

## Integrantes
Nome 1 — RM
Nome 2 — RM
Nome 3 — RM
│   ├── system_prompts.json
│   └── templates.json
│
├── output/
│   ├── resultados.csv
│   └── graficos/
│
└── docs/
    └── CP02_Grupo.pdf

# Licença

Projeto acadêmico desenvolvido para fins educacionais.

