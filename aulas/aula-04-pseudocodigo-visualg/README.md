# Aula 4 - Do problema ao pseudocódigo

**Data:** 31/08  
**Conteúdo-base:** **UA6 - Representação de algoritmos em forma de pseudocódigo** + **UA7 - Desenvolvimento de algoritmos sequenciais através de pseudocódigo (VisuAlg)**

## Objetivos
- compreender o papel do pseudocódigo;
- reconhecer a estrutura de um algoritmo sequencial;
- identificar entrada, processamento e saída;
- utilizar declaração, leitura, atribuição e escrita;
- implementar e testar algoritmos simples no VisuAlg.

## 18h30-18h40 | Revisão lúdica - Você é o computador
Dê instruções propositalmente vagas, como “calcule a área daquela peça”. Pergunte: quais dados estão faltando? O computador pode adivinhar?

Retome:
- algoritmo;
- variável;
- tipos de dados;
- entrada, processamento e saída;
- operadores.

## 18h40-18h55 | O que é pseudocódigo?
Pseudocódigo descreve um algoritmo de forma estruturada, próxima da linguagem humana, sem exigir inicialmente todas as regras de uma linguagem de programação.

```text
algoritmo "nome"
var
   variaveis
inicio
   comandos
fimalgoritmo
```

## 18h55-19h10 | Entrada, processamento e saída
Problema: calcular a área de uma chapa.

- entrada: comprimento e largura;
- processamento: area <- comprimento * largura;
- saída: área calculada.

```text
algoritmo "area_chapa"
var
   comprimento, largura, area: real
inicio
   escreva("Comprimento: ")
   leia(comprimento)
   escreva("Largura: ")
   leia(largura)
   area <- comprimento * largura
   escreva("Area = ", area)
fimalgoritmo
```

## 19h10-19h25 | Primeiro contato com VisuAlg
1. abrir o ambiente;
2. digitar o algoritmo;
3. executar;
4. fornecer dados;
5. observar a saída;
6. alterar valores e testar novamente.

## 19h25-19h40 | Engenharia em ação
### Produção
Receber quantidade produzida e custo unitário e calcular custo do lote.

### Mecânica
Receber medidas de uma peça e calcular uma grandeza geométrica simples.

### Elétrica
Receber tensão e corrente e calcular potência: `P = V * I`.

## 19h40-19h47 | Desafio em dupla
Escolha um dos três contextos, identifique entrada, processamento e saída e escreva o pseudocódigo.

## 19h47-19h50 | Ticket de saída
Qual é a diferença entre dizer a solução de um problema e escrever uma solução que o computador consiga executar?

## Revisão
A revisão deve retomar os conteúdos das aulas anteriores antes do novo conteúdo.
