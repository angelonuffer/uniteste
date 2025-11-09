# uniteste

Um framework de testes para a linguagem 0. Permite agrupar suítes de testes, fazer asserções e imprimir um resumo dos resultados.

## iguais : função

`valores : lista< número | texto >` => `uniteste : objeto`

Compara dois valores (igualdade simples).

## listas_iguais : função

`listas : lista<lista< número | texto >>` => `uniteste : objeto`

Compara listas elemento a elemento.

## descrever : função

`{ nome : texto testes : lista<uniteste> }` => `uniteste : objeto`

Agrupa testes sob um nome.

## exibir : função

`uniteste : objeto` => `código : texto`

Recebe um objeto no formato uniteste e retorna o código nodejs do processo para executar os testes.

- O processo imprime mensagens por teste e retorna código de saída `0` se todos passaram, ou `1` caso contrário.
- Mensagens de falha descrevem o valor obtido e o esperado.

## uniteste : objeto

- `passaram : número` - Quantidade de testes que passaram.
- `mensagens : lista<lista<texto>>` - Mensagens retornadas pelos testes.