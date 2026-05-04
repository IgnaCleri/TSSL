# Ejercicios: Transformada de Fourier en Tiempo Continuo

## Como usar esta guia

Orden sugerido:

1. pares y propiedades basicas
2. corrimientos y modulaciones
3. sistemas LIT
4. ejercicios tipo parcial

Objetivo:

- reconocer pares clasicos
- usar propiedades sin integrar de mas
- trabajar fase, parte real y \(X(0)\)
- resolver salidas de sistemas en frecuencia

---

## 1. Guia de catedra: propiedades directas

### Ejercicio 1

Obtener la Transformada de Fourier de

\[
x(t)=u(t-2)-u(t-6)
\]

aplicando propiedades.

**Fuente:** [practico-04-guia-transformada-fourier-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-04-guia-transformada-fourier-resuelto-borgnino.pdf)

### Ejercicio 2

Obtener la Transformada de Fourier de

\[
x(t)=e^{-6|t|}
\]

**Fuente:** [practico-04-guia-transformada-fourier-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-04-guia-transformada-fourier-resuelto-borgnino.pdf)

### Ejercicio 3

Obtener la Transformada de Fourier de

\[
x(t)=\frac{10}{5+jt}
\]

**Fuente:** [practico-04-guia-transformada-fourier-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-04-guia-transformada-fourier-resuelto-borgnino.pdf)

### Ejercicio 4

Obtener la Transformada de Fourier de

\[
x(t)=\frac{1}{9+t^2}
\]

**Fuente:** [practico-04-guia-transformada-fourier-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-04-guia-transformada-fourier-resuelto-borgnino.pdf)

### Ejercicio 5

Obtener la Transformada de Fourier de

\[
x(t)=e^{j4t}u(t)e^{-8t}
\]

**Fuente:** [practico-04-guia-transformada-fourier-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-04-guia-transformada-fourier-resuelto-borgnino.pdf)

### Ejercicio 6

Obtener la Transformada de Fourier de

\[
x(t)=e^{j3t}\big(u(t+2)-u(t-2)\big)
\]

**Fuente:** [practico-04-guia-transformada-fourier-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-04-guia-transformada-fourier-resuelto-borgnino.pdf)

### Ejercicio 7

Obtener la Transformada de Fourier de

\[
x(t)=5e^{-7|t+2|}
\]

**Fuente:** [practico-04-guia-transformada-fourier-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-04-guia-transformada-fourier-resuelto-borgnino.pdf)

### Ejercicio 8

Obtener la Transformada de Fourier de

\[
x(t)=t(u(t+3)-u(t-3))
\]

**Fuente:** [practico-04-guia-transformada-fourier-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-04-guia-transformada-fourier-resuelto-borgnino.pdf)

---

## 2. Guia de catedra: ecuaciones diferenciales y sistemas

### Ejercicio 9

Obtener \(y(t)\) de la ecuación diferencial

\[
y'(t)-6y(t)=x(t),
\qquad
x(t)=u(t)e^{-6t}
\]

usando Transformada de Fourier.

**Fuente:** sección `(2)` de [practico-04-guia-transformada-fourier-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-04-guia-transformada-fourier-resuelto-borgnino.pdf)

### Ejercicio 10

Obtener \(y(t)\) para

\[
4y(t)-y''(t)=x(t),
\qquad
x(t)=e^{-10|t|}
\]

**Fuente:** sección `(2)` de [practico-04-guia-transformada-fourier-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-04-guia-transformada-fourier-resuelto-borgnino.pdf)

### Ejercicio 11

Obtener

\[
y(t)=x(t)*h(t)
\]

para

\[
x(t)=2+\cos(2t)+2\cos\left(\frac{t}{2}\right),
\qquad
h(t)=2\frac{\sin(t)}{t}
\]

**Fuente:** sección `(3)` de [practico-04-guia-transformada-fourier-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-04-guia-transformada-fourier-resuelto-borgnino.pdf)

### Ejercicio 12

Obtener

\[
y(t)=x(t)*h(t)
\]

para

\[
x(t)=\cos(t)+2\cos\left(\frac{t}{2}\right),
\qquad
h(t)=2\frac{\sin(2t)}{t}
\]

**Fuente:** sección `(3)` de [practico-04-guia-transformada-fourier-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-04-guia-transformada-fourier-resuelto-borgnino.pdf)

---

## 3. Parciales y simulacros

### Ejercicio 13

Sea la señal

