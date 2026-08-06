# Relatório comparativo entre `tagset_ptbr` e o Anexo 8.1 de Berber Sardinha, Kauffmann & Acunzo 2012

## 1. Objetivo

Este relatório compara dois tagsets para português brasileiro:

- **Tagset 1**: `tagset_ptbr`, o tagset atualmente em teste e revisão.
- **Tagset 2**: `Berber_Sardinha_Kauffmann_Acunzo_2012_Annex_8_1.md`, tagset anterior usado em análise multidimensional do português brasileiro.

A comparação procura responder:

1. **O que do tagset 2 já está contemplado no tagset 1?**
2. **O que está ausente ou pouco especificado no tagset 1 em relação ao tagset 2?**
3. **O que existe no tagset 1 que não aparece no tagset 2?**
4. **O tagset 1 cobre os casos relevantes?**
5. **Que revisões são recomendáveis?**

---

# 2. Visão geral da comparação

O **tagset 1** é mais amplo em termos de:

- português brasileiro contemporâneo;
- variação;
- oralidade;
- escrita digital;
- marcadores conversacionais;
- construções não padrão;
- colocação pronominal;
- clíticos;
- recursos discursivos.

O **tagset 2**, por outro lado, é mais detalhado em categorias típicas da **Análise Multidimensional**, especialmente:

- subclasses semânticas e funcionais de adjetivos, advérbios, substantivos e verbos;
- distinções finas entre tipos de oração subordinada com **que**;
- orações reduzidas de infinitivo controladas por diferentes classes lexicais;
- marcadores de posicionamento/stance;
- categorias de verbos modais, privados, públicos, persuasivos etc.;
- distinções entre passiva com agente, sem agente e pronominal;
- categorias quantitativas como extensão média da oração, extensão média da palavra, contagem de palavras e razão forma-ocorrência.

Em termos gerais:

> **O tagset 1 cobre boa parte das categorias gerais do tagset 2, mas frequentemente em nível mais amplo. O tagset 2 contém muitas distinções analíticas finas que ainda não estão explicitadas no tagset 1.**

---

# 3. Categorias do tagset 2 já contempladas no tagset 1

A tabela abaixo mostra os principais grupos do tagset 2 e sua correspondência no tagset 1.

## 3.1 Correspondências gerais

