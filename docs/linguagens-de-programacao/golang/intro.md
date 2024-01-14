# Introdução Golang

## Packages

Todo programa em Go é baseado em pacotes, e é executado a partir do pacote main (e dentro da função main, assim como a linguagem Java).

Por convenção o nome do pacote é sempre a última parte do pacote importado, por exemplo o pacote `math/rand`, quando formos chamar ele a nível de código, chamaremos como `rand`.

## Imports

Você pode realizar imports em go de duas formas. Sendo a mais indicada o modelo "factored":

```
import (
  "fmt"
  "math"
)
```

Contudo também se é possível importar da seguinte forma:

```
import "fmt"
import "math"
```

## Exported names

Quando vamos usar métodos de algum pacote, existem os nomes "importados" e "não importados". O que nos sinaliza eles é a questão da captalização das letras.

Por exemplo, o pacote `math` possui o método `Pi` que nos retorna o valor de pi. Conseguimos acessar ele depois de importar o método.

Contudo se ele tivesse outro método chamado `pi` com letras minúsculas não poderíamos importar ele.
