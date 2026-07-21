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

**Resposta obtida:**
[O conceito de prompt negativo é abordado nas fontes como uma ferramenta essencial para refinar os resultados da Inteligência Artificial, embora sua aplicação varie drasticamente entre a criação visual e a análise de textos administrativos ou jurídicos.
O que é comum entre os contextos
Em ambos os casos, o prompt negativo é tratado como a estratégia de definir o que a IA não deve fazer ou o que deve ser removido do resultado final
. O objetivo comum é o refinamento da qualidade, utilizando a exclusão para evitar que a ferramenta entregue resultados genéricos, ruidosos ou incorretos [5, Source 3]. Em suma, o segredo da precisão muitas vezes reside no comando de "limpar" o que não é desejado
.
O que é específico de cada contexto
1. Geração de Imagens (Artigo de Dicas Técnicas)
Neste contexto, o prompt negativo é focado na estética e na correção técnica visual:
Finalidade: É usado para eliminar "ruídos" visuais e deformações físicas que o algoritmo costuma gerar por padrão
.
Elementos Excluídos: O foco está em remover marcas d'água, textos indesejados na imagem, assinaturas e defeitos anatômicos, como "olhos desalinhados", "pele de cera" ou "deformações"
.
Comandos Técnicos: São citados comandos específicos de ferramentas de imagem, como o parâmetro --no no Midjourney ou campos dedicados em softwares como o Stable Diffusion
.
2. Contexto Jurídico e Administrativo (Notícia OABRJ e IFG)
No âmbito jurídico (OABRJ) e administrativo (IFG), o prompt negativo é uma estratégia de segurança e fidedignidade:
Finalidade: O foco principal é a redução de alucinações, ou seja, impedir que a IA crie informações factuais falsas ou invente dados que não constam nos documentos originais [Source 3, 95].
Critérios de Rejeição: Em processos administrativos, como os do IFG, isso se traduz em "instruções adicionais" ou "critérios de rejeição" dentro do prompt
. Por exemplo, instruir o modelo a não adicionar explicações ou a rejeitar informações se elas não estiverem explicitamente vinculadas ao período da licença
.
Validação Factual: Enquanto na imagem se busca evitar uma "pele de cera", no Direito busca-se evitar que a IA mencione leis inexistentes ou interprete de forma errônea um requerimento, garantindo que o "Auditor" (LLM de validação) descarte qualquer dado não comprovado no texto original
.
Enquanto o artigo de imagens usa o prompt negativo para garantir a perfeição visual, a notícia da OABRJ e os estudos do IFG o utilizam para garantir a verdade factual e a conformidade legal
.]

**Fontes citadas pela IA:** [quais documentos ela usou]

**O que funcionou / não funcionou:**
A IA teve sucesso.

---

### Prompt 2 — Aprofundamento técnico (CoT)
**Pergunta feita:**
> "Com base no artigo sobre Chain-of-Thought, explique a diferença entre Zero-Shot CoT e Few-Shot CoT com um exemplo prático de cada, fora do contexto médico do artigo original."

