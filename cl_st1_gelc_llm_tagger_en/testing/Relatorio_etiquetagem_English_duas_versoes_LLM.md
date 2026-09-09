Etiquetagem automática em inglês, em duas versões do ChatGPT

Relatório

Projeto LLM Tagging

Patrícia Pereira Bertoli e Carlos Henrique Kauffmann

21/09/2026

Diferentemente de analisar uma variável específica, fizemos um
experimento que busca verificar como modelos de LLM diferentes se
comportam na realização de uma mesma tarefa de etiquetagem.

Nossos procedimentos foram:

1\. Selecionamos o arquivo 00000209_16.txt, composto de um texto de
autoria de Henry James com 961 palavras (4.577 caracteres sem espaço ou
5.446 caracteres com espaço)

2\. Fizemos o upload do arquivo e do tagset simultaneamente em dois "Mac
Air" diferentes, sendo (1) um com a versão chatGPT 5.5 gratuita e (2)
outro com a versão 5.6 think paga. Demos o seguinte prompt:

> "You are a Corpus Linguist annotating texts for Part of Speech. For
> this task, you are being provided with a tagset and a text to tag as
> attachments. Tag the following text using this tagset. Enter each tag
> between {} after each case. Eg. A {1} casa {902, 23, 25}."

A partir daí, o passo a passo pode ser resumido em:

+-----------------------------------+-----------------------------------+
| (1) GPT 5.5 (Consolidated)        | (2) GPT 5.6 Think (Itemized)      |
+===================================+===================================+
| Não conseguiu processar o arquivo | Processou o texto inteiro, mas    |
| inteiro                           | demorou mais tempo do que o 5.5   |
|                                   | incluindo as fragmentações        |
+-----------------------------------+-----------------------------------+
| Informou que o máximo de palavras |                                   |
| que conseguiria processar seria   |                                   |
| entre 100 e 120 palavras          |                                   |
+-----------------------------------+-----------------------------------+
| Solicitamos a fragmentação do     |                                   |
| Texto original, o que resultou em |                                   |
| 13 fragmentos                     |                                   |
+-----------------------------------+-----------------------------------+
| Cada fragmento foi etiquetado     |                                   |
| individualmente                   |                                   |
+-----------------------------------+-----------------------------------+
| O programa não conseguiu agrupar  |                                   |
| os fragmentos etiquetados         |                                   |
+-----------------------------------+-----------------------------------+
| A consolidação foi feita à mão    |                                   |
+-----------------------------------+-----------------------------------+
| Os itens etiquetados foram        | Os itens foram etiquetados        |
| colocados cada um em uma linha    | mantendo-se alinhamento textual   |
+-----------------------------------+-----------------------------------+
| e.g.                              | e.g.                              |
|                                   |                                   |
| I {3,906}                         | I {3,906} was {22} left           |
|                                   | {24,30,33,902,907}, for {69} the  |
| was {22,30}                       | {1} time {9,14}, on {69}          |
|                                   | perceiving                        |
| left {33,902}                     | {26,51,80,94,112,907,908,911}     |
|                                   |                                   |
| , { }                             |                                   |
|                                   |                                   |
| for {49,69,901}                   |                                   |
|                                   |                                   |
| the {1}                           |                                   |
|                                   |                                   |
| time {9,17}                       |                                   |
|                                   |                                   |
| , { } on                          |                                   |
|                                   |                                   |
| {69}                              |                                   |
|                                   |                                   |
| perceiving {26,907,112}           |                                   |
+-----------------------------------+-----------------------------------+

Uma vez etiquetados os dois arquivos, solicitamos que o GPT 5.6 fizesse
uma comparação entre os dois arquivos etiquetados, a partir do seguinte
comando:

> "Compare this document (text_consolidated.txt) to your output
> (00000209_16_tagged.txt). Make a list of their differences"

O output pode ser resumido da seguinte forma:

-   Os itens lexicais dos dois textos são idênticos

-   660 unidades apresentaram tag sets idênticos

-   A etiquetagem apresentou a seguinte variação:

-   37 diferenças de tokenização ou segmentação

-   268 etiquetas diferentes

-   216 marcas de pontuação etiquetadas de forma diferente

