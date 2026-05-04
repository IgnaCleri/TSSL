# Clase: Transformada de Laplace en Tiempo Continuo

## Objetivo

Entender la Transformada de Laplace con foco en ejercicios de parcial:

- definicion
- region de convergencia
- polos y ceros
- propiedades
- relacion con estabilidad y causalidad
- uso en ecuaciones diferenciales y sistemas LIT

---

## 1. Idea central

La Transformada de Laplace extiende la idea de la Transformada de Fourier y permite trabajar con señales que no siempre tienen TF.

La definicion bilateral es

\[
X(s)=\int_{-\infty}^{\infty}x(t)e^{-st}\,dt
\]

con

\[
s=\sigma+j\omega
\]

La variable \(s\) tiene:

- parte real \(\sigma\)
- parte imaginaria \(\omega\)

Idea conceptual:

\[
\text{Laplace agrega una exponencial real que ayuda a la convergencia}
\]

---

## 2. Region de convergencia (ROC)

La Transformada de Laplace no queda definida solo por \(X(s)\), sino por:

- la expresion algebraica
- su region de convergencia

La ROC es el conjunto de valores de \(s\) para los cuales la integral converge.

Esto es crucial porque una misma expresion algebraica puede corresponder a distintas señales si cambia la ROC.

Ejemplo clasico:

\[
\frac{1}{s+a}
\]

puede corresponder a:

\[
e^{-at}u(t)
\qquad\text{con ROC } \Re\{s\}>-a
\]

o a

\[
-e^{-at}u(-t)
\qquad\text{con ROC } \Re\{s\}<-a
\]

---

## 3. Transformada unilateral

Muchas veces en ecuaciones diferenciales con condiciones iniciales se usa la transformada unilateral:

\[
X^+(s)=\int_0^{\infty}x(t)e^{-st}\,dt
\]

En problemas de sistemas y señales conceptuales suele pesar mas la bilateral y la ROC.

En problemas de ecuaciones diferenciales, la unilateral suele ser la mas comoda.

---

## 4. Polos y ceros

Si

\[
X(s)=\frac{N(s)}{D(s)}
\]

entonces:

- ceros: raices de \(N(s)\)
- polos: raices de \(D(s)\)

Los polos son especialmente importantes porque condicionan:

- ROC
- estabilidad
- causalidad
- forma temporal de la señal

---

## 5. Pares basicos

### Exponencial causal

\[
e^{-at}u(t)\;\longleftrightarrow\;\frac{1}{s+a}
\qquad
\text{ROC: }\Re\{s\}>-a
\]

### Exponencial anticausal

\[
-e^{-at}u(-t)\;\longleftrightarrow\;\frac{1}{s+a}
\qquad
\text{ROC: }\Re\{s\}<-a
\]

### Seno causal

\[
\sin(\omega_0 t)u(t)\;\longleftrightarrow\;\frac{\omega_0}{s^2+\omega_0^2}
\qquad
\text{ROC: }\Re\{s\}>0
\]

### Coseno causal

\[
\cos(\omega_0 t)u(t)\;\longleftrightarrow\;\frac{s}{s^2+\omega_0^2}
\qquad
\text{ROC: }\Re\{s\}>0
\]

### Potencia de \(t\)

\[
t^n e^{-at}u(t)\;\longleftrightarrow\;\frac{n!}{(s+a)^{n+1}}
\qquad
\text{ROC: }\Re\{s\}>-a
\]

---

## 6. Propiedades importantes

### Linealidad

\[
\alpha x_1(t)+\beta x_2(t)\;\longleftrightarrow\;\alpha X_1(s)+\beta X_2(s)
\]

### Desplazamiento temporal

Si

\[
y(t)=x(t-t_0)
\]

entonces, cuidando causalidad y corrimientos:

\[
y(t)=x(t-t_0)u(t-t_0)
\;\longleftrightarrow\;
e^{-st_0}X(s)
\]

### Desplazamiento en \(s\)

Si

\[
y(t)=e^{-at}x(t)
\]

entonces

\[
Y(s)=X(s+a)
\]

### Derivacion en tiempo

\[
\frac{d}{dt}x(t)\;\longleftrightarrow\;sX(s)
\]

en bilateral, bajo condiciones adecuadas.

En unilateral:

