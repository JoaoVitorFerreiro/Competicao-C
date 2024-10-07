
# **Documentação de Funções Essenciais em C**

## 1. **Entrada e Saída de Dados**

As funções de entrada e saída são essenciais para comunicação com o usuário.

- **`printf`**: Exibe dados na tela.

```c
printf("Digite um número: ");
```

- **`scanf`**: Lê dados fornecidos pelo usuário.

```c
int numero;
scanf("%d", &numero);
```

### Exemplo Comentado:

```c
#include <stdio.h>

int main() {
    int idade;
    
    // Exibe a mensagem pedindo a idade do usuário
    printf("Digite sua idade: ");
    
    // Lê o valor digitado pelo usuário e armazena na variável idade
    scanf("%d", &idade);
    
    // Exibe a idade informada
    printf("Sua idade é: %d anos", idade);
    
    return 0;
}
```

---

## 2. **Estruturas Condicionais**

As estruturas condicionais permitem que seu programa tome decisões com base em condições.

- **`if`, `else if`, `else`**: Utilizados para decisões.

```c
if (idade >= 18) {
    printf("Maior de idade");
} else {
    printf("Menor de idade");
}
```

### Exemplo Comentado:

```c
#include <stdio.h>

int main() {
    int nota;
    
    printf("Digite a nota do aluno (0 a 10): ");
    scanf("%d", &nota);
    
    // Verifica se a nota é maior ou igual a 7
    if (nota >= 7) {
        printf("Aluno aprovado!");
    } else if (nota >= 5) {
        // Nota entre 5 e 6.9
        printf("Aluno em recuperação.");
    } else {
        // Nota abaixo de 5
        printf("Aluno reprovado.");
    }
    
    return 0;
}
```

---

## 3. **Estruturas de Repetição**

São usadas para repetir blocos de código.

- **`for`**: Repetição com contagem controlada.

```c
for (int i = 0; i < 10; i++) {
    printf("%d", i);
}
```

- **`while`**: Repetição enquanto a condição for verdadeira.

```c
int i = 0;
while (i < 10) {
    printf("%d", i);
    i++;
}
```

### Exemplo Comentado:

```c
#include <stdio.h>

int main() {
    int i;
    
    // Exibe os números de 1 a 5 usando for
    for (i = 1; i <= 5; i++) {
        printf("Contagem: %d
", i);
    }
    
    return 0;
}
```

---

## 4. **Arrays (Vetores)**

Arrays armazenam múltiplos valores de um mesmo tipo de dado.

- Declaração e Acesso:

```c
int numeros[5] = {1, 2, 3, 4, 5};
printf("%d", numeros[2]);  // Acessa o terceiro elemento
```

### Exemplo Comentado:

```c
#include <stdio.h>

int main() {
    int numeros[3];
    
    // Preenchendo o array
    for (int i = 0; i < 3; i++) {
        printf("Digite um número: ");
        scanf("%d", &numeros[i]);
    }
    
    // Exibindo os valores do array
    for (int i = 0; i < 3; i++) {
        printf("Número %d: %d\n", i + 1, numeros[i]);
    }
    
    return 0;
}
```

---

## 5. **Funções**

Funções permitem organizar melhor o código, dividindo-o em blocos reutilizáveis.

- Declaração de Função:

```c
int soma(int a, int b) {
    return a + b;
}
```

- Chamando uma Função:

```c
int resultado = soma(3, 4);
printf("Resultado: %d", resultado);
```

### Exemplo Comentado:

```c
#include <stdio.h>

// Função que calcula o dobro de um número
int dobro(int numero) {
    return numero * 2;
}

int main() {
    int valor;
    
    // Solicitando um valor ao usuário
    printf("Digite um número: ");
    scanf("%d", &valor);
    
    // Chamando a função dobro e exibindo o resultado
    printf("O dobro de %d é %d\n", valor, dobro(valor));
    
    return 0;
}
```

---

## 6. **Estruturas (Structs)**

Structs permitem agrupar diferentes tipos de dados em uma única variável.

- Declaração:

```c
struct Aluno {
    char nome[50];
    int idade;
    float nota;
};
```

- Acesso:

```c
struct Aluno aluno1;
aluno1.idade = 18;
```

### Exemplo Comentado:

```c
#include <stdio.h>

// Definição da struct Aluno
struct Aluno {
    char nome[50];
    int idade;
    float nota;
};

int main() {
    struct Aluno aluno1;
    
    // Recebendo os dados do aluno
    printf("Digite o nome do aluno: ");
    scanf("%s", aluno1.nome);
    printf("Digite a idade do aluno: ");
    scanf("%d", &aluno1.idade);
    printf("Digite a nota do aluno: ");
    scanf("%f", &aluno1.nota);
    
    // Exibindo os dados
    printf("Nome: %s\n", aluno1.nome);
    printf("Idade: %d\n", aluno1.idade);
    printf("Nota: %.2f\n", aluno1.nota);
    
    return 0;
}
```

---

## 7. **Manipulação de Strings**

Strings são arrays de caracteres terminados em `\0`.

- **`gets` e `puts`**: Funções para ler e exibir strings.

```c
char nome[50];
gets(nome);  // Lê a string
puts(nome);  // Exibe a string
```

- Funções comuns: `strlen` (comprimento), `strcpy` (cópia), `strcmp` (comparação).

### Exemplo Comentado:

```c
#include <stdio.h>
#include <string.h>

int main() {
    char palavra1[20], palavra2[20];
    
    // Recebendo duas palavras
    printf("Digite a primeira palavra: ");
    gets(palavra1);
    printf("Digite a segunda palavra: ");
    gets(palavra2);
    
    // Comparando as palavras
    if (strcmp(palavra1, palavra2) == 0) {
        printf("As palavras são iguais.\n");
    } else {
        printf("As palavras são diferentes.\n");
    }
    
    return 0;
}
```
