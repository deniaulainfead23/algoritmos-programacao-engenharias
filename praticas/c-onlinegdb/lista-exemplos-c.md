# Lista de exemplos em C para OnlineGDB

Todos os programas abaixo são independentes e podem ser copiados e executados no **OnlineGDB** usando a linguagem **C**.

> Sugestão: peça aos alunos para lerem o código antes da execução e preverem o resultado.

---

# 1. Programas simples

## Exemplo 1 - Área de uma chapa retangular

```c
#include <stdio.h>

int main() {
    float largura, comprimento, area;

    printf("Digite a largura da chapa: ");
    scanf("%f", &largura);

    printf("Digite o comprimento da chapa: ");
    scanf("%f", &comprimento);

    area = largura * comprimento;

    printf("Area da chapa = %.2f\n", area);
    return 0;
}
```

## Exemplo 2 - Potência elétrica

```c
#include <stdio.h>

int main() {
    float tensao, corrente, potencia;

    printf("Digite a tensao em volts: ");
    scanf("%f", &tensao);

    printf("Digite a corrente em amperes: ");
    scanf("%f", &corrente);

    potencia = tensao * corrente;

    printf("Potencia = %.2f W\n", potencia);
    return 0;
}
```

## Exemplo 3 - Custo de um lote

```c
#include <stdio.h>

int main() {
    int quantidade;
    float custoUnitario, custoTotal;

    printf("Quantidade de pecas: ");
    scanf("%d", &quantidade);

    printf("Custo por peca: R$ ");
    scanf("%f", &custoUnitario);

    custoTotal = quantidade * custoUnitario;

    printf("Custo total do lote = R$ %.2f\n", custoTotal);
    return 0;
}
```

---

# 2. Exemplos com IF / ELSE

## Exemplo 1 - Temperatura do motor

```c
#include <stdio.h>

int main() {
    float temperatura;

    printf("Digite a temperatura do motor: ");
    scanf("%f", &temperatura);

    if (temperatura > 80) {
        printf("ALERTA: temperatura elevada\n");
    } else {
        printf("Temperatura normal\n");
    }

    return 0;
}
```

## Exemplo 2 - Estoque mínimo

```c
#include <stdio.h>

int main() {
    int estoque, minimo;

    printf("Quantidade atual em estoque: ");
    scanf("%d", &estoque);

    printf("Estoque minimo: ");
    scanf("%d", &minimo);

    if (estoque < minimo) {
        printf("Solicitar reposicao\n");
    } else {
        printf("Estoque suficiente\n");
    }

    return 0;
}
```

## Exemplo 3 - Classificação da tensão

```c
#include <stdio.h>

int main() {
    float tensao;

    printf("Digite a tensao medida: ");
    scanf("%f", &tensao);

    if (tensao < 210) {
        printf("Tensao baixa\n");
    } else if (tensao <= 230) {
        printf("Tensao dentro da faixa\n");
    } else {
        printf("Tensao alta\n");
    }

    return 0;
}
```

---

# 3. Exemplos com SWITCH / CASE

## Exemplo 1 - Modo de operação de uma máquina

```c
#include <stdio.h>

int main() {
    int opcao;

    printf("1 - Manual\n");
    printf("2 - Semiautomatico\n");
    printf("3 - Automatico\n");
    printf("Escolha o modo: ");
    scanf("%d", &opcao);

    switch (opcao) {
        case 1:
            printf("Modo MANUAL selecionado\n");
            break;
        case 2:
            printf("Modo SEMIAUTOMATICO selecionado\n");
            break;
        case 3:
            printf("Modo AUTOMATICO selecionado\n");
            break;
        default:
            printf("Opcao invalida\n");
    }

    return 0;
}
```

## Exemplo 2 - Dia da manutenção

