Você é um/a linguista de corpus especializado/a em Análise Multidimensional, anotação linguística e português brasileiro.

Você receberá três documentos:

1. O tagset 1 atual, que deve ser revisado.
2. O tagset 2 anterior, usado como referência comparativa.
3. Um relatório comparativo entre o tagset 1 e o tagset 2, contendo recomendações de revisão.

Sua tarefa é produzir uma versão revisada do tagset 1, em Markdown, incorporando seletivamente as recomendações do relatório.

## Objetivo

Revise o tagset 1 preservando sua arquitetura ampla e contemporânea, especialmente suas categorias relativas a:

- português brasileiro atual;
- variação linguística;
- usos não padrão;
- oralidade;
- conversação;
- escrita digital;
- redes sociais;
- gírias, emojis, hashtags e alternância de código.

Ao mesmo tempo, incorpore ao tagset 1 as categorias analíticas essenciais do tagset 2, principalmente aquelas relevantes para Análise Multidimensional, stance/posicionamento, complementação e controle oracional.

Não copie mecanicamente todas as categorias do tagset 2. Faça uma revisão seletiva, coerente e operacional.

## Princípios obrigatórios

1. Preserve, sempre que possível, as categorias já existentes no tagset 1.
2. Não remova categorias relacionadas a português brasileiro contemporâneo, oralidade, conversação, escrita digital ou variação linguística.
3. Não inclua medidas quantitativas no tagset.
4. Use exemplos em português brasileiro para orientar a anotação por LLM.
5. Inclua exemplos suficientes para orientar a anotação por LLM, preferencialmente de 3 a 6 exemplos por categoria nova.
6. Evite listas excessivamente longas; use “etc.” quando a lista for apenas exemplificativa.
7. Evite redundâncias desnecessárias.
8. Mantenha categorias agregadas apenas quando forem úteis para anotação ou análise posterior.
9. Preserve IDs numéricos explícitos para todas as categorias.
10. Ao criar categorias novas, formule-as no mesmo estilo das categorias existentes: número da tag + nome da categoria + dois-pontos + exemplos breves em português brasileiro.
11. Os exemplos das categorias novas devem ser comparáveis, em extensão e formato, aos exemplos já presentes no tagset 1.
12. Para categorias estruturais ou oracionais, inclua exemplos de construções completas, não apenas palavras isoladas.
13. Quando gerar exemplos de formas não padrão relevantes para o português brasileiro, marque cada exemplo com `(forma não padrão)`.

## Medidas quantitativas

Não inclua categorias como:

- quantidade de palavras;
- extensão média da palavra;
- extensão média da oração;
- razão forma-ocorrência;
- TTR;
- métricas estatísticas ou computacionais semelhantes.

Essas medidas devem ser tratadas como métricas de pós-processamento, não como etiquetas aplicadas diretamente ao texto.

Ao final, inclua uma breve nota dizendo que medidas quantitativas foram deixadas fora do tagset e devem ser calculadas separadamente.

## Estilo dos exemplos

Para categorias novas, forneça exemplos no mesmo padrão do tagset 1.

Use preferencialmente este formato:

142. nome da categoria: exemplo 1, exemplo 2, exemplo 3, construção exemplificativa, etc.

Para categorias estruturais ou oracionais, inclua exemplos de construções completas, não apenas palavras isoladas.

Exemplos de formato esperado:

- orações completivas com `que` controladas por verbo dicendi/comunicação: disse que viria, afirmou que estava certo, explicou que não poderia ir, contou que tinha visto, etc.
- infinitivo controlado por verbo de desejo/volição: quero sair, prefiro ficar, desejo participar, espero conseguir, etc.
- passiva analítica com agente: foi aprovado pelo comitê, foi escrito pela autora, foi analisado pelos pesquisadores, etc.
- advérbios não factuais/evidenciais: supostamente, alegadamente, aparentemente, presumivelmente, etc.

Quando houver exemplos não padrão relevantes, inclua-os e marque-os com `(forma não padrão)`.

## Exemplos de formas não padrão, variáveis ou informais

Quando criar, revisar ou expandir exemplos, inclua exemplos de formas não padrão, variáveis ou informais sempre que forem linguisticamente relevantes para a categoria.

Sempre que um exemplo representar uma forma não padrão segundo a norma gramatical tradicional, mas relevante para análise linguística do português brasileiro, marque-o explicitamente com `(forma não padrão)`.

Use exatamente esta marcação, entre parênteses:

`(forma não padrão)`

Exemplos:

- orações relativas: a pessoa que eu falei ontem (forma não padrão), um problema onde a gente precisa conversar mais (forma não padrão)
- pronomes de objeto direto: vi eles (forma não padrão), encontrei ela (forma não padrão), mandei eles embora (forma não padrão)
- regência/preposição variável ou não padrão: fui na casa deles (forma não padrão), cheguei em São Paulo (forma não padrão), assisti o filme (forma não padrão)
- próclise em início de frase: me disseram que ele veio (forma não padrão), se fala muito disso (forma não padrão)
- relativas resumptivas: o rapaz que eu falei com ele (forma não padrão), uma figura que eles não têm controle sobre ela (forma não padrão)

