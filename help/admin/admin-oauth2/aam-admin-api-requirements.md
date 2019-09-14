---
description: Cosas que debe animar a los clientes a que sepan cuándo trabajan con las API de Audience Manager.
seo-description: Cosas que debe animar a los clientes a que sepan cuándo trabajan con las API de Audience Manager.
seo-title: Requisitos de API y recomendaciones
title: Requisitos de API y recomendaciones
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# Requisitos de API y recomendaciones {#api-requirements-and-recommendations}

Cosas que debe animar a los clientes a que sepan cuándo trabajan con Audience Manager [!DNL API]s.

## Requisitos {#requirements}

Tenga en cuenta lo siguiente al trabajar con [!DNL Audience Manager] código [!DNL API] :

* **** Parámetros de solicitud: Todos los parámetros de solicitud son obligatorios a menos que se especifique lo contrario.
* **[!DNL JSON]** tipo de contenido: Especifique `content-type: application/json` y ** `accept: application/json` en el código.

* **** Solicitudes y respuestas: Enviar solicitudes como un [!DNL JSON] objeto con el formato correcto. [!DNL Audience Manager] responde con datos con [!DNL JSON] formato. Las respuestas del servidor pueden contener datos solicitados, un código de estado o ambos.

* **** Acceso: Su [!DNL Audience Manager] asesor le proporcionará un ID de cliente y una clave que le permitirá realizar [!DNL API] solicitudes.

* **** Ejemplos de documentación y código: El texto en *cursiva* representa una variable que se proporciona o pasa al crear o recibir [!DNL API] datos. Reemplace el texto *en cursiva* con su propio código, parámetros u otra información requerida.

## Recomendaciones: Creación de un usuario de API genérico {#recommendations}

Se recomienda crear una cuenta de usuario técnica independiente para trabajar con Audience Manager [!DNL API]s. Es una cuenta genérica que no está vinculada a un usuario específico de la organización del cliente ni asociada a él. Este tipo de cuenta de [!DNL API] usuario ayuda a realizar dos tareas:

* Identifique qué servicio llama a la [!DNL API] (por ejemplo, llamadas desde una aplicación cliente que usa nuestras [!DNL API]llamadas o para realizar cambios masivos).
* Proporcionar acceso ininterrumpido a los [!DNL API]informes. Una cuenta vinculada a un empleado específico puede eliminarse cuando abandone la empresa. Esto impedirá que sus clientes trabajen con el [!DNL API] código disponible. Una cuenta genérica que no está vinculada a un empleado en particular ayuda a evitar este problema.

Como ejemplo o caso de uso para este tipo de cuenta, digamos que sus clientes desean cambiar muchos segmentos a la vez con las Herramientas [de administración](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/bult-management-tools/bulk-management-intro.html)masiva. Para hacerlo, necesitan [!DNL API] acceso. En lugar de agregar permisos a un usuario específico, cree una cuenta de usuario no específica que tenga las credenciales, la clave y el secreto adecuados para realizar [!DNL API] [!DNL API] llamadas. Esto también es útil si el cliente desarrolla sus propias aplicaciones que utilizan [!DNL Audience Manager] [!DNL API]s.