\[
\mathcal{L}\{x'(t)\}=sX(s)-x(0)
\]

### Integracion

\[
\int_{-\infty}^{t}x(\tau)\,d\tau\;\longleftrightarrow\;\frac{X(s)}{s}
\]

### Convolucion

\[
x(t)*h(t)\;\longleftrightarrow\;X(s)H(s)
\]

---

## 7. ROC y propiedades del sistema

### Señal lateral derecha

Si la señal es derecha, la ROC queda a la derecha del polo mas a la derecha.

### Señal lateral izquierda

Si la señal es izquierda, la ROC queda a la izquierda del polo mas a la izquierda.

### Señal bilateral

La ROC queda como franja entre polos.

### Estabilidad

Para un sistema LIT estable, la respuesta al impulso \(h(t)\) debe ser absolutamente integrable.

En Laplace eso implica:

\[
\text{la ROC debe incluir al eje } j\omega
\]

### Causalidad

Para un sistema LIT causal:

- \(h(t)\) es derecha
- la ROC queda a la derecha del polo mas a la derecha

---

## 8. Relacion con Transformada de Fourier

La Transformada de Fourier es un caso particular de Laplace evaluada sobre el eje imaginario:

\[
X(j\omega)=X(s)\big|_{s=j\omega}
\]

pero esto solo vale si la ROC incluye al eje \(j\omega\).

Por eso:

- si el eje \(j\omega\) no está en la ROC, no existe la TF
- si sí está, puede evaluarse \(H(j\omega)\) desde \(H(s)\)

---

## 9. Como resolver ejercicios

### Caso A: te piden TL y ROC

1. descomponer la señal en sumas conocidas
2. aplicar tabla y linealidad
3. hallar la ROC de cada termino
4. intersectar ROC

### Caso B: te piden inversa y posibles ROC

1. factorizar denominador
2. hacer fracciones simples si hace falta
3. proponer cada forma temporal posible
4. asociar la ROC correcta

### Caso C: ecuaciones diferenciales

1. transformar ambos lados
2. incorporar condiciones iniciales
3. despejar \(Y(s)\)
4. invertir

### Caso D: sistemas LIT

Si

\[
H(s)=\frac{Y(s)}{X(s)}
\]

entonces:

- polos y ROC te dan estabilidad/causalidad
- la inversa da \(h(t)\)

---

## 10. Ejemplos rapidos

### Ejemplo 1

\[
x(t)=e^{-2t}u(t)
\]

Entonces

\[
X(s)=\frac{1}{s+2},
\qquad
\text{ROC: }\Re\{s\}>-2
\]

### Ejemplo 2

\[
x(t)=te^{2t}u(t)
\]

Entonces

\[
X(s)=\frac{1}{(s-2)^2},
\qquad
\text{ROC: }\Re\{s\}>2
\]

### Ejemplo 3

\[
x(t)=\sin(4t)u(t)+\cos(4t)u(t)
\]

Entonces

\[
X(s)=\frac{4}{s^2+16}+\frac{s}{s^2+16}
\]

con

\[
\text{ROC: }\Re\{s\}>0
\]

---

## 11. Ayudas practicas para parcial

### Ayuda 1

La ROC no se adivina: se deduce del tipo de señal.

### Ayuda 2

Si el sistema es estable, el eje \(j\omega\) tiene que quedar dentro de la ROC.

### Ayuda 3

Si el sistema es causal, la ROC tiene que estar a la derecha del polo mas a la derecha.

### Ayuda 4

Si te dan polos y te preguntan por causalidad o estabilidad, muchas veces ni hace falta hacer la inversa completa.

### Ayuda 5

Si hay ecuación diferencial, Laplace suele ser el camino mas directo.

---

## 12. Errores tipicos

### Error 1

Olvidar que la misma expresion algebraica puede tener distintas ROC.

### Error 2

Confundir polo con cero.

### Error 3

Olvidar incluir condiciones iniciales en la unilateral.

### Error 4

Decir que la TF existe sin verificar si el eje \(j\omega\) está en la ROC.

### Error 5

Concluir estabilidad solo mirando polos, sin mirar ROC.

---

## 13. Checklist minimo

Deberias poder:

- escribir la definición de Laplace
- hallar ROC de señales basicas
- identificar polos y ceros
- relacionar ROC con causalidad y estabilidad
- resolver inversas con distintas ROC
- resolver ecuaciones diferenciales simples
- obtener \(H(s)\) y \(h(t)\)

---

## 14. Resumen express

\[
X(s)=\int_{-\infty}^{\infty}x(t)e^{-st}\,dt
\]

\[
s=\sigma+j\omega
\]

\[
e^{-at}u(t)\;\longleftrightarrow\;\frac{1}{s+a}
\qquad
\text{ROC: }\Re\{s\}>-a
\]

\[
\sin(\omega_0 t)u(t)\;\longleftrightarrow\;\frac{\omega_0}{s^2+\omega_0^2}
\]

\[
x*h\;\longleftrightarrow\;X(s)H(s)
\]

Para estabilidad:

\[
j\omega \in \text{ROC}
\]

Para causalidad:

\[
\text{ROC a la derecha del polo mas a la derecha}
\]

---

## 15. Cierre

La Transformada de Laplace es la herramienta mas potente del parcial para:

- estudiar sistemas
- trabajar polos y ROC
- resolver ecuaciones diferenciales

En práctica, casi todo termina en una de estas ideas:

- usar tabla y propiedades con cuidado
- pensar bien la ROC
- inferir estabilidad y causalidad a partir de polos y ROC
