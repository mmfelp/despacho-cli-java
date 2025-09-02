## HU-1 — Despacho gratis (compra alta, dentro de radio)

Como cliente
Quiero que si mi compra es > $50.000 y la distancia ≤ 20 km
Para obtener despacho gratis y pagar solo el valor de la compra

Actores: Cliente
Prioridad: Alta

Criterios de aceptación:

Dado una compra de $60.000
Y una distancia de 15 km
Cuando ejecuto el cálculo
Entonces el costo de despacho es 0
Y el total a pagar es $60.000

Dado una compra de $50.000
Y una distancia de 20 km
Cuando ejecuto el cálculo
Entonces el costo de despacho es 0
Y el total a pagar es $50.000

## HU-2 — Despacho $150/km (compra media)

Como cliente
Quiero que si mi compra está entre $25.000 y $49.999
Para que el despacho se calcule a $150 por km

Actores: Cliente
Prioridad: Alta

Criterios de aceptación:

Dado una compra de $40.000
Y una distancia de 10 km
Cuando ejecuto el cálculo
Entonces el costo de despacho es $1.500
Y el total a pagar es $41.500

Dado una compra de $25.000
Y una distancia de 5 km
Cuando ejecuto el cálculo
Entonces el costo de despacho es $750
Y el total a pagar es $25.750

## HU-3 — Despacho $300/km (compra baja)

Como cliente
Quiero que si mi compra es menor a $25.000
Para que el despacho se calcule a $300 por km

Actores: Cliente
Prioridad: Alta

Criterios de aceptación:

Dado una compra de $20.000
Y una distancia de 8 km
Cuando ejecuto el cálculo
Entonces el costo de despacho es $2.400
Y el total a pagar es $22.400

## HU-4 — Fuera de radio (> 20 km)

Como cliente fuera del radio
Quiero saber que no hay despacho si la distancia supera los 20 km
Para evitar cálculos que no aplican

Actores: Cliente
Prioridad: Alta

Criterios de aceptación:

Dado una distancia de 25 km
Cuando ejecuto el cálculo
Entonces el sistema informa "La opción de despacho a domicilio no se encuentra disponible"
Y el programa finaliza sin calcular totales

## HU-5 — Validación de entradas negativas

Como cliente
Quiero ser notificado si ingreso valores negativos
Para corregirlos antes del cálculo

Actores: Cliente
Prioridad: Media

Criterios de aceptación:

Dado una compra de -$1.000
Y una distancia de 10 km
Cuando ejecuto el cálculo
Entonces el sistema informa "Monto de compra inválido"
Y no realiza el cálculo

Dado una compra de $30.000
Y una distancia de -3 km
Cuando ejecuto el cálculo
Entonces el sistema informa "Distancia inválida"
Y no realiza el cálculo

## HU-6 — Mensajes claros (resumen de operación)

Como cliente
Quiero ver un resumen claro del costo de despacho y total
Para entender qué estoy pagando

Actores: Cliente
Prioridad: Media

Criterios de aceptación:

Dado una compra y distancia válidas
Cuando se calcula el despacho
Entonces el sistema muestra "Costo de despacho: <monto>"
Y "Total a pagar: <monto>"

## HU-7 — Validación de correo Gmail

Como usuario que se registra
Quiero ingresar un correo @gmail.com válido
Para completar un registro básico en la app

Actores: Usuario
Prioridad: Baja (opcional para esta entrega CLI)

Criterios de aceptación:

Dado el correo "cliente@gmail.com"
Cuando valido el formato
Entonces el sistema acepta el correo

Dado el correo "cliente@outlook.com"
Cuando valido el formato
Entonces el sistema rechaza el correo
Y muestra "Debe ser una cuenta Gmail (@gmail.com)"
