___
# Proposta de Pesquisa

## Título do Projeto

Foi escolhido o seguinte título: 
	Análise Estática Independente de Linguagem: Um Framework Genérico Orientado a Gramáticas Formais e Casamento de Padrões.
## Integrantes

Caio Xavier da Silva - 1142725371

## Metodologia Escolhida

Design Science Research

## Objetivo Geral

Criar um gerador de analisador estático agnóstico a linguagem, utilizando Modelos de Linguagem de Grande Escala (LLMs) para a geração automatizada de gramáticas formais e estruturação de Árvores de Sintaxe Abstrata (AST).

## Objetivos Específicos

- Investigar o estado da arte de ferramentas de análise estática baseadas em AST e pattern matching.
   
- Implementar o motor principal do linter, capaz de receber a gramática gerada, construir a AST do código-fonte e aplicar regras de verificação.

- Validar a eficácia da ferramenta gerando linters para pelo menos duas linguagens distintas e comparando os resultados com ferramentas de mercado.


## Hipótese de Pesquisa

A dependência de implementações manuais de gramáticas restringe a escalabilidade de ferramentas de análise estática. A hipótese desta pesquisa é que a integração de Modelos de Linguagem de Grande Escala (LLMs) para a síntese dinâmica de gramáticas viabiliza a construção de um linter verdadeiramente agnóstico, proporcionando alta flexibilidade de adaptação a novas linguagens sem apresentar uma degradação de desempenho estrutural (AST) que inviabilize seu uso prático.

## Métricas de Avaliação

Para validar a eficácia e a flexibilidade do framework proposto, a avaliação será dividida em análises quantitativas e qualitativas, baseadas na comparação do gerador com analisadores estáticos nativos das respectivas linguagens (quando existentes) e na aplicação em linguagens carentes desse suporte. O critério de "sucesso" será desmembrado nas seguintes métricas:

1. **Precisão (Precision) e Revocação (Recall) na Detecção de Padrões:** O linter gerado deverá ser capaz de identificar violações de código com uma taxa de acerto mínima de 80% em relação aos linters nativos. Para isso, serão mensurados os Verdadeiros Positivos (_VP_), Falsos Positivos (_FP_) e Falsos Negativos (_FN_). A qualidade da detecção será avaliada pela Precisão e Revocação, onde a Precisão indica a proporção de alertas corretos e a Revocação indica a capacidade de não omitir erros existentes. O balanceamento entre ambas será medido pelo F1-Score.

2. **Desempenho e Complexidade de Travessia:** Será avaliado o tempo de execução (em milissegundos) necessário para que o motor de busca percorra os nós da Árvore de Sintaxe Abstrata (AST) e aplique as regras. O objetivo é garantir que o overhead introduzido pela natureza agnóstica do gerador mantenha a ferramenta viável para uso em pipelines de Integração Contínua (CI).
   
3. **Taxa de Geração Gramatical Bem-Sucedida:** Como o framework depende de Modelos de Linguagem (LLMs) para a síntese da gramática formal, será calculada a taxa de vezes em que a IA consegue gerar uma definição sintática capaz de realizar o parsing de um código-fonte válido sem falhas estruturais, buscando um limiar de estabilidade operacional de no mínimo 80%.