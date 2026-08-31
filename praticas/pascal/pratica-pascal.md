
# Lista de exemplos em Pascal para OnlineGDB

Todos os programas abaixo são independentes e podem ser copiados e executados no **OnlineGDB**, escolhendo a linguagem **Pascal**.

> Sugestão: peça aos alunos que leiam cada código, prevejam o resultado e somente depois cliquem em **Run**.

## Leitura e escrita em Pascal

| Comando | O que faz | Exemplo |
|---|---|---|
| `readln(variavel);` | Lê um valor e guarda na variável | `readln(idade);` |
| `write('Texto');` | Mostra algo e permanece na mesma linha | `write('Digite a idade: ');` |
| `writeln('Texto');` | Mostra algo e pula para a próxima linha | `writeln('Resultado');` |
| `writeln(valor:0:2);` | Mostra um número real com duas casas decimais | `writeln(area:0:2);` |

### Diferença em relação à linguagem C

Em C, a leitura normalmente usa o endereço da variável:

```c
scanf("%f", &largura);
```

Em Pascal, escrevemos a variável diretamente:

```pascal
readln(largura);
```

Não se escreve `&` e não se usa `%d` ou `%f`. O comando `readln` já conhece o tipo declarado da variável. Internamente, o procedimento consegue modificar a variável por passagem por referência, mas o compilador Pascal cuida disso.

---

# 1. Programas simples

## Exemplo 1 - Área de uma chapa retangular

```pascal
program AreaChapa;

var
  largura, comprimento, area: Double;

begin
  write('Digite a largura da chapa: ');
  readln(largura);

  write('Digite o comprimento da chapa: ');
  readln(comprimento);

  area := largura * comprimento;

  writeln('Area da chapa = ', area:0:2);
end.
```

Observe que a atribuição em Pascal utiliza `:=`:

```pascal
area := largura * comprimento;
```

O sinal `=` é usado em comparações; `:=` guarda um valor em uma variável.

## Exemplo 2 - Potência elétrica

```pascal
program PotenciaEletrica;

var
  tensao, corrente, potencia: Double;

begin
  write('Digite a tensao em volts: ');
  readln(tensao);

  write('Digite a corrente em amperes: ');
  readln(corrente);

  potencia := tensao * corrente;

  writeln('Potencia = ', potencia:0:2, ' W');
end.
```

## Exemplo 3 - Custo de um lote

```pascal
program CustoLote;

var
  quantidade: Integer;
  custoUnitario, custoTotal: Double;

begin
  write('Quantidade de pecas: ');
  readln(quantidade);

  write('Custo por peca: R$ ');
  readln(custoUnitario);

  custoTotal := quantidade * custoUnitario;

  writeln('Custo total do lote = R$ ', custoTotal:0:2);
end.
```

---

# 2. Exemplos com IF / ELSE

## Exemplo 1 - Temperatura do motor

```pascal
program TemperaturaMotor;

var
  temperatura: Double;

begin
  write('Digite a temperatura do motor: ');
  readln(temperatura);

  if temperatura > 80 then
    writeln('ALERTA: temperatura elevada')
  else
    writeln('Temperatura normal');
end.
```

> Atenção: não coloque ponto e vírgula antes do `else`.

## Exemplo 2 - Estoque mínimo

```pascal
program EstoqueMinimo;

var
  estoque, minimo: Integer;

begin
  write('Quantidade atual em estoque: ');
  readln(estoque);

  write('Estoque minimo: ');
  readln(minimo);

  if estoque < minimo then
    writeln('Solicitar reposicao')
  else
    writeln('Estoque suficiente');
end.
```

## Exemplo 3 - Classificação da tensão

```pascal
program ClassificacaoTensao;

var
  tensao: Double;

begin
  write('Digite a tensao medida: ');
  readln(tensao);

  if tensao < 210 then
    writeln('Tensao baixa')
  else if tensao <= 230 then
    writeln('Tensao dentro da faixa')
  else
    writeln('Tensao alta');
end.
```

---

# 3. Exemplos com CASE

Em Pascal, o `case` cumpre o papel semelhante ao `switch/case` de C. Não é necessário escrever `break`.

## Exemplo 1 - Modo de operação de uma máquina

```pascal
program ModoMaquina;

var
  opcao: Integer;

begin
  writeln('1 - Manual');
  writeln('2 - Semiautomatico');
  writeln('3 - Automatico');
  write('Escolha o modo: ');
  readln(opcao);

  case opcao of
    1: writeln('Modo MANUAL selecionado');
    2: writeln('Modo SEMIAUTOMATICO selecionado');
    3: writeln('Modo AUTOMATICO selecionado');
  else
    writeln('Opcao invalida');
  end;
end.
```

## Exemplo 2 - Dia da manutenção

