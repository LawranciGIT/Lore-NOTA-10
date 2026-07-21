# 📓 Miniguia de Estudos com NotebookLM — Engenharia de Prompts de IA

> Projeto desenvolvido como parte do desafio da [DIO](https://www.dio.me/) sobre uso de Inteligência Artificial como ferramenta de aprendizagem ativa, utilizando o **NotebookLM** para curadoria de fontes, engenharia de prompts e construção de um caderno temático.

---

## 🎯 Contexto e Objetivos

**Assunto escolhido:** Engenharia de Prompts (Prompt Engineering) para modelos de linguagem (LLMs)

**Por que esse tema?**
Prompt engineering é uma habilidade cada vez mais essencial para quem trabalha com IA generativa no dia a dia — tanto para uso pessoal quanto profissional. Escolhi esse tema porque ele é imediatamente aplicável (posso testar o que aprendo na hora) e porque entender a fundo como estruturar prompts melhora diretamente a qualidade de tudo que eu produzo com ferramentas como Claude, ChatGPT e o próprio NotebookLM.

**Objetivos de estudo:**
- [ ] Entender os princípios fundamentais que tornam um prompt eficaz (clareza, contexto, estrutura, exemplos)
- [ ] Conhecer as principais técnicas avançadas (chain-of-thought, few-shot, role prompting, uso de tags/delimitadores)
- [ ] Comparar as recomendações oficiais de diferentes fornecedores (Anthropic, OpenAI, Google)
- [ ] Construir um conjunto de prompts reutilizáveis para acelerar meus estudos e trabalhos futuros

---

## 📚 Curadoria de Fontes

Fontes abertas selecionadas e carregadas no NotebookLM:

| # | Título | Tipo | Link | Por que essa fonte? |
|---|--------|------|------|----------------------|
| 1 | Prompt Engineering — Overview | Documentação oficial (Anthropic) | https://docs.claude.com/en/docs/build-with-claude/prompt-engineering/overview | Fonte oficial da Anthropic, com técnicas específicas para modelos Claude e boas práticas gerais aplicáveis a qualquer LLM |
| 2 | Prompt Engineering Guide (GPT) | Documentação oficial (OpenAI) | https://platform.openai.com/docs/guides/prompt-engineering | Traz a perspectiva da OpenAI, com foco em mensagens de sistema, few-shot e redução de alucinações |
| 3 | Prompt Engineering (whitepaper) | PDF técnico (Google / Lee Boonstra, via Kaggle) | https://www.kaggle.com/whitepaper-prompt-engineering | Whitepaper aprofundado do Google sobre configuração de modelo, técnicas avançadas e boas práticas de documentação de prompts |
| 4 | Prompt Engineering Guide | Guia comunitário aberto (DAIR.AI) | https://www.promptingguide.ai/ | Referência colaborativa muito usada, cobre teoria e técnicas com exemplos práticos e comparações entre modelos |
| 5 | Prompt Engineering Best Practices (Vertex AI) | Documentação oficial (Google Cloud) | https://cloud.google.com/vertex-ai/docs/generative-ai/prompt-engineering/best-practices | Foco em uso em produção/nível empresarial, complementando as fontes mais introdutórias acima |

> 💡 **Critério de seleção:** priorizei documentação oficial dos três principais fornecedores de LLM (para ter múltiplas perspectivas) somada a um guia comunitário de referência (DAIR.AI), garantindo tanto profundidade técnica quanto uma visão consolidada e didática.

---

## 🧪 Engenharia de Prompts e "Cicatrizes"

> ⚠️ **Ação necessária:** as caixas abaixo têm um esqueleto pronto com exemplos de prompts estratégicos. Rode-os no seu NotebookLM (após subir as 5 fontes acima) e substitua as respostas de exemplo pelas respostas reais que você recebeu — isso é o que comprova sua curadoria de fato.

### Prompt 1 — Levantamento geral
**Pergunta feita:**
> "Com base nas fontes carregadas, quais são os 5 princípios mais citados para escrever um bom prompt? Cite de qual fonte veio cada princípio."

**Resposta obtida (resumo):**
[Cole aqui o resumo real gerado pelo NotebookLM]

**Fontes citadas pela IA:** [quais documentos ela usou]

**O que funcionou / não funcionou:**
[ex: a resposta trouxe bons pontos mas misturou dois princípios parecidos — precisei pedir para separar]

---

### Prompt 2 — Refinamento com formato
**Pergunta feita:**
> "Refaça a resposta anterior em uma tabela comparativa: Princípio | Fonte | Exemplo prático de aplicação."

**Resposta obtida (resumo):**
[Cole aqui a resposta real]

**Diferença em relação ao Prompt 1:**
[ex: pedir formato de tabela deixou a comparação entre fornecedores muito mais clara]

---

### Prompt 3 — Aprofundamento técnico
**Pergunta feita:**
> "Explique a técnica de chain-of-thought prompting citada nas fontes. Em que situações ela é mais útil e quais são suas limitações, segundo os documentos?"

**Resposta obtida (resumo):**
[Cole aqui a resposta real]

**O que funcionou / não funcionou:**
[ex: a IA generalizou demais na primeira tentativa; ao pedir "cite trechos específicos de cada fonte" a resposta ficou mais rica e rastreável]

---

### Dificuldades encontradas (troubleshooting)
- [ex: quando a pergunta era muito aberta, o NotebookLM tendia a resumir de forma genérica, sem aprofundar]
- [ex: pedir explicitamente "cite a fonte" melhorou a rastreabilidade das respostas]
- [ex: respostas muito longas — precisei pedir "responda em bullet points de no máximo 1 linha cada"]

**Lição aprendida:** Prompts mais específicos e com formato de saída definido (tabela, bullet points, número de itens) geram respostas muito mais úteis do que perguntas abertas e genéricas.

---

## 📖 Miniguia de Estudo (Entrega Final)

### Resumo estruturado do assunto

**1. O que é engenharia de prompts**
É o processo de estruturar instruções para modelos de linguagem de forma a obter respostas mais precisas, relevantes e consistentes. Não é sobre "adivinhar palavras mágicas", mas sobre comunicar claramente contexto, objetivo e formato esperado da resposta.

**2. Princípios fundamentais**
- **Clareza e especificidade:** instruções vagas geram respostas vagas. Quanto mais específico o pedido (formato, tom, público-alvo, extensão), melhor o resultado.
- **Contexto:** fornecer informações de fundo (quem é o usuário, qual o objetivo final) ajuda o modelo a calibrar a resposta.
- **Exemplos (few-shot prompting):** mostrar 1-3 exemplos do resultado esperado costuma melhorar drasticamente a consistência das respostas.
- **Divisão de tarefas complexas:** pedir para o modelo "pensar passo a passo" (chain-of-thought) ou dividir uma tarefa grande em etapas menores reduz erros em problemas complexos.
- **Iteração:** o primeiro prompt raramente é o ideal — refinar com base na resposta obtida é parte do processo, não uma falha.

**3. Técnicas avançadas**
- **Role prompting:** atribuir um papel ao modelo ("aja como um revisor técnico") ajusta o tom e o nível de detalhe da resposta.
- **Uso de delimitadores/tags:** separar claramente instruções, contexto e dados de entrada (com XML tags, markdown ou aspas) reduz ambiguidade, especialmente em prompts longos.
- **Definição de formato de saída:** especificar explicitamente o formato desejado (JSON, tabela, lista) evita retrabalho de reformatação manual.
- **Prompt chaining:** encadear múltiplos prompts, onde a saída de um alimenta o próximo, ajuda a resolver tarefas que seriam difíceis de resolver em um único prompt.

---

### 📘 Glossário

| Termo | Definição |
|-------|-----------|
| **Prompt** | Instrução ou pergunta enviada a um modelo de linguagem para obter uma resposta |
| **Prompt Engineering** | Prática de projetar e refinar prompts para obter respostas mais precisas e úteis de um modelo de IA |
| **Few-shot Prompting** | Técnica de fornecer alguns exemplos de entrada/saída dentro do prompt para orientar o formato da resposta |
| **Zero-shot Prompting** | Pedir ao modelo que execute uma tarefa sem fornecer nenhum exemplo prévio |
| **Chain-of-Thought (CoT)** | Técnica que instrui o modelo a expor o raciocínio passo a passo antes de chegar à resposta final, útil em problemas lógicos e matemáticos |
| **Role Prompting** | Atribuir uma persona ou papel ao modelo (ex: "aja como um professor") para ajustar tom e profundidade da resposta |
| **Alucinação** | Quando o modelo gera informação incorreta ou inventada com aparência de fato verdadeiro |
| **Contexto (context window)** | Quantidade de texto (instruções, histórico, documentos) que o modelo consegue considerar em uma única interação |
| **Temperatura** | Parâmetro que controla o grau de aleatoriedade/criatividade das respostas geradas pelo modelo |
| **RAG (Retrieval-Augmented Generation)** | Técnica em que o modelo busca informações em uma base de dados/documentos externos antes de gerar a resposta — é como o NotebookLM funciona |

---

### 🔁 Prompts Reutilizáveis para Revisão

Conjunto de prompts prontos para usar em revisões futuras no NotebookLM (ou outra IA):

1. `"Resuma os principais conceitos de [tema] em até 5 bullet points, citando a fonte de cada um."`
2. `"Crie 5 perguntas de revisão estilo quiz sobre [tema], com gabarito, baseadas nas fontes carregadas."`
3. `"Explique [conceito X] como se eu tivesse 12 anos, usando uma analogia do dia a dia."`
4. `"Compare [conceito A] e [conceito B] citados nas fontes, destacando semelhanças, diferenças e em qual documento cada um é mencionado."`
5. `"Com base nas fontes carregadas, quais são os pontos de divergência ou complementaridade entre os autores sobre [tema]?"`
6. `"Monte uma tabela com: Técnica | Quando usar | Exemplo prático, baseada no conteúdo das fontes sobre [tema]."`

---

## 🛠️ Ferramentas Utilizadas
- [NotebookLM](https://notebooklm.google/)
- GitHub (versionamento e portfólio)

## ✅ Status
- [x] Repositório criado
- [ ] Fontes carregadas no NotebookLM
- [ ] Prompts testados e documentados (respostas reais coladas)
- [ ] Miniguia final revisado com base nos testes reais
- [ ] Entrega feita na plataforma DIO