**Resposta obtida:**
[A técnica de Chain-of-Thought (CoT), ou Cadeia de Pensamento, é uma estratégia de engenharia de prompt que incentiva os modelos de IA a "pensarem em voz alta", decompondo problemas complexos em etapas lógicas intermediárias antes de apresentarem a resposta final
. A principal diferença entre as abordagens Zero-Shot e Few-Shot reside na forma como o modelo é instruído a realizar esse raciocínio.
Abaixo, explico as diferenças com exemplos práticos fora do contexto médico:
1. Zero-Shot CoT
Nesta abordagem, não são fornecidos exemplos de resolução ao modelo
. A instrução baseia-se puramente em comandos diretos que forçam a IA a explicar seu raciocínio
. É a forma mais simples de usar CoT, sendo útil quando não se tem exemplos prontos ou se deseja testar a capacidade de generalização do modelo
.
Como funciona: Adiciona-se uma frase como "pense passo a passo" ou "explique seu raciocínio" ao comando inicial
.
Exemplo Prático (Logística):
Prompt: "Um caminhão de entregas sai com 50 pacotes. Em cada uma das primeiras 3 paradas, ele deixa 5 pacotes. Na quarta parada, ele retira 10 pacotes de devolução. Quantos pacotes ele tem agora? Pense passo a passo."
Raciocínio da IA: 1. O caminhão começou com 50 pacotes. 2. Nas 3 primeiras paradas, saíram 3 x 5 = 15 pacotes. 3. Sobraram 50 - 15 = 35 pacotes. 4. Na quarta parada, entraram mais 10 pacotes. 5. Total final: 35 + 10 = 45 pacotes.
2. Few-Shot CoT
Nesta técnica, o modelo recebe alguns exemplos (shots) que mostram tanto o problema quanto a sequência de passos lógicos usados para resolvê-lo antes de receber a tarefa real
. Isso ajuda a IA a entender o formato e a profundidade de raciocínio esperados
.
Como funciona: Fornece-se um ou mais pares de "problema + raciocínio passo a passo" como referência
.
Exemplo Prático (Planejamento de Marketing):
Prompt: "Exemplo: Se uma campanha de e-mail teve 1000 envios e uma taxa de clique de 5%, quantos cliques ela gerou? Raciocínio:
Identificar o total de envios: 1000.
Converter a porcentagem em decimal: 5% = 0,05.
Multiplicar o total pelo decimal: 1000 * 0,05 = 50. Resposta: 50 cliques.
Agora faça este: Se um post patrocinado custou R$ 500 e gerou 250 cliques, qual foi o custo por clique (CPC)?"
A IA replicará a estrutura de passos para chegar ao resultado de R$ 2,00.
Por que a explicação deve vir antes da solução?
As fontes destacam que o CoT é mais eficaz quando o modelo explica o raciocínio antes de fornecer a solução final
. Como os LLMs funcionam prevendo a próxima palavra baseada nas anteriores, gerar os passos lógicos primeiro cria um "embasamento" detalhado que torna a resposta final muito mais precisa e interpretável
.

---

### Prompt 3 — Aplicação prática
**Pergunta feita:**
> "Baseado nos prompts de marketing e nos prompts de geração de imagem das fontes, monte um prompt único que uma pequena empresa poderia usar para criar uma campanha de post com imagem e texto, aplicando também um prompt negativo."

**Resposta obtida (resumo):**
Para criar uma campanha completa de post para redes sociais (texto + imagem), uma pequena empresa deve unir a fórmula de camadas de contexto da geração de imagens
 com a especificidade estratégica dos prompts de marketing
.
Abaixo, apresento um prompt estruturado único que você pode adaptar para o seu negócio, seguido pela aplicação do prompt negativo para garantir a qualidade final.
Prompt Mestre: Campanha de Post para Pequena Empresa
"Aja como um especialista em Marketing e Diretor de Fotografia.
PARTE 1 - O TEXTO (Marketing): Crie um post para Instagram de um <inserir seu negócio, ex: café artesanal> focado na persona <inserir seu público, ex: jovens profissionais urbanos>
. O objetivo é educar o público sobre <inserir tema, ex: os benefícios da torra média> usando uma técnica de storytelling envolvente
. Inclua um título chamativo que prenda a atenção e um CTA (Call to Action) persuasivo para gerar cliques
.
PARTE 2 - A IMAGEM (Visual): Descreva uma imagem ultra-realista para este post seguindo esta estrutura: Sujeito: <descrever o objeto, ex: uma xícara de café fumegante sobre uma mesa de madeira rústica> + Detalhes do Ambiente: <ex: grãos de café espalhados e luz solar entrando pela janela> + Tipo de Luz: Iluminação de 'Golden Hour' (luz solar suave e lateral, tons quentes)
 + Estilo Técnico: Fotografia tirada com lente 85mm, abertura f/1.4, foco nítido no sujeito e fundo sutilmente desfocado (bokeh cinematográfico)
.
PARTE 3 - PROMPT NEGATIVO: Aplique os seguintes critérios de rejeição para o resultado final: Na imagem: não inclua texto, marcas d'água, assinaturas, deformações, aparência de plástico ou 'pele de cera'
. No texto: não invente dados ou alucine informações que não foram fornecidas (não adicione explicações extras fora do contexto da marca) [Source 3, 117]."
Por que este prompt funciona?
Camadas de Contexto (Imagem): Em vez de pedir apenas uma "imagem bonita" (que gera resultados artificiais), o comando define elementos técnicos como a lente (85mm) e a iluminação (Golden Hour) para criar profundidade e realismo profissional
.
Foco em Personas e Intenção (Marketing): O prompt segue a recomendação da HubSpot de não ser genérico, vinculando o post a uma persona e a um objetivo de storytelling claro
.
Refinamento via Prompt Negativo:
Contexto Visual: Remove "ruídos" comuns em IAs de imagem, como textos mal formados e texturas artificiais
.
Contexto Factual: Aplica o conceito jurídico/administrativo de segurança, impedindo que a IA alucine informações falsas sobre o seu produto ou negócio [Source 3, 95].
Ao usar este comando, a IA gera tanto o planejamento do conteúdo quanto a descrição técnica visual, permitindo que a empresa mantenha a consistência da voz de marca em todos os canais
.

---

### Dificuldades encontradas (troubleshooting)
- A IA precisou gerenciar limitações intrínsecas discutidas nos textos.

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
- [x] Fontes carregadas no NotebookLM
- [x] Prompts testados e documentados (respostas reais coladas)
- [x] Miniguia final revisado com base nos testes reais
- [x] Entrega feita na plataforma DIO