-   48 diferenças superficiais, envolvendo aspas, estilo de apóstrofe,
    letra maiúscula, mas com etiquetas idênticas

A fim de reorganizarmos a questão da pontuação, foi solicitado um novo
arquivo, com os itens separados por linhas e a pontuação marcada sem
etiqueta, com o seguinte prompt:

> itemize the tagged set updated with one lexical item per line,
> including its correspondent tags, leave punctuation marks in
> independent lines, even when they do not have a tag or tag set,
> following it order in the original text. like this:
>
> I {3,906}
>
> was {22,30}
>
> left {33,902}
>
> , { }
>
> for {49,69,901}
>
> the {1}
>
> time {9,17}
>
> , { } on
>
> {69}
>
> perceiving {26,907,112}

A partir daí, solicitou-se uma nova compração em forma de tabela, com o
seguinte prompt:

> Compare Text_Consolidated(1).txt to 00000209_16_tagged_itemized.txt.
> Make a comparative table of their differences

O output foi um arquivo Excel nomeado
comparison_Text_Consolidated_vs_itemized.xlsx, em anexo a este
relatório.

A análise da tabela contrastiva pode ser resumida da seguinte maneira:

-   tag order

-   Formating markers

-   Punctuation/Text

-   Tag order + Tokenization

-   Tag set

-   Tag set + Tokenization

-   Tokenization

Os seguintes casos foram desprezados, conforme as justificativas:

1)  Tag order - as etiquetas são as mesmas, apenas colocadas em ordem
    distinta\
    e.g.

facing {24,907,112} versus facing {24,112,907}

2)  Formatting markers referem-se aos travessões

3)  Punctuation/text referem-se às aspas

Dessa forma, restaram para a análise as seguintes situações

**A) Tokenization**

