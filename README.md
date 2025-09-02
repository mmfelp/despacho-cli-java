# Despacho a domicilio (CLI en Java)

## Requerimientos Funcionales (RF)

RF-01 – Ingreso de monto de compra:
El sistema permite ingresar el monto de compra en pesos (entero ≥ 0).

RF-02 – Ingreso de distancia:
El sistema permite ingresar la distancia en kilómetros (entero ≥ 0).

RF-03 – Validación de radio máximo:
Si km > 20, el sistema informa que el despacho no está disponible y termina el proceso sin cálculos.

RF-04 – Cálculo de costo de despacho (compra alta):
Si valor > 50000 y km ≤ 20 ⇒ costo de despacho = $0.

RF-05 – Cálculo de costo de despacho (compra media):
Si 25000 ≤ valor ≤ 50000 y km ≤ 20 ⇒ costo de despacho = 150 × km.
(Nota: aquí se incluye $50.000 exactos.)

RF-06 – Cálculo de costo de despacho (compra baja):
Si valor < 25000 y km ≤ 20 ⇒ costo de despacho = 300 × km.

RF-07 – Total a pagar:
El sistema calcula total = valor + costoDespacho.

RF-08 – Mensajes de resultado:
El sistema muestra costo de despacho y total a pagar en todos los casos aplicables.

RF-09 – Validación de correo Gmail:
Si se solicita registro, el sistema valida formato @gmail.com (sin persistencia en esta versión CLI).


## Estructura del proyecto
```text
despacho-cli-java/
├─ src/
│  └─ Main.java
├─ bin/                
├─ docs/
│  ├─ proceso.md
│  ├─ linea-por-linea.md
│  ├─ historias-usuario.md
│  └─ cronograma.md
├─ README.md
└─ .gitignore
```
## Historiias de Usuario 
https://github.com/mmfelp/despacho-cli-java/blob/main/docs/historias-usuario.md

## Compilación (CLI)
```bash
javac -d bin src/Main.java
```

## Ejecución (CLI)
```bash
java -cp bin Main
```

## Evidencias
Ver `docs/proceso.md`.
