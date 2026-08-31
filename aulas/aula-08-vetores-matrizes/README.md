# Aula 8 - Vetores e matrizes

**Data:** 28/09  
**Conteúdo-base:** **UA12 - Estruturas de Dados Homogêneas do Tipo Matriz**

## Objetivos
- compreender variável simples, vetor e matriz;
- usar índices;
- percorrer estruturas com repetição;
- organizar conjuntos de dados.

## Revisão lúdica
Mostre 5 valores no quadro. Pergunte: precisamos criar `valor1`, `valor2`, `valor3`, `valor4`, `valor5`?

## Vetor
Coleção unidimensional de valores do mesmo tipo.

```text
temperaturas[1..5]
```

## Matriz
Organização bidimensional por linha e coluna.

```text
producao[1..3, 1..4]
```

## Índices
O índice indica a posição do elemento.

## Percorrendo vetor
```text
para i de 1 ate 5 faca
   leia(temperaturas[i])
fimpara
```

## Percorrendo matriz
Normalmente exige dois laços.

```text
para linha de 1 ate 3 faca
   para coluna de 1 ate 4 faca
      leia(dados[linha,coluna])
   fimpara
fimpara
```

## Aplicações
- Produção: produção por setor e turno.
- Mecânica: temperatura por sensor e instante.
- Elétrica: tensão por circuito e ponto de medição.

## Exercício
Criar uma matriz 3x3 de medições e identificar o maior valor após a leitura.
