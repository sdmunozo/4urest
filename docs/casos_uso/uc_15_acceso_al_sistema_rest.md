---
sidebar_position: 6
---

# Acceso al Sistema Rest

**Caso de Uso No. 15**

## Narrativa

El cajero del restaurante necesita ingresar al sistema de gestión Rest para realizar sus operaciones diarias. Esta funcionalidad garantiza que solo los cajeros autorizados tengan acceso a las funciones pertinentes a su rol y, en caso de intentos repetidos de acceso no autorizado, se bloquee el usuario temporalmente.

## Casos de uso

Título del caso de uso: **ACCESO AL SISTEMA REST**

## Diagrama:

![User Case 15](/img/uc/uc_15.png)

## Definición

**Actores:**  Cajero

**Descripción:** Permite al Cajero del restaurante acceder al sistema Rest para gestionar sus tareas diarias, asegurando que solo los cajeros autorizados tengan acceso y bloqueando usuarios tras intentos fallidos.

**Precondiciones:** Tener unas credenciales válidas de cajero.

**Pos condiciones:** Cajero accede al sistema o usuario bloqueado por intentos fallidos.

**Versión:** 0.0.1

**Fecha de creación:** [Fecha actual]

**Fecha de actualización:** [Fecha actual + cambios]

**Flujos**

### Flujo Básico: Apertura de sesión

| ID | Actor | ID | Sistema | Excepción o Error |
|---|:---:|---|:---:|:---:|
| 1 | Ingresa nombre de usuario y contraseña. | 2 | Valida las credenciales. | R1 R2 |
| 3 | Accede al sistema. | 4 | Muestra el dashboard o interfaz principal para el Cajero. |  |

### Flujo Básico: Bloqueo de usuario

| ID | Actor | ID | Sistema | Excepción o Error |
|---|:---:|---|:---:|:---:|
| 1 | Ingresa de forma errónea las credenciales repetidas veces. | 2 | Registra los intentos fallidos. |  |
| 3 |  | 4 | Luego de un límite de intentos, bloquea temporalmente al usuario e informa del bloqueo. | R3 |

## Errores

| ID | Nombre | Respuesta del sistema |
|---|---|---|
| R1 | Credenciales incorrectas | Si el nombre de usuario o la contraseña son incorrectos, se muestra un mensaje indicando que las credenciales son inválidas. |
| R2 | Usuario no registrado | Si el usuario ingresado no existe en la base de datos, se mostrará un mensaje indicando que no está registrado. |
| R3 | Límite de intentos superado | Si se supera el límite de intentos de acceso, el sistema bloquea al usuario temporalmente y muestra un mensaje de bloqueo. |

## Excepciones

| ID | Nombre | Respuesta del sistema |
|---|---|---|
| E1 | Sin conexión a la base de datos | Si no hay conexión con la base de datos, se muestra un mensaje de error y se impide el acceso. |

## Requerimientos especiales

* Conexión a la base de datos para validar credenciales.
* Funcionalidad de límite de intentos y bloqueo.

## Observaciones

* Se recomienda a los cajeros no compartir sus credenciales y cambiar la contraseña con regularidad.