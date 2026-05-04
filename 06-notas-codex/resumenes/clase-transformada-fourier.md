# Clase: Transformada de Fourier en Tiempo Continuo

## Objetivo

Entender la Transformada de Fourier en tiempo continuo con foco en ejercicios de parcial:

- que representa
- cuando se usa
- definicion y transformada inversa
- propiedades utiles
- relacion con sistemas LIT
- atajos y errores tipicos

---

## 1. Idea central

La Transformada de Fourier toma una señal en tiempo y la describe en frecuencia.

Si \(x(t)\) es una señal aperiódica continua, su transformada es

\[
X(j\omega)=\int_{-\infty}^{\infty}x(t)e^{-j\omega t}\,dt
\]

y la transformada inversa es

\[
x(t)=\frac{1}{2\pi}\int_{-\infty}^{\infty}X(j\omega)e^{j\omega t}\,d\omega
\]

Idea conceptual:

\[
\text{la señal se descompone en frecuencias continuas, no discretas}
\]

---

## 2. Cuándo se usa

La Transformada de Fourier continua se usa principalmente cuando la señal es:

- de tiempo continuo
- no periódica o tratada como aperiódica

Comparacion importante:

- Serie de Fourier: frecuencias discretas
- Transformada de Fourier: espectro continuo

---

## 3. Interpretacion de \(X(j\omega)\)

\[
X(j\omega)
\]

indica cuanto contenido tiene la señal alrededor de cada frecuencia \(\omega\).

Puede escribirse como

\[
X(j\omega)=|X(j\omega)|e^{j\angle X(j\omega)}
\]

donde:

- \(|X(j\omega)|\): magnitud
- \(\angle X(j\omega)\): fase

---

## 4. Señales periodicas y TF

Si la señal es periódica, su Transformada de Fourier no suele ser una funcion "normal", sino una suma de impulsos en frecuencia.

Si

\[
x(t)=\sum_{k=-\infty}^{\infty} a_k e^{jk\omega_0 t}
\]

entonces

\[
X(j\omega)=2\pi\sum_{k=-\infty}^{\infty} a_k \delta(\omega-k\omega_0)
\]

Esto conecta directamente Serie de Fourier con Transformada de Fourier.

---

## 5. Pares basicos que conviene recordar

### Delta

\[
\delta(t)\;\longleftrightarrow\;1
\]

\[
1\;\longleftrightarrow\;2\pi\delta(\omega)
\]

### Exponencial decreciente causal

\[
e^{-at}u(t)\;\longleftrightarrow\;\frac{1}{a+j\omega}
\qquad a>0
\]

### Rectangulo centrado

Si

\[
x(t)=u(t+T)-u(t-T)
\]

entonces

\[
X(j\omega)=\frac{2\sin(\omega T)}{\omega}
\]

### Exponencial bilateral

\[
e^{-a|t|}\;\longleftrightarrow\;\frac{2a}{a^2+\omega^2}
\qquad a>0
\]

---

## 6. Propiedades importantes

### Linealidad

\[
\alpha x_1(t)+\beta x_2(t)\;\longleftrightarrow\;\alpha X_1(j\omega)+\beta X_2(j\omega)
\]

### Desplazamiento temporal

Si

\[
y(t)=x(t-t_0)
\]

entonces

\[
Y(j\omega)=e^{-j\omega t_0}X(j\omega)
\]

### Desplazamiento en frecuencia

Si

\[
y(t)=e^{j\omega_0 t}x(t)
\]

entonces

\[
Y(j\omega)=X\big(j(\omega-\omega_0)\big)
\]

### Escalado temporal

Si

\[
y(t)=x(at)
\]

entonces

\[
Y(j\omega)=\frac{1}{|a|}X\left(j\frac{\omega}{a}\right)
\]

### Conjugacion

\[
x^*(t)\;\longleftrightarrow\;X^*(-j\omega)
\]

### Derivacion en tiempo

\[
\frac{d}{dt}x(t)\;\longleftrightarrow\;j\omega X(j\omega)
\]

### Multiplicacion por \(t\)

\[
tx(t)\;\longleftrightarrow\;j\frac{dX(j\omega)}{d\omega}
\]

### Convolucion en tiempo

\[
x(t)*h(t)\;\longleftrightarrow\;X(j\omega)H(j\omega)
\]

### Multiplicacion en tiempo

\[
x(t)h(t)\;\longleftrightarrow\;\frac{1}{2\pi}X(j\omega)*H(j\omega)
\]

Esta es una de las propiedades mas importantes de parcial.

---

## 7. Simetrias utiles

### Señal real

Si \(x(t)\) es real:

\[
X(-j\omega)=X^*(j\omega)
\]

Entonces:

- la magnitud es par
- la fase es impar

### Señal par y real

Si \(x(t)\) es real y par:

- \(X(j\omega)\) es real y par

### Señal impar y real

Si \(x(t)\) es real e impar:

- \(X(j\omega)\) es puramente imaginaria e impar

Esto ahorra mucho trabajo en ejercicios de justificacion.

