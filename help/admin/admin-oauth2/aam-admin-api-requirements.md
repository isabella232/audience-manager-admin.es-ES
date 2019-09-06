---
description: Cosas que debe alentar a sus clientes a saber cuándo funcionan con las API de Audience Manager.
seo-description: Cosas que debe alentar a sus clientes a saber cuándo funcionan con las API de Audience Manager.
seo-title: Requisitos de API y Recomendaciones
title: Requisitos de API y Recomendaciones
uuid: eba 9 cf 92-f 0 c 8-4394-8532-0 de 9 a 2 e 7 b 103
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# Requisitos de API y Recomendaciones {#api-requirements-and-recommendations}

Cosas que debe alentar a sus clientes a saber cuándo funcionan con Audience Manager [!DNL API]s.

## Requisitos {#requirements}

Tenga en cuenta lo siguiente cuando trabaje con [!DNL Audience Manager][!DNL API] código:

* **Parámetros de solicitud:** Se requieren todos los parámetros de solicitud a menos que se especifique lo contrario.
* **[!DNL JSON]tipo de contenido:** Especifique `content-type: application/json`*y* `accept: application/json` en su código.

* **Solicitudes y respuestas:** Envíe solicitudes como objeto formateado [!DNL JSON] correctamente. [!DNL Audience Manager] responde con [!DNL JSON] datos formateados. Las respuestas del servidor pueden contener los datos solicitados, un código de estado o ambos.

* **Acceso:** [!DNL Audience Manager] Su consultor le proporcionará un ID de cliente y una clave que le permitirán [!DNL API] realizar solicitudes.

* **Documentación y muestras de código:** El texto en *cursiva* representa una variable que usted proporciona o pasa al realizar o recibir [!DNL API] datos. Sustituya *texto en cursiva* por su propio código, parámetros u otra información requerida.

## Recomendaciones: Crear un usuario de API genérica {#recommendations}

Se recomienda crear una cuenta de usuario técnica independiente para trabajar con Audience Manager [!DNL API]s. Cuenta genérica que no está asociada a un usuario específico de la organización del cliente ni asociado con él. Este tipo de [!DNL API] cuenta de usuario ayuda a llevar a cabo dos tareas:

* Identifique qué servicio llama a ( [!DNL API] por ejemplo, llamadas desde una aplicación cliente que utiliza nuestras [!DNL API]s o desde realizar cambios masivos).
* Proporcione acceso ininterrumpido a las [!DNL API]s. Una cuenta vinculada a un empleado específico puede eliminarse cuando abandonan la empresa. Esto evitará que sus clientes trabajen con [!DNL API] el código disponible. Una cuenta genérica que no está vinculada a un empleado en particular ayuda a evitar este problema.

Como ejemplo o caso de uso para este tipo de cuenta, supongamos que sus clientes quieren cambiar muchos segmentos a la vez con las herramientas de administración [masiva](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/bult-management-tools/bulk-management-intro.html). Para ello, necesitan [!DNL API] acceso. En lugar de agregar permisos a un usuario específico, cree una cuenta [!DNL API] de usuario no específica que tenga las credenciales, clave y secreto adecuados para [!DNL API] realizar llamadas. Esto también resulta útil si el cliente desarrolla sus propias aplicaciones que utilizan las [!DNL Audience Manager][!DNL API]s.
