# Aula 6 - Fluxo de controle: estruturas de decisão

**Data:** 14/09  
**Conteúdo-base:** **UA10 - Fluxo de Controle: Estruturas de Decisão**

## Objetivos
- consolidar decisões simples, compostas e encadeadas;
- usar operadores relacionais e lógicos;
- acompanhar o fluxo de execução;
- realizar teste de mesa.

## Revisão lúdica
“Qual caminho o algoritmo percorre?” A professora apresenta uma condição e os alunos apontam qual bloco seria executado.

## Decisão simples
Executa um bloco apenas quando a condição é verdadeira.

## Decisão composta
Escolhe entre dois caminhos.

## Decisão encadeada
Permite testar uma nova condição quando a anterior não atende ao caso.

```text
se nota >= 7 entao
   escreva("Faixa A")
senao
   se nota >= 5 entao
      escreva("Faixa B")
   senao
      escreva("Faixa C")
   fimse
fimse
```

## Operadores lógicos
- E: todas as condições precisam ser verdadeiras;
- OU: basta uma condição verdadeira;
- NAO: inverte o valor lógico.

## Aplicações
- Produção: liberar lote se quantidade e inspeção estiverem adequadas.
- Mecânica: operar equipamento se temperatura e pressão estiverem na faixa.
- Elétrica: acionar alerta se tensão ou corrente ultrapassar limite.

## Teste de mesa
Executar manualmente o algoritmo para 3 conjuntos de entradas.

## Exercício final
Criar algoritmo que receba duas medições e determine se o sistema está em situação normal, atenção ou crítica.
