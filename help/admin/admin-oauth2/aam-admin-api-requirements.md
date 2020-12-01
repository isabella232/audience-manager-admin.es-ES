---
description: Cosas que debe animar a sus clientes a que sepan cuándo trabajan con las API de Audience Manager.
seo-description: Cosas que debe animar a sus clientes a que sepan cuándo trabajan con las API de Audience Manager.
seo-title: Requisitos y recomendaciones de API
title: Requisitos y recomendaciones de API
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 3%

---


# Requisitos y recomendaciones de API {#api-requirements-and-recommendations}

Cosas que debe animar a sus clientes a que sepan cuando están trabajando con el Audience Manager [!DNL API]s.

## Requisitos {#requirements}

Tenga en cuenta lo siguiente al trabajar con el código [!DNL Audience Manager] [!DNL API]:

* **Parámetros de solicitud:** Todos los parámetros de solicitud son obligatorios a menos que se especifique lo contrario.
* **[!DNL JSON]tipo de contenido:** especifique  `content-type: application/json` ** `accept: application/json` y el código.

* **Solicitudes y respuestas:** Enviar solicitudes como  [!DNL JSON] objeto con el formato correcto. [!DNL Audience Manager] responde con datos  [!DNL JSON] formateados. Las respuestas del servidor pueden contener datos solicitados, un código de estado o ambos.

* **Acceso:** Su  [!DNL Audience Manager] asesor le proporcionará un ID de cliente y una clave que le permitirá realizar  [!DNL API] solicitudes.

* **Muestras de documentación y código:** El texto en  ** cursiva representa una variable que se proporciona o pasa al crear o recibir  [!DNL API] datos. Reemplace el texto *en cursiva* por su propio código, parámetros u otra información requerida.

## Recommendations: Crear un usuario de API genérica {#recommendations}

Se recomienda crear una cuenta de usuario técnica independiente para trabajar con el Audience Manager [!DNL API]s. Es una cuenta genérica que no está vinculada a un usuario específico de la organización del cliente ni asociada a él. Este tipo de cuenta de usuario [!DNL API] ayuda a lograr dos cosas:

* Identifique qué servicio llama a [!DNL API] (por ejemplo: llamadas desde una aplicación cliente que usa nuestro [!DNL API]s o de realizar cambios masivos).
* Proporcione acceso ininterrumpido a [!DNL API]s. Una cuenta vinculada a un empleado específico puede ser eliminada cuando deja la compañía. Esto impedirá que sus clientes trabajen con el código [!DNL API] disponible. Una cuenta genérica que no está vinculada a un empleado en particular ayuda a evitar este problema.

Como ejemplo o caso de uso para este tipo de cuenta, digamos que sus clientes desean cambiar muchos segmentos a la vez con las [Herramientas de administración masiva](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/bult-management-tools/bulk-management-intro.html). Para ello, necesitan [!DNL API] acceso. En lugar de agregar permisos a un usuario específico, cree una cuenta de usuario [!DNL API] no específica que tenga las credenciales, la clave y el secreto adecuados para realizar [!DNL API] llamadas. Esto también es útil si el cliente desarrolla sus propias aplicaciones que utilizan [!DNL Audience Manager] [!DNL API]s.
