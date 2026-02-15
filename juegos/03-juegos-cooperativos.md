Un **juego cooperativo** se centra en la colaboración entre jugadores, donde el objetivo no es competir, sino **maximizar beneficios conjuntos**.

### Representación matemática

Se describe mediante un par (\Gamma = (N, \nu)):

- (N = {1, \dots, n}) representa el conjunto de jugadores, llamado **gran coalición**.
- (\nu : 2^N \to \mathbb{R}) es la **función característica**, que asigna a cada coalición (C \subseteq N) un valor real (\nu(C)), reflejando la **recompensa que ese grupo puede lograr trabajando juntos**.
- Se asume que (\nu(\emptyset) = 0), es decir, sin jugadores no hay recompensa.

### Interpretación

- Cada subgrupo de jugadores puede formar **coaliciones** y obtener una recompensa específica.
- La función característica permite analizar **cómo distribuir los beneficios** de manera justa o eficiente entre los miembros.

### Ejemplo conceptual

Si tres jugadores A, B y C forman coaliciones:

- (\nu({A}) = 2), (\nu({B}) = 3), (\nu({C}) = 1)
- (\nu({A,B}) = 6), (\nu({A,C}) = 4), (\nu({B,C}) = 5)
- (\nu({A,B,C}) = 10)

Esto indica que **la colaboración genera valor agregado**: la coalición completa gana más que la suma de esfuerzos individuales, reflejando el incentivo para cooperar.
