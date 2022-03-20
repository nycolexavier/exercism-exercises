Desafio Lucian's Luscious Lasagna do site [exercism](https://exercism.org/dashboard)


Coisas que precisamos fazer:
- Task 1: Definir a constante `EXPECTED_MINUTES_IN_OVEN` que representa com quantos minutos vai precisar ficar no forno. Deve ser exportada. O valor que temos que dar a essa `const` é de 40.

```
    const PREPARATION_MINUTES_PER_LAYER = 2;

    export const EXPECTED_MINUTES_IN_OVEN = 40;
```

- Task: 2 Implementar a função `remainingMinutesInOven()` que leva como parâmetro os minutos reais que esteve no forno e retorne quantos minutos a lasanha ainda precisa permanecer no forno, com base no tempo de forno esperado em minutos da tarefa anterior.
[gif de tela azul]

Vamos com calma para entender melhor? 

- 1️⃣ Primeiro, nós temos uma função que se chama ``remainingMinutesInOven`, certo? 
- 2️⃣ Ela tem um parâmetro (o que está entre parênteses na função, lembrou?) 
- 3️⃣ Beleza, temos uma função, ela tem um parâmetro mas, o que ela tem que retornar para nós? 
- 4️⃣ O tempo que precisa ficar no forno que está sendo definido pela const `EXPECTED_MINUTES_IN_OVEN` e nós precisamos do tempo que já ficou no forno que a const `actualMinutesInOven`
- 4️⃣ Entãooo para termos a conta exata precisamos SUBTRAIR. Ficou claro pra ti? Me conta ae!

```
    export function remainingMinutesInOven(actualMinutesInOven) `
    {
        return EXPECTED_MINUTES_IN_OVEN - actualMinutesInOven;
    }
```

- Task 3: Implementar a função `preparationTimeInMinutes()` que está pegando o número de camadas que você tem como parâmetro (`numberOfLayers`) e retornar quantos minutos você gastou preparando-a, supondo que você leve 2 minutos para fazer isso.

Explicação: a função precisa retornar quantos minutos você vai levar para todas as camadas. Para isso, vamos precisar de dois valores, o quantidade de camadas (que ali esta sendo passada como um parâmetro `numberOfLayers`) e quanto tempo vou levar para fazer cada camada ``PREPARATION_MINUTES_PER_LAYER`. Com essa informação podemos MULTIPLICAR e chegar no resultado, assim:

```
    export function preparationTimeInMinutes(numberOfLayers) 
    {
        return numberOfLayers * PREPARATION_MINUTES_PER_LAYER;
    }
```

Vamos para a última task!

- [ ] Implemente a função `totalTimeInMinutes` que está recebendo dois parâmetros, o `numberOfLayers` e o `atualMinutesInOven`. A função deve retornar quantos minutos no total você trabalhou, que é a soma do tempo de preparo (guarda essa informação) e o tempo em minutos que ficou no forno, somando esses dois, nós temos a nossa resposta?

``` 
    export function totalTimeInMinutes(numberOfLayers, actualMinutesInOven) 
    {
        return preparationTimeInMinutes(numberOfLayers) + actualMinutesInOven;
    }

```


Durante o conclusão desse artigo, tive algumas dúvidas, esses links me ajudaram, espero que faça o mesmo com você: 
[import e export](https://blog.betrybe.com/tecnologia/import-e-export/#3)

Feito com ❤ por [Nycole](https://github.com/nycolexavier)