| Grupo no tagset 2                         |                                                                 Exemplos de tags do tagset 2 |                                                         Correspondência no tagset 1 | Grau de cobertura                                              | Comentário                                                                                                               |
|-------------------------------------------|---------------------------------------------------------------------------------------------:|------------------------------------------------------------------------------------:|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Artigos definidos                         |                                                                                   `<artdef>` |                                                                1. artigos definidos | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Artigos indefinidos                       |                                                                                 `<artindef>` |                                                              2. artigos indefinidos | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Contrações                                |                                                                                  `<contrac>` |                 3. contrações de preposição + artigo; 84. contrações preposicionais | **Completa/parcial**                                           | O tagset 1 cobre bem contrações preposicionais, mas poderia explicitar outras contrações, se relevantes.                 |
| Preposições                               |                                                                                   `<prpall>` | 82. todas as preposições simples; 83. locuções prepositivas; 906. todas_preposicoes | **Completa**                                                   | O tagset 1 é até mais explícito quanto a locuções e variação.                                                            |
| Pronomes demonstrativos                   |                                                                                   `<prndem>` |                        4. determinantes demonstrativos; 16. pronomes demonstrativos | **Completa**                                                   | O tagset 1 distingue determinantes e pronomes.                                                                           |
| Pronomes possessivos                      |                                                                                  `<prnposs>` |                              5. determinantes possessivos; 15. pronomes possessivos | **Completa**                                                   | Boa cobertura.                                                                                                           |
| Pronomes relativos                        |                                                  `<prnrelprep>`, `<prnqualcujo>`, `<prnque>` |                                       18. pronomes relativos; 97. orações relativas | **Parcial/boa**                                                | O tagset 1 cobre relativos, mas não separa todos os subtipos do tagset 2.                                                |
| Quantificadores                           |                                                                                   `<prnqtf>` |                              6. determinantes indefinidos; 17. pronomes indefinidos | **Parcial**                                                    | Quantificadores aparecem, mas não como categoria própria.                                                                |
| Substantivos abstratos                    |                                                                                    `<nabst>` |                                                          23. substantivos abstratos | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Substantivos concretos                    |                                                                                    `<nconc>` |                                                          24. substantivos concretos | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Substantivos animados                     |                                                                                    `<nanim>` |                                                           25. substantivos animados | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Substantivos de quantidade                |                                                                                    `<nqtty>` |                                                      27. substantivos de quantidade | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Substantivos cognitivos                   |                                                                                    `<ncogn>` |                                                         28. substantivos cognitivos | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Substantivos próprios                     |                                                                                    `<nprop>` |                                                           21. substantivos próprios | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Substantivos técnicos                     |                                                                                    `<ntech>` |                                                           30. substantivos técnicos | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Nominalizações                            |                                                                 `<nominlz>`, `<nominlzsubj>` |                                                                  31. nominalizações | **Parcial**                                                    | O tagset 1 cobre nominalizações, mas não distingue nominalização em posição de sujeito.                                  |
| Todos os substantivos                     |                                                                                     `<nall>` |                                                             902. todos_substantivos | **Parcial**                                                    | O tagset 2 define “todos, exceto nominalizações”; o tagset 1 agrega substantivos incluindo nominalizações em outro item. |
| Adjetivos atributivos                     |                                                         `<adjattr>`, `<adjpost>`, `<adjpre>` |                                            32. adjetivos qualificativos atributivos | **Parcial**                                                    | O tagset 1 não diferencia pré- e pós-modificação.                                                                        |
| Adjetivos predicativos                    |                                                                                  `<adjpred>` |                                           33. adjetivos qualificativos predicativos | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Adjetivos avaliativos                     |                                                                                  `<adjeval>` |                                                           35. adjetivos avaliativos | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Adjetivos relacionais                     |                                                                                  `<adjrela>` |                                                           34. adjetivos relacionais | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Adjetivos de tamanho                      |                                                                                  `<adjsize>` |                                                            36. adjetivos de tamanho | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Adjetivos temporais                       |                                                                                  `<adjtime>` |                                                      37. adjetivos de idade e tempo | **Completa**                                                   | Categoria contemplada.                                                                                                   |
| Adjetivos de cor                          |                                                                                  `<adjcolr>` |                                                                38. adjetivos de cor | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Adjetivos pátrios/de origem               |                                                                                  `<adjaffi>` |                                             39. adjetivos de nacionalidade e origem | **Completa**                                                   | Boa correspondência.                                                                                                     |
| Todos os adjetivos                        |                                                                                   `<adjall>` |                                                                903. todos_adjetivos | **Completa/parcial**                                           | Agregado contemplado.                                                                                                    |
| Advérbios de tempo                        |                                                                                  `<advtime>` |                                                              70. advérbios de tempo | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Advérbios de lugar                        |                                                                                    `<advpl>` |                                                              71. advérbios de lugar | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Advérbios de modo                         |                                                                                `<advmanner>` |                                                               72. advérbios de modo | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Advérbios de intensidade                  |                                                                                  `<advints>` |                                             73. advérbios de quantidade/intensidade | **Completa/parcial**                                           | Contemplado, mas pode haver sobreposição com amplificadores.                                                             |
| Amplificadores                            |                                                                                  `<advampl>` |                                       78. advérbios intensificadores/amplificadores | **Completa**                                                   | Boa correspondência.                                                                                                     |
| Atenuadores/hedges                        |                                                                                  `<advhedg>` |                                                   81. advérbios de mitigação/hedges | **Completa**                                                   | Boa correspondência.                                                                                                     |
| Atitudinais                               |                                                                                   `<advatt>` |                                                           79. advérbios atitudinais | **Completa**                                                   | Boa correspondência.                                                                                                     |
| Probabilidade                             |                                                                                  `<advlikl>` |                                               76. advérbios de dúvida/probabilidade | **Completa/parcial**                                           | Contemplado.                                                                                                             |
| Factivos                                  |                                                                                  `<advfact>` |                                                  80. advérbios epistêmicos/factivos | **Completa/parcial**                                           | Contemplado, embora o rótulo combine epistêmicos e factivos.                                                             |
| Negação                                   |                                                                       `<advneg>`, `<advnao>` |                                                            75. advérbios de negação | **Parcial**                                                    | O tagset 1 não separa `não` dos demais advérbios negativos.                                                              |
| Todos os advérbios                        |                                                                                   `<advall>` |                                                                905. todos_adverbios | **Completa/parcial**                                           | Agregado contemplado.                                                                                                    |
| Conjunções coordenativas aditivas         |                                                                                    `<cjadd>` |                                               86. conjunções coordenativas aditivas | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Conjunções coordenativas adversativas     |                                                                                    `<cjadv>` |                                           88. conjunções coordenativas adversativas | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Conjunção coordenativa alternativa `ou`   |                                                                                     `<cjou>` |                                           87. conjunções coordenativas alternativas | **Completa/parcial**                                           | O tagset 1 inclui `ou`, mas não isola `ou` como tag própria.                                                             |
| Coordenadas conclusivas                   |                                                                                   `<cjcncl>` |                         118. marcadores de consequência; parcialmente em conjunções | **Parcial**                                                    | O tagset 1 trata mais como marcador/conector; falta categoria coordenativa conclusiva.                                   |
| Coordenadas frasais/oracionais            |                                                                 `<cjcoorphr>`, `<cjcoorcls>` |                                                        86–88; 907. todas_conjuncoes | **Parcial**                                                    | O tagset 1 não distingue coordenação frasal vs. oracional.                                                               |
| Subordinativas causais                    |                                                                                   `<cjcaus>` |                                               89. conjunções subordinativas causais | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Subordinativas condicionais               |                                                                                   `<cjcond>` |                                          90. conjunções subordinativas condicionais | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Subordinativas concessivas                |                                                                                  `<cjcncsv>` |                                           91. conjunções subordinativas concessivas | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Subordinativas temporais                  |                                                                                   `<cjtemp>` |                                             92. conjunções subordinativas temporais | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Subordinativas finais                     |                                                                                  `<cjfinal>` |                                                94. conjunções subordinativas finais | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Subordinativas comparativas/proporcionais |                                                                                   `<cjprop>` |                                          95. conjunções subordinativas comparativas | **Parcial**                                                    | Proporcionais não estão explicitadas como categoria separada.                                                            |
| Subordinativas conformativas              |                                                                                   `<cjcnfm>` |                                                                                   — | **Ausente**                                                    | Falta categoria explícita.                                                                                               |
| Modais                                    | `<mdconseguir>`, `<mddever>`, `<mdhaver>`, `<mdpoder>`, `<mdprecisar>`, `<mdter>`, `<mdall>` |                                                      50. verbos modais e semimodais | **Parcial**                                                    | O tagset 1 agrupa todos; o tagset 2 separa verbo por verbo.                                                              |
| Modais de obrigação                       |                                                                                  `<mdoblig>` |                                                      50. verbos modais e semimodais | **Parcial**                                                    | Obrigação não está isolada.                                                                                              |
| Verbos auxiliares                         |                                                                                    `<vbaux>` |                                                               41. verbos auxiliares | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Verbos de comunicação                     |                                                                                   `<vbcomm>` |                                                           43. verbos de comunicação | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Verbos mentais/cognitivos                 |                                                                                   `<vbment>` |                                                       44. verbos cognitivos/mentais | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Verbos causativos                         |                                         `<vbcaus...>` em categorias oracionais; tipo lexical |                                                               47. verbos causativos | **Parcial/boa**                                                | O tipo verbal está contemplado; faltam muitas construções controladas por verbo causativo.                               |
| Verbos existenciais                       |                                                                                  `<vbexist>` |                                                             48. verbos existenciais | **Completa**                                                   | Categoria contemplada.                                                                                                   |
| Verbos aspectuais                         |                                                                                  `<vbaspct>` |                                             49. verbos aspectuais; 65–66 perífrases | **Completa/parcial**                                           | Boa cobertura, mas sem todas as subdivisões do tagset 2.                                                                 |
| Verbos de ocorrência                      |                                                                                    `<vbocc>` |                                    48. verbos existenciais inclui ocorrer/acontecer | **Parcial**                                                    | O tagset 1 não separa ocorrência de existência.                                                                          |
| Verbos de ação                            |                                                                                    `<vbact>` |                                                                 40. verbos lexicais | **Parcial**                                                    | Não há classe específica “verbos de ação”.                                                                               |
| Presente do indicativo                    |                                                                                   `<vbpres>` |                                                          51. presente do indicativo | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Pretérito do indicativo                   |                                                                                   `<vbpast>` |                            52. pretérito perfeito simples; 53. pretérito imperfeito | **Parcial/mais detalhado no tagset 1 para tempos específicos** | O tagset 1 distingue perfeito e imperfeito.                                                                              |
| Pretérito imperfeito                      |                                                                                   `<vbimpf>` |                                                            53. pretérito imperfeito | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Mais-que-perfeito                         |                                                                                  `<vbplupf>` |                                  54. pretérito mais-que-perfeito simples e composto | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Futuro do presente                        |                                                                                `<vbfutpres>` |                                                              55. futuro do presente | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Futuro perifrástico                       |                                                                                  `<vbfutir>` |                                                             56. futuro perifrástico | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Futuro do pretérito                       |                                                                                `<vbfutpret>` |                                                 57. futuro do pretérito/condicional | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Presente do subjuntivo                    |                                                                                `<vbsubpres>` |                                                          60. presente do subjuntivo | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Pretérito do subjuntivo                   |                                                                                `<vbsubpast>` |                                              61. pretérito imperfeito do subjuntivo | **Completa/parcial**                                           | Contempla sobretudo o imperfeito do subjuntivo.                                                                          |
| Futuro do subjuntivo                      |                                                                                 `<vbsubfut>` |                                                            62. futuro do subjuntivo | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Imperativo                                |                                                                                    `<vbimp>` |                                  58. imperativo afirmativo; 59. imperativo negativo | **Completa/mais detalhada no tagset 1**                        | O tagset 1 distingue afirmativo e negativo.                                                                              |
| Infinitivo                                |                                                                                    `<vbinf>` |                                   100. orações de infinitivo; formas verbais em 904 | **Parcial**                                                    | Falta tag específica para verbo no infinitivo como forma verbal.                                                         |
| Infinitivo pessoal                        |                                                                                 `<vinfpers>` |                                                                                   — | **Ausente**                                                    | Importante para PB/português.                                                                                            |
| Gerúndio                                  |                                                                                 `<vbgerall>` |                               101. orações de gerúndio; 64. perífrases progressivas | **Parcial**                                                    | Falta tag específica para verbo no gerúndio fora de oração/perífrase.                                                    |
| Particípio passado                        |                                                                                `<vbpastprt>` |                                   102. orações de particípio; 67. passiva analítica | **Parcial**                                                    | Falta tag específica para particípio como forma verbal.                                                                  |
| Aspecto perfeito                          |                                                                                `<vbpfaspct>` |                                                       63. aspecto perfeito composto | **Completa/parcial**                                           | Boa cobertura.                                                                                                           |
| Forma progressiva                         |                                                     `<vbprog>`, `<vbprogphr>`, `<vbproginf>` |                               64. perífrases progressivas; 101. orações de gerúndio | **Parcial**                                                    | O tagset 2 tem distinções mais finas.                                                                                    |
| Voz passiva com agente                    |                                                                                `<clpasspor>` |                                                           67. voz passiva analítica | **Parcial**                                                    | O tagset 1 não distingue passiva com agente.                                                                             |
| Voz passiva sem agente                    |                                                                               `<clpassless>` |                                                           67. voz passiva analítica | **Parcial**                                                    | O tagset 1 não distingue passiva sem agente.                                                                             |
| Voz passiva pronominal                    |                                                                                 `<clsepass>` |                                                68. voz passiva sintética/pronominal | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Omissão de sujeito                        |                                                                                 `<subjdrop>` |                                                     104. elipse de sujeito/pro-drop | **Completa**                                                   | Categoria diretamente contemplada.                                                                                       |
| Marcadores discursivos                    |                                                                                 `<discmrkr>` |                                                                        116–122; 910 | **Completa/mais detalhada no tagset 1**                        | O tagset 1 é mais rico aqui.                                                                                             |
| Marcador de foco                          |                                                                                 `<focusmkr>` |                                                         77. advérbios focalizadores | **Completa/parcial**                                           | Contemplado como advérbios focalizadores.                                                                                |
| Interrogativas com advérbio interrogativo |                                                                                     `<qsqu>` |                   99. orações interrogativas indiretas; 19. pronomes interrogativos | **Parcial**                                                    | Falta distinção clara entre interrogativa direta/indireta e com/sem advérbio.                                            |
| Questões tag                              |                                                                                   `<qsttag>` |                                                       131. perguntas de confirmação | **Completa/parcial**                                           | Boa correspondência funcional.                                                                                           |
| Interrogativas sem advérbio interrogativo |                                                                                     `<qsyn>` |       131. perguntas de confirmação; estruturas interrogativas gerais não separadas | **Parcial**                                                    | Falta categoria para interrogativa polar/sim-não.                                                                        |
| Oração reduzida de particípio             |                                                                                `<clpostnom>` |                                                          102. orações de particípio | **Parcial**                                                    | O tagset 2 especifica modificador pós-nominal; o tagset 1 é mais geral.                                                  |

