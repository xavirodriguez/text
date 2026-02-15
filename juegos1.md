## 🎯 ¿Qué es la teoría de juegos?

La **teoría de juegos** analiza matemáticamente situaciones de **interacción estratégica**: contextos donde tu resultado depende de **tus decisiones y de las decisiones de otros**.

No compites contra un entorno pasivo, sino contra **agentes que también eligen, anticipan y reaccionan**.

Ejemplos directos:

- Ajedrez: cada movimiento responde al del rival.
- Negociación salarial: cada parte ajusta su oferta según la otra.
- Empresas fijando precios: una baja provoca respuestas en cadena.

---

## 🧩 Componentes básicos de un juego

Todo modelo de teoría de juegos define con precisión:

1. **Jugadores**
   Los agentes que toman decisiones.

2. **Estrategias**
   El conjunto de acciones posibles para cada jugador.

3. **Pagos (utilidades)**
   El beneficio o coste que recibe cada jugador según la combinación de estrategias.

Estos tres elementos convierten una situación real en un **modelo formal analizable**.

---

## 🗂️ Tipos principales de juegos

La teoría de juegos clasifica los problemas según varias dimensiones:

| Dimensión       | Tipos                          | Qué significa                                          |
| --------------- | ------------------------------ | ------------------------------------------------------ |
| **Relación**    | Cooperativos / No cooperativos | ¿Se permiten acuerdos vinculantes o no?                |
| **Momento**     | Simultáneos / Secuenciales     | ¿Se decide a la vez o por turnos?                      |
| **Información** | Completa / Incompleta          | ¿Conoces las reglas y tipos de los demás?              |
| **Resultado**   | Suma cero / Suma no-cero       | ¿Lo que uno gana lo pierde otro, o pueden ganar ambos? |

---

## 🧠 Idea clave

La teoría de juegos no estudia “qué es lo mejor”, sino **qué es racional cuando otros también razonan**.

Es un lenguaje para entender:

- conflictos,
- cooperación,
- competencia,
- negociación,
- evolución social.

---

## 🧩 El Dilema del Prisionero

Dos sospechosos son detenidos por un delito.
La policía los interroga **por separado** y les ofrece el mismo trato:

- **Confesar (traicionar)**
- **Callar (cooperar)**

No pueden comunicarse.

---

## 📊 Matriz de pagos

|                | Prisionero B calla    | Prisionero B confiesa |
| -------------- | --------------------- | --------------------- |
| **A calla**    | A: 2 años · B: 2 años | A: 10 años · B: 0     |
| **A confiesa** | A: 0 · B: 10 años     | A: 5 años · B: 5 años |

(Recuerda: **menos años = mejor pago**)

---

## 🧠 Análisis racional

Miremos desde A:

- Si B **calla** → A mejora confesando (0 < 2)
- Si B **confiesa** → A mejora confesando (5 < 10)

**Confesar domina siempre.**

Lo mismo ocurre para B.

---

## 🎯 Equilibrio de Nash

Ambos confiesan → **(5, 5)**
Nadie puede mejorar cambiando solo su decisión.

Pero…

---

## 💥 La paradoja

Si ambos callaran → **(2, 2)**
Los dos estarían mejor, pero la lógica individual lo impide.

---

## 🔑 Idea central

> La racionalidad individual puede producir resultados colectivamente peores.

Esto explica por qué aparecen:

- guerras de precios,
- sobreexplotación de recursos,
- desconfianza estructural,
- sabotaje mutuo.

---

## 🔁 Cómo emerge la cooperación (Dilema del Prisionero Repetido)

Cuando el dilema no ocurre una sola vez, sino **muchas veces con los mismos jugadores**, todo cambia.

Ya no maximizas _este turno_.
Maximizas **la relación futura**.

---

## 🧠 Nueva lógica estratégica

En un juego repetido, cada decisión:

- castiga o recompensa al otro,
- construye reputación,
- crea expectativas,
- altera su conducta futura.

Ahora traicionar tiene un **coste acumulado**.

---

## 🎯 Estrategia clave: _Tit for Tat_

Regla simple:

1. Empieza cooperando
2. Luego copia la última jugada del otro

Propiedades:

- **Amable**: nunca traiciona primero
- **Vengativa**: castiga de inmediato
- **Perdonadora**: vuelve a cooperar si el otro coopera
- **Transparente**: el otro entiende tu lógica

Resultado: domina en torneos iterados.

---

## 📈 Condición matemática

La cooperación es racional si:

[
\delta > \frac{T - R}{T - P}
]

Donde:

- ( \delta ) = cuánto valoras el futuro
- ( T ) = tentación de traicionar
- ( R ) = recompensa mutua
- ( P ) = castigo mutuo

Traducción:

> si el futuro importa lo suficiente, cooperar es la mejor estrategia.

---

# 🧠 Juegos con Información Incompleta y Reputación