Os problemas relacionados com Tokenization envolvem as contrações. A
etiquetagem feita pelo (1) GPT 5.5 considerou itens distintos, já a
etiquetagem feita pelo (6) GPT 5.6 considerou como um único item:

  --------------------------------------------------------------------------------
  **DIFFERENCE       **Context**            **GPT 5.5 -      **GPT 5.6 -
  TYPE**                                    Consolidated**   Itemized**
  ------------------ ---------------------- ---------------- ---------------------
  Tag order +        Everything . It        does {83,109} +  doesn't {83,107,109}
  Tokenization       \[doesn't\] matter .   n't {107}        
                     I've                                    

  Tag order +        damned . And           that {7b,906} +  that's
  Tokenization       \[that's\] why , to    's {22,107,109}  {7b,22,107,109,906}
  --------------------------------------------------------------------------------

Nos exemplos acima, embora haja a diferença no processo de etiquetagem
as etiquetas são as mesmas. Todavia, os exemplos a seguir, apresentam
diferenças substanciais:

  ---------------------------------------------------------------------------------
  **DIFFERENCE       **Context**       **GPT 5.5 -      **GPT 5.6 - Itemized**
  TYPE**                               Consolidated**   
  ------------------ ----------------- ---------------- ---------------------------
  Tag set +          . " As \[I've\]   I {3,906} + 've  I've {3,23,107,109,906}
  Tokenization       told you ,        {23,31a,107}     

  Tag set +          " " Because       you {4,906} +    you've {4,23,107,109,906}
  Tokenization       \[you've\] made   've {23,31a,107} 
                     up your                            

  Tag set +          only way .        What {68,903} +  What's
  Tokenization       \[What's\] ' out  's {22,107,109}  {8,22,68,107,109,903,906}
                     ,                                  

  Tag set +          " Well ,          there {42,78} +  there's {22,107,109}
  Tokenization       \[there's\] that  's {22,107,109}  
                     awful reason                       
  ---------------------------------------------------------------------------------

**[Sugestão A:]{.mark}**

[É preciso deixar claro no prompt do tag set como o a contração deve ser
estritamente considerada, seja como parte integrante do item lexical ou
não. Por exemplo:]{.mark}

[Para **doesn't** deveria ser **does {83,109} + n't {107}** ou **doesn't
{83,107,109}**. Defendemos a primeira opção com etiquetas
separadas.]{.mark}

**B) Etiquetas diferentes**

A tabela contrastiva apresentou 319 itens com etiquetas diferentes. Os
problemas de Tag set são os que podem causar maiores problemas para a
replicabilidade de estudos que contem com a etiquetagem pelo GPT.
Podemos destacar os seguintes itens recorrentes:

**Caso B.1.** etiqueta para ponto de interrogação (?)

O GPT 5.5 etiquetou o ponto de interrogação, exclamação e algumas aspas
como 67 (wh-questions all clauses tagged as wh-questions) e 903 (allwh =
all wh-structures (wh_ques, wh_cl); enquanto o GPT 5.6 deixou sem
etiqueta.

Exemplos

  --------------------------------------------------------------------------
  **DIFFERENCE       **Context**              **GPT 5.5 -      **GPT 5.6 --
  TYPE**                                      Consolidated**   Itemized**
  ------------------ ------------------------ ---------------- -------------
  **Tagset para                                                
  (?)**                                                        

                     --- \_ you \[?\] \_ " "  ? {67,903}       ? { }

                     you a reason \[?\] " "   ? {67,903}       ? { }
                     For                                       

                     your leaving us \[?\]    ? {67,903}       ? { }
                     Yes ; they                                

                     the lost ? \["\] " Of    " {67,903}       " { }
                     the                                       

                     them --- ? \["\] " She   ? {67,903}       ? { }
                     wants                                     

                     them --- ? \["\] " She   " {67,903}       " { }
                     wants                                     

                     write --- ? \["\]        ? {67,903}       ? { }
                     Remembering she couldn't                  

                     write --- ? \["\]        " {67,903}       " { }
                     Remembering she couldn't                  

                     least known what \[!\] " ! {67,903}       ! { }
                     Mrs .                                     
  --------------------------------------------------------------------------

**[Sugestão B.1:]{.mark}**

[É preciso deixar claro no prompt quais etiquetas devem seguir essas
marcas de pontuação especificamente]{.mark}

**Caso B.2.** etiquetas que consideram um item tanto por sua
especificidade quanto por sua generalidade (all), mas de forma diferente
pelos dois programas

Exemplos

  --------------------------------------------------------------------------
  **DIFFERENCE       **Context**              **GPT 5.5 -      **GPT 5.6 --
  TYPE**                                      Consolidated**   Itemized**
  ------------------ ------------------------ ---------------- -------------
                     The tears were \[again\] again {43}       again {42,43}
                     in her eyes                               

                     I had not \[fully\]      fully {42,70}    fully
                     intended , and                            {42,70,915}

                     --- I can \[hear\] you   hear {26,907}    hear
                     all .                                     {26,80,907}
  --------------------------------------------------------------------------

[**Sugestão B.2:** que todas as etiquetas "all", verb all (xxx) sejam
uma tarefa do counter (pós-etiquetagem) e não do tagging]{.mark}

**Caso B3.** Expressões que poderiam ser consideradas como tal e não
como itens individuais

Of course

At last

In the least

Make up one's mind

Take into account

After all

  ----------------------------------------------------------------------------------
  **DIFFERENCE       **Context**             **GPT 5.5 -      **GPT 5.6 --
  TYPE**                                     Consolidated**   Itemized**
  ------------------ ----------------------- ---------------- ----------------------
  **Expressões que   Oh , of \[course\] , of course {9,14}    course {42,73,915}
  foram separadas**  course                                   

                     course , of \[course\]  course {9,14}    course {42,73,915}
                     ! ' ---                                  

                                                              

                     " I at \[last\]         last {42}        last {42,43}
                     answered ; and                           

                                                              

                     never in the \[least\]  least {42}       least {42,71,915}
                     known what !                             

                     really in the \[least\] least {42}       least {42,71,915}
                     know them .                              

                                                              

                     I've made \[up\] my     up {42}          up {88}
                     mind                                     

                     Because you've made     up {42}          up {88}
                     \[up\] your mind ?                       

                     matter . I've \[made\]  made {24,907     made {26,31a,907}
                     up my mind                               

                     Because you've \[made\] made {24,907     made {26,31a,907}
                     up your mind                             

                                                              

                     to take into            account {9,13}   account
                     \[account\] that they                    {9,13,51,94,908,911}
                     were                                     

                                                              

                     whole thing . \[After\] After {69}       all {42,45,901}
                     all ,                                    

                     thing . After \[all\] , all {42}         all {42,45,901}
                     " I                                      
  ----------------------------------------------------------------------------------

[**Sugestão B.3:** criar etiquetas específicas para expressões, pois
quando separadas geral incosistência na etiquetagem]{.mark}

**Caso B4.** "TIME"

A palavra "time" foi considerada por ambas versões como 9 (all nouns)
mas o GPT 5.5 considerou também como 17. Quantity nouns, enquanto o GPT
6 considerou como 14. other abstract nouns

  ---------------------------------------------------------------------------
  **DIFFERENCE       **Context**              **GPT 5.5 -      **GPT 5.6 --
  TYPE**                                      Consolidated**   Itemized**
  ------------------ ------------------------ ---------------- --------------
  **Tag diferentes   , for the \[time\] , on  time {9,17}      time {9,14}
  para time**        perceiving                                

                     had by this \[time\]     time {9,17}      time {9,14}
                     formed the habit                          
  ---------------------------------------------------------------------------

[**Sugestão B.4:** desambiguar. Deixar claro o quê cada item
significa]{.mark}

**Caso B5.** Etiquetadores consideraram aspectos diferentes para
adicionar os tags e não todos. Algumas vezes, consideraram outros
indicativos na frase para marcar o tempo verbal

  ------------------------------------------------------------------------------------
  **DIFFERENCE       **Context**      **GPT 5.5 -      **GPT 5.6 -- Itemized**
  TYPE**                              Consolidated**   
  ------------------ ---------------- ---------------- -------------------------------
  **Been foi         child who has    been {22,31a}    been {22}
  categorizado como  \[been\]                          
  present perfect**  expelled --- "                    

  **Been foi         had I not        been {22,31b}    been {22}
  categorizado como  \[been\]                          
  past perfect**     prepared . I                      

  **Expeted recebeu  had so perfectly expected         expected
  etiqueta de simple \[expected\]     {26,907,30}      {26,31b,52,80,94,907,908,911}
  past e past        that the return                   
  perfect, além das                                    
  genéricas**                                          

  **GPT 5.5 marcou   I \[had\] then   had {23,31b}     had {21,23,30,900}
  past perfect; gpt  to come                           
  5.6 marcou                                           
  participio**                                         

  **GPT 5.5 marcou   " My question    had {23,31b}     had {23,30}
  past perfect; gpt  \[had\] a                         
  5.6 marcou         sarcastic force                   
  passado**                                            

  **GPT 5.5 marcou   away from me     had {48,901}     had {23}
  condicional; gpt   \[had\] I not                     
  5.6 generalizou**  been                              

  **GPT 5.5          But what had     happened         happened {31b,79,907}
  generalizou; gpt   \[happened\] to  {79,907}         
  5.6 marcou past    you ?                             
  perfect e                                            
  generalizou**                                        
  ------------------------------------------------------------------------------------

**Caso B6 -** Erros na etiquetagem

1.  *Allusion* recebeu etiqueta de verbo pelo GPT 5.5

  ------------------------------------------------------------------------
  **Context**                       **GPT 5.5 -       **GPT 5.6 --
                                    Consolidated**    Itemized**
  --------------------------------- ----------------- --------------------
  they made no \[allusion\] to my   allusion          allusion {9,10,14}
  having                            {9,[25]{.mark}}   

                                                      
  ------------------------------------------------------------------------

2.  *Down* recebeu etiqueta de general adverbs, activity transitivity
    phrasal verbs e occurrence phrasal verb individualmente e break
    recebeu outra etiqueta

  ------------------------------------------------------------------------
  **Context**                       **GPT 5.5 -       **GPT 5.6 --
                                    Consolidated**    Itemized**
  --------------------------------- ----------------- --------------------
  engage to break \[down\] on the   down {42}         down {85}
  first                                               

  , inconsequently break \[down\] . down {42}         down {90}
  The tears                                           
  ------------------------------------------------------------------------

3.  *How* recebeu etiqueta 68. wh-clauses all clauses with
    wh-complementizer, pelo GOT 5.5 mesmo estando no início de uma
    pergunta, sendo, portanto 67.

  ------------------------------------------------------------------------
  **Context**                       **GPT 5.5 -       **GPT 5.6 --
                                    Consolidated**    Itemized**
  --------------------------------- ----------------- --------------------
  up . " \[How\] do you communicate How {68,903}      How {67,903}

  ------------------------------------------------------------------------

4.  *Incosistência entre os modelos*

Ou seja, há inconsistência entre as classificações feitas pelos modelos.

  ------------------------------------------------------------------------
  **Context**                       **GPT 5.5 -       **GPT 5.6 --
                                    Consolidated**    Itemized**
  --------------------------------- ----------------- --------------------
  now clearly so \[many\] of these  many {17}         many {8,906}
  for                                                 

  ------------------------------------------------------------------------

*MANY* recebeu tag de pronome nominal e substantivo quantitativo, em
cada um dos modelos. As duas classificações me parecem corretas, mas há
que ser uma e a outra.

  ------------------------------------------------------------------------
  **Context**                       **GPT 5.5 -       **GPT 5.6 --
                                    Consolidated**    Itemized**
  --------------------------------- ----------------- --------------------
  can hear you \[all\] . But        all {42}          all {8,906}
  nonetheless                                         

  thing . After \[all\] , " I       all {42}          all {42,45,901}
  ------------------------------------------------------------------------

*ALL* recebeu tag de pronome general adverbs pelo GPT 5.5 e apenas no
segundo exemplo no GPT 5.6., o qual também incluiu pronome nominal (8);
conjunção adverbial (45), allconj (901) e allpro (906). De fato, ALL é
pronome no primeiro exemplo e advérbio no segundo, mas faz parte de uma
expressão.

Comportamento semelhante pode ser visto nas etiquetas conferidas a AWAY

  ------------------------------------------------------------------------
  **Context**                       **GPT 5.5 -       **GPT 5.6 --
                                    Consolidated**    Itemized**
  --------------------------------- ----------------- --------------------
  the " put \[away\] " --- of       away {42}         away {9,12}

  fairly have fallen \[away\] from  away {42}         away {84}
  me had                                              
  ------------------------------------------------------------------------

*Home* recebeu etiqueta de substantivo (9; 15) pelo GPT 5.6 quando
exerce função de adverbio (42; 78)

  ------------------------------------------------------------------------
  **Context**                       **GPT 5.5 -       **GPT 5.6 --
                                    Consolidated**    Itemized**
  --------------------------------- ----------------- --------------------
  . I came \[home\] , my dear       home {42,78}      home {9,15}

  ------------------------------------------------------------------------

5.  *Incongruência do tag . GPT 5.6 apresentou a etiqueta correta*

+--------------------------------+----------------+-------------------+
| **Context**                    | **GPT 5.5 --   | **GPT 5.6 --      |
|                                | Consolidated** | Itemized**        |
|                                |                |                   |
|                                | **ERRADA**     | **CORRETA**       |
+================================+================+===================+
| " But --- \[a\] --- which ?    | a {2}          | a {110}           |
|                                |                |                   |
|                                | 2\. Indefinite | 110\. prtcle =    |
|                                | article: a     | discourse         |
|                                |                | particles, e.g.   |
|                                |                | now, well, anyway |
+--------------------------------+----------------+-------------------+
| bribed her to \[silence\] ; a  | silence        | silence {9,14}    |
| silence                        | {25,907}       |                   |
+--------------------------------+----------------+-------------------+
| silence ; a \[silence\] that , | silence {9,25} | silence {9,14}    |
| however                        |                |                   |
+--------------------------------+----------------+-------------------+
|                                | 25\.           | 9\. all nouns:    |
|                                | communication  | all words         |
|                                | verbs e.g.,    | identified as     |
|                                | acknowledge,   | nouns by          |
|                                | answer, claim, | automatic tagger  |
|                                | discuss        |                   |
|                                |                | 14\. other        |
|                                | allverb = all  | abstract nouns    |
|                                | lexical verbs  | e.g., advantage,  |
|                                | (actv, commv,  | background,       |
|                                | mentalv,       | culture, model    |
|                                | causev,        |                   |
|                                | occurv,        |                   |
|                                | existv,        |                   |
|                                |                |                   |
|                                | aspectv), e.g. |                   |
|                                | produce,       |                   |
|                                | report, think, |                   |
|                                | occur, exist   |                   |
+--------------------------------+----------------+-------------------+
|                                |                |                   |
+--------------------------------+----------------+-------------------+

6.  *Incongruência do tag: GPT 5.5 apresentou a etiqueta correta*

+--------------------------------+----------------+-------------------+
| **Context**                    | **GPT 5.5 --   | **GPT 5.6 --      |
|                                | Consolidated** | Itemized**        |
|                                |                |                   |
|                                | **CORRETA**    | **ERRADA**        |
+================================+================+===================+
| then to come \[back\] to meet  | back {42}      | back {84} --      |
| a                              |                | etiquetou apenas  |
|                                | 42\. general   | BACK, mas         |
|                                | adverbs        | considerou a      |
|                                |                | expressão         |
|                                |                |                   |
|                                |                | 84\. act_ipv =    |
|                                |                | activity          |
|                                |                | intransitive      |
|                                |                | phrasal verbs,    |
|                                |                | e.g. go on, come  |
|                                |                | back              |
+--------------------------------+----------------+-------------------+
| please them --- \[so\] long as | so {49,901}    | so {42}           |
| they                           |                |                   |
+--------------------------------+----------------+-------------------+
| that note ; \[so\] that even   | so {49,901}    | so {42}           |
| now                            |                |                   |
+--------------------------------+----------------+-------------------+
| He's exquisite --- \[so\] it   | so {49,901}    | so {42,45,901}    |
| can be                         |                |                   |
|                                |                | 42\. general      |
|                                |                | adverbs           |
|                                |                |                   |
|                                |                | 45\. adverbial    |
|                                |                | conjuncts e.g.,   |
|                                |                | however,          |
|                                |                | therefore, thus,  |
|                                |                | including, for    |
|                                |                | example,          |
|                                |                |                   |
|                                |                | 49\.              |
|                                |                | subordinating     |
|                                |                | conjunctions      |
|                                |                | (other) e.g., as, |
|                                |                | except            |
|                                |                |                   |
|                                |                | 901\. allconj =   |
|                                |                | all conjunctions  |
|                                |                | (o_and, p_and,    |
|                                |                | sub_cnd,          |
|                                |                | sub_othr,         |
|                                |                | conjncts), e.g.   |
|                                |                |                   |
|                                |                | and, but, if,     |
|                                |                | although, however |
+--------------------------------+----------------+-------------------+

7.  GPT 5.6 colocou todos os tags possíveis, inclusive alguns errado
    (Surtou)

+--------------------------------+----------------+--------------------+
| **Context**                    | **GPT 5.5 -    | **GPT 5.6 --       |
|                                | Consolidated** | Itemized**         |
+================================+================+====================+
| he thinks I'm \[afraid\] to    | afraid         | afraid \*          |
| --- and                        | {36,905}       |                    |
|                                |                | {36,55,9           |
|                                |                | 8,905,909,913,914} |
+--------------------------------+----------------+--------------------+
|                                |                | 55, por exemplo:\  |
|                                |                | that-clause        |
|                                |                | controlled by      |
|                                |                | attitudinal        |
|                                |                | adjective e.g.,    |
|                                |                | I\'m afraid        |
|                                |                | that\..., They     |
|                                |                |                    |
|                                |                | must be aware      |
|                                |                | that\..., You\'re  |
|                                |                | surprised that\... |
+--------------------------------+----------------+--------------------+
| yes , they \[asked\] me to say | asked          | asked              |
|                                | {25,81,907,30} | {25,30,            |
|                                |                | 59,82,907,912,914} |
+--------------------------------+----------------+--------------------+
|                                | 25\.           | 59\. to-clause     |
|                                | communication  | controlled by      |
|                                | verbs e.g.,    | speech verb e.g.,  |
|                                | acknowledge,   | ask \<someone\>    |
|                                | answer, claim, | to\..., claim      |
|                                | discuss        | to\...,            |
|                                |                |                    |
|                                | 81\. pub_vb =  | show how to..      |
|                                | public verbs,  |                    |
|                                | e.g. say,      | 82\. sua_vb =      |
|                                | report, claim, | suasive verbs,     |
|                                | assert         | e.g. ask, insist,  |
|                                |                | recommend, suggest |
|                                | 907\. allverb  |                    |
|                                | = all lexical  | 912\. all_vto =    |
|                                | verbs          | to-clauses         |
|                                |                | controlled by      |
|                                | 30\. simple    | verbs              |
|                                | past tense     |                    |
|                                | e.g., they     | 914\. all_to = all |
|                                | claimed, she   | to-clauses         |
|                                | concluded, he  | (all_vto, all_jto) |
|                                | found, I       |                    |
|                                | reported       |                    |
+--------------------------------+----------------+--------------------+
| \[Because\] you've made up     | Because {111}  | Because            |
|                                |                | {49,111,901}       |
+--------------------------------+----------------+--------------------+
|                                |                |                    |
+--------------------------------+----------------+--------------------+
|                                |                |                    |
+--------------------------------+----------------+--------------------+
| I see her \[best\] : facing    | best {42,70}   | best {42}          |
| the                            |                |                    |
+--------------------------------+----------------+--------------------+
|                                | 70\. amplifr = |                    |
|                                | amplifier      |                    |
|                                | adverbs, e.g.  |                    |
|                                | absolutely,    |                    |
|                                | entirely,      |                    |
|                                | completely     |                    |
+--------------------------------+----------------+--------------------+
| were now clearly \[so\] many   | so {42}        | so {42,70,915}     |
| of these                       |                |                    |
+--------------------------------+----------------+--------------------+
| --- when he's \[so\] clever    | so {42}        | so {42,70,915}     |
| and beautiful                  |                |                    |
+--------------------------------+----------------+--------------------+
|                                |                | Todas as           |
|                                |                | possibilidades:    |
|                                |                |                    |
|                                |                | 42\. general       |
|                                |                | adverbs            |
|                                |                |                    |
|                                |                | 70\. amplifr =     |
|                                |                | amplifier adverbs, |
|                                |                | e.g. absolutely,   |
|                                |                | entirely,          |
|                                |                | completely         |
|                                |                |                    |
|                                |                | 915\. all_advl =   |
|                                |                | all stance and     |
|                                |                | degree adverbials  |
|                                |                | (amplifr,          |
|                                |                | downtone, atadvl,  |
|                                |                |                    |
|                                |                | fctadvl, lklydvl,  |
|                                |                | nonfadvl), e.g.    |
|                                |                | completely,        |
|                                |                | probably,          |
|                                |                | unfortunately      |
+--------------------------------+----------------+--------------------+

\* A questão é: a etiqueta deve ser atribuída só a afraid ou à frase?

**Conclusão:**

Quando se considera um texto com 1.000 palavras etiquetadas pelos
modelos GPT 5.5 gratuito e 5.6 pago, pode-se concluir que **não é
possível confiar em nenhum dos modelos plenamente** para uma etiquetagem
precisa.

Ainda que tenham recebido o mesmo texto e o mesmo prompt, os resultados
foram 60% idênticos. Dos 40% de diferença, 10% consideramos
irrelevantes. Todavia, 30% de erro parece-nos um índice alto.

O modelo 5.5 parece não considerar todas as possibilidades de *POS* ou
*derived features* para cada item etiquetado. Já o 5.6 pago considera
mais aspectos dos itens lexicais e, portanto, atribui mais etiquetas,
porém, algumas delas são erradas e algumas consideraram uma sequência de
palavras ao etiquetar um único item.

Neste relatório, apresentamos pontualmente algumas das discrepâncias que
encontramos. O arquivo do Excell em anexo apresenta o resultado
completo.

Uma possibilidade que talvez possa amenizar essas confusões seria
processar a etiquetagem em duas etapas. Na primeira, considerar apenas
as subcategorias e, numa segunda, computar as categorias gerais (ALL).
