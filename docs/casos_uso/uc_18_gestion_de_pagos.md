---
sidebar_position: 6
---


# Gestión de Pagos

**Caso de Uso No. 18**

## Narrativa

Para que el proceso de pago en el restaurante sea eficiente y transparente, es vital que el cajero tenga herramientas adecuadas para gestionar los pagos de los clientes. El sistema debería permitir al cajero procesar pagos, dar cambio, aplicar descuentos si es necesario y emitir recibos detallados.

## Casos de uso

Título del caso de uso: **GESTIÓN DE PAGOS**

## Diagrama:

![User Case 18](/img/uc/uc_18.png)

## Definición

**Actores:**  Cajero

**Descripción:** Permite al Cajero gestionar el cobro a los clientes, incluyendo procesar pagos, dar cambio, aplicar descuentos y emitir recibos.

**Precondiciones:** Haber ingresado al sistema con la cuenta de Cajero. El cliente debe tener una orden pendiente de pago.

**Pos condiciones:** Orden pagada y cliente recibe su recibo detallado.

**Versión:** 0.0.1

**Fecha de creación:** [Fecha actual]

**Fecha de actualización:** [Fecha actual + cambios]

**Flujos**

### Flujo Básico: Procesar Pago

| ID | Actor | ID | Sistema | Excepción o Error |
|---|:---:|---|:---:|:---:|
| 1 | Selecciona la orden pendiente de pago. | 2 | Muestra el detalle de la orden incluyendo el total a pagar. |  |
| 3 | Ingresa la cantidad recibida por el cliente. | 4 | Calcula el cambio a devolver. | R1 |
| 5 | Confirma el pago. | 6 | Marca la orden como pagada y emite un recibo. |  |

### Flujo Básico: Aplicar Descuento

| ID | Actor | ID | Sistema | Excepción o Error |
|---|:---:|---|:---:|:---:|
| 1 | Selecciona la opción de aplicar descuento a la orden. | 2 | Muestra las opciones de descuentos disponibles. |  |
| 3 | Elige el descuento a aplicar. | 4 | Aplica el descuento y muestra el nuevo total. | R2 |
| 5 | Confirma el nuevo total. | 6 | Actualiza el total de la orden con el descuento. |  |

## Errores

| ID | Nombre | Respuesta del sistema |
|---|---|---|
| R1 | Cantidad insuficiente | Si la cantidad ingresada es menor al total a pagar, se muestra un mensaje indicando que la cantidad es insuficiente. |
| R2 | Descuento no aplicable | Si el descuento seleccionado no es aplicable a la orden actual (por ejemplo, descuento solo para ciertos platillos y no están en la orden), se muestra un mensaje de error. |

## Excepciones

| ID | Nombre | Respuesta del sistema |
|---|---|---|
| E1 | Sin conexión a la base de datos | Si no hay conexión con la base de datos, se muestra un mensaje de error y se impide realizar la operación. |
| E2 | Impresora de recibos no disponible | Si no es posible imprimir el recibo debido a un problema con la impresora, se muestra un mensaje indicando el problema. |

## Requerimientos especiales

* Conexión a la base de datos.
* Impresora de recibos conectada y en funcionamiento.

## Observaciones

* En caso de aplicar un descuento, es importante que el recibo detalle qué descuento fue aplicado y la razón del mismo.