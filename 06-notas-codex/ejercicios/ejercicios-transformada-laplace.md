# Ejercicios: Transformada de Laplace en Tiempo Continuo

## Como usar esta guia

Orden sugerido:

1. transformada y ROC de señales
2. inversa con distintas ROC
3. ecuaciones diferenciales
4. ejercicios tipo parcial

Objetivo:

- practicar tabla y propiedades
- dominar ROC
- distinguir causalidad y estabilidad
- resolver sistemas y ecuaciones diferenciales

---

## 1. Guia de catedra: TL y ROC

### Ejercicio 1

Obtener la Transformada de Laplace y la region de convergencia de

\[
x(t)=e^{-2t}u(t)
\]

y determinar si es estable o no.

**Fuente:** [practico-05-guia-transformada-laplace-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-05-guia-transformada-laplace-resuelto-borgnino.pdf)

### Ejercicio 2

Obtener la TL y la ROC de

\[
x(t)=e^{-3t}[u(t-2)-u(t-5)]
\]

y determinar si es estable o no.

**Fuente:** [practico-05-guia-transformada-laplace-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-05-guia-transformada-laplace-resuelto-borgnino.pdf)

### Ejercicio 3

Obtener la TL y la ROC de

\[
x(t)=2u(t)-1
\]

**Fuente:** [practico-05-guia-transformada-laplace-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-05-guia-transformada-laplace-resuelto-borgnino.pdf)

### Ejercicio 4

Obtener la TL y la ROC de

\[
x(t)=\sin(4t)u(t)+\cos(4t)u(t)
\]

**Fuente:** [practico-05-guia-transformada-laplace-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-05-guia-transformada-laplace-resuelto-borgnino.pdf)

### Ejercicio 5

Obtener la TL y la ROC de

\[
x(t)=te^{2t}u(t)
\]

**Fuente:** [practico-05-guia-transformada-laplace-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-05-guia-transformada-laplace-resuelto-borgnino.pdf)

### Ejercicio 6

Obtener la TL y la ROC de

\[
x(t)=\sin^2(t)u(t)
\]

**Fuente:** [practico-05-guia-transformada-laplace-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-05-guia-transformada-laplace-resuelto-borgnino.pdf)

### Ejercicio 7

Obtener la TL y la ROC de

\[
x(t)=\sin(t+\pi)u(t)
\]

**Fuente:** [practico-05-guia-transformada-laplace-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-05-guia-transformada-laplace-resuelto-borgnino.pdf)

### Ejercicio 8

Obtener la TL y la ROC de

\[
x(t)=(t+1)(u(t)-u(t-1))-u(t-1)
\]

**Fuente:** [practico-05-guia-transformada-laplace-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-05-guia-transformada-laplace-resuelto-borgnino.pdf)

---

## 2. Inversa de Laplace y ROC

### Ejercicio 9

Hallar la transformada inversa de Laplace de

\[
X(s)=\frac{2}{s+3}
\]

y determinar las ROC posibles y sus propiedades.

**Fuente:** sección `(2)` de [practico-05-guia-transformada-laplace-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-05-guia-transformada-laplace-resuelto-borgnino.pdf)

### Ejercicio 10

Hallar la inversa de

\[
X(s)=-\frac{1}{s^2+49}
\]

y discutir ROC posibles.

**Fuente:** sección `(2)` de [practico-05-guia-transformada-laplace-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-05-guia-transformada-laplace-resuelto-borgnino.pdf)

### Ejercicio 11

Hallar la inversa de

\[
X(s)=\frac{s}{4(s^2-1)}
\]

y discutir ROC posibles.

**Fuente:** sección `(2)` de [practico-05-guia-transformada-laplace-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-05-guia-transformada-laplace-resuelto-borgnino.pdf)

### Ejercicio 12

Hallar la inversa de

\[
X(s)=\frac{s^2-3s-9}{s^3-9s}
\]

y discutir ROC posibles.

**Fuente:** sección `(2)` de [practico-05-guia-transformada-laplace-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-05-guia-transformada-laplace-resuelto-borgnino.pdf)

---

## 3. Ecuaciones diferenciales

### Ejercicio 13

Resolver

\[
y'(t)+2y(t)=\sin(t),
\qquad y(0)=0
\]

usando Laplace.

**Fuente:** sección `(3)` de [practico-05-guia-transformada-laplace-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-05-guia-transformada-laplace-resuelto-borgnino.pdf)

### Ejercicio 14

Resolver

\[
y''(t)-y'(t)=\frac{1}{2}t,
\qquad
y(0)=0,
\qquad
y'(0)=0
\]

**Fuente:** sección `(3)` de [practico-05-guia-transformada-laplace-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-05-guia-transformada-laplace-resuelto-borgnino.pdf)

### Ejercicio 15

Resolver

\[
y''(t)-7y'(t)+12y(t)=10,
\qquad
y(0)=0,
\qquad
y'(0)=4
\]

