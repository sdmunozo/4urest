---
sidebar_position: 4
---


# Analizar Reportes y Métricas

**Caso de Uso No. 3**

## Narrativa

Para mantener el restaurante funcionando de manera eficiente y garantizar un buen rendimiento financiero, el administrador necesita acceso a reportes detallados y métricas relevantes del negocio. Estos reportes permitirán al administrador obtener una visión clara de las ventas, ingresos, propinas, productos más vendidos, feedback de clientes y otros indicadores clave.

## Casos de uso

Título del caso de uso: **ANALIZAR REPORTES Y MÉTRICAS**

## Diagrama:

![User Case 3](/img/uc/uc_3.png)

## Definición

**Actores:**  Admin

**Descripción:** El Admin tiene la capacidad de acceder a reportes detallados y métricas relevantes para evaluar el desempeño del restaurante en distintas áreas.

**Precondiciones:** Haber ingresado al sistema con la cuenta de Admin. El sistema debe mostrar el menú con las opciones para el perfil administrador.

**Pos condiciones:** Admin obtiene la información detallada y métricas de interés.

**Versión:** 0.0.1

**Fecha de creación:** [Fecha actual]

**Fecha de actualización:** [Fecha actual + cambios]

## Flujos

### Flujo Básico: Acceder a Reporte de Ventas

| ID | Actor | ID | Sistema | Excepción o Error |
|---|:---:|---|:---:|:---:|
| 1 | Selecciona la opción de "Reporte de Ventas". | 2 | Muestra el reporte detallado de ventas por periodo. | E1 |
| 3 | Puede filtrar por fechas o productos específicos. | 4 | Actualiza el reporte según los filtros seleccionados. | E1 |

### Flujo Básico: Consultar Productos Más Vendidos

| ID | Actor | ID | Sistema | Excepción o Error |
|---|:---:|---|:---:|:---:|
| 1 | Selecciona la opción de "Productos Más Vendidos". | 2 | Muestra una lista de los productos más vendidos con sus cantidades. | E1 |

### Flujo Básico: Analizar Feedback de Clientes

| ID | Actor | ID | Sistema | Excepción o Error |
|---|:---:|---|:---:|:---:|
| 1 | Selecciona la opción de "Feedback de Clientes". | 2 | Muestra los comentarios y valoraciones de los clientes. | E1 |
| 3 | Puede responder o tomar acciones basadas en el feedback. | 4 | Registra las acciones tomadas por el Admin. | E1 |

## Errores

N/A

## Excepciones

| ID | Nombre | Respuesta del sistema |
|---|---|---|
| E1 | Sin conexión a la base de datos | Si no hay conexión con la base de datos, se muestra un mensaje de error y se impide realizar la operación. |

## Requerimientos especiales

* Conexión a la base de datos.
* Gráficos interactivos para mejor visualización (opcional).

## Observaciones

N/A