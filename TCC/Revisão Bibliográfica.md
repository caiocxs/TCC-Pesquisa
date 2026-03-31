___

# 2.1 Inteligência Artificial

A Inteligência Artificial (IA) possui diversas versões segundo pesquisadores, sendo dividido sua definição como a fidelidade de uma performance humana, ou uma definição formal de raciocinalidade. A partir de ambas dimensões, temos quatro possíveis combinações, sendo respectivamente: Agir de forma humana, Pensamento de forma
humana, Pensamento racional e Agir racionalmente.

Agir de forma humana, proposto por Alan Turing (1950), tendo o objetivo inicial de descobrir se era possível um computador gerar respostas indiferenciáveis de um humano. Sendo necessário possuir processamento de nossa linguagem, memória do conhecimento, raciocínio e aprendizado se adaptar e identificar padrões.

Pensamento de forma humana, sendo um modelo cognitivo, tal que a partir de uma teoria de como é um raciocínio humano, aplica à um programa computacional. Fazendo parte da área da Ciência Cognitiva, que junta Inteligência Artificial com técnicas experimentais da psicologia para construir teorias precisas e praticáveis sobre a mente humana.

Pensamento racional, utiliza a filosofia de leis de pensamento, onde a lógica exige um conhecimento absoluto sobre o mundo, uma condição que, na realidade, raramente é alcançada. Isso nos permite a construção de um modelo capaz de pensamentos racionais, que a partir de informações cruas para um entendimento de como funciona o mundo.

Agir racionalmente, é definido como um agente racional, agente sendo aquele que realiza uma tarefa, como um programa de computador, porém ao ser racional, permite que ele opere autonomamente, entender seu ambiente e se adaptar à diferentes circunstâncias para realizar objetivos. Um agente racional é aquele que atua para realizar o objetivo da melhor forma, ou quando existe incerteza, a melhor forma possível.

*\[Artificial Intelligence: A Modern Approach, Global Edition, 4ed - Artificial Intelligence_ A Modern Approach]*

## 2.1.1 Linguagem Natural

Um sistema formal amplamente utilizado para modelar a estrutura constituinte em linguagens naturais é a Gramática Livre de Contexto (GLC). Também conhecidas como gramáticas de estrutura de frase, as GLCs baseiam-se em um formalismo que é estritamente equivalente à Forma de Backus-Naur (BNF), um padrão universal para a especificação da sintaxe em computação.

Uma Gramática Livre de Contexto consiste em um conjunto de regras ou produções, tal que cada um expressa a forma em que os símbolos da linguagem podem ser ordenados e agrupados, e um léxico de palavras e símbolos. Uma GLC como essa, define o que chamamos de linguagem formal. Em uma linguagem formal, existe uma divisão estrita: as sentenças (cadeias de palavras) que podem ser derivadas pelas regras da gramática, enquanto as que não podem ser derivadas são agramaticais.

Contudo, essa linha rígida entre o que "pertence" ou "não pertence" à linguagem caracteriza apenas gramáticas formais, servindo como um modelo muito simplificado de como as linguagens naturais realmente funcionam. Ao contrário das linguagens de programação, determinar se uma dada sentença é válida ou faz sentido em uma linguagem natural depende inerentemente do contexto. Na linguística computacional, o uso dessas linguagens formais para tentar modelar a complexidade das linguagens naturais é chamada de gramática generativa, desde que a linguagem passa a ser definida pelo conjunto de possíveis sentenças "geradas" pela sua gramática.

*\[Speech and Language Processing: An Introduction to Natural Language Processing, Computational Linguistics and Speech Recognition]*


\[4](Count-Min Sketch e Variantes para Contagem de Frequências e Ranking PMI em Processamento de Linguagem Natural de Larga Escala em Português)
\[5](Kajal: Extracting Grammar of a Source Code Using Large Language Models)
## 2.1.2 Modelos de Linguagens de Larga Escala (LLM)