---

# 4. O que falta no tagset 1 em relação ao tagset 2

A principal lacuna do tagset 1 não está nas categorias gramaticais básicas, mas nas **distinções finas de função discursiva, controle oracional e stance** presentes no tagset 2.

## 4.1 Categorias claramente ausentes ou pouco especificadas

| Área               | Categoria do tagset 2                                                                                                                         | Situação no tagset 1       | Recomendação                                                                                                                       |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| Contagens textuais | `<clauselgth>` extensão média de oração; `<wl>` extensão média de palavra; `<wrcount>` quantidade de palavras; `<ttr>` razão forma-ocorrência | **Ausentes**               | Decidir se o tagset 1 deve incluir traços quantitativos ou se estes serão calculados fora da anotação.                             |
| Adjetivos          | `<adjpre>` adjetivo pré-modificador; `<adjpost>` adjetivo pós-modificador                                                                     | **Não separados**          | Acrescentar distinção entre adjetivo atributivo pré-nominal e pós-nominal.                                                         |
| Adjetivos          | `<adjsup>` superlativos                                                                                                                       | **Ausente**                | Incluir “adjetivos superlativos”.                                                                                                  |
| Adjetivos          | `<adjtopi>` topical                                                                                                                           | **Ausente/parcial**        | Verificar se “relacional” cobre; possivelmente criar “adjetivos tópicos/temáticos”.                                                |
| Adjetivos          | `<adjexceval>` todos exceto avaliativos                                                                                                       | **Ausente como agregado**  | Só necessário se for útil para análise quantitativa.                                                                               |
| Advérbios          | `<advnao>` `não` separado                                                                                                                     | **Ausente**                | Incluir tag específica para `não`, pois é muito frequente e analiticamente relevante.                                              |
| Advérbios          | `<advneg>` negação exceto `não`                                                                                                               | **Ausente como distinção** | Separar “não” dos demais negativos: nunca, jamais, tampouco etc.                                                                   |
| Advérbios          | `<advcomp>` comparativos                                                                                                                      | **Ausente**                | Incluir advérbios comparativos, se relevante.                                                                                      |
| Advérbios          | `<advcmpd>` compostos                                                                                                                         | **Ausente**                | Incluir advérbios compostos/locuções adverbiais.                                                                                   |
| Advérbios          | `<advlong>` advérbios longos                                                                                                                  | **Ausente**                | Provavelmente só necessário para replicar a AMD original.                                                                          |
| Advérbios          | `<advnonf>` não factuais                                                                                                                      | **Ausente/parcial**        | Distinguir de factivos e probabilísticos.                                                                                          |
| Advérbios          | `<advemph>` enfatizadores                                                                                                                     | **Parcial**                | O tagset 1 tem intensificadores e focalizadores, mas poderia incluir “enfatizadores”.                                              |
| Advérbios          | `<advdown>` suavizadores/downtoners                                                                                                           | **Parcial**                | O tagset 1 tem hedges, mas “downtoner” pode ser separado.                                                                          |
| Coordenação        | `<cjcoorphr>` coordenada frasal; `<cjcoorcls>` coordenada oracional                                                                           | **Ausentes**               | Incluir distinção entre coordenação de sintagmas e coordenação de orações.                                                         |
| Coordenação        | `<cjcncl>` conclusivas                                                                                                                        | **Parcial**                | Criar categoria específica para coordenativas conclusivas: portanto, logo, pois etc.                                               |
| Subordinação       | `<cjcnfm>` conformativa                                                                                                                       | **Ausente**                | Incluir conjunções conformativas: conforme, segundo, como, consoante.                                                              |
| Subordinação       | `<cjprop>` proporcional                                                                                                                       | **Parcial/ausente**        | Incluir proporcionais: à medida que, quanto mais... mais etc.                                                                      |
| Modais             | modais separados: conseguir, dever, haver que/de, parecer, poder, precisar, ter que/de                                                        | **Agrupados**              | Criar subcategorias por modal ou pelo menos por valor semântico: possibilidade, obrigação, necessidade, evidencialidade/aparência. |
| Modais             | `<mdoblig>` verbos de obrigação                                                                                                               | **Parcial**                | Incluir categoria explícita de obrigação/necessidade.                                                                              |
| Verbos             | `<vbact>` ação                                                                                                                                | **Ausente específica**     | Criar “verbos de ação/atividade”.                                                                                                  |
| Verbos             | `<vbfacil>` facilitação                                                                                                                       | **Ausente**                | Incluir se a distinção for analiticamente importante.                                                                              |
| Verbos             | `<vbocc>` ocorrência                                                                                                                          | **Parcial**                | Separar ocorrência de existência.                                                                                                  |
| Verbos             | `<vbpriv>` privados; `<vbpubl>` públicos; `<vbsua>` persuasivos                                                                               | **Ausentes**               | Importantes para stance/AMD; recomenda-se incluir.                                                                                 |
| Verbos             | `<vb1>`, `<vb2>`, `<vb3>` pessoa verbal                                                                                                       | **Ausentes**               | Incluir pessoa verbal se a anotação puder detectar flexão.                                                                         |
| Verbos             | `<vbindic>` modo indicativo                                                                                                                   | **Parcial**                | O tagset 1 separa tempos, mas não tem agregado “modo indicativo”.                                                                  |
| Verbos             | `<vball>` todos                                                                                                                               | **Contemplado em 904**     | Já existe agregado.                                                                                                                |
| Formas verbais     | `<vbinf>`, `<vinfpers>`, `<vbgerall>`, `<vbpastprt>`                                                                                          | **Parcial**                | Criar tags específicas para infinitivo, infinitivo pessoal, gerúndio e particípio.                                                 |
| Passiva            | `<clpasspor>` com agente; `<clpassless>` sem agente                                                                                           | **Parcial**                | Dividir a voz passiva analítica entre com agente e sem agente.                                                                     |
| Auxiliar clivado   | `<advsplit>` auxiliares com clivagem/split auxiliary                                                                                          | **Ausente**                | Incluir se houver interesse em construções como auxiliar separado por advérbio.                                                    |
| Substantivos       | `<nplac>` lugar; `<ngrpi>` institucionais                                                                                                     | **Ausentes/parciais**      | O tagset 1 tem coletivos, mas não “institucionais” nem “de lugar”.                                                                 |
| Substantivos       | `<clnsbjc>` substantivo em posição de sujeito                                                                                                 | **Ausente**                | Incluir se a posição sintática for relevante.                                                                                      |
| Substantivos       | `<nominlzsubj>` nominalização em posição de sujeito                                                                                           | **Ausente**                | Recomendável para compatibilidade com o tagset 2.                                                                                  |
| Interrogativas     | `<qsqu>`, `<qsyn>`                                                                                                                            | **Parcial**                | Incluir interrogativas diretas com/sem elemento interrogativo.                                                                     |
| Orações de stance  | grande bloco de subordinadas com `que` e infinitivo controladas por verbo, substantivo, adjetivo, advérbio, preposição                        | **Principal lacuna**       | Acrescentar seção específica de “orações de posicionamento/stance”.                                                                |

