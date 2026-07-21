# 📓 Miniguia de Estudos com NotebookLM — Prompts de IA

> Projeto desenvolvido como parte do desafio da [DIO](https://www.dio.me/) sobre uso de Inteligência Artificial como ferramenta de aprendizagem ativa, utilizando o **NotebookLM** para curadoria de fontes, engenharia de prompts e construção de um caderno temático.

---

## 🎯 Contexto e Objetivos

**Assunto escolhido:** Prompts de IA — como estruturar comandos eficazes para diferentes contextos de uso (criação de imagens, marketing, uso profissional/jurídico e técnicas avançadas de raciocínio)

**Por que esse tema?**
Prompts de IA deixaram de ser um "truque" isolado e viraram uma habilidade transversal: a mesma lógica de estruturação de comando aparece tanto ao gerar uma imagem quanto ao pedir uma campanha de marketing ou uma pesquisa jurídica. Escolhi reunir fontes de áreas diferentes justamente para entender o que é *específico* de cada contexto e o que é *princípio universal* de um bom prompt.

**Objetivos de estudo:**
- [ ] Entender como a estrutura de um prompt muda conforme o objetivo (imagem, texto de marketing, pesquisa técnica/jurídica)
- [ ] Aprender a técnica de **prompt negativo** e por que ela reduz alucinações da IA
- [ ] Compreender a técnica de **Chain-of-Thought (CoT)** e quando ela melhora a precisão das respostas
- [ ] Identificar pontos em comum entre as recomendações de fontes tão diferentes (marketing, direito, acadêmico, geração de imagem)
- [ ] Construir um conjunto de prompts reutilizáveis para o meu dia a dia

---

## 📚 Curadoria de Fontes

Fontes abertas selecionadas e carregadas no NotebookLM:

| # | Título | Tipo / Foco | Link | Por que essa fonte? |
|---|--------|-------------|------|----------------------|
| 1 | 10 prompts (e comandos) para extrair imagens ultra-realistas e ilustrações profissionais da IA | Artigo (Substack) — geração de imagem | https://prompspravoce.substack.com/p/10-prompts-e-comandos-para-extrair | Traz uma perspectiva bem prática e "de camadas" (sujeito + ambiente + luz + estilo técnico) para prompts de imagem, incluindo o uso de prompt negativo para limpar resultados |
| 2 | 20 prompts de IA para marketing para usar agora! | Artigo (blog HubSpot Brasil) — marketing digital | https://br.hubspot.com/blog/marketing/prompts-de-ia-para-marketing | Fonte de uma empresa de referência em marketing, mostra como estruturar prompts com contexto e variáveis (`<persona>`, `<negócio>`) para tarefas reais do dia a dia |
| 3 | Advoga AI: domine o prompt negativo e reduza os riscos de alucinação da IA | Notícia (OABRJ) — uso jurídico/profissional | https://www.oabrj.org.br/noticias/advoga-ai-domine-prompt-negativo-reduza-os-riscos-alucinacao-ia | Explica a técnica de **prompt negativo** sob a ótica da segurança profissional, reforçando por que dizer à IA "o que não fazer" é tão importante quanto dizer "o que fazer" |
| 4 | TCC — Bacharelado em Ciência da Computação (IFG), Daniel Vitor | Trabalho de Conclusão de Curso (PDF acadêmico) | https://repositorio.ifg.edu.br/bitstream/prefix/2550/1/TCC_Daniel_Vitor_BCC_Final.pdf | Fonte acadêmica formal sobre o tema, traz embasamento teórico e metodológico que complementa os artigos mais informais das outras fontes |
| 5 | Chain-of-Thought Prompting: O Que é e Como Usar? | Artigo técnico (blog Mario Filho, ML) | https://mariofilho.com/chain-of-thought-prompting/ | Explica com profundidade técnica a diferença entre Zero-Shot CoT e Few-Shot CoT, com exemplo prático de ganho de precisão em um caso real (Medprompt/GPT-4) |

> 💡 **Critério de seleção:** propositalmente misturei fontes de naturezas diferentes — um blog de nicho, uma empresa de marketing, uma entidade profissional (OAB), um trabalho acadêmico e um blog técnico de ML — para ver se o NotebookLM consegue cruzar essas perspectivas e apontar os princípios que se repetem em todas.

---

## 🧪 Engenharia de Prompts e "Cicatrizes"

> ⚠️ **Ação necessária:** os prompts abaixo são sugestões estratégicas de ponto de partida. Rode-os no seu NotebookLM (após subir as 5 fontes acima) e substitua as respostas de exemplo pelas respostas reais — isso é o que comprova sua curadoria de fato.

### Prompt 1 — Cruzamento entre fontes
**Pergunta feita:**
> "Todas as fontes carregadas falam de alguma forma sobre 'prompt negativo'. Compare como o artigo de geração de imagens e a notícia da OABRJ tratam esse conceito. O que é comum e o que é específico de cada contexto?"

**Resposta obtida (resumo):**
[Cole aqui o resumo real gerado pelo NotebookLM]

**Fontes citadas pela IA:** [quais documentos ela usou]

**O que funcionou / não funcionou:**
[ex: a IA conseguiu comparar bem os dois contextos, mas precisei pedir explicitamente para não misturar as citações das duas fontes]

---

### Prompt 2 — Aprofundamento técnico (CoT)
**Pergunta feita:**
> "Com base no artigo sobre Chain-of-Thought, explique a diferença entre Zero-Shot CoT e Few-Shot CoT com um exemplo prático de cada, fora do contexto médico do artigo original."

**Resposta obtida (resumo):**
[Cole aqui a resposta real]

**O que funcionou / não funcionou:**
[ex: pedir um exemplo "fora do contexto original" forçou a IA a generalizar o conceito em vez de só repetir o exemplo do texto]

---

### Prompt 3 — Aplicação prática
**Pergunta feita:**
> "Baseado nos prompts de marketing e nos prompts de geração de imagem das fontes, monte um prompt único que uma pequena empresa poderia usar para criar uma campanha de post com imagem e texto, aplicando também um prompt negativo."

**Resposta obtida (resumo):**
[Cole aqui a resposta real]

**Diferença em relação aos prompts anteriores:**
[ex: esse pedido de "síntese" obrigou o NotebookLM a combinar informações de 2 fontes diferentes em uma única resposta prática]

---

### Dificuldades encontradas (troubleshooting)
- [ex: como as fontes têm formatos muito diferentes (blog, notícia institucional, PDF acadêmico), o NotebookLM às vezes priorizava as fontes mais "textuais" e ignorava trechos do PDF — precisei citar o nome do TCC explicitamente no prompt]
- [ex: pedir "cite a fonte" foi essencial para não confundir a técnica de prompt negativo do contexto de imagem com a do contexto jurídico]
- [ex: respostas muito genéricas quando a pergunta não especificava o contexto (marketing vs. imagem vs. jurídico)]

**Lição aprendida:** Quando as fontes vêm de domínios muito diferentes, é essencial nomear explicitamente qual fonte (ou contexto) você quer que a IA use — perguntas genéricas fazem o modelo "misturar" ou generalizar demais.

---

## 📖 Miniguia de Estudo (Entrega Final)

### Resumo estruturado do assunto

**1. Prompt como estrutura, não como "frase mágica"**
Independentemente do domínio (imagem, marketing, jurídico, técnico), um bom prompt segue uma lógica parecida: contexto + objetivo específico + formato de saída esperado. O artigo de geração de imagens chama isso de "camadas de contexto" (sujeito + ambiente + luz + estilo); o artigo de marketing usa variáveis como `<persona>` e `<negócio>` para o mesmo efeito.

**2. Prompt negativo: dizer o que a IA NÃO deve fazer**
Duas fontes bem diferentes (geração de imagem e uso jurídico) convergem nesse ponto: especificar restrições explícitas — seja no campo negativo do Midjourney, seja como "não invente jurisprudência" para um assistente jurídico — reduz erros e alucinações. É uma técnica simples, mas que atua como uma camada extra de proteção contra respostas inventadas.

**3. Contexto muda a técnica, mas não o princípio**
- Para **imagem**: especificar lente, luz, enquadramento e estilo evita resultados genéricos.
- Para **marketing**: usar variáveis reutilizáveis (persona, produto, setor) permite adaptar o mesmo prompt para várias campanhas.
- Para **uso profissional/jurídico**: o foco é reduzir riscos — prompt negativo e verificação de fontes são prioridade.
- Para **raciocínio complexo (CoT)**: pedir para o modelo "pensar passo a passo" (zero-shot) ou fornecer exemplos de raciocínio (few-shot) melhora a precisão em tarefas que exigem lógica ou várias etapas.

**4. Chain-of-Thought (CoT) na prática**
CoT incentiva o modelo a expor etapas intermediárias de raciocínio antes da resposta final. Isso não só melhora a precisão (como mostrado no case do Medprompt/GPT-4 aplicado à medicina) como torna o processo mais transparente e auditável — algo especialmente valioso em contextos profissionais como o jurídico.

---

### 📘 Glossário

| Termo | Definição |
|-------|-----------|
| **Prompt** | Instrução ou pergunta enviada a um modelo de IA para obter uma resposta |
| **Prompt Negativo** | Técnica de indicar explicitamente o que a IA **não** deve fazer ou incluir na resposta (ex: "não invente jurisprudência", ou o campo `--no` no Midjourney), usada para reduzir erros e alucinações |
| **Alucinação** | Quando a IA gera informação incorreta, desatualizada ou inventada com aparência de fato verdadeiro |
| **Chain-of-Thought (CoT)** | Técnica que incentiva o modelo a "pensar passo a passo", decompondo o raciocínio em etapas intermediárias antes da resposta final |
| **Zero-Shot CoT** | Aplicação do CoT sem exemplos prévios — basta instruir o modelo a "pensar passo a passo" |
| **Few-Shot CoT** | Aplicação do CoT fornecendo exemplos de raciocínio passo a passo antes da tarefa real, ajudando o modelo a entender o formato esperado |
| **Camadas de contexto (prompt de imagem)** | Estrutura de prompt para geração de imagens que combina sujeito + ambiente + tipo de luz + estilo técnico (lente/câmera ou estilo de arte) |
| **Variável de prompt** | Espaço reservado dentro de um prompt (ex: `<persona>`, `<negócio>`) que pode ser substituído para reaproveitar o mesmo comando em diferentes contextos |
| **AEO (Answer Engine Optimization)** | Otimização de conteúdo para ser bem interpretado e citado por ferramentas de busca por IA (ChatGPT, Perplexity), citado na fonte de marketing como um desdobramento moderno do SEO |

---

### 🔁 Prompts Reutilizáveis para Revisão

Conjunto de prompts prontos para usar em revisões futuras no NotebookLM (ou outra IA):

1. `"Resuma os principais conceitos de [tema] em até 5 bullet points, citando a fonte de cada um."`
2. `"Compare como [fonte A] e [fonte B] tratam o conceito de [X], destacando o que é específico de cada contexto e o que é um princípio comum."`
3. `"Baseado nas fontes carregadas, monte um prompt negativo para uma tarefa de [contexto], listando pelo menos 4 restrições explícitas."`
4. `"Explique [conceito técnico] com um exemplo Zero-Shot e um exemplo Few-Shot, fora do contexto original do texto."`
5. `"Crie 5 perguntas de revisão estilo quiz sobre [tema], com gabarito, baseadas nas fontes carregadas."`
6. `"Combine as recomendações de [fonte 1] e [fonte 2] em um único prompt prático que eu possa usar amanhã para [tarefa real]."`

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
