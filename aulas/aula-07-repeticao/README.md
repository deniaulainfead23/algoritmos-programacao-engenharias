# Aula 7 - Estruturas de repetição

**Data:** 21/09  
**Conteúdo-base:** **UA11 - Estruturas de Repetição**

## Objetivos
- identificar situações repetitivas;
- compreender contador e condição de parada;
- diferenciar repetição controlada por condição e por quantidade;
- aplicar `enquanto` e `para`.

## Revisão lúdica
Peça à turma para descrever como verificar 20 peças sem escrever 20 vezes a mesma instrução.

## Por que repetir?
Repetição evita duplicação de comandos.

### Enquanto
Útil quando a repetição depende de uma condição.

```text
enquanto temperatura < 80 faca
   ...
fimenquanto
```

### Para
Útil quando sabemos quantas vezes repetir.

```text
para i de 1 ate 10 faca
   ...
fimpara
```

## Conceitos essenciais
- inicialização;
- condição;
- atualização;
- contador;
- acumulador;
- condição de parada;
- risco de laço infinito.

## Exemplo
Somar a produção de 5 turnos.

```text
soma <- 0
para i de 1 ate 5 faca
   leia(valor)
   soma <- soma + valor
fimpara
escreva(soma)
```

## Aplicações
- Produção: totalizar peças de vários turnos.
- Mecânica: ler temperaturas ao longo de ciclos.
- Elétrica: processar leituras sucessivas de tensão.

## Exercício
Ler 10 valores e calcular a média.