---

# 5. Grande lacuna: orações de stance e complementação

O ponto mais importante para revisão do tagset 1 é a ausência de uma seção detalhada equivalente às categorias do tagset 2 para **orações controladas por adjetivos, substantivos, verbos, advérbios e preposições**.

O tagset 1 já possui:

98. orações completivas com `que`;

100. orações de infinitivo;

97. orações relativas;

99. interrogativas indiretas.

Mas o tagset 2 distingue muito mais:

## 5.1 Subordinadas com `que`

| Tipo no tagset 2                                        | Exemplos de tags               | Situação no tagset 1                 | Recomendação                                                          |
|---------------------------------------------------------|--------------------------------|--------------------------------------|-----------------------------------------------------------------------|
| Com `que` controlada por adjetivo                       | `<clqueeadj>`, `<adjque>`      | Apenas “orações completivas com que” | Criar subcategoria.                                                   |
| Com `que` controlada por adjetivo atitudinal            | `<adjattique>`                 | Ausente                              | Incluir: “é lamentável que”, “é surpreendente que”.                   |
| Com `que` controlada por adjetivo avaliativo            | `<clqueadjeval>`               | Ausente                              | Incluir: “é bom que”, “é importante que”.                             |
| Com `que` controlada por adjetivo de certeza            | `<clqueadjcert>`               | Ausente                              | Incluir: “é certo que”, “é claro que”.                                |
| Com `que` controlada por adjetivo de probabilidade      | `<adjliklque>`                 | Ausente                              | Incluir: “é provável que”, “é possível que”.                          |
| Com `que` controlada por adjetivo factivo               | `<adjfactque>`                 | Ausente                              | Incluir: “é evidente que”, “é verdade que”.                           |
| Com `que` controlada por advérbio                       | `<clqueeadv>`                  | Ausente                              | Incluir: “certamente que”, “possivelmente que”, se aplicável.         |
| Com `que` controlada por preposição                     | `<clqueeprp>`                  | Ausente                              | Incluir se houver casos produtivos.                                   |
| Com `que` controlada por substantivo                    | `<nounque>`                    | Parcialmente implícito               | Incluir: “a ideia de que”, “o fato de que”, “a possibilidade de que”. |
| Com `que` controlada por substantivo factual            | `<nfactlque>`                  | Ausente                              | Incluir.                                                              |
| Com `que` controlada por substantivo não factual        | `<nnonfcque>`                  | Ausente                              | Incluir.                                                              |
| Com `que` controlada por substantivo de atitude         | `<nattitque>`                  | Ausente                              | Incluir.                                                              |
| Com `que` controlada por substantivo de probabilidade   | `<nliklhque>`                  | Ausente                              | Incluir.                                                              |
| Com `que` controlada por verbo                          | `<clqueevb>`                   | Parcialmente em 98                   | Subdividir por tipo de verbo.                                         |
| Com `que` controlada por verbo de probabilidade         | `<vbprobque>`                  | Ausente                              | Incluir: “parece que”, “tende a que” etc.                             |
| Com `que` controlada por verbo dicendi                  | `<vbspchque>`                  | Parcial                              | 43 cobre verbo dicendi, mas não a construção com `que`.               |
| Com `que` controlada por verbo no indicativo/subjuntivo | `<vbqueindic>`, `<vbquesubjc>` | Ausente                              | Muito relevante para PB.                                              |

