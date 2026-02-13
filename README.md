# Projeto Agente de Carreira Adaptativa (ACA) 🤖🚀

O **Agente de Carreira Adaptativa (ACA)** é uma solução inteligente desenvolvida em Python que utiliza **Large Language Models (LLMs)** para atuar como um consultor estratégico de carreira. O projeto foca no fenômeno do *Future of Work*, ajudando profissionais a navegarem na transição entre o mercado tradicional e a era da automação.

---

## 🎯 Objetivo e Visão Geral

O objetivo central é mitigar o impacto da automação através de análises preditivas e planos de ação personalizados. O agente não apenas identifica riscos, mas atua proativamente na sugestão de:
* **Upskilling:** Identificação de gaps técnicos e sugestão de cursos/habilidades complementares.
* **Reskilling:** Mapeamento de competências transferíveis para migração total de área.

---

## ✨ Funcionalidades Implementadas

### 🔍 1. Engine de Análise de Risco de Automação
O sistema processa a descrição das tarefas diárias do usuário e, através de processamento de linguagem natural, estima a probabilidade de automação de cada atividade, gerando um score de vulnerabilidade profissional.

### 🗺️ 2. Gerador de Roadmap de Competências
Com base no perfil atual, o agente consulta uma base de conhecimento (via LLM) para listar as ferramentas e conceitos de IA que o profissional precisa dominar para se tornar um "trabalhador aumentado" pela tecnologia.

### 🎭 3. Simulador de Entrevistas de Alta Fidelidade
O agente assume o papel de um recrutador técnico exigente. Ele utiliza **Engenharia de Prompt** avançada para:
* Avaliar respostas baseadas em lógica e profundidade.
* Fornecer feedback instantâneo sobre pontos de melhoria.
* Simular cenários de pressão reais do mercado.

---

## 🛠️ Stack Tecnológica e Arquitetura

* **Linguagem:** Python 3.x
* **Modelo de IA:** OpenAI GPT-4 / GPT-3.5 (via API)
* **Técnicas de IA:**
    * *Zero-shot e Few-shot Prompting* para classificação de riscos.
    * *System Role Definition* para criação de personas de mentoria.
* **Ambiente:** Jupyter Notebook (Google Colab) com integração de variáveis de ambiente para segurança de chaves.

---

## 🚀 Como Configurar e Rodar

1. **Chave de API:** Obtenha sua `OPENAI_API_KEY` no painel da OpenAI.
2. **Ambiente:** No Google Colab, adicione sua chave nas "Secrets" (ícone de chave na lateral) com o nome `OPENAI_API_KEY`.
3. **Execução:**
    ```python
    # O código utiliza a biblioteca openai
    pip install openai
    ```
4. **Interação:** Siga as instruções no notebook para inserir seu cargo atual e iniciar a consultoria.

---

## 🎓 Contexto do Projeto
Desenvolvido para a disciplina de **Prompt e Inteligência Artificial (Ciência da Computação)**, visando a aplicação prática de agentes autônomos no planejamento de carreira moderno.
