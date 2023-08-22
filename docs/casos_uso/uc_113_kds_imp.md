---
sidebar_position: 7
---

# Recepción De Órdenes Por Impresora De Comandas

**Caso de Uso No. 113**

## Narrativa

Con la creciente demanda de agilidad en la cocina y para asegurar que las órdenes sean recibidas incluso en casos donde el KDS digital pueda presentar fallos, se implementa una alternativa de recepción de órdenes a través de una impresora de comandas. Esto permite que la cocina reciba de manera física la orden, garantizando una preparación eficiente y puntual de los platillos.

## Casos de uso

Título del caso de uso: **RECEPCIÓN DE ÓRDENES POR IMPRESORA DE COMANDAS**

## Diagrama:

![User Case 113](/img/uc/uc_113.png)

## Definición

**Actores:** Cocina

**Descripción:** Permite al equipo de Cocina recibir órdenes de manera física a través de una impresora de comandas, como alternativa al sistema digital de KDS.

**Precondiciones:** Existencia de una orden pendiente para la cocina y correcta conexión de la impresora.

**Pos condiciones:** La orden es impresa en la comanda y lista para ser procesada por el equipo de cocina.

**Versión:** 0.0.1

**Fecha de creación:** [Fecha actual]

**Fecha de actualización:** [Fecha actual + cambios]

**Flujos**

### Flujo Básico: Recepción de Orden

| ID | Actor | ID | Sistema | Excepción o Error |
|---|:---:|---|:---:|:---:|
| 1 | Espera la recepción de nuevas órdenes. | 2 | Detecta una nueva orden y envía la información a la impresora de comandas. | E1 |
| 3 | Recibe la comanda impresa con los detalles de la orden. |  |  |  |
| 4 | Comienza la preparación de los platillos de acuerdo a la comanda. |  |  |  |

## Errores

N/A

## Excepciones

| ID | Nombre | Respuesta del sistema |
|---|---|---|
| E1 | Fallo en la impresora | Si detecta que la impresora no está funcionando correctamente o no hay conexión con ella, se mostrará una alerta en el KDS digital, indicando la necesidad de revisar la impresora. |

## Requerimientos especiales

* Conexión correcta y funcionamiento óptimo de la impresora de comandas.

## Observaciones

El sistema debe ser capaz de detectar cualquier fallo en la conexión o funcionamiento de la impresora y alertar al equipo de cocina y administrativo de manera inmediata.