Não corrija nem elimine essas formas. Elas devem ser preservadas como exemplos analiticamente relevantes de variação, oralidade, informalidade ou português brasileiro contemporâneo.

Use `(forma não padrão)` apenas quando a forma for realmente não padrão em relação à norma tradicional. Não marque como não padrão exemplos que sejam simplesmente informais, digitais, coloquiais ou recentes, a menos que também violem claramente uma expectativa normativa tradicional.

Por exemplo:

- `vc`, `pq`, `tbm`, `kkk`, `cringe`, `slay`, `#fyp`, emojis e hashtags devem ser tratados como formas digitais, informais ou contemporâneas, mas não necessariamente como `(forma não padrão)`.
- `vi eles`, `fui na casa deles`, `a pessoa que eu falei ontem` e `me disseram que ele veio` devem ser marcados como `(forma não padrão)` quando usados como exemplos.

## Revisões prioritárias

### 1. Orações de stance/posicionamento

Crie ou expanda uma seção específica para orações de stance, complementação e controle oracional.

Inclua categorias para:

- orações completivas com `que` controladas por verbo dicendi/comunicação;
- orações completivas com `que` controladas por verbo cognitivo/mental;
- orações completivas com `que` controladas por verbo de desejo/volição;
- orações completivas com `que` controladas por verbo de probabilidade;
- orações completivas com `que` controladas por adjetivo avaliativo;
- orações completivas com `que` controladas por adjetivo de certeza;
- orações completivas com `que` controladas por adjetivo de probabilidade;
- orações completivas com `que` controladas por substantivo factual;
- orações completivas com `que` controladas por substantivo não factual;
- orações completivas com `que` controladas por substantivo de atitude;
- orações completivas com `que` no indicativo;
- orações completivas com `que` no subjuntivo.

Inclua exemplos em português brasileiro para cada categoria, seguindo o estilo do tagset 1.

### 2. Orações de infinitivo

Refine as orações de infinitivo por tipo de controlador.

Inclua categorias para:

- infinitivo controlado por verbo de desejo/volição;
- infinitivo controlado por verbo cognitivo/mental;
- infinitivo controlado por verbo causativo;
- infinitivo controlado por verbo modal ou semimodal;
- infinitivo controlado por adjetivo avaliativo;
- infinitivo controlado por adjetivo de facilidade/dificuldade;
- infinitivo controlado por substantivo;
- infinitivo introduzido por preposição.

Use exemplos como:

- quero sair;
- prefiro ficar;
- decidi sair;
- penso em fazer;
- fez calar;
- mandou sair;
- pode fazer;
- precisa estudar;
- é importante estudar;
- é fácil entender;
- a decisão de sair;
- a vontade de mudar;
- para fazer;
- ao sair;
- sem dizer.

### 3. Advérbios de stance, grau e negação

Refine a seção de advérbios para distinguir:

- `não` como advérbio de negação separado;
- advérbios negativos exceto `não`, como nunca, jamais, tampouco;
- advérbios de probabilidade, como talvez, provavelmente, possivelmente;
- advérbios factivos, como certamente, sem dúvida, de fato;
- advérbios não factuais/evidenciais, como supostamente, alegadamente, aparentemente;
- advérbios atitudinais, como infelizmente, felizmente, curiosamente;
- amplificadores/intensificadores, como muito, totalmente, completamente;
- downtoners/suavizadores, como quase, um pouco, parcialmente;
- hedges/atenuadores, como meio que, tipo, mais ou menos, talvez;
- enfatizadores, como realmente, mesmo, justamente, de fato;
- advérbios comparativos;
- locuções adverbiais ou advérbios compostos, se relevantes.

### 4. Verbos relevantes para Análise Multidimensional

Mantenha as categorias verbais já existentes, mas acrescente ou explicite:

- verbos de ação/atividade;
- verbos de ocorrência;
- verbos de facilitação;
- verbos privados, relacionados a cognição, percepção, crença ou sentimento;
- verbos públicos, relacionados a atos comunicativos públicos;
- verbos persuasivos/suasivos;
- verbos de desejo/volição;
- verbos de probabilidade;
- verbos modais e semimodais, distinguindo quando possível:
    - possibilidade;
    - obrigação;
    - necessidade;
    - capacidade;
    - evidencialidade/aparência.

### 5. Formas verbais, modo, aspecto e voz

Inclua ou explicite categorias para:

- verbo no infinitivo;
- infinitivo pessoal;
- verbo no gerúndio;
- particípio passado;
- modo indicativo como categoria agregada, se útil;
- passiva analítica com agente;
- passiva analítica sem agente;
- passiva sintética/pronominal.

Mantenha as distinções já existentes de tempo, modo e aspecto quando forem adequadas.

### 6. Adjetivos

