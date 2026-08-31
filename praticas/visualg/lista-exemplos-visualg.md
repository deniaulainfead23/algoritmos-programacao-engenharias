# Lista de exemplos práticos em VisuAlg

Material para copiar, colar e executar no **VisuAlg**.

Os exemplos estão organizados em cinco grupos: algoritmos simples, `SE`, `ESCOLHA/CASO`, `PARA` e `ENQUANTO`.

> Sugestão didática: antes de executar, peça aos alunos para preverem a saída do algoritmo.

---

# 1. Algoritmos simples

## Exemplo 1 - Área de uma chapa retangular

```text
algoritmo "area_chapa"
var
   largura, comprimento, area: real
inicio
   escreva("Digite a largura da chapa: ")
   leia(largura)
   escreva("Digite o comprimento da chapa: ")
   leia(comprimento)

   area <- largura * comprimento

   escreval("Area da chapa = ", area)
fimalgoritmo
```

## Exemplo 2 - Potência elétrica

```text
algoritmo "potencia_eletrica"
var
   tensao, corrente, potencia: real
inicio
   escreva("Digite a tensao em volts: ")
   leia(tensao)
   escreva("Digite a corrente em amperes: ")
   leia(corrente)

   potencia <- tensao * corrente

   escreval("Potencia = ", potencia, " W")
fimalgoritmo
```

## Exemplo 3 - Custo de um lote

```text
algoritmo "custo_lote"
var
   quantidade: inteiro
   custoUnitario, custoTotal: real
inicio
   escreva("Quantidade de pecas: ")
   leia(quantidade)
   escreva("Custo por peca: R$ ")
   leia(custoUnitario)

   custoTotal <- quantidade * custoUnitario

   escreval("Custo total do lote = R$ ", custoTotal)
fimalgoritmo
```

---

# 2. Exemplos com SE

## Exemplo 1 - Temperatura de um motor

```text
algoritmo "temperatura_motor"
var
   temperatura: real
inicio
   escreva("Digite a temperatura do motor: ")
   leia(temperatura)

   se temperatura > 80 entao
      escreval("ALERTA: temperatura elevada")
   senao
      escreval("Temperatura normal")
   fimse
fimalgoritmo
```

## Exemplo 2 - Estoque mínimo

```text
algoritmo "estoque_minimo"
var
   estoque, minimo: inteiro
inicio
   escreva("Quantidade atual em estoque: ")
   leia(estoque)
   escreva("Estoque minimo: ")
   leia(minimo)

   se estoque < minimo entao
      escreval("Solicitar reposicao")
   senao
      escreval("Estoque suficiente")
   fimse
fimalgoritmo
```

## Exemplo 3 - Classificação de tensão

```text
algoritmo "classificar_tensao"
var
   tensao: real
inicio
   escreva("Digite a tensao medida: ")
   leia(tensao)

   se tensao < 210 entao
      escreval("Tensao baixa")
   senao
      se tensao <= 230 entao
         escreval("Tensao dentro da faixa")
      senao
         escreval("Tensao alta")
      fimse
   fimse
fimalgoritmo
```

---

# 3. Exemplos com ESCOLHA/CASO

## Exemplo 1 - Modo de operação de uma máquina

```text
algoritmo "modo_maquina"
var
   opcao: inteiro
inicio
   escreval("1 - Manual")
   escreval("2 - Semiautomatico")
   escreval("3 - Automatico")
   escreva("Escolha o modo: ")
   leia(opcao)

   escolha opcao
      caso 1
         escreval("Modo MANUAL selecionado")
      caso 2
         escreval("Modo SEMIAUTOMATICO selecionado")
      caso 3
         escreval("Modo AUTOMATICO selecionado")
      outrocaso
         escreval("Opcao invalida")
   fimescolha
fimalgoritmo
```

## Exemplo 2 - Dia da manutenção