Os Modelos de Linguagens de Larga Escala (LLMs), em sua maioria, baseiam-se na arquitetura *Transformer*, originalmente projetada para tarefas sequenciais, como tradução automática. A arquitetura consiste em dois principais componentes: o Codificador (*Encoder*), qual converte uma entrada de *tokens* para uma sequência de vetores representativos (frequentemente chamada de estado oculto ou contexto), e Decodificador (*Decoder*), que utiliza o contexto gerado pelo codificador para gerar iterativamente uma sequência de tokens de saída, um token por vez.

Com o passar dos anos, esses blocos funcionais foram adaptados para atuar como modelos independentes. Embora existam centenas de variações de Transformers, a maioria se encaixa em um desses três tipos:

Apenas Codificador (*Encoder-only*): Esses modelos convertem uma sequência de texto de entrada em uma representação numérica, sendo muito eficiente para tarefas como classificação de texto ou reconhecimento de entidades nomeadas. A representação computada para cada token nessa arquitetura depende tanto do contexto à esquerda (antes do token) quanto á direita (depois do token), esse mecanismo geralmente denominado como atenção bidirecional.

Apenas Decodificador (*Decoder-only*): Dada uma entrada de texto (por exemplo "No almoço, eu comi um..."), esses modelos autocompletam a sequência prevendo iterativamente a palavra subsequente mais provável. A família de modelos GPT pertence a essa classe. Nesse caso, a representação computada para um token recebido depende exclusivamente do contexto à sua esquerda, esse comportamento é conhecido como atenção causal ou autorregressiva.

Codificador-Decodificador (*Encoder-decoder*): Utilizados para modelar mapeamentos complexos de uma sequência de texto para outra, esses modelos são proje para tradução automática e tarefas de sumarização. 

*\[Natural Language Processing with Transformers: Building Language Applications with Hugging Face]*

## 2.1.3 Aprendizado de regras baseado em LLMs

Modelos de Linguagens de Larga Escala (LLMs) as vezes requerem adaptações, como projetos com APIs não documentadas ou ferramentas especializadas, essa adaptação, na maioria dos casos, temos opções para estas adaptações como ajustar pesos do modelo (fine-tuning) ou utilizar recuperação de exemplos (few-shot prompting), sendo abordagens eficazes, porém não possuem suporte para abstrações, reutilização e interpretabilidade de caso a caso. No lugar dessas opções, essa abordagem utiliza LLM para induzir e refinar regras lógicas, tais que podem assumir formatos de linguagem natural, lógica de primeira ordem (FOL) ou sintaxes específicas, as metodologias a partir dessa abordagem são:

Geração de Regras a partir de Experiência e Falhas, 

*\[RIMRULE: Improving Tool-Using Language Agents via MDL-Guided Rule Learning]*
*\[RLIE: Rule Generation with Logistic Regression, Iterative Refinement, and Evaluation for Large Language Models]*

# 2.2 Análise Estática


\[1](KNighter: Transforming Static Analysis with LLM-Synthesized Checkers)
\[3](Concurrency Bug Detection via Static Analysis and Large Language Models)
\[6](Fact-Aligned and Template-Constrained Static Analyzer Rule Enhancement with LLMs)
\[10](Beyond Deductive Datalog: How Datalog is used to perform AI tasks for program analysis)
\[11](Vulnerability Patch Verification for Military Software Systems Through AI-Driven Code-Level Rule Generation)
## 2.2.1 Síntese de Regras


\[9](Rewrite Rule Inference Using Equality Saturation)
\[12](RulER: Automated Rule-Based Semantic Error Localization and Repair for Code Translation)
\[13](RLIE: Rule Generation with Logistic Regression, Iterative Refinement, and Evaluation for Large Language Models)

## 2.2.2 Reparo de Programa Automatizado

\[12](RulER: Automated Rule-Based Semantic Error Localization and Repair for Code Translation)

