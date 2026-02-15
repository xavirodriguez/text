# Teoría de juegos: estructura, cooperación y diseño de incentivos

La **teoría de juegos** analiza matemáticamente situaciones de **interacción estratégica**: escenarios donde el resultado de cada jugador depende no solo de sus decisiones, sino también de las decisiones de otros. Cada agente actúa anticipando y respondiendo al comportamiento de los demás.

Ejemplos cotidianos: fijación de precios en mercados oligopólicos, negociaciones salariales, conflictos internacionales, e incluso dinámicas sociales o ecológicas.

---

## Componentes y formalización

Un juego se define mediante:

1. **Jugadores** (i \in N)
2. **Estrategias** (S_i), conjunto de acciones posibles.
3. **Pagos (utilidades)** (u_i: S_1 \times ... \times S_n \to \mathbb{R})

Estas estructuras permiten modelar situaciones reales de forma **analizable y reproducible**, y distinguir entre distintos tipos de interacción:

- Cooperativos / No cooperativos
- Simultáneos / Secuenciales
- Información completa / incompleta
- Suma cero / suma no cero

**Idea central:** la racionalidad individual puede generar resultados subóptimos a nivel colectivo.

---

## Dilema del Prisionero

Dos jugadores enfrentan la opción de **cooperar (callar)** o **traicionar (confesar)**. La matriz de pagos es:

|                | B calla     | B confiesa |
| -------------- | ----------- | ---------- |
| **A calla**    | 2 · 2 años  | 10 · 0     |
| **A confiesa** | 0 · 10 años | 5 · 5 años |

**Análisis racional:** para cada jugador, **confesar domina**. Esto produce un **equilibrio de Nash (5,5)**.

**Paradoja:** ambos podrían mejorar colectivamente cooperando (2,2), pero la lógica individual lo impide. Esto introduce el contraste **Nash vs Pareto**: estabilidad vs eficiencia colectiva.

---

## Juegos repetidos y cooperación sostenida

Cuando el juego se repite con los mismos jugadores:

- El horizonte temporal se vuelve relevante.
- Cada decisión influye en la **reputación futura**.
- Se maximiza la utilidad intertemporal:

[
\sum_{t=0}^{\infty} \delta^t u_i^t
]

donde (\delta \in (0,1)) representa **valor del futuro/paciencia**.

### Tit for Tat

Estrategia simple y robusta:

1. Cooperar en la primera ronda.
2. Repetir la última acción del otro.

Propiedades:

- Amable: nunca inicia traición.
- Vengativa: castiga inmediatamente.
- Perdonadora: vuelve a cooperar si el otro lo hace.
- Transparente: facilita aprendizaje y predicción.

La estrategia domina en torneos iterados, mostrando que **la cooperación emerge de la repetición y la reputación**.

---

## Juegos con información incompleta

Cuando al menos un jugador **desconoce el tipo, incentivos o pagos del otro**, se modela como **juego bayesiano**:

- Cada jugador tiene un tipo (\theta_i \in \Theta_i)
- Conoce su tipo, pero no el de los demás
- Mantiene creencias (\mu(\theta\_{-i}))
- Estrategia óptima:

[
s*i^\* = \arg\max*{s*i \in S_i} \mathbb{E}*{\theta*{-i}}[u_i(s_i, s*{-i}, \theta)]
]

**Reputación:** las acciones pasadas generan señales, actualizadas mediante Bayes:

[
\mu_{t+1}(\theta_i) = \frac{\mu_t(\theta_i) P(a_i^t|\theta_i)}{\sum_{\theta'} \mu_t(\theta') P(a_i^t|\theta')}
]

Incluso jugadores oportunistas pueden **imitar a cooperadores** para preservar reputación, generando **cooperación estratégica inducida**.

---

## Señalización vs Cribado

En juegos bayesianos, revelar tipos es crítico:

1. **Señalización (Signaling)**

   - Actúa quien conoce su tipo.
   - Emite señales costosas que separan tipos.
   - Condición de separación:

[
u_H(s_H)-c(s_H,\theta_H) > u_H(s_L)-c(s_L,\theta_H)
]

2. **Cribado (Screening)**

   - Actúa quien desconoce el tipo.
   - Diseña opciones (contratos, menús) que inducen autoselección.
   - Restricciones de incentivo y participación aseguran revelación veraz.

**Principio estructural:** no se fuerza información; se diseña para que se revele automáticamente.

---

## Compromisos creíbles

Un compromiso es **secuencialmente racional** si **romperlo no es rentable en ningún sub-juego**.

Métodos:

- **Autolimitación:** restringir el espacio de acciones futuras.
- **Reglas automáticas:** ejecución determinista de acciones contingentes.
- **Garantías externas:** árbitros o mecanismos verificables.

Resultado: la cooperación se convierte en **equilibrio sub-juego perfecto**.

---

## Equilibrios múltiples y coordinación

Cuando existen varios equilibrios de Nash:

- El problema central es **selección de equilibrio**, no solo incentivos.
- Herramientas: señales focales, historia compartida, protocolos predefinidos.
- Permite reducir la ambigüedad estratégica y sostener cooperación en entornos complejos.

---

## Diseño de juegos e instituciones

Para inducir cooperación:

1. **Definir actores y tipos**: conocer incentivos y riesgos.
2. **Ajustar pagos**: hacer la cooperación más atractiva que la desviación.
3. **Introducir observabilidad y reputación**: historial impacta decisiones futuras.
4. **Garantizar compromisos creíbles**: restricciones irreversibles, reglas automáticas, árbitros.
5. **Coordinar expectativas**: reducir ambigüedad frente a equilibrios múltiples.

> La cooperación no depende de moralidad, sino de la **arquitectura estratégica e institucional**.
