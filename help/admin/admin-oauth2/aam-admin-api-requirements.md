---
description: Cosas que debe animar a sus clientes a que sepan cuándo trabajan con las API de Audience Manager.
seo-description: Things you should encourage your clients to be aware of when they're working with the Audience Manager APIs.
seo-title: API Requirements and Recommendations
title: Requisitos y recomendaciones de API
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
exl-id: 24f90732-31a6-436d-862b-e6871d279c7a
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 2%

---

# Requisitos y recomendaciones de API {#api-requirements-and-recommendations}

Cosas que debe animar a sus clientes a tener en cuenta cuando estén trabajando con el Audience Manager [!DNL API]s.

## Requisitos {#requirements}

Tenga en cuenta lo siguiente al trabajar con código [!DNL Audience Manager] [!DNL API]:

* **Parámetros de solicitud:**  Todos los parámetros de solicitud son obligatorios a menos que se especifique lo contrario.
* **[!DNL JSON]tipo de contenido:** especifique  `content-type: application/json` ** `accept: application/json` y en su código.

* **Solicitudes y respuestas:** envíe solicitudes como  [!DNL JSON] objeto con el formato correcto. [!DNL Audience Manager] responde con datos  [!DNL JSON] formateados. Las respuestas del servidor pueden contener datos solicitados, un código de estado o ambos.

* **Acceso:** el  [!DNL Audience Manager] consultor le proporcionará un ID de cliente y una clave que le permitirán realizar  [!DNL API] solicitudes.

* **Ejemplos de documentación y código:** el texto en  ** cursiva representa una variable que se proporciona o pasa al crear o recibir  [!DNL API] datos. Reemplace el texto *cursiva* con su propio código, parámetros u otra información requerida.

## Recommendations: Crear un usuario de API genérico {#recommendations}

Se recomienda crear una cuenta de usuario técnica independiente para trabajar con el Audience Manager [!DNL API]s. Se trata de una cuenta genérica que no está vinculada a un usuario específico de la organización del cliente ni asociada a él. Este tipo de cuenta de usuario [!DNL API] ayuda a lograr dos cosas:

* Identifique qué servicio llama a [!DNL API] (por ejemplo, llamadas de una aplicación cliente que usa nuestro [!DNL API]s o de realizar cambios masivos).
* Proporcione acceso ininterrumpido a [!DNL API]s. Una cuenta vinculada a un empleado específico puede ser eliminada cuando abandone la empresa. Esto impedirá que sus clientes trabajen con el código [!DNL API] disponible. Una cuenta genérica que no está ligada a un empleado en particular ayuda a evitar este problema.

Como ejemplo o caso de uso para este tipo de cuenta, supongamos que sus clientes desean cambiar muchos segmentos a la vez con las [herramientas de administración masiva](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/bult-management-tools/bulk-management-intro.html). Para ello, necesitan [!DNL API] acceso. En lugar de agregar permisos a un usuario específico, cree una cuenta de usuario [!DNL API] no específica que tenga las credenciales, la clave y el secreto adecuados para realizar llamadas [!DNL API]. Esto también resulta útil si el cliente desarrolla sus propias aplicaciones que utilizan [!DNL Audience Manager] [!DNL API]s.
