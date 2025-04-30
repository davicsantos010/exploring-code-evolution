# Explorando evolução de código

Neste exercício, iremos explorar a evolução de código em sistemas reais.

Iremos utilizar a ferramenta [GitEvo](https://github.com/andrehora/gitevo).
Essa ferramenta analisa a evolução de código em repositórios Git nas seguintes linguagens: Python, JavaScript, TypeScript e Java.

Você deve submeter via Moodle apenas o link do seu `fork`, conforme descrito abaixo.

# Passo 1: Selecionar repositório a ser analisado

Selecione um repositório relevante na linguagem de sua preferência (Python, JavaScript, TypeScript ou Java).
Você pode encontrar projetos interessantes nos links abaixo:

- Python: https://github.com/topics/python?l=python
- JavaScript: https://github.com/topics/javascript?l=javascript
- TypeScript: https://github.com/topics/typescript?l=typescript
- Java: https://github.com/topics/java?l=java

# Passo 2: Instalar e rodar a ferramenta GitEvo

Instale a ferramenta [GitEvo](https://github.com/andrehora/gitevo) com o comando:

```
pip install gitevo
```

Rode a ferramenta no repositório selecionado através do seguinte comando (dependendo da linguagem do projeto que escolheu):

```shell
# Python
$ gitevo -r python <git_url>

# JavaScript
$ gitevo -r js <git_url>

# TypeScript
$ gitevo -r ts <git_url>

# Java
$ gitevo -r java <git_url>
```

Onde `<git_url>` é URL do repositório a ser analisado.
Por exemplo, para analisar o projeto Flask escrito em Python:

```
$ gitevo -r python https://github.com/pallets/flask
```

# Passo 3: Explorar os gráficos de evolução de código (`index.html`)

Ao rodar a ferramenta [GitEvo](https://github.com/andrehora/gitevo), o arquivo `index.html` é gerado com diversos gráficos de evolução de código.

Abra o arquivo `index.html` e observe com atenção os gráficos gerados.

# Passo 4: Explicar um gráfico de evolução de código

Selecione um dos gráficos de evolução e explique-o com suas palavras.
Por exemplo, você pode:

- Detalhar a evolução ao longo do tempo, 
- Detalhar se as curvas estão de acordo com boas práticas,
- Explicar grandes alterações nas curvas,
- Explorar a documentação do repositório em busca de explicações para grandes alterações
- Etc.

Seja criativo!

# Exercício

Para responder este exercício, primeiramente, você deve fazer um `fork` deste repositório.
No Moodle, você deve submeter apenas a URL do seu `fork`.

Em seguida, adicione o arquivo gerado `index.html` no seu fork.

Por fim, responda as questões abaixo no seu `fork`: 

1. Repositório selecionado: https://github.com/OpenInterpreter/open-interpreter

2. Gráfico selecionado: Data structures
  
3. Explicação: O gráfico mostra a evolução do uso de diferentes estruturas de dados (dictionary, list, tuple, set) entre os anos de 2023 e 2025 no repositório OpenInterpreter.
 - Datalhamento da evolução ao longo do tempo:
     - Dictionaries (azul): O crescimento mais expressivo. Partiu de praticamente 0 em 2023 e ultrapassou 450 ocorrências em 2025. Isso indica que a estrutura de mapeamento chave-valor está se tornando central no projeto. Pode estar associada a um maior uso de arquivos de configuração, armazenamento de estados, ou manipulação de JSON, o que é comum em sistemas que interpretam comandos ou interagem com APIs externas.
     - Lists (rosa): Crescimento consistente, embora mais moderado. O número de listas passa de 0 em 2023 para cerca de 300 em 2025. Isso reflete um uso crescente de coleções ordenadas, talvez para armazenamento de sequências de instruções, tokens ou históricos de execução.
     - Tuples (laranja): Embora menos frequente, tem um crescimento contínuo. Isso pode indicar um esforço para representar dados imutáveis de maneira mais explícita, algo que pode ser comum em projetos que valorizam segurança e previsibilidade em execuções.
     - Sets (amarelo): Estável e praticamente inalterado. Isso pode indicar que conjuntos não são uma necessidade frequente no domínio de aplicação do Open Interpreter, ou que seu uso foi substituído por outras abordagens mais controladas, como listas com verificação manual de duplicidade.

  - Considerações sobre boas práticas:
    -  O aumento expressivo no uso de dicionários pode indicar uma crescente necessidade de armazenar e acessar dados de forma eficiente através de chaves. Dicionários são poderosos para organizar informações não sequenciais e realizar buscas rápidas, o que pode ser uma boa prática em muitas situações.
    -  O crescimento constante no uso de listas sugere a necessidade contínua de sequências ordenadas de itens que podem ser modificados. Listas são estruturas de dados fundamentais e seu uso crescente é esperado em projetos de software.
    -  O crescimento mais lento das tuplas pode indicar que elas estão sendo utilizadas para armazenar coleções de itens que não devem ser alterados após a criação. Tuplas oferecem imutabilidade, o que pode ser uma boa prática para garantir a integridade de certos dados.
    -  A estabilidade no uso de conjuntos pode sugerir que eles são utilizados em cenários específicos onde a unicidade dos elementos e operações de conjunto (união, interseção, diferença) são importantes, mas não são uma necessidade predominante no código.

  - Grandes alterações nas curvas: A alteração mais notável é o forte crescimento da curva dos dicionários entre 2024 e 2025. Isso sugere que houve uma mudança significativa na arquitetura ou nas funcionalidades do "open-interpreter" que demandou um uso muito maior de dicionários. 