```c
#include <stdio.h>

int main() {
    int dia;

    printf("Digite um numero de 1 a 5: ");
    scanf("%d", &dia);

    switch (dia) {
        case 1:
            printf("Segunda-feira\n");
            break;
        case 2:
            printf("Terca-feira\n");
            break;
        case 3:
            printf("Quarta-feira\n");
            break;
        case 4:
            printf("Quinta-feira\n");
            break;
        case 5:
            printf("Sexta-feira\n");
            break;
        default:
            printf("Dia invalido\n");
    }

    return 0;
}
```

## Exemplo 3 - Tipo de material

```c
#include <stdio.h>

int main() {
    int codigo;

    printf("1 - Aco\n");
    printf("2 - Aluminio\n");
    printf("3 - Cobre\n");
    printf("Codigo do material: ");
    scanf("%d", &codigo);

    switch (codigo) {
        case 1:
            printf("Material: Aco\n");
            break;
        case 2:
            printf("Material: Aluminio\n");
            break;
        case 3:
            printf("Material: Cobre\n");
            break;
        default:
            printf("Codigo desconhecido\n");
    }

    return 0;
}
```

---

# 4. Exemplos com FOR

## Exemplo 1 - Exibir números de 1 a 10

```c
#include <stdio.h>

int main() {
    int i;

    for (i = 1; i <= 10; i++) {
        printf("%d\n", i);
    }

    return 0;
}
```

## Exemplo 2 - Somar produção de 5 turnos

```c
#include <stdio.h>

int main() {
    int i;
    float producao, total = 0;

    for (i = 1; i <= 5; i++) {
        printf("Producao do turno %d: ", i);
        scanf("%f", &producao);
        total = total + producao;
    }

    printf("Producao total = %.2f\n", total);
    return 0;
}
```

## Exemplo 3 - Média de 6 medições

```c
#include <stdio.h>

int main() {
    int i;
    float valor, soma = 0, media;

    for (i = 1; i <= 6; i++) {
        printf("Digite a medicao %d: ", i);
        scanf("%f", &valor);
        soma = soma + valor;
    }

    media = soma / 6;
    printf("Media das medicoes = %.2f\n", media);

    return 0;
}
```

---

# 5. Exemplos com WHILE

## Exemplo 1 - Contagem de 1 a 5

```c
#include <stdio.h>

int main() {
    int i = 1;

    while (i <= 5) {
        printf("%d\n", i);
        i++;
    }

    return 0;
}
```

## Exemplo 2 - Ler temperaturas até atingir o limite

```c
#include <stdio.h>

int main() {
    float temperatura;

    printf("Digite a temperatura: ");
    scanf("%f", &temperatura);

    while (temperatura < 80) {
        printf("Temperatura ainda abaixo do limite\n");
        printf("Digite uma nova temperatura: ");
        scanf("%f", &temperatura);
    }

    printf("ALERTA: limite atingido ou ultrapassado\n");
    return 0;
}
```

## Exemplo 3 - Somar valores até digitar zero

```c
#include <stdio.h>

int main() {
    float valor, total = 0;

    printf("Digite um valor (0 encerra): ");
    scanf("%f", &valor);

    while (valor != 0) {
        total = total + valor;

        printf("Digite outro valor (0 encerra): ");
        scanf("%f", &valor);
    }

    printf("Total acumulado = %.2f\n", total);
    return 0;
}
```

---

# Desafios para os alunos

1. Altere o programa da temperatura para criar as faixas `normal`, `atencao` e `critica`.
2. Acrescente desconto no custo do lote quando houver mais de 100 peças.
3. No exemplo com `FOR`, mostre também o maior valor digitado.
4. No exemplo com `WHILE`, conte quantos valores foram digitados antes do zero.
5. No `SWITCH`, acrescente uma quarta opção.

# Como executar no OnlineGDB

1. Acesse o OnlineGDB.
2. Escolha a linguagem **C**.
3. Apague o código de exemplo do editor.
4. Copie um dos programas desta página.
5. Cole no editor.
6. Clique em **Run**.
7. Informe os valores solicitados no console.