---

## 8. Relacion con sistemas LIT

Si un sistema LIT tiene respuesta al impulso \(h(t)\), entonces:

\[
H(j\omega)=\mathcal{F}\{h(t)\}
\]

se llama respuesta en frecuencia.

Si la entrada es \(x(t)\), la salida es

\[
y(t)=x(t)*h(t)
\]

y en frecuencia:

\[
Y(j\omega)=X(j\omega)H(j\omega)
\]

Interpretacion:

- la convolucion en tiempo se vuelve multiplicacion en frecuencia
- cada frecuencia de la entrada es amplificada o atenuada por \(H(j\omega)\)

---

## 9. Como resolver ejercicios

### Caso A: te piden la TF de una señal

1. mirar si coincide con un par conocido
2. si no coincide, intentar obtenerla por propiedades
3. si la señal es por tramos, separar
4. usar simetria para verificar

### Caso B: te piden fase, parte real o valor en \(\omega=0\)

No siempre conviene calcular toda la transformada.

Ideas utiles:

\[
X(0)=\int_{-\infty}^{\infty}x(t)\,dt
\]

Si la señal es un corrimiento temporal:

\[
x(t-t_0)\;\Rightarrow\;e^{-j\omega t_0}X(j\omega)
\]

### Caso C: salida de un sistema LIT

1. hallar \(X(j\omega)\)
2. hallar \(H(j\omega)\)
3. multiplicar

\[
Y(j\omega)=X(j\omega)H(j\omega)
\]

4. si hace falta, volver con la inversa

---

## 10. Ejemplos rapidos

### Ejemplo 1

Sea

\[
x(t)=u(t-2)-u(t-6)
\]

Es un pulso rectangular desplazado. Su transformada puede pensarse como un sinc desplazado con fase lineal:

\[
X(j\omega)=e^{-j4\omega}\frac{2\sin(2\omega)}{\omega}
\]

La parte importante es reconocer:

- ancho total \(4\)
- centro en \(t=4\)

### Ejemplo 2

Sea

\[
x(t)=e^{-6|t|}
\]

Por par conocido:

\[
X(j\omega)=\frac{12}{36+\omega^2}
\]

### Ejemplo 3

Si

\[
x(t)=e^{j4t}u(t)e^{-8t}
\]

entonces

\[
x(t)=e^{-(8-j4)t}u(t)
\]

y

\[
X(j\omega)=\frac{1}{8+j(\omega-4)}
\]

---

## 11. Ayudas practicas para parcial

### Ayuda 1

Si ves desplazamientos temporales, casi seguro conviene sacar primero la señal base y despues aplicar fase:

\[
e^{-j\omega t_0}
\]

### Ayuda 2

Si la señal es par, casi nunca deberia aparecer una fase complicada.

### Ayuda 3

Para \(\omega=0\):

\[
X(0)=\int x(t)\,dt
\]

Esto evita calcular toda la TF.

### Ayuda 4

Si hay convolucion en tiempo, conviene pasar a frecuencia.

### Ayuda 5

Si hay multiplicacion en tiempo, preparate para convolucion en frecuencia.

---

## 12. Errores tipicos

### Error 1

Olvidar el signo del exponente:

\[
X(j\omega)=\int x(t)e^{-j\omega t}\,dt
\]

### Error 2

Confundir desplazamiento en tiempo con desplazamiento en frecuencia.

### Error 3

No reconocer señales pares o impares.

### Error 4

Calcular toda la transformada cuando solo te piden fase o \(X(0)\).

### Error 5

Olvidar el factor \(\frac{1}{2\pi}\) en la propiedad de multiplicacion en tiempo.

---

## 13. Checklist minimo

Deberias poder:

- escribir la definición y la inversa
- reconocer pares basicos
- usar desplazamiento temporal y modulación
- justificar simetrias
- calcular \(X(0)\) sin rehacer todo
- analizar un sistema LIT en frecuencia

---

## 14. Resumen express

\[
X(j\omega)=\int_{-\infty}^{\infty}x(t)e^{-j\omega t}\,dt
\]

\[
x(t)=\frac{1}{2\pi}\int_{-\infty}^{\infty}X(j\omega)e^{j\omega t}\,d\omega
\]

\[
x(t-t_0)\;\longleftrightarrow\;e^{-j\omega t_0}X(j\omega)
\]

\[
e^{j\omega_0 t}x(t)\;\longleftrightarrow\;X\big(j(\omega-\omega_0)\big)
\]

\[
\frac{d}{dt}x(t)\;\longleftrightarrow\;j\omega X(j\omega)
\]

\[
x*h\;\longleftrightarrow\;XH
\]

\[
xh\;\longleftrightarrow\;\frac{1}{2\pi}X*H
\]

---

## 15. Cierre

La Transformada de Fourier permite mirar la señal desde la frecuencia.

En parcial, casi todo termina en una de estas tres ideas:

- reconocer pares conocidos
- aplicar propiedades con prolijidad
- usar \(Y=XH\) para sistemas LIT