\[
x(t)=u(-t+5)-u(-t+1)
\]

Seleccionar la fase correcta de su Transformada de Fourier y justificar.

**Fuente:** [parcial-01-2023-recuperatorio-comision-2.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/02-parciales/01-primer-parcial/parcial-01-2023-recuperatorio-comision-2.pdf)

### Ejercicio 14

En el sistema LIT del parcial 2024, calcular la Transformada de Fourier de la respuesta al impulso \(h(t)\) dada gráficamente.

**Fuente:** ejercicio 2(a) de [parcial-01-2024-cursado.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/02-parciales/01-primer-parcial/parcial-01-2024-cursado.pdf)

### Ejercicio 15

Sea

\[
x(t)=-u(t+1)+u(t+3)
\]

1. determinar la fase de su Transformada de Fourier usando propiedades
2. determinar \(X(j\omega)\) para \(\omega=0\) sin calcular toda la transformada

**Fuente:** ejercicio 4 de [parcial-01-2024-cursado.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/02-parciales/01-primer-parcial/parcial-01-2024-cursado.pdf)

### Ejercicio 16

Sea la señal del ejercicio 4 de la variante B del parcial 2024:

\[
x(t)=2\sin(2\pi t)\,[u(t+1/2)-u(t-1/2)]-[u(t+1)-u(t-1)]
\]

Determinar la parte real de la Transformada de Fourier usando propiedades.

**Fuente:** [parcial-01-2024-cursado.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/02-parciales/01-primer-parcial/parcial-01-2024-cursado.pdf)

### Ejercicio 17

En el recuperatorio intensivo 2024, determinar mediante propiedades:

1. la señal temporal cuya TF es la parte real de \(X(j\omega)\)
2. la parte impar de \(X(j\omega)\)

**Fuente:** [parcial-01-2024-recuperatorio-intensivo-2024-02-28.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/02-parciales/01-primer-parcial/parcial-01-2024-recuperatorio-intensivo-2024-02-28.pdf)

### Ejercicio 18

Calcular la Transformada de Fourier de

\[
y(t)=x(t)\tilde{s}(t)
\]

con

\[
x(t)=2e^{j\frac{\pi}{2}t}\sin(t),
\qquad
\tilde{s}(t)=\sum_{k=-\infty}^{\infty}\delta(t-k)
\]

y graficar \(Y(j\omega)\).

**Fuente:** ejercicio 2 de [parcial-01-2025-redictado.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/02-parciales/01-primer-parcial/parcial-01-2025-redictado.pdf)

### Ejercicio 19

Sea

\[
x(t)=2+\cos\left(\frac{1}{2}t\right)+\cos(2t)+\cos\left(\frac{3}{4}t\right),
\qquad
h(t)=2\frac{\sin(t)}{t}
\]

1. obtener la Serie de Fourier de la entrada
2. obtener la Serie de Fourier de la salida usando la Transformada de Fourier del sistema

**Fuente:** [simulacro-parcial-01-enunciado.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/02-parciales/03-simulacros/simulacro-parcial-01-enunciado.pdf)

### Ejercicio 20

Para el mismo sistema del simulacro, calcular la salida si

\[
x(t)=\cos(6t)
\]

y explicar qué produce el sistema sobre la señal de entrada.

**Fuente:** [simulacro-parcial-01-enunciado.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/02-parciales/03-simulacros/simulacro-parcial-01-enunciado.pdf)

---

## 4. Orden sugerido de practica

### Nivel 1

- Ejercicio 1
- Ejercicio 2
- Ejercicio 4
- Ejercicio 5

### Nivel 2

- Ejercicio 6
- Ejercicio 7
- Ejercicio 8
- Ejercicio 15

### Nivel 3

- Ejercicio 9
- Ejercicio 10
- Ejercicio 11
- Ejercicio 12
- Ejercicio 14

### Nivel 4

- Ejercicio 13
- Ejercicio 16
- Ejercicio 17
- Ejercicio 18
- Ejercicio 19
- Ejercicio 20

---

## 5. Sugerencia de resolucion

En cada ejercicio intentar:

1. decidir si conviene par conocido o propiedad
2. revisar simetria antes de integrar
3. si te piden fase o \(X(0)\), no calcular toda la TF sin necesidad
4. si hay sistema LIT, pasar a frecuencia y usar

\[
Y(j\omega)=X(j\omega)H(j\omega)
\]

5. verificar al final si la magnitud/fase tienen sentido con la señal original
