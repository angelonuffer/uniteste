# uniteste.0 — Guia rápido

Um micro-framework de testes para a linguagem .0. Permite agrupar suítes de testes, fazer asserções básicas e imprimir um resumo dos resultados.

## Principais funções

*   `uniteste.descrever({título testes})`: Agrupa testes sob um nome. Retorna um objeto no formato uniteste com `passaram` e `mensagens`.
*   `uniteste.iguais([valor_obtido valor_esperado])`: Compara dois valores (igualdade simples). Retorna um objeto no formato uniteste.
*   `uniteste.listas_iguais([lista1 lista2])`: Compara listas elemento a elemento. Retorna um objeto no formato uniteste.
*   `uniteste.exibir({passaram mensagens})`: Recebe um objeto no formato uniteste e retorna o código nodejs do processo para executar os testes.

## Exemplo mínimo

```
uniteste = ./código/0

uniteste.exibir(uniteste.descrever({ nome: "Aritmética" testes: [
  uniteste.iguais([(1 + 1) 2])
  uniteste.iguais([(2 + 3) 5])
]}))
```

## Executando os testes

*   É necessário o interpretador 0 (repositório angelonuffer/0).
*   Execução local:

    ```sh
    node 0/código/0_node.js testes/0
    ```

## Saída

*   O runner imprime mensagens por teste e retorna código de saída `0` se todos passaram, ou `1` caso contrário.
*   Mensagens de falha descrevem o valor obtido e o esperado.