**Fuente:** sección `(3)` de [practico-05-guia-transformada-laplace-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-05-guia-transformada-laplace-resuelto-borgnino.pdf)

---

## 4. Oppenheim / capitulo 9

### Ejercicio 16

Determinar la Transformada de Laplace, la ROC asociada y el diagrama de polos y ceros de

\[
x(t)=e^{-2t}u(t)+e^{-3t}u(t)
\]

**Fuente:** problema 9.21(a) en [practico-oppenheim-cap09-transformada-laplace.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/oppenheim/practico-oppenheim-cap09-transformada-laplace.pdf)

### Ejercicio 17

Determinar la Transformada de Laplace, la ROC asociada y el diagrama de polos y ceros de

\[
x(t)=e^{-4t}u(t)+e^{-5t}\sin(5t)u(t)
\]

**Fuente:** problema 9.21(b) en [practico-oppenheim-cap09-transformada-laplace.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/oppenheim/practico-oppenheim-cap09-transformada-laplace.pdf)

---

## 5. Parciales

### Ejercicio 18

Sea \(H(s)\) la Transformada de Laplace de la respuesta al impulso de un sistema LIT estable, con polos dados en el enunciado.

Se pide:

1. encontrar la ecuación diferencial que relaciona entrada y salida
2. determinar la respuesta al impulso \(h(t)\)
3. decir si el sistema es causal o no

**Fuente:** ejercicio 2 de [parcial-01-2023-recuperatorio-comision-2.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/02-parciales/01-primer-parcial/parcial-01-2023-recuperatorio-comision-2.pdf)

### Ejercicio 19

Dada la ecuación diferencial

\[
\frac{d^2y}{dt^2}+2\frac{dy}{dt}-3y(t)=\frac{dx}{dt}+x(t)
\]

1. determinar \(H(s)\)
2. explicar por qué el sistema no es causal
3. usando Fourier o Laplace, calcular la salida para

\[
x(t)=e^{-t}u(t-2)
\]

**Fuente:** [parcial-01-2023-recuperatorio-comision-bolsa.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/02-parciales/01-primer-parcial/parcial-01-2023-recuperatorio-comision-bolsa.pdf)

### Ejercicio 20

Sea el sistema LIT causal definido por la ecuación diferencial

\[
\frac{d^2y}{dt^2}-\frac{dy}{dt}-3y(t)=\frac{dx}{dt}-2x(t)
\]

1. calcular la respuesta al impulso \(h(t)\)
2. decir si el sistema es estable
3. si se agrega en cascada un sistema con

\[
H_1(s)=s+\alpha
\]

determinar \(\alpha\) para que el sistema total sea estable

**Fuente:** [parcial-01-2024-cursado.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/02-parciales/01-primer-parcial/parcial-01-2024-cursado.pdf)

### Ejercicio 21

Si la función de transferencia racional de un sistema en Laplace tiene polos en

\[
\sigma=-1
\qquad \text{y} \qquad
\sigma=2
\]

indicar la opción incorrecta y justificar:

- puede ser causal
- puede ser estable
- puede ser estable y causal

**Fuente:** [parcial-01-2024-intensivo-2024-02-09.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/02-parciales/01-primer-parcial/parcial-01-2024-intensivo-2024-02-09.pdf)

### Ejercicio 22

Sea un sistema LIT causal y estable cuya Transformada de Laplace racional de su respuesta al impulso tiene dos polos reales con

\[
|p_1|=2,
\qquad
|p_2|=4
\]

1. dibujar la ROC que cumpla esas propiedades
2. obtener la señal en el tiempo

**Fuente:** [parcial-01-2025-redictado.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/02-parciales/01-primer-parcial/parcial-01-2025-redictado.pdf)

### Ejercicio 23

Misma idea que el anterior, pero para un sistema no causal y estable:

1. dibujar una ROC posible
2. obtener la señal en el tiempo

**Fuente:** variante B de [parcial-01-2025-redictado.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/02-parciales/01-primer-parcial/parcial-01-2025-redictado.pdf)

---

## 6. Orden sugerido de practica

### Nivel 1

- Ejercicio 1
- Ejercicio 2
- Ejercicio 4
- Ejercicio 5

### Nivel 2

- Ejercicio 9
- Ejercicio 10
- Ejercicio 11
- Ejercicio 16
- Ejercicio 17

### Nivel 3

- Ejercicio 13
- Ejercicio 14
- Ejercicio 15
- Ejercicio 18
- Ejercicio 19

### Nivel 4

- Ejercicio 20
- Ejercicio 21
- Ejercicio 22
- Ejercicio 23

---

## 7. Sugerencia de resolucion

En cada ejercicio intentar:

1. obtener primero la expresion algebraica
2. decidir la ROC antes de sacar conclusiones
3. marcar polos y ceros
4. si hay sistema, revisar eje \(j\omega\) y lado derecho/izquierdo
5. si hay condiciones iniciales, usar Laplace unilateral con prolijidad