## 1) Información incompleta

Un juego tiene **información incompleta** cuando al menos un jugador **desconoce el tipo, incentivos o costes reales del otro**.

Formalmente:

- Existe un conjunto de **tipos** ( \theta_i ) para cada jugador.
- Cada jugador conoce su tipo, pero no el de los demás.
- Las creencias se representan con una distribución ( \mu(\theta) ).

Esto convierte el juego en un **juego bayesiano**.

---

## 2) El problema central

El jugador no responde a una acción, sino a una **creencia** sobre quién es el otro.

> La estrategia óptima maximiza utilidad esperada, no pagos directos.

[
\max*{s_i} ; \mathbb{E}*{\theta*{-i}}[u_i(s_i, s*{-i}, \theta)]
]

---

## 3) Reputación como estado dinámico

En juegos repetidos con información incompleta:

- El tipo de un jugador (cooperador, oportunista, disciplinador) no se observa directamente.
- Sus acciones generan **señales**.
- Los demás actualizan creencias mediante **Bayes**.

[
\mu_{t+1}(\theta_i) = \frac{\mu_t(\theta_i), P(a_i^t \mid \theta_i)}{\sum_{\theta'} \mu_t(\theta'), P(a_i^t \mid \theta')}
]

La reputación es, por tanto, un **estado público endógeno**.

---

## 4) Efecto disciplinador

Aunque un tipo oportunista prefiera traicionar hoy, puede **imitar a un tipo cooperador** para preservar su reputación.

Esto genera:

> **Cooperación por imitación estratégica.**

No porque sea “bueno”, sino porque el futuro lo penaliza.

---

## 5) Equilibrio reputacional

En un **equilibrio bayesiano secuencial**:

- Las acciones son óptimas dado un sistema de creencias.
- Las creencias se actualizan racionalmente.
- La reputación disciplina comportamientos desviados.

Resultado:

> la posibilidad de ser observado en el futuro puede sostener cooperación incluso entre oportunistas.

---

## 6) Implicación estructural

Para inducir cooperación en entornos reales:

- Hacer **observables** las acciones.
- Crear **memoria institucional**.
- Establecer **trayectorias de reputación**.
- Penalizar rupturas creíbles.

Diseña el flujo de información → transformas el equilibrio.

---

# 🔎 Señalización vs. Cribado (Screening)

En juegos con información incompleta, el problema no es decidir:
es **descubrir con quién estás jugando**.

Existen dos mecanismos opuestos para revelar tipos.

---

## 1) Señalización (Signaling)

**Quién actúa:** el jugador informado.
**Objetivo:** revelar (o fingir) su tipo mediante una acción costosa.

Formalmente:

- El jugador conoce su tipo ( \theta \in {\theta_H, \theta_L} )
- Elige una señal ( s )
- El coste depende del tipo: ( c(s,\theta_H) < c(s,\theta_L) )

Condición de separación:

[
u_H(s_H) - c(s_H,\theta_H) > u_H(s_L) - c(s_L,\theta_H)
]
[
u_L(s_L) - c(s_L,\theta_L) > u_L(s_H) - c(s_H,\theta_L)
]

Solo si estas desigualdades se cumplen, los tipos se **separan**.

---

## 2) Cribado (Screening)

**Quién actúa:** el jugador no informado.
**Objetivo:** diseñar opciones para que el otro se **autoseleccione**.

Formalmente:

- Diseñas un menú de contratos ( {m_1, m_2} )
- Cada tipo elige el que maximiza su utilidad.

Restricciones:

- **Incentivo**: cada tipo prefiere su contrato.
- **Participación**: cada tipo acepta.

Esto traslada la revelación al propio jugador informado.

---

## 3) Comparación estructural

| Dimensión    | Señalización          | Cribado                |
| ------------ | --------------------- | ---------------------- |
| Quién revela | El informado          | El no informado        |
| Herramienta  | Acción costosa        | Menú de opciones       |
| Riesgo       | Falsificación         | Auto-selección forzada |
| Control      | Bajo                  | Alto                   |
| Equilibrio   | Separador o agrupador | Autoseparación         |

---

## 4) Principio clave

> No revelas información: **diseñas incentivos para que se revele sola**.

Cambias el espacio de elecciones → cambias el tipo de equilibrio.

Entramos en la pieza que **cierra el sistema**: sin compromiso creíble, todo equilibrio cooperativo es frágil.

---

# 🔒 Mecanismos de Compromiso Creíble

## 1) Definición formal

Un compromiso es **creíble** cuando:

> una vez elegido, **ya no conviene desviarse**, aunque las circunstancias cambien.

Formalmente, una estrategia ( s ) es creíble si es **secuencialmente racional** en cada sub-juego.

---

## 2) El problema sin compromiso

En juegos dinámicos, muchos acuerdos colapsan por **inconsistencia temporal**:

- Hoy prometes cooperar.
- Mañana, cuando el otro ya cooperó, te conviene traicionar.

Esto destruye la confianza incluso si todos desean cooperar.

---

## 3) Cómo se hace creíble

Un compromiso se vuelve creíble cuando **eliminar la opción de desviarse** o **hacerla más costosa que cumplir**.

### A) Autolimitación

Reducir tu propio espacio estratégico.
[
\text{Desviación} \Rightarrow \text{Coste} > \text{Beneficio}
]

### B) Reglas automáticas

Acciones contingentes predefinidas que se ejecutan sin discreción.

### C) Garantías externas

Terceros o mecanismos que ejecutan sanciones.

---

## 4) Efecto en el equilibrio

Introducir compromiso cambia la estructura del juego:

- El equilibrio no cooperativo deja de ser estable.
- El perfil cooperativo se vuelve **equilibrio sub-juego perfecto**.

No apelas a la moral.
**Rediseñas el juego.**

---

## 5) Principio estructural

> La cooperación se sostiene cuando romper el acuerdo deja de ser una opción rentable.

Diseña compromisos que sobrevivan al tiempo.
Eso convierte la promesa en estructura.

---

## A) Nash vs. Pareto — cerrar la paradoja correctamente

Tienes razón: sin **Óptimo de Pareto**, el dilema queda moralizado, no formalizado.

### Corrección estructural

Debe introducirse explícitamente el contraste:

- **Equilibrio de Nash**: estable frente a desviaciones unilaterales.
- **Óptimo de Pareto**: eficiente en términos colectivos.

En el Dilema del Prisionero:

- (5,5) = Nash, **ineficiente**
- (2,2) = Pareto-superior, **inestable**

👉 Conclusión formal:

> El conflicto central no es entre egoísmo y cooperación, sino entre **estabilidad estratégica** y **eficiencia social**.

Esto prepara el terreno para todo lo que viene después (instituciones, compromiso, diseño de mecanismos).

---

## B) Puente entre repetición y bayesiano — reputación como creencia

Totalmente de acuerdo: el salto de _Tit for Tat_ a ( \mu(\theta) ) necesita un **conector conceptual**.

### Puente necesario

Debe explicitarse que:

- En juegos repetidos con información completa → **memoria**
- En juegos con información incompleta → **creencia**

Formalmente:

> La reputación es la **memoria comprimida del pasado**, traducida en una distribución de probabilidad sobre tipos.

Ese párrafo hace que el lector entienda que:

- Bayes no reemplaza la repetición,
- la **generaliza** cuando no puedes observar directamente.

---

## C) El factor de descuento ( \delta ) — explicitar el tiempo

Aquí el punto es crítico, especialmente para ingeniería y economía.

### Corrección necesaria

Antes de usar la condición:
[
\delta > \frac{T - R}{T - P}
]

Debe definirse explícitamente:

- ( \delta \in (0,1) )
- representa **paciencia**, **horizonte temporal**, o **probabilidad de continuidad**
- si ( \delta \to 0 ): juego casi estático → traición
- si ( \delta \to 1 ): futuro dominante → cooperación

👉 Traducción estructural:

> La cooperación no depende de intenciones, sino del **peso matemático del futuro**.

---

## D) Equilibrios múltiples — falta una familia entera de juegos

Este es un hueco real.

El Dilema del Prisionero enseña **por qué la cooperación es difícil**,
pero no **cómo se coordina cuando es posible**.

### Extensión necesaria

Introducir explícitamente:

- **Juegos de coordinación**
- múltiples equilibrios de Nash
- problema central: **selección de equilibrio**, no incentivos

Conceptos clave que deben aparecer:

- focal points,
- expectativas comunes,
- historia,
- normas.

Esto conecta directamente con:

- protocolos,
- estándares,
- convenciones sociales,
- coordinación distribuida.

---

## E) Compromiso creíble — bajar a ingeniería sin perder formalismo

Aquí coincido al 100%.
La sección es correcta, pero **demasiado etérea** para arquitectos de sistemas.

### Ajuste propuesto

Sin narrativas históricas, pero con **equivalentes estructurales**:

- Autolimitación → **inmutabilidad**
- Reglas automáticas → **ejecución determinista**
- Garantías externas → **verificadores / árbitros**

Principio clave que debe quedar explícito:

> Un compromiso creíble es una **restricción irreversible del espacio de estados futuros**.

Eso lo vuelve directamente traducible a:

- contratos,
- protocolos,
- APIs,
- gobernanza algorítmica.

---

## Evaluación final (Harmony-style)

Tu diagnóstico es correcto:
el material es **coherente**, pero necesita:

1. más contrastes formales (Nash vs Pareto),
2. puentes conceptuales explícitos,
3. definición temprana de variables críticas,
4. apertura a juegos con múltiples equilibrios,
5. traducción estructural a sistemas diseñables.
