# 🚀 Sideproject — Estado de cuenta

**Repositorio:** `sideproject-estado-de-cuenta` · **Tipo:** ETL en Python puro · **Tiempo:** 3–4 h · **Después de:** los dos grandes integradores de este módulo

> Reglas, README y lista de cierre: [`SIDEPROJECTS.md`](docs/REGLAS.md). **No hay solución: el diseño es tuyo.**

## El caso

Un amigo te pasa los movimientos de su tarjeta en un CSV y te pide saber en qué se le va el dinero. Todavía no hay pandas ni funciones avanzadas: solo listas, tuplas, diccionarios, sets y bucles. Es tu primer ETL: **extraer** del archivo, **transformar** a un resumen y **cargar** a un reporte.

Datos: `datos/movimientos.csv` (léelo con `csv.DictReader`).

## Qué practicas

| Tema | Dónde aparece |
|---|---|
| Listas y tuplas | Los movimientos y los pares (categoría, total) ordenados |
| Diccionarios | Acumular por cuenta y por categoría |
| Sets | Comercios distintos, cuentas sin depósitos |
| Condicionales y bucles | Filtrar, clasificar y recorrer |

## Hitos

**Hito 1 — Leer.** Carga el CSV en una lista de diccionarios y convierte `monto` a número.
*Comprueba:* 400 movimientos; el primero tiene un `monto` de tipo `float`.

**Hito 2 — Totales.** Total y número de movimientos por `tipo`.
*Comprueba:* la suma de los cuatro conteos es 400.

**Hito 3 — En qué se va el dinero.** Las 3 categorías con más gasto, de mayor a menor (solo compras).
*Comprueba:* compruébalo a mano con una hoja de cálculo.

**Hito 4 — Por cuenta.** Para cada cuenta: movimientos, gasto total, compra más grande y comercios distintos.
*Comprueba:* elige una cuenta y verifica sus cuatro números a mano.

**Hito 5 — Reporte.** Escribe el resultado en `reporte.txt`, alineado y legible.
*Comprueba:* tu amigo lo entendería sin que se lo expliques.

## Preguntas para defenderlo

- ¿Por qué un diccionario y no una lista para acumular por cuenta?
- ¿Dónde usaste un set y qué habrías tenido que escribir sin él?
- ¿Qué pasa en tu programa con la `categoria` de un depósito?

## Súbelo de nivel

- El mes con más gasto y la diferencia contra el mes anterior.
- Cuando termines `02_funciones_y_poo`, vuelve y repártelo en funciones.