```text
algoritmo "dia_manutencao"
var
   dia: inteiro
inicio
   escreva("Digite um numero de 1 a 5: ")
   leia(dia)

   escolha dia
      caso 1
         escreval("Segunda-feira")
      caso 2
         escreval("Terca-feira")
      caso 3
         escreval("Quarta-feira")
      caso 4
         escreval("Quinta-feira")
      caso 5
         escreval("Sexta-feira")
      outrocaso
         escreval("Dia invalido")
   fimescolha
fimalgoritmo
```

## Exemplo 3 - Tipo de material

```text
algoritmo "tipo_material"
var
   codigo: inteiro
inicio
   escreval("1 - Aco")
   escreval("2 - Aluminio")
   escreval("3 - Cobre")
   escreva("Codigo do material: ")
   leia(codigo)

   escolha codigo
      caso 1
         escreval("Material: Aco")
      caso 2
         escreval("Material: Aluminio")
      caso 3
         escreval("Material: Cobre")
      outrocaso
         escreval("Codigo desconhecido")
   fimescolha
fimalgoritmo
```

---

# 4. Exemplos com PARA

## Exemplo 1 - Exibir números de 1 a 10

```text
algoritmo "contagem_1_a_10"
var
   i: inteiro
inicio
   para i de 1 ate 10 faca
      escreval(i)
   fimpara
fimalgoritmo
```

## Exemplo 2 - Somar produção de 5 turnos

```text
algoritmo "soma_producao"
var
   i: inteiro
   producao, total: real
inicio
   total <- 0

   para i de 1 ate 5 faca
      escreva("Producao do turno ", i, ": ")
      leia(producao)
      total <- total + producao
   fimpara

   escreval("Producao total = ", total)
fimalgoritmo
```

## Exemplo 3 - Média de 6 medições

```text
algoritmo "media_medicoes"
var
   i: inteiro
   valor, soma, media: real
inicio
   soma <- 0

   para i de 1 ate 6 faca
      escreva("Digite a medicao ", i, ": ")
      leia(valor)
      soma <- soma + valor
   fimpara

   media <- soma / 6
   escreval("Media das medicoes = ", media)
fimalgoritmo
```

---

# 5. Exemplos com ENQUANTO

## Exemplo 1 - Contagem de 1 a 5

```text
algoritmo "contagem_enquanto"
var
   i: inteiro
inicio
   i <- 1

   enquanto i <= 5 faca
      escreval(i)
      i <- i + 1
   fimenquanto
fimalgoritmo
```

## Exemplo 2 - Ler temperaturas até atingir o limite

```text
algoritmo "monitorar_temperatura"
var
   temperatura: real
inicio
   escreva("Digite a temperatura: ")
   leia(temperatura)

   enquanto temperatura < 80 faca
      escreval("Temperatura ainda abaixo do limite")
      escreva("Digite uma nova temperatura: ")
      leia(temperatura)
   fimenquanto

   escreval("ALERTA: limite atingido ou ultrapassado")
fimalgoritmo
```

## Exemplo 3 - Somar valores até o usuário digitar zero

```text
algoritmo "somar_ate_zero"
var
   valor, total: real
inicio
   total <- 0

   escreva("Digite um valor (0 encerra): ")
   leia(valor)

   enquanto valor <> 0 faca
      total <- total + valor
      escreva("Digite outro valor (0 encerra): ")
      leia(valor)
   fimenquanto

   escreval("Total acumulado = ", total)
fimalgoritmo
```

---

# Desafios para modificar os exemplos

1. No exemplo da temperatura, crie três faixas: normal, atenção e crítica.
2. No custo do lote, acrescente um desconto de 5% quando a quantidade for maior que 100.
3. No exemplo com `PARA`, informe também o maior valor digitado.
4. No exemplo com `ENQUANTO`, conte quantos valores foram informados antes do zero.
5. No `ESCOLHA/CASO`, acrescente uma quarta opção de material.
