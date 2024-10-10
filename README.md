# Desafio Controle de Fluxo

Este projeto foi desenvolvido como parte de um desafio de programação em Java para exercitar fluxos condicionais, loops e tratamento de exceções. O objetivo é implementar um sistema contador que recebe dois números inteiros e imprime a contagem entre eles, lançando uma exceção personalizada se os parâmetros forem inválidos.

## 📋 Descrição do Desafio

O sistema deverá receber dois números inteiros como parâmetros via terminal. Com base nesses números, o programa:
- Valida se o primeiro número é maior que o segundo.
- Lança a exceção `ParametrosInvalidosException` caso o primeiro número seja maior que o segundo, exibindo a mensagem: **"O segundo parâmetro deve ser maior que o primeiro"**.
- Realiza a contagem e imprime no console as iterações entre os números, exemplo:
  - Entrada: `12` e `30`
  - Saída: "Imprimindo o número 1", "Imprimindo o número 2", até "Imprimindo o número 18".

## 🚀 Tecnologias Utilizadas

- **Java**: Linguagem de programação principal para implementação do sistema.
- **Tratamento de Exceções**: Uso de exceção personalizada `ParametrosInvalidosException`.
- **Repetições**: Uso da estrutura `for` para iterar e realizar a contagem.

## 🔧 Estrutura do Projeto

O projeto está dividido em duas classes principais:

1. **`ParametrosInvalidosException`**: Exceção personalizada para quando o segundo parâmetro for menor ou igual ao primeiro.
2. **`Contador`**: Contém a lógica de validação dos parâmetros e a contagem dos números.

### Exemplo de Código

```java
if (parametroUm >= parametroDois) {
    throw new ParametrosInvalidosException("O segundo parâmetro deve ser maior que o primeiro");
}

int contagem = parametroDois - parametroUm;

for (int i = 1; i <= contagem; i++) {
    System.out.println("Imprimindo o número " + i);
}
