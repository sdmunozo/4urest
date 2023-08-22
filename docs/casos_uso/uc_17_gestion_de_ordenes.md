---
sidebar_position: 6
---

# Gestión de Ordenes

**Caso de Uso No. 17**

## Narrativa

Con el objetivo de ofrecer un servicio eficiente en el restaurante, el sistema debe permitir al cajero manejar las ordenes de los clientes. Este manejo involucra la creación de una orden, asignación de clientes, gestión de comandas con sus respectivos modificadores, cambios de mesas y meseros, así como la aplicación de cancelaciones y descuentos según sea necesario.

## Casos de uso

Título del caso de uso: **GESTIÓN DE ORDENES**

## Diagrama:

![User Case 17](/img/uc/uc_17.png)

## Definición

**Actores:**  Cajero

**Descripción:** Permite al cajero del restaurante manejar eficientemente todas las operaciones relacionadas con las órdenes de los clientes desde su creación hasta su cierre.

**Precondiciones:** Haber ingresado al sistema con la cuenta de Cajero. El sistema debe mostrar el menú con las opciones para el perfil cajero.

**Pos condiciones:** La orden es gestionada correctamente según las necesidades presentadas durante la atención al cliente.

**Versión:** 0.0.1

**Fecha de creación:** [Fecha actual]

**Fecha de actualización:** [Fecha actual + cambios]

**Flujos**

### Flujo Básico: Crear una orden

| ID | Actor | ID | Sistema | Excepción o Error |
|---|:---:|---|:---:|:---:|
| 1 | Selecciona la opción de crear nueva orden. | 2 | Muestra el formulario para crear una orden. |  |
| 3 | Llena los campos necesarios y selecciona los platillos/detalles. | 4 | Valida la información y registra la nueva orden en el sistema. | R1 R2 |

### Flujo Básico: Cambio de mesa

| ID | Actor | ID | Sistema | Excepción o Error |
|---|:---:|---|:---:|:---:|
| 1 | Selecciona la orden a cambiar de mesa. | 2 | Muestra las mesas disponibles. | E1 |
| 3 | Selecciona la nueva mesa. | 4 | Actualiza la ubicación de la orden en el sistema. |  |

### Flujo Básico: Aplicar descuentos

| ID | Actor | ID | Sistema | Excepción o Error |
|---|:---:|---|:---:|:---:|
| 1 | Selecciona la orden a la que quiere aplicar un descuento. | 2 | Muestra las opciones de descuento disponibles. | E2 |
| 3 | Selecciona el descuento a aplicar y confirma. | 4 | Aplica el descuento y actualiza el total de la orden. |  |

## Errores

| ID | Nombre | Respuesta del sistema |
|---|---|---|
| R1 | Orden vacía | Si no se selecciona ningún platillo o detalle, se muestra un mensaje indicando que la orden no puede estar vacía. |
| R2 | Datos inválidos | Si se ingresan datos que no corresponden al tipo esperado, se mostrará un mensaje de error. |

## Excepciones

| ID | Nombre | Respuesta del sistema |
|---|---|---|
| E1 | Sin mesas disponibles | Si todas las mesas están ocupadas, se muestra un mensaje indicando que no hay mesas disponibles. |
| E2 | Descuentos no disponibles | Si no hay descuentos disponibles o no aplicables a la orden, se muestra un mensaje de error. |

## Requerimientos especiales

* Acceso a la base de datos actualizada del menú y de las mesas disponibles.

## Observaciones

N/A