## 5.2 Orações reduzidas de infinitivo

| Tipo no tagset 2                       | Exemplos de tags             | Situação no tagset 1         | Recomendação                                                                     |
|----------------------------------------|------------------------------|------------------------------|----------------------------------------------------------------------------------|
| Infinitivo controlado por adjetivo     | `<clinfadj>`                 | Parcial em 100               | Subdividir.                                                                      |
| Por adjetivo atitudinal                | `<adjattiinf>`               | Ausente                      | Incluir: “feliz por fazer”, “surpreso ao ver”.                                   |
| Por adjetivo de afeição                | `<clinfadjaff>`              | Ausente                      | Incluir se útil.                                                                 |
| Por adjetivo avaliativo                | `<clinfadjeval>`             | Ausente                      | “importante fazer”, “bom saber”.                                                 |
| Por adjetivo de certeza                | `<clinfadjcert>`             | Ausente                      | “certo de vencer”.                                                               |
| Por adjetivo de facilidade/dificuldade | `<clinfadjease>`             | Ausente                      | “fácil de entender”, “difícil de aceitar”.                                       |
| Por adjetivo de probabilidade          | `<adjliklinf>`               | Ausente                      | “provável de ocorrer” etc.                                                       |
| Por adjetivo de volição                | `<clinfadjwill>`             | Ausente                      | “disposto a fazer”.                                                              |
| Por adjetivo factivo                   | `<adjfactinf>`               | Ausente                      | Incluir, se mantida a taxonomia.                                                 |
| Por preposição                         | `<clinfprp>`                 | Parcial em 100               | Incluir: “para fazer”, “ao sair”, “sem dizer”.                                   |
| Por substantivo atitudinal             | `<nattitinf>`                | Ausente                      | Incluir.                                                                         |
| Por substantivo de probabilidade       | `<nliklhinf>`                | Ausente                      | Incluir.                                                                         |
| Por substantivo dicendi                | `<vbspchinf>`                | Ausente                      | Incluir ou revisar rótulo, pois a descrição mistura substantivo e verbo dicendi. |
| Por substantivo factual/não factual    | `<nfactlinf>`, `<nnonfcinf>` | Ausente                      | Incluir.                                                                         |
| Por verbo causativo                    | `<vbcausque>`                | Parcial em verbos causativos | Incluir construção.                                                              |
| Por verbo de cognição                  | `<vbcogninf>`                | Parcial em verbos cognitivos | Incluir construção.                                                              |
| Por verbo de desejo                    | `<vbdesrinf>`                | Ausente                      | Incluir: “querer fazer”, “preferir sair”.                                        |
| Por verbo de probabilidade             | `<vbprobinf>`                | Ausente                      | Incluir: “parecer ser”, “tender a ocorrer”.                                      |

---

# 6. O que existe no tagset 1 que não aparece no tagset 2

O tagset 1 inclui várias categorias relevantes para português brasileiro contemporâneo e para corpora digitais que não aparecem, ou aparecem apenas de modo muito indireto, no tagset 2.

## 6.1 Categorias novas ou mais desenvolvidas no tagset 1

