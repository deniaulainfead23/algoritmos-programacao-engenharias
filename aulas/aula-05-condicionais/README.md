# Aula 5 - O computador começa a decidir

**Data:** 07/09  
**Conteúdo-base:** **UA8 - Comandos condicionais de múltipla escolha** + **UA9 - Comandos condicionais compostos**

## Objetivos
- compreender decisão em algoritmos;
- utilizar `se`, `senao` e múltipla escolha;
- relacionar operadores relacionais e lógicos às decisões;
- construir soluções para situações reais de Engenharia.

## 18h30-18h40 | Revisão lúdica - Verdadeiro ou falso?
Projete situações:
- temperatura = 80; temperatura > 70?
- estoque = 0; estoque > 0?
- corrente = 10; corrente <= 10?

## 18h40-18h55 | Condicional composta
```text
se condicao entao
   comando
senao
   outro_comando
fimse
```

Exemplo:
```text
se temperatura > 80 entao
   escreva("ALERTA")
senao
   escreva("Temperatura normal")
fimse
```

## 18h55-19h10 | Múltipla escolha
Quando existe uma variável com várias alternativas bem definidas, pode-se usar `escolha/caso`.

```text
escolha(opcao)
caso 1
   ...
caso 2
   ...
outrocaso
   ...
fimescolha
```

## 19h10-19h25 | Três Engenharias, a mesma lógica
- Produção: classificar prioridade de pedido.
- Mecânica: classificar faixa de temperatura.
- Elétrica: selecionar modo de operação de um sistema.

## 19h25-19h40 | Desafio
Sistema recebe um código de operação: 1 = ligar, 2 = desligar, 3 = manutenção. Produza pseudocódigo com escolha/caso.

## 19h40-19h47 | Caça ao erro
Apresente um `se/senao` com mensagens invertidas. A turma corrige.

## Ticket de saída
Quando usar `se/senao` e quando usar `escolha/caso`?
