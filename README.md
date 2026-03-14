# 📓 Caderno Temático — Engenharia de Prompts com IA Generativa

> Projeto desenvolvido com apoio do [NotebookLM](https://notebooklm.google.com/) como parte de um caderno de estudos temático estruturado.

---

## 1. 🎯 Contexto e Objetivos

**Tema escolhido:** Engenharia de Prompts aplicada a modelos de linguagem (LLMs)

A engenharia de prompts é a prática de projetar instruções eficazes para extrair respostas de qualidade de modelos de IA. Com a popularização de ferramentas como ChatGPT, Claude e Gemini, saber comunicar-se estrategicamente com esses sistemas tornou-se uma competência técnica valorizada no mercado.

### Objetivos de Estudo

- Compreender os fundamentos teóricos dos LLMs e como eles processam instruções
- Aprender técnicas consolidadas de prompting (zero-shot, few-shot, chain-of-thought)
- Praticar a criação de prompts reutilizáveis para diferentes contextos profissionais
- Desenvolver senso crítico sobre os limites e riscos do uso de IA generativa

---

## 2. 📚 Curadoria de Fontes

Fontes abertas selecionadas e utilizadas no NotebookLM:

| # | Título | Tipo | Link |
|---|--------|------|------|
| 1 | **Prompt Engineering Guide** — DAIR.AI | Texto/Web | [promptingguide.ai](https://www.promptingguide.ai/) |
| 2 | **A Prompt Pattern Catalog to Enhance Prompt Engineering with ChatGPT** — Jules White et al. (2023) | PDF/ArXiv | [arxiv.org/abs/2302.11382](https://arxiv.org/abs/2302.11382) |
| 3 | **Large Language Models are Zero-Shot Reasoners** — Kojima et al. (2022) | PDF/ArXiv | [arxiv.org/abs/2205.11916](https://arxiv.org/abs/2205.11916) |
| 4 | **Chain-of-Thought Prompting Elicits Reasoning in LLMs** — Wei et al. (2022) | PDF/ArXiv | [arxiv.org/abs/2201.11903](https://arxiv.org/abs/2201.11903) |
| 5 | **OpenAI Prompt Engineering Best Practices** | Texto/Web | [platform.openai.com/docs/guides/prompt-engineering](https://platform.openai.com/docs/guides/prompt-engineering) |

---

## 3. 🔧 Engenharia de Prompts e "Cicatrizes"

### Perguntas estratégicas elaboradas

```
1. "O que diferencia um prompt eficaz de um prompt genérico?"
2. "Quais são as principais técnicas de prompting descritas nas fontes?"
3. "Como o chain-of-thought melhora a qualidade das respostas da IA?"
4. "Quais são os erros mais comuns ao formular prompts?"
5. "Como criar um prompt reutilizável para revisão de conteúdo técnico?"
```

### Variações testadas e aprendizados

| Prompt Original | Variação Testada | Resultado | Aprendizado |
|----------------|-----------------|-----------|-------------|
| "Explique prompt engineering" | "Explique prompt engineering como se eu fosse um dev iniciante, com exemplos práticos" | ✅ Mais didático e aplicável | Contexto + público-alvo melhora a resposta |
| "Liste técnicas de prompting" | "Compare zero-shot, few-shot e chain-of-thought em uma tabela com exemplos" | ✅ Estrutura clara e comparável | Pedir formato específico economiza iterações |
| "O que é alucinação em IA?" | "Dê exemplos reais de alucinação e como minimizá-la no prompt" | ⚠️ Parcialmente útil | Pedir exemplos concretos ainda foi necessário em follow-up |

### 🩹 Dificuldades encontradas (Troubleshooting)

- **Respostas genéricas demais:** Quando o prompt não especificava nível de profundidade, o NotebookLM tendia a resumir superficialmente. *Solução:* adicionar "com base nas fontes carregadas, aprofunde em..."
- **Referências cruzadas imprecisas:** Em algumas respostas, a IA misturava conceitos de fontes diferentes sem distingui-los. *Solução:* pedir explicitamente "cite de qual fonte essa informação vem."
- **Perda de contexto em sessões longas:** Após muitas perguntas, as respostas perdiam coerência com o material original. *Solução:* reiniciar a sessão e recarregar o contexto com um prompt-âncora.

---

## 4. 📖 Miniguia de Estudo

### 4.1 Resumos Estruturados

#### O que são LLMs?
Modelos de linguagem de grande escala (LLMs) são sistemas treinados em vastos corpora textuais que aprendem padrões estatísticos da linguagem. Eles não "entendem" no sentido humano — preveem o próximo token com base no contexto fornecido.

#### Técnicas Fundamentais de Prompting

**Zero-shot:** Instrução direta sem exemplos.
> *"Classifique o sentimento deste texto: 'Adorei o produto!'"*

**Few-shot:** Instrução acompanhada de exemplos para guiar o modelo.
> *"Positivo: 'Adorei!' / Negativo: 'Péssimo!' / Agora classifique: 'Mais ou menos.'"*

**Chain-of-Thought (CoT):** Instrui o modelo a raciocinar passo a passo antes de responder.
> *"Pense passo a passo e então responda: qual é o maior número primo abaixo de 50?"*

**Role Prompting:** Atribui um papel ao modelo para calibrar tom e profundidade.
> *"Você é um professor universitário de ciência da computação. Explique redes neurais."*

---

### 4.2 Glossário

| Termo | Definição |
|-------|-----------|
| **LLM** | Large Language Model — modelo de IA treinado em grandes volumes de texto |
| **Prompt** | Instrução ou entrada textual fornecida a um modelo de IA |
| **Token** | Unidade básica de texto processada pelo modelo (aproximadamente 4 caracteres) |
| **Zero-shot** | Técnica onde o modelo responde sem exemplos prévios no prompt |
| **Few-shot** | Técnica que inclui exemplos no prompt para guiar a resposta |
| **Chain-of-Thought** | Estratégia que induz o modelo a raciocinar em etapas intermediárias |
| **Alucinação** | Quando o modelo gera informações falsas com aparência de verdade |
| **Temperatura** | Parâmetro que controla a criatividade/aleatoriedade das respostas |
| **Contexto** | Todo o texto disponível para o modelo no momento da resposta |
| **Fine-tuning** | Processo de ajuste fino de um modelo com dados específicos de um domínio |

---

### 4.3 Prompts Reutilizáveis

```markdown
## 🔁 Kit de Prompts para Revisão e Estudo

### Resumo de Conceito
"Com base no material carregado, resuma [CONCEITO] em até 5 bullet points 
objetivos, destacando a ideia central e exemplos práticos."

### Comparação de Técnicas
"Compare [TÉCNICA A] e [TÉCNICA B] em uma tabela com colunas: definição, 
quando usar, exemplo prático e limitação."

### Geração de Glossário
"A partir das fontes fornecidas, extraia os 10 termos técnicos mais 
importantes e defina cada um em no máximo 2 linhas."

### Questões de Revisão
"Crie 5 perguntas de revisão sobre [TEMA], variando entre nível básico, 
intermediário e avançado. Inclua as respostas esperadas ao final."

### Aplicação Prática
"Dê 3 exemplos de como [CONCEITO] pode ser aplicado em um contexto 
profissional de [ÁREA]. Seja específico e prático."

### Troubleshooting de Prompt
"Analise este prompt: '[SEU PROMPT]'. Aponte o que está impreciso, 
sugira melhorias e reescreva uma versão otimizada."
```

---

## 🗂️ Estrutura do Repositório

```
📁 caderno-prompt-engineering/
├── README.md               ← este arquivo
├── /fontes                 ← PDFs e links das fontes utilizadas
├── /prompts-log.md         ← registro completo de prompts e respostas
└── /miniguia-final.md      ← versão exportada do guia de estudos
```

---

*Projeto desenvolvido com NotebookLM + curadoria manual de fontes abertas.*