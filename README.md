# Calculadora JAK · Simulador ARESI

Aplicación web estática para simular la devolución de una ARESI, mes a mes, combinando:

- devolución económica (€)
- generación de puntos
- puntos iniciales donados/ahorrados

La herramienta calcula automáticamente el tiempo estimado total, separando:

- meses para devolver el préstamo económico
- meses para generar el ahorro de puntos necesario

## Características

- Simulación mensual detallada en tabla
- Cálculo automático de saldo, pago acumulado y puntos
- Edición rápida del pago mensual por mes
- Propagación gradual de cambios de pago desde un mes concreto
- Estado persistente en `localStorage`
- Enlace compartible con estado codificado en la URL (`?d=...`)
- Reset rápido con `?d=reset`
- Interfaz responsive con Bootstrap 5

## Tecnologías

- HTML5
- Vue 3 (CDN, build `prod` global)
- Bootstrap 5 + Bootstrap Icons (CDN)
- JavaScript vanilla

## Estructura del proyecto

```text
calculadora-jak/
├─ index.html      # Aplicación completa (UI + lógica)
└─ README.md
```

## Uso

La calculadora está publicada en GitHub Pages y se puede usar directamente aquí:

- https://adelafoofur82.github.io/calculadora-jak/

## Cómo usar la calculadora

1. Introduce el dinero prestado (€).
2. Define la entrega mensual (€). Aquí te calcula pensando en lo que puedes aportar cada mes, incluyendo tanto la devolución de deuda como la aportación como ahorro.
3. Añade puntos iniciales (si los hay).
4. Ajusta pagos mensuales en la tabla si necesitas escenarios no lineales.
5. Copia el enlace para compartir exactamente la misma simulación.

## Persistencia y compartición

- El estado se guarda automáticamente en `localStorage` con la clave:
  - `calculadora_jak_estado_v1`
- El enlace compartible usa un payload codificado (base64 URL-safe) en `?d=`.
- Si se abre con `?d=reset`, se limpia el estado guardado.