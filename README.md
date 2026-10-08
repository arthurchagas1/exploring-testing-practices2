# Explorando Práticas de Teste

Neste exercício, vamos explorar práticas de teste em sistemas reais utilizando a ferramenta [TestMiner](https://andrehora.github.io/testminer).

O TestMiner permite visualizar e analisar testes de software em repositórios do GitHub, fornecendo dados sobre como os projetos organizam seus testes, como eles evoluem entre versões e quais bibliotecas de teste são utilizadas.
Explore a ferramenta antes de começar para se familiarizar com seu funcionamento.

Mais detalhes no GitHub da ferramenta: https://github.com/andrehora/testminer.

---

## Passo 1: Selecionar DOIS repositórios

Escolha dois repositórios reais que possuam testes de software.
Abaixo estão alguns links para ajudá-lo a encontrar projetos interessantes:

- Python: https://github.com/topics/python?l=python
- JavaScript: https://github.com/topics/javascript?l=javascript
- TypeScript: https://github.com/topics/typescript?l=typescript
- Java: https://github.com/topics/java?l=java

- Tópicos: [ai](https://andrehora.github.io/testminer/#topic:ai), [llm](https://andrehora.github.io/testminer/#topic:llm), [api](https://andrehora.github.io/testminer/#topic:api), [nodejs](https://andrehora.github.io/testminer/#topic:nodejs), [android](https://andrehora.github.io/testminer/#topic:android)

- Por organização: [Google](https://andrehora.github.io/testminer/#google), [Microsoft](https://andrehora.github.io/testminer/#microsoft), [Apple](https://andrehora.github.io/testminer/#apple), [Facebook](https://andrehora.github.io/testminer/#facebook), [Netflix](https://andrehora.github.io/testminer/#netflix), 
[GitHub](https://andrehora.github.io/testminer/#github), [Apache](https://andrehora.github.io/testminer/#apache), [HuggingFace](https://andrehora.github.io/testminer/#huggingface)

## Passo 2: Explorar os repositórios selecionados

Busque os repositórios escolhidos no [TestMiner](https://andrehora.github.io/testminer) e analise os dados de teste gerados pela ferramenta.

## Passo 3: Explicar as prática de teste

Para cada repositório, escolha uma prática ou dado de teste relevante e explique com suas próprias palavras.

---

## Instruções de entrega

1. Faça um `fork` deste repositório (saiba mais sobre forks [aqui](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo)).
2. Responda às questões abaixo diretamente neste arquivo `README.md` do seu fork. Pode adicionar imagens para enriquecer sua explicação.
3. No Moodle, submeta apenas a URL do seu fork.

---

## Respostas

### Repositório 1

Repositório: https://github.com/fastapi/fastapi

URL TestMiner: https://andrehora.github.io/testminer/#fastapi/fastapi

Explicação: No branch `main`, o TestMiner classifica 370 itens como testes e também identifica helpers, benchmarks, testes de CI e smoke tests. A listagem mostra áreas como `tutorial001`, `security`, `tutorial003`, `tutorial002` e `response`, o que sugere que a suíte está organizada por funcionalidades e também cobre exemplos da documentação. Outro dado interessante é a identificação de `pytest` e de plugins como `pytest-cov`, `pytest-xdist` e `pytest-timeout`: além de escrever testes, o projeto dispõe de ferramentas para medir cobertura, distribuir a execução e limitar testes demorados. Esses indicadores são úteis para entender a estrutura e as ferramentas de teste sem precisar começar lendo cada arquivo. As contagens são a classificação apresentada pelo TestMiner, não necessariamente o número de casos de teste individuais.

### Repositório 2

Repositório: https://github.com/prisma/prisma

URL TestMiner: https://andrehora.github.io/testminer/#prisma/prisma

Explicação: No branch `main`, o painel do TestMiner identifica 632 itens na categoria de testes, 884 em E2E, 580 fixtures e 1.060 helpers de teste. Para mim, o dado mais relevante é a presença expressiva de E2E junto com fixtures: isso aponta para uma estratégia que não depende só de testes unitários, mas também exercita fluxos completos e prepara dados/configurações para cenários de teste. A ferramenta ainda destaca nomes recorrentes como `index`, `get`, `type`, `migrate` e `schema`, dando pistas das áreas do produto que recebem cobertura. Como no FastAPI, esses valores são itens classificados pelo TestMiner e não devem ser lidos como contagem exata de funções de teste ou de execuções. A análise é um retrato do branch consultado e pode mudar conforme o repositório evolui.
