# Singleton

Definição:

> Garantir que uma classe tenha somente uma instância no programa e fornecer um ponto de acesso global para a mesma.

## Principal problema que ele apresenta

O singleton acaba ferindo o princípio da responsabilidade única, porque algumas pessoas discutem que o fato de ele controlar seu próprio ciclo de vida (fora o que já fazem por default).

---

## Principais problemas que ele se propõe e resolver

### **Garantir que uma classe apenas tenha uma única instância**

Ou seja, garantir que o acesso a algum recurso (ex - banco de dados) seja mais controlado, ou seja, ao invés de termos várias instâncias do mesmo objeto, temos apenas um e ele controla a disponibilização desse recurso.

> ⚠️ Isso é impossível de ser realizado se a classe ainda pode ser instanciada através do `constructor`, por isso sempre deixamos ele como privado nessas situações e criamos um método que cheque se precisamos criar uma instância ou reutilizar uma já existente.

### Provém um ponto de acesso global para a instância

Em qualquer parte do projeto (independentemente do arquivo) essa propriedade deve poder ser acessada.

> 💡 Em JS, cada vez que fazemos um import, é uma espécie de singleton pq não estamos criando novas instâncias, apenas referenciando uma já existente.

Ele também previne que o código possa ser sobrescrito por outra implementação, visto que teremos sempre apenas uma instância do objeto. Caso queiramos sobrescrever algum comportamento pré-definido, precisamos fazer com que o singleton espere isso.

---

## Observações

Com esse padrão, temos algo chamado `lazy initialization` que basicamente é criar o objeto/instância apenas quando ele é necessário e não quando o programa inicia.

É mais difícil usar esse padrão em linguagens que permitem multi threads, muito porque se torna complexo evitar que sejam criadas instâncias em cada thread.

Uma das recomendações de quando usar esse padrão é também quando você precisa usar uma variável de ambiente em várias partes importante do programa, porque elas podem ser sobrescritas mas o singleton não.

---

## Links interessantes

[[Refactoring Guru] Singleton](https://refactoring.guru/design-patterns/singleton)

[[Otávio Miranda] \***\*Singleton Teoria - Padrões de Projeto - Parte 4/45\*\***](https://www.youtube.com/watch?v=x9h8MgAvi_I&list=PLbIBj8vQhvm0VY5YrMrafWaQY2EnJ3j8H&index=4)

[[StackOverflow] Discussão sobre como singleton pode ferir o princípio da responsabilidade única](https://stackoverflow.com/questions/137975/what-are-drawbacks-or-disadvantages-of-singleton-pattern)
