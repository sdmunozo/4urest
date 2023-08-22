---
sidebar_position: 1
---

# Gestión de Perfil

 **Caso de Uso No. 1**

## Narrativa

El sistema necesita permitir a los administradores gestionar los perfiles de los usuarios. Esto incluye agregar nuevos perfiles, modificar la información de perfiles existentes, eliminar perfiles y consultar la lista e información detallada de los perfiles.

## Casos de uso

Título del caso de uso: **GESTIÓN DE PERFILES**

## Diagrama

![User Case Perfil](/img/uc/uc_perfil.png)

## Definición

**Actores:** Admin

**Descripción:** Permite al Admin del sistema realizar la gestión completa de los datos de los perfiles, que incluye agregar nuevos perfiles, modificar información de perfiles existentes, eliminar perfiles y consultar la lista e información detallada de los perfiles.

**Precondiciones:** Haber ingresado al sistema con la cuenta de Admin. Ubicarse en Menú Principal/Perfiles.

**Pos condiciones:** Datos de algún perfil modificados o un perfil agregado/eliminado.

**Versión:** 0.0.1

**Fecha de creación:** [Fecha actual]

**Fecha de actualización:** [Fecha actual + cambios]

## Flujos

### Flujo Básico: Agregar Perfil

| ID | Actor | ID | Sistema | Excepción o Error |
|---|:---:|---|:---:|:---:|
| 1 | En "Perfiles", selecciona la opción de agregar perfil. | 2 | Muestra el formulario para agregar un nuevo perfil. |  |
| 3 | Ingresa la información del nuevo perfil y presiona "Guardar". | 4 | Valida la información y añade el perfil al menú. | R1 R2 E1 |
|  | | 5 | Muestra mensaje de "Perfil añadido con éxito". |  |

### Flujo Básico: Modificar Perfil

| ID | Actor | ID | Sistema | Excepción o Error |
|---|:---:|---|:---:|:---:|
| 1 | En "Perfiles", selecciona un perfil. | 2 | Muestra los datos del perfil en el formulario. |  |
| 3 | Modifica los datos del perfil y presiona "Guardar". | 4 | Valida la información y modifica el perfil en el menú. | R1 R2 E1 |
|  | | 5 | Muestra mensaje de "Perfil modificado con éxito". |  |

### Flujo Básico: Eliminar Perfil

| ID | Actor | ID | Sistema | Excepción o Error |
|---|:---:|---|:---:|:---:|
| 1 | En "Perfiles", selecciona el perfil que desea eliminar.  | 2 | Muestra los datos del perfil en el formulario. |  |
| 3 | Presiona "Eliminar". | 4 | Solicita confirmación para eliminar. |  |
| 5 | Confirma eliminación. | 6 | Elimina (soft delete) el perfil seleccionado de la base de datos. | E1 |
| | | 7 | Muestra mensaje de "Perfil eliminado con éxito". |  |

## Errores

| ID | Nombre | Respuesta del sistema |
|---|---|---|
| R1 | Campos vacíos | Si no se completan todos los campos requeridos, se muestra un mensaje indicando que es necesario llenarlos. |
| R2 | Datos inválidos | Si se ingresan datos que no corresponden al tipo esperado (por ejemplo, letras en un campo numérico), se mostrará un mensaje de error. |

## Excepciones

| ID | Nombre | Respuesta del sistema |
|---|---|---|
| E1 | Sin conexión a la base de datos | Si no hay conexión con la base de datos, se muestra un mensaje de error y se impide realizar la operación. |

## Requerimientos especiales

* Conexión a la base de datos.

## Observaciones

N/A

## Entidades

### B_Perfil

| Columna       | Tipo de dato | Descripción           |
|---------------|--------------|-----------------------|
| id            | smallint     | Clave primaria        |
| nombre        | nvarchar(20) | Nombre de perfil      |

## Diagrama EBC

![User Case Perfil](../../EBC/EBC_Gestion_De_Perfil.png)