```pascal
program DiaManutencao;

var
  dia: Integer;

begin
  write('Digite um numero de 1 a 5: ');
  readln(dia);

  case dia of
    1: writeln('Segunda-feira');
    2: writeln('Terca-feira');
    3: writeln('Quarta-feira');
    4: writeln('Quinta-feira');
    5: writeln('Sexta-feira');
  else
    writeln('Dia invalido');
  end;
end.
```

## Exemplo 3 - Tipo de material

```pascal
program TipoMaterial;

var
  codigo: Integer;

begin
  writeln('1 - Aco');
  writeln('2 - Aluminio');
  writeln('3 - Cobre');
  write('Codigo do material: ');
  readln(codigo);

  case codigo of
    1: writeln('Material: Aco');
    2: writeln('Material: Aluminio');
    3: writeln('Material: Cobre');
  else
    writeln('Codigo desconhecido');
  end;
end.
```

---

# 4. Exemplos com FOR

## Exemplo 1 - Exibir números de 1 a 10

```pascal
program NumerosDeUmADez;

var
  i: Integer;

begin
  for i := 1 to 10 do
    writeln(i);
end.
```

## Exemplo 2 - Somar produção de 5 turnos

```pascal
program ProducaoTurnos;

var
  i: Integer;
  producao, total: Double;

begin
  total := 0;

  for i := 1 to 5 do
  begin
    write('Producao do turno ', i, ': ');
    readln(producao);
    total := total + producao;
  end;

  writeln('Producao total = ', total:0:2);
end.
```

## Exemplo 3 - Média de 6 medições

```pascal
program MediaMedicoes;

var
  i: Integer;
  valor, soma, media: Double;

begin
  soma := 0;

  for i := 1 to 6 do
  begin
    write('Digite a medicao ', i, ': ');
    readln(valor);
    soma := soma + valor;
  end;

  media := soma / 6;
  writeln('Media das medicoes = ', media:0:2);
end.
```

---

# 5. Exemplos com WHILE

## Exemplo 1 - Contagem de 1 a 5

```pascal
program Contagem;

var
  i: Integer;

begin
  i := 1;

  while i <= 5 do
  begin
    writeln(i);
    i := i + 1;
  end;
end.
```

## Exemplo 2 - Ler temperaturas até atingir o limite

```pascal
program LimiteTemperatura;

var
  temperatura: Double;

begin
  write('Digite a temperatura: ');
  readln(temperatura);

  while temperatura < 80 do
  begin
    writeln('Temperatura ainda abaixo do limite');
    write('Digite uma nova temperatura: ');
    readln(temperatura);
  end;

  writeln('ALERTA: limite atingido ou ultrapassado');
end.
```

## Exemplo 3 - Somar valores até digitar zero

```pascal
program SomaAteZero;

var
  valor, total: Double;

begin
  total := 0;

  write('Digite um valor (0 encerra): ');
  readln(valor);

  while valor <> 0 do
  begin
    total := total + valor;

    write('Digite outro valor (0 encerra): ');
    readln(valor);
  end;

  writeln('Total acumulado = ', total:0:2);
end.
```

Em Pascal, o operador “diferente de” é `<>`. Em C, o equivalente é `!=`.

---

# Quadro rápido: C e Pascal

| Objetivo | C | Pascal |
|---|---|---|
| Ler inteiro | `scanf("%d", &idade);` | `readln(idade);` |
| Ler real | `scanf("%f", &nota);` | `readln(nota);` |
| Mostrar sem pular linha | `printf("Texto");` | `write('Texto');` |
| Mostrar e pular linha | `printf("Texto\n");` | `writeln('Texto');` |
| Atribuir | `area = largura * comprimento;` | `area := largura * comprimento;` |
| Igualdade | `a == b` | `a = b` |
| Diferente | `a != b` | `a <> b` |
| E lógico | `&&` | `and` |
| OU lógico | `\|\|` | `or` |
| Bloco | `{ ... }` | `begin ... end` |
| Seleção | `switch` | `case` |

---

# Desafios para os alunos

1. Altere o programa da temperatura para criar as faixas `normal`, `atencao` e `critica`.
2. Acrescente desconto no custo do lote quando houver mais de 100 peças.
3. No exemplo com `FOR`, mostre também o maior valor digitado.
4. No exemplo com `WHILE`, conte quantos valores foram digitados antes do zero.
5. No `CASE`, acrescente uma quarta opção.

# Como executar no OnlineGDB

1. Acesse [OnlineGDB](https://www.onlinegdb.com/).
2. No seletor de linguagem, escolha **Pascal**.
3. Apague o código de exemplo do editor.
4. Copie somente um programa desta lista por vez.
5. Cole o programa no editor.
6. Clique em **Run**.
7. Informe os valores solicitados no console.

> Para números decimais, digite com ponto no OnlineGDB, por exemplo: `7.5`.
