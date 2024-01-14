# Utility Types

Anotações feitas com base na palestra
[Typescript - Utility Types](https://www.youtube.com/watch?v=V2D8IghrsgQ "@embed")

## Partial`<type>`

O tipo que você declara dentro das chaves, se torna opcional. Então por exemplo se tivermos uma interface User, tudo dentro dele se torna opcional (nome, e-mail, etc).

## Required `<type>`

O tipo declarado dentro das chaves, ao contrário do Partial se torna totalmente obrigatório, mesmo se tiver itens opcionais.

## Pick`<Type, Keys>`

Você consegue construir uma interface apenas com as propriedades que você quer, referenciando o Tipo e as chaves desse tipo que você quer.

## Omit`<Type, Keys>`

Oposto do Pick, aqui você decide o que quer ocultar da interface.

## Record`<Keys,Type>`

Imaginemos que você tem uma interface onde as chaves são números, e todos eles seguem um formato de ter como valor um objeto com duas strings, aqui você pode definir isso sem maiores problemas. A ideia é criar um tipo repetível.