| Área                                                                             |                                                               Categorias do tagset 1 | Presença no tagset 2            | Comentário                                                                                                     |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------:|---------------------------------|----------------------------------------------------------------------------------------------------------------|
| Determinantes                                                                    | 4–8: demonstrativos, possessivos, indefinidos, numerais, interrogativos/exclamativos | Parcial                         | O tagset 2 trata muitos desses itens como pronomes ou não os separa com tanto detalhe.                         |
| Numerais                                                                         |               7.1–7.4: cardinais, ordinais, multiplicativos, partitivos/fracionários | Ausente como seção própria      | Relevante para anotação gramatical ampla.                                                                      |
| Pronomes retos e oblíquos                                                        |                                                                                 9–14 | Parcial                         | O tagset 2 distingue pessoa e posição de sujeito/objeto, mas o tagset 1 é mais pedagógico e explícito.         |
| Pronome reto como objeto                                                         |                                    12. pronomes de objeto direto incluindo “vi eles” | Ausente explícito               | Muito relevante para PB.                                                                                       |
| Objeto indireto preposicionado                                                   |                                                           13. “para mim”, “para ele” | Parcial/ausente                 | Boa inclusão para PB.                                                                                          |
| Formas pronominais neutras                                                       |                                                                                   20 | Parcial                         | O tagset 2 não destaca essa categoria.                                                                         |
| Substantivos comuns                                                              |                                                                                   22 | Parcial                         | O tagset 2 tem `nall`, mas não categoria simples equivalente.                                                  |
| Substantivos coletivos                                                           |                                                                                   26 | Parcial                         | O tagset 2 tem institucionais, não coletivos em geral.                                                         |
| Substantivos de processo                                                         |                                                                                   29 | Ausente no tagset 2             | Presente em tradição de tagsets de AMD em inglês, mas não no Anexo 8.1 do PB.                                  |
| Verbos copulativos                                                               |                                                                                   42 | Parcial                         | O tagset 2 tem `ser/estar`, mas não a categoria ampla com parecer, ficar, permanecer, continuar.               |
| Verbos de percepção                                                              |                                                                                   45 | Ausente específica              | Pode ser relevante para stance/cognição.                                                                       |
| Verbos de movimento                                                              |                                                                                   46 | Ausente específica              | Categoria nova.                                                                                                |
| Imperativo afirmativo/negativo                                                   |                                                                                58–59 | Mais detalhado que tagset 2     | O tagset 2 só tem imperativo geral.                                                                            |
| Perífrases incoativas                                                            |                                                                                   65 | Parcial                         | Relaciona-se a aspectuais, mas está mais explícito no tagset 1.                                                |
| Perífrases terminativas                                                          |                                                                                   66 | Parcial                         | Idem.                                                                                                          |
| Construções impessoais                                                           |                                                                                   69 | Parcial                         | Tagset 2 tem omissão de sujeito e passivas, mas não “impessoais” como grupo.                                   |
| Advérbios de afirmação                                                           |                                                                                   74 | Ausente específica              | Útil para anotação ampla.                                                                                      |
| Advérbios focalizadores                                                          |                                                                                   77 | Parcial                         | Relacionado a marcador de foco.                                                                                |
| Locuções prepositivas                                                            |                                                                                   83 | Ausente como categoria própria  | Boa inclusão.                                                                                                  |
| Regência/preposição variável ou não padrão                                       |                                                                                   85 | Ausente                         | Muito relevante para PB.                                                                                       |
| Consecutivas                                                                     |                                                                                   93 | Ausente explícita no tagset 2   | Boa inclusão.                                                                                                  |
| Comparativas                                                                     |                                                                                   95 | Parcial                         | O tagset 2 tem advérbios comparativos e proporcionais, mas não uma categoria ampla de conjunções comparativas. |
| Integrantes                                                                      |                                                                                   96 | Parcial                         | Relaciona-se às completivas com `que`, mas o tagset 1 explicita.                                               |
| Orações interrogativas indiretas                                                 |                                                                                   99 | Parcial                         | O tagset 2 tem interrogativas, mas com outro recorte.                                                          |
| Orações sem verbo/elípticas                                                      |                                                                                  103 | Parcial/ausente                 | Boa categoria para oralidade e escrita informal.                                                               |
| Elipse de outros constituintes                                                   |                                                                                  105 | Ausente                         | Relevante para conversação.                                                                                    |
| Construções com `se`                                                             |                                                                                  106 | Parcial                         | Tagset 2 separa passiva pronominal, mas tagset 1 inclui vários usos.                                           |
| Tópico-comentário/deslocamento à esquerda                                        |                                                                                  107 | Ausente                         | Muito importante para PB oral.                                                                                 |
| Relativas resumptivas                                                            |                                                                                  108 | Ausente                         | Muito relevante para PB não padrão e oralidade.                                                                |
| Ordem não canônica                                                               |                                                                                  109 | Ausente                         | Boa categoria sintático-discursiva.                                                                            |
| Colocação pronominal                                                             |                                                                              110–115 | Ausente                         | Excelente inclusão para PB.                                                                                    |
| Marcadores discursivos por função                                                |                                                                              116–122 | Mais detalhado que tagset 2     | Tagset 2 tem apenas marcador discursivo geral e marcador de foco.                                              |
| Interjeições, vocativos, muletilhas, hesitações, repetições, risos, interrupções |                                                                              123–131 | Ausentes ou pouco desenvolvidos | Muito relevantes para corpus oral/conversacional/digital.                                                      |
| Português digital                                                                |                                                                              132–141 | Ausente                         | Área completamente nova e pertinente.                                                                          |
| Emojis, hashtags, grafias expressivas                                            |                                                                              137–139 | Ausente                         | Essencial para redes sociais.                                                                                  |
| Alternância de código                                                            |                                                                                  140 | Ausente                         | Relevante em corpora digitais e acadêmicos.                                                                    |
| Marcadores de oralidade em escrita digital                                       |                                                                                  141 | Ausente                         | Boa categoria para PB digital.                                                                                 |

---

# 7. Tabela-síntese por área

| Área                   | Cobertura do tagset 1 em relação ao tagset 2 | Principais lacunas                                                                                               | Comentário para revisão                                                           |
|------------------------|----------------------------------------------|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| Artigos e preposições  | Alta                                         | Poucas                                                                                                           | O tagset 1 cobre bem.                                                             |
| Pronomes               | Média/alta                                   | Pessoa em posição de sujeito; relativo com preposição; objeto raro; quantificadores separados                    | O tagset 1 é bom para PB, mas pode incorporar distinções do tagset 2.             |
| Substantivos           | Média/alta                                   | Lugar, institucionais, posição de sujeito, nominalização em sujeito                                              | Recomenda-se acrescentar subcategorias se o objetivo for compatibilidade com AMD. |
| Adjetivos              | Média                                        | Pré/pós-nominal, superlativo, topical, exceto avaliativo                                                         | Adjetivos precisam de refinamento.                                                |
| Advérbios              | Média                                        | `não` separado, negativos exceto `não`, comparativos, compostos, longos, não factuais, enfatizadores, downtoners | Advérbios precisam de refinamento analítico.                                      |
| Conjunções             | Média                                        | Coordenadas conclusivas, frasais/oracionais, conformativas, proporcionais                                        | Boa base, mas faltam distinções do tagset 2.                                      |
| Verbos                 | Média                                        | Verbos de ação, ocorrência, facilitação, privados, públicos, persuasivos, pessoa verbal                          | Boa base lexical, mas menos alinhada à AMD.                                       |
| Tempos/modos/aspecto   | Alta/média                                   | Infinitivo pessoal, infinitivo, gerúndio e particípio como formas; indicativo agregado                           | O tagset 1 é detalhado em tempos, mas faltam algumas formas.                      |
| Voz passiva            | Média                                        | Passiva com agente vs. sem agente                                                                                | Separação recomendável.                                                           |
| Orações                | Baixa/média                                  | Grande bloco de stance clauses e controle oracional                                                              | Esta é a maior lacuna.                                                            |
| Marcadores discursivos | Alta                                         | Poucas em relação ao tagset 2                                                                                    | O tagset 1 é mais completo.                                                       |
| Oralidade/conversação  | Muito alta                                   | Não se aplica                                                                                                    | Grande avanço do tagset 1.                                                        |
| Português digital      | Muito alta                                   | Não se aplica                                                                                                    | Grande avanço do tagset 1.                                                        |
| Medidas quantitativas  | Baixa                                        | Contagem de palavras, TTR, extensão média etc.                                                                   | Decidir se entram no tagset ou em pós-processamento.                              |

---

# 8. Recomendações para revisar o tagset 1

## 8.1 Recomendações prioritárias

Eu recomendaria priorizar as seguintes revisões.

### 1. Criar uma seção de **orações de posicionamento / stance clauses**

Essa é a principal diferença substantiva entre os tagsets.

Sugestão de nova seção:

| Nova categoria sugerida                                                 | Inspiração no tagset 2       |
|-------------------------------------------------------------------------|------------------------------|
| orações completivas com `que` controladas por verbo dicendi             | `<vbspchque>`                |
| orações completivas com `que` controladas por verbo cognitivo/mental    | `<vbcognque>` / `<clqueevb>` |
| orações completivas com `que` controladas por verbo de desejo/volição   | `<vbdesrque>`                |
| orações completivas com `que` controladas por verbo de probabilidade    | `<vbprobque>`                |
| orações completivas com `que` controladas por adjetivo avaliativo       | `<clqueadjeval>`             |
| orações completivas com `que` controladas por adjetivo de certeza       | `<clqueadjcert>`             |
| orações completivas com `que` controladas por adjetivo de probabilidade | `<adjliklque>`               |
| orações completivas com `que` controladas por substantivo factual       | `<nfactlque>`                |
| orações completivas com `que` controladas por substantivo não factual   | `<nnonfcque>`                |
| orações completivas com `que` controladas por substantivo de atitude    | `<nattitque>`                |
| orações completivas com `que` no indicativo                             | `<vbqueindic>`               |
| orações completivas com `que` no subjuntivo                             | `<vbquesubjc>`               |

### 2. Refinar as **orações de infinitivo**

O tagset 1 tem “orações de infinitivo”, mas o tagset 2 distingue o controlador.

Sugestões:

| Nova categoria sugerida                                      | Exemplo                                   |
|--------------------------------------------------------------|-------------------------------------------|
| infinitivo controlado por verbo de desejo                    | “quero sair”, “prefiro ficar”             |
| infinitivo controlado por verbo cognitivo                    | “penso em fazer”, “decidi sair”           |
| infinitivo controlado por verbo causativo                    | “fez sair”, “mandou calar”                |
| infinitivo controlado por verbo modal/semimodal              | “pode fazer”, “precisa estudar”           |
| infinitivo controlado por adjetivo avaliativo                | “é importante estudar”                    |
| infinitivo controlado por adjetivo de facilidade/dificuldade | “é fácil entender”, “difícil aceitar”     |
| infinitivo controlado por substantivo                        | “a decisão de sair”, “a vontade de mudar” |
| infinitivo introduzido por preposição                        | “para fazer”, “ao sair”, “sem dizer”      |

### 3. Separar melhor advérbios de stance e grau

O tagset 1 já tem uma boa base, mas poderia distinguir:

| Categoria recomendada            | Motivo                                                                    |
|----------------------------------|---------------------------------------------------------------------------|
| `não`                            | Muito frequente e analiticamente importante.                              |
| advérbios negativos exceto `não` | Para separar “não” de “nunca”, “jamais”, “tampouco”.                      |
| amplificadores                   | Já existe, mas pode ser mantido claramente separado de intensidade geral. |
| downtoners/suavizadores          | Diferenciar de hedges.                                                    |
| hedges                           | “talvez”, “meio que”, “tipo”, “mais ou menos”.                            |
| enfatizadores                    | “realmente”, “mesmo”, “de fato”, “justamente”.                            |
| factivos                         | “certamente”, “sem dúvida”, “de fato”.                                    |
| não factuais/evidenciais         | “supostamente”, “alegadamente”, “aparentemente”.                          |
| probabilidade                    | “provavelmente”, “possivelmente”, “talvez”.                               |

### 4. Refinar verbos segundo categorias da AMD

O tagset 1 já inclui verbos de comunicação, cognitivos, causativos, existenciais e aspectuais. Faltam algumas distinções importantes:

| Categoria recomendada       | Correspondência no tagset 2       |
|-----------------------------|-----------------------------------|
| verbos de ação/atividade    | `<vbact>`                         |
| verbos de ocorrência        | `<vbocc>`                         |
| verbos de facilitação       | `<vbfacil>`                       |
| verbos privados             | `<vbpriv>`                        |
| verbos públicos             | `<vbpubl>`                        |
| verbos persuasivos/suasivos | `<vbsua>`                         |
| verbos de desejo/volição    | aparece nas categorias oracionais |
| verbos de probabilidade     | aparece nas categorias oracionais |

### 5. Separar passivas

O tagset 1 deveria distinguir:

| Categoria atual                      | Subdivisões recomendadas                                   |
|--------------------------------------|------------------------------------------------------------|
| 67. voz passiva analítica            | passiva analítica com agente; passiva analítica sem agente |
| 68. voz passiva sintética/pronominal | manter como está                                           |

Isso permitiria equivalência com:

- `<clpasspor>`: passiva com agente;
- `<clpassless>`: passiva sem agente;
- `<clsepass>`: passiva pronominal.

### 6. Incluir formas verbais específicas

Embora o tagset 1 tenha tempos e estruturas, seria útil acrescentar:

| Categoria recomendada | Motivo                              |
|-----------------------|-------------------------------------|
| verbo no infinitivo   | Equivalente a `<vbinf>`.            |
| infinitivo pessoal    | Importante no português.            |
| verbo no gerúndio     | Equivalente a `<vbgerall>`.         |
| particípio passado    | Equivalente a `<vbpastprt>`.        |
| modo indicativo       | Agregado equivalente a `<vbindic>`. |

### 7. Refinar adjetivos

Adicionar:

| Categoria recomendada           | Correspondência no tagset 2                 |
|---------------------------------|---------------------------------------------|
| adjetivo atributivo pré-nominal | `<adjpre>`                                  |
| adjetivo atributivo pós-nominal | `<adjpost>`                                 |
| adjetivos superlativos          | `<adjsup>`                                  |
| adjetivos tópicos/temáticos     | `<adjtopi>`                                 |
| adjetivos exceto avaliativos    | `<adjexceval>`, se necessário como agregado |

---

# 9. O tagset 1 cobre os casos relevantes?

## 9.1 Sim, cobre muitos casos relevantes

O tagset 1 é especialmente forte para:

- categorias gramaticais básicas;
- português brasileiro contemporâneo;
- fenômenos de variação;
- usos não padrão;
- colocação pronominal;
- oralidade;
- conversação;
- escrita digital;
- redes sociais;
- emojis, hashtags, gírias e abreviações;
- marcadores discursivos.

Nesse sentido, ele é **mais adequado que o tagset 2** para corpora atuais, especialmente se os dados incluírem:

- conversas;
- redes sociais;
- WhatsApp;
- TikTok/Instagram/X;
- transcrições orais;
- textos informais;
- textos com alternância entre português e inglês.

## 9.2 Mas ainda não cobre suficientemente os casos da AMD clássica

Se o objetivo é também aproximar o tagset 1 da tradição do tagset 2 e permitir comparação com os estudos multidimensionais anteriores, então ainda faltam categorias importantes, sobretudo:

1. **stance clauses**;
2. **subordinadas com `que` controladas por verbo/adjetivo/substantivo**;
3. **orações de infinitivo controladas por verbo/adjetivo/substantivo/preposição**;
4. **subtipos de advérbios de stance**;
5. **subtipos de verbos funcionais da AMD**;
6. **distinções de passiva com/sem agente**;
7. **posição sintática de substantivos e nominalizações**;
8. **adjetivos pré- e pós-nominais**;
9. **`não` separado dos demais negativos**;
10. **medidas quantitativas**, se forem desejadas dentro do mesmo sistema.

---

# 10. Proposta de orientação para revisão

Eu sugeriria não simplesmente copiar as 190 categorias do tagset 2 para o tagset 1. Isso deixaria o tagset 1 muito pesado e possivelmente redundante. Em vez disso, a revisão poderia seguir três níveis.

## Nível 1 — Manter categorias amplas já existentes

Essas categorias são úteis para anotação geral e para LLMs:

- artigos;
- determinantes;
- pronomes;
- substantivos;
- adjetivos;
- verbos;
- tempos e modos;
- advérbios;
- preposições;
- conjunções;
- orações;
- marcadores discursivos;
- oralidade;
- português digital.

## Nível 2 — Acrescentar categorias analíticas essenciais do tagset 2

Principalmente:

- stance clauses;
- complementação com `que`;
- infinitivo controlado;
- advérbios de stance;
- tipos verbais AMD;
- passiva com/sem agente;
- infinitivo pessoal;
- `não` separado.

## Nível 3 — Deixar medidas quantitativas fora do tagset ou como seção separada

Categorias como:

- quantidade de palavras;
- extensão média da palavra;
- extensão média da oração;
- razão forma-ocorrência.

Esses traços talvez sejam melhor tratados como **métricas computacionais de pós-processamento**, não como etiquetas aplicadas diretamente a palavras ou expressões no texto.

---

# 11. Tabela final de ação recomendada

| Prioridade  | Ação                                                                                              | Justificativa                                            |
|-------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| Alta        | Criar seção de orações de stance/complementação                                                   | É a maior lacuna em relação ao tagset 2.                 |
| Alta        | Subdividir orações com `que` por controlador: verbo, adjetivo, substantivo                        | Essencial para compatibilidade com AMD.                  |
| Alta        | Subdividir orações de infinitivo por controlador                                                  | Essencial para análise de posicionamento e modalidade.   |
| Alta        | Separar `não` dos demais advérbios negativos                                                      | Muito relevante para PB e frequente nos dados.           |
| Alta        | Separar passiva com agente, sem agente e pronominal                                               | Permite equivalência com categorias do tagset 2.         |
| Média       | Adicionar verbos privados, públicos, persuasivos, ocorrência, ação e facilitação                  | Refina a análise multidimensional.                       |
| Média       | Adicionar adjetivo pré-nominal/pós-nominal e superlativo                                          | Melhora compatibilidade com tagset 2.                    |
| Média       | Adicionar infinitivo pessoal, gerúndio e particípio como formas verbais                           | Importante para português.                               |
| Média       | Adicionar substantivos de lugar, institucionais, em posição de sujeito e nominalização em sujeito | Útil para AMD.                                           |
| Baixa/média | Incluir medidas quantitativas                                                                     | Talvez melhor fora do tagset, como métricas automáticas. |
| Manter      | Categorias de oralidade, variação e digital                                                       | São pontos fortes do tagset 1 e não devem ser removidos. |

---

# 12. Conclusão

O **tagset 1 já cobre uma parte substancial do tagset 2**, especialmente em categorias gerais de artigos, pronomes, substantivos, adjetivos, verbos, advérbios, preposições, conjunções, tempos verbais, passivas, relativas, elipse de sujeito e marcadores discursivos.

No entanto, o **tagset 1 ainda não cobre suficientemente o nível de detalhamento analítico do tagset 2**, principalmente nas categorias de:

- orações com `que`;
- orações reduzidas de infinitivo;
- controle por verbos, substantivos e adjetivos;
- stance/posicionamento;
- subtipos finos de advérbios;
- subtipos funcionais de verbos;
- distinções de passiva;
- posição sintática de substantivos e nominalizações.

Por outro lado, o **tagset 1 tem avanços importantes que não aparecem no tagset 2**, sobretudo em:

- português brasileiro não padrão;
- colocação pronominal;
- tópico-comentário;
- relativas resumptivas;
- regência variável;
- oralidade;
- conversação;
- escrita digital;
- hashtags, emojis, gírias e alternância de código.

Minha avaliação é que o caminho ideal é **preservar a arquitetura ampla e contemporânea do tagset 1**, mas acrescentar uma camada de categorias inspiradas no tagset 2, especialmente para **stance clauses** e distinções de Análise Multidimensional. Assim, o tagset 1 ficaria ao mesmo tempo:

1. mais adequado ao português brasileiro atual;
2. mais compatível com estudos anteriores;
3. mais útil para análise multidimensional;
4. mais robusto para LLMs;
5. mais sensível a corpora digitais e conversacionais.