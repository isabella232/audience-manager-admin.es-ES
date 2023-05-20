---
description: Cosas que debe animar a sus clientes a tener en cuenta cuando trabajan con las API de Audience Manager.
seo-description: Things you should encourage your clients to be aware of when they're working with the Audience Manager APIs.
seo-title: API Requirements and Recommendations
title: Requisitos y recomendaciones de API
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
exl-id: 24f90732-31a6-436d-862b-e6871d279c7a
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 2%

---

# Requisitos y recomendaciones de API {#api-requirements-and-recommendations}

Cosas que debe animar a sus clientes a tener en cuenta cuando trabajan con el Audience Manager [!DNL API]s.

## Requisitos {#requirements}

Tenga en cuenta lo siguiente al trabajar con [!DNL Audience Manager] [!DNL API] código:

* **Parámetros de solicitud:** Todos los parámetros de solicitud son obligatorios a menos que se especifique lo contrario.
* **[!DNL JSON]tipo de contenido:** Especificar `content-type: application/json` *y* `accept: application/json` en el código.

* **Solicitudes y respuestas:** Envío de solicitudes como una solicitud con el formato correcto [!DNL JSON] objeto. [!DNL Audience Manager] responde con [!DNL JSON] datos con formato. Las respuestas del servidor pueden contener datos solicitados, un código de estado o ambos.

* **Acceso:** Su [!DNL Audience Manager] El consultor de le proporcionará un ID de cliente y una clave que le permitirán realizar [!DNL API] solicitudes.

* **Documentación y ejemplos de código:** Texto en *cursiva* representa una variable que se proporciona o se pasa al realizar o recibir [!DNL API] datos. Reemplazar *en cursiva* texto con su propio código, parámetros u otra información necesaria.

## Recommendations: Crear un usuario de API genérico {#recommendations}

Se recomienda crear una cuenta de usuario técnica independiente para trabajar con el Audience Manager [!DNL API]s. Es una cuenta genérica que no está vinculada a un usuario específico de la organización del cliente ni asociada a él. Este tipo de [!DNL API] La cuenta de usuario de ayuda a lograr dos cosas:

* Identificar qué servicio llama al [!DNL API] (por ejemplo, llamadas de una aplicación cliente que utiliza nuestro [!DNL API]s o de realizar cambios masivos).
* Proporcionar acceso ininterrumpido al [!DNL API]s. Una cuenta vinculada a un empleado específico puede ser eliminada cuando se va de la compañía. Esto evitará que sus clientes trabajen con el disponible [!DNL API] código. Una cuenta genérica que no esté vinculada a un empleado en particular ayuda a evitar este problema.

Como ejemplo o caso de uso para este tipo de cuenta, supongamos que sus clientes desean cambiar muchos segmentos a la vez con [Herramientas de administración masiva](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/bulk-management-tools/bulk-management-intro.html?lang=en). Para ello, necesitan [!DNL API] acceso. En lugar de agregar permisos a un usuario específico, cree un de tipo no específico, [!DNL API] cuenta de usuario que tiene las credenciales, la clave y el secreto adecuados para realizar [!DNL API] llamadas. Esto también resulta útil si los clientes desarrollan sus propias aplicaciones que utilizan el [!DNL Audience Manager] [!DNL API]s.
