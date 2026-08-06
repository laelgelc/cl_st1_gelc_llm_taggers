# Manual de Avaliação da Etiquetagem

Versão de 31 de Julho de 2026 18:16:16 +00:00

## 1 Objetivo

O objetivo desta atividade é avaliar a qualidade da etiquetagem automática produzida pelo GPT 5.6.

Há três equipes:

- Inglês (en)
- Português Brasileiro (ptbr)
- Espanhol (es)

## 2 Preparação do conjunto de teste

Cada equipe deverá criar um conjunto de teste para cada etiqueta do tagset da língua pela qual é responsável.

Cada arquivo deverá ter o nome:
```text
<idioma>_<categoria>_test_file.txt
```
Exemplos:
```text
en_31_test_file.txt
ptbr_59_test_file.txt
es_114_test_file.txt
```
Cada arquivo deverá conter exatamente 50 frases numeradas, uma por linha.

As frases deverão obedecer aos seguintes critérios:

- 25 frases contendo a categoria;
- 25 frases sem a categoria;
- frases completas;
- pelo menos 20 palavras por frase;
- frases embaralhadas.

Cada arquivo deverá ser acompanhado por um gabarito:
```text
<idioma>_<categoria>_answer_key.txt
```
Exemplo:
```text
Sentence 1 = YES
Sentence 2 = NO
...
Sentence 50 = YES
```
## 3 Etiquetagem

Cada arquivo deverá ser submetido ao GPT 5.6 para etiquetagem.

Caso seja necessário dividir o arquivo em várias partes, isso é permitido. Entretanto, a etiquetagem final deverá ser reunida em um único arquivo, mantendo a ordem original das frases.

## 4 Avaliação

Comparar a etiquetagem com o gabarito.

**TP** A categoria está presente e foi identificada corretamente.

**FP** A categoria não está presente, mas foi identificada.

**FN** A categoria está presente, mas não foi identificada.

## 5 Exemplos

Nos exemplos a seguir, as etiquetas são fictícias e não correspondem aos tagsets utilizados no projeto.

Suponha que a categoria avaliada seja 114, no arquivo `ptbr_114_test_file.txt`. Neste exemplo fictício, a etiqueta 114 corresponde a uma conjunção subordinada.

### 5.1 TP

Acerto do LLM. Colocou a etiqueta certa na palavra certa.

**Etiqueta certa:** Aquela a que se refere o test file, isto é, a etiqueta em questão, que é o foco da avaliação.

**Palavra certa:** A palavra que recebeu a etiqueta merece essa etiqueta.

## 6 Exemplos

Nos exemplos, as etiquetas são fictícias e não correspondem aos tagsets que usamos.

Suponha que a categoria avaliada seja 114, no arquivo `ptbr_114_test_file.txt`. Nesse exemplo fictício, 114 corresponde a conjunção subordinada.

### 6.1 TP

Acerto do LLM. Colocou a etiqueta certa na palavra certa.

**Etiqueta certa:** Aquela a que se refere o test file, aquela em questão, que é o foco da avaliação.

**Palavra certa:** A palavra que recebeu a etiqueta merece essa etiqueta.

```text
Text: Ele afirmou que chegaria cedo.

Tagging: Ele{25} afirmou{412} que{114,31} chegaria{412} cedo{83}{4}

Resultado: TP
```

### 6.2 FP

Erro do LLM. Colocou a etiqueta certa na palavra errada.

**Etiqueta certa:** Aquela a que se refere o test file, aquela em questão, que é o foco da avaliação.

**Palavra errada:** A etiqueta em questão não se aplica à palavra em que foi colocada.

```text
Text: Tenho certeza disso.

Tagging: Tenho{412} certeza{905} disso{114,27}.{4}

Resultado: FP
```

### 6.3 FN

Erro do LLM. Colocou a etiqueta errada na palavra certa.

**Etiqueta errada:** A etiqueta colocada na palavra em questão não é correta.

**Palavra certa:** A palavra que recebeu a etiqueta indevida mereceria a etiqueta em questão.

```text
Text: Ela explicou que precisaria sair cedo.

Tagging: Ela{25} explicou{412} que{31} precisaria{412} sair{412} cedo{83}.{4}

Resultado: FN
```

## 7 Resultados

Registrar TP, FP e FN para cada categoria. Esses valores serão utilizados para calcular precisão (precision) e cobertura (recall).

## 8 Medidas de desempenho

Ao final da avaliação, serão calculadas as seguintes medidas para cada categoria.

### 8.1 Precisão

Entre todas as ocorrências identificadas pelo etiquetador, qual proporção estava correta?

**Precisão = TP / (TP + FP)**

### 8.2 Cobertura (Recall)

Entre todas as ocorrências que realmente pertencem à categoria, qual proporção foi identificada?

**Cobertura = TP / (TP + FN)**