Refine a seção de adjetivos para incluir ou explicitar:

- adjetivos atributivos pré-nominais;
- adjetivos atributivos pós-nominais;
- adjetivos predicativos;
- adjetivos avaliativos;
- adjetivos relacionais;
- adjetivos de tamanho;
- adjetivos de tempo/idade;
- adjetivos de cor;
- adjetivos de nacionalidade/origem;
- adjetivos superlativos;
- adjetivos tópicos/temáticos, se a distinção for útil.

### 7. Substantivos

Mantenha as categorias existentes e acrescente ou explicite, quando adequado:

- substantivos de lugar;
- substantivos institucionais;
- substantivos em posição de sujeito;
- nominalizações em posição de sujeito.

### 8. Conjunções e subordinação

Mantenha as categorias existentes e acrescente ou explicite:

- conjunções coordenativas conclusivas;
- coordenação frasal;
- coordenação oracional;
- conjunções subordinativas conformativas;
- conjunções subordinativas proporcionais.

### 9. Fenômenos específicos do português brasileiro

Preserve e, se necessário, refine categorias relacionadas a:

- pro-drop/omissão de sujeito;
- pronome reto em posição de objeto, como “vi eles”;
- objeto indireto preposicionado, como “para mim”, “para ele”, “para a gente”;
- regência/preposição variável ou não padrão, como “fui na casa deles”;
- próclise;
- ênclise;
- mesóclise;
- próclise em início de frase;
- alternância entre clítico e pronome pleno;
- tópico-comentário/deslocamento à esquerda;
- relativas resumptivas;
- relativas não padrão;
- ordem não canônica de constituintes.

Quando essas categorias incluírem exemplos não padrão segundo a norma tradicional, marque os exemplos relevantes com `(forma não padrão)`.

### 10. Português digital, oralidade e conversação

Preserve categorias relativas a:

- formas reduzidas e abreviações;
- grafias expressivas ou alongadas;
- gírias;
- expressões avaliativas recentes;
- empréstimos e termos de redes sociais;
- hashtags;
- emojis;
- emoticons;
- sufixos e formações produtivas digitais;
- alternância de código;
- marcadores de oralidade em escrita digital;
- interjeições;
- vocativos;
- muletilhas;
- hesitações;
- repetições;
- reformulações;
- risos;
- sobreposições/interrupções;
- perguntas de confirmação.

Não elimine essas categorias, pois elas são pontos fortes do tagset 1 e são relevantes para corpora orais, conversacionais e digitais.

## Numeração e Markdown

Produza o tagset revisado em Markdown.

Use títulos e subtítulos claros.

Preserve IDs numéricos explícitos para todas as tags.

Mantenha, sempre que possível, a numeração do tagset 1 para categorias que permanecerem iguais ou muito semelhantes.

Quando inserir novas categorias, atribua novos IDs de forma coerente, sem reutilizar IDs já existentes para categorias diferentes.

Para categorias derivadas/agregadas, continue usando IDs altos, como 900+, se isso já estiver adotado no tagset 1.

### Atenção especial a tags hierárquicos

Quando uma tag tiver numeração hierárquica, como `7.1.`, `7.2.`, `56.1.`, `56.2.`, etc., mantenha cada tag em linha própria e separe essas linhas das demais com uma linha em branco antes e depois.

Use este formato:

7.1. determinantes numerais cardinais: um, dois, três, quatro, cinco, etc.

7.2. determinantes numerais ordinais: primeiro, segundo, terceiro, quarto, quinto, etc.

7.3. determinantes numerais multiplicativos: dobro, duplo, triplo, quádruplo, etc.

Não crie uma linha vazia com um número principal sem conteúdo. Por exemplo, não crie uma tag “7.” vazia se as categorias reais forem apenas “7.1.”, “7.2.”, “7.3.” e “7.4.”.

## Controle de qualidade da revisão

Antes de finalizar, verifique se o tagset revisado:

1. preserva as categorias fortes do tagset 1;
2. incorpora seletivamente as categorias analíticas essenciais do tagset 2;
3. não inclui medidas quantitativas;
4. inclui exemplos claros em português brasileiro;
5. marca exemplos não padrão relevantes com `(forma não padrão)`;
6. não marca como não padrão exemplos que sejam apenas digitais, recentes ou informais;
7. mantém a numeração explícita;
8. não cria IDs duplicados;
9. não cria tags vazias;
10. mantém linhas individualizadas para tags hierárquicos;
11. evita redundâncias excessivas;
12. é utilizável como tagset para anotação por LLM.

## Saída esperada

Forneça como resposta:

1. Uma breve nota explicando os princípios adotados na revisão.
2. O tagset 1 revisado completo em Markdown.
3. Uma breve lista das principais mudanças feitas em relação ao tagset 1 original.
4. Uma breve nota indicando que medidas quantitativas foram deixadas fora do tagset e devem ser calculadas em pós-processamento.

Não produza análise extensa antes do tagset. O foco principal deve ser entregar o tagset revisado.