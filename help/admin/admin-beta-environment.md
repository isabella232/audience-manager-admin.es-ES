---
description: El entorno beta sirve para probar implementaciones de Audience Manager. Los cambios realizados en la versión beta no afectan a los datos de producción. El entorno beta de Audience Manager es una versión independiente a menor escala del entorno de producción. Todos los datos que desee probar deben introducirse y recopilarse en este entorno.
seo-description: The beta environment is for testing Audience Manager implementations. Changes made in beta do not affect production data. The Audience Manager beta environment is a smaller-scale, standalone version of the production environment. All the data that you want to test must be entered and collected in this environment.
seo-title: Beta Environment
solution: Audience Manager
title: Entorno beta
uuid: 6a253f4e-96e7-4395-a783-a8eb213b7daf
exl-id: 78d5a1ff-c016-4366-ba34-9814a0d92067
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 3%

---

# Entorno beta {#beta-environment}

El entorno beta sirve para probar implementaciones de Audience Manager. Los cambios realizados en la versión beta no afectan a los datos de producción. El entorno beta de Audience Manager es una versión independiente a menor escala del entorno de producción. Todos los datos que desee probar deben introducirse y recopilarse en este entorno.

## Información general {#overview}

<!-- beta_environment_admin.xml -->

| Servicio | URL/Nombre de host | Pasos para aprovisionar |
|--- |--- |--- |
| S3 |  | Consulte [Aprovisionar bloques de Amazon S3](admin-beta-environment.md#provision-s3-buckets). |
| DCS | https&amp;colon;//dcs-beta.demdex.net/... | No se necesitan pasos adicionales de nuestro lado. Consulte [Acceso al DCS en el entorno beta](admin-beta-environment.md#access-dcs-beta-environment). |
| IU | https&amp;colon;//bank-beta.demdex.com | Los datos se copian mensualmente de la producción al entorno beta. Las credenciales de producción son válidas para la versión beta. |
| API | https&amp;colon;//api-beta.demdex.com/... | Los datos se copian mensualmente de la producción al entorno beta. Las credenciales de producción son válidas para la versión beta. |

## Aprovisionar bloques de Amazon S3 {#provision-s3-buckets}

>[!NOTE]
>
>Nos estamos alejando del uso de [!DNL FTP/SFTP]. Además, tenga en cuenta que las transferencias de datos salientes no funcionan para el entorno beta.

Para aprovisionar [!DNL S3] depósitos para datos entrantes:

1. Utilice el [**SKMS Solicitar ayuda de TechOps**](https://skms.adobe.com/) función.
1. Ir a **[!UICONTROL Request TechOps Help]** en el carril de navegación izquierdo.
1. Entrada **[!UICONTROL Request Search]**, escriba Audience Manager en el campo de búsqueda.
1. Desplácese hacia abajo en los resultados de búsqueda y haga clic en **Audience Manager - Aprovisionamiento de cuentas entrantes/salientes de S3**.
1. Rellene los campos de la ventana de aprovisionamiento y especifique **Entorno de zona protegida** en el **[!UICONTROL Environment]** field.

>[!NOTE]
>
>Desalentamos el uso de [!DNL FTP/SFTP] y fomentar el uso de [!UICONTROL Amazon S3]. Las razones por las que fomentamos el uso de [!UICONTROL Amazon S3] se enumeran en [Amazon S3:Acerca de](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html).

## Acceso al DCS en el entorno beta {#access-dcs-beta-environment}

Para acceder a [!UICONTROL DCS] en el entorno beta:

1. Crear un [!UICONTROL DCS] llamada a, utilizando [!DNL curl] [mando](https://curl.haxx.se/docs/manpage.html). [!DNL Curl] es una herramienta para transferir datos desde o hacia un servidor mediante uno de los muchos protocolos admitidos.

   Por ejemplo: `curl -v https://dcs-beta.demdex.net/event`

1. Compruebe que la solicitud fue atendida por la versión beta [!UICONTROL DCS] buscando &quot;&quot;.[!DNL sandbox]&quot; en el [!UICONTROL DCS] encabezado de respuesta.

   Por ejemplo:

   ```
   curl -v http://dcs-beta.demdex.net/?event
   [...]
   < DCS: va6-sandbox-dcs-3.sandbox.demdex.com <release_number>
   [...]
   ```

<!--
1. Determine the load balancer's endpoint IP addresses.

   Run the `dig` [command](https://en.wikipedia.org/wiki/Dig_(command)) to determine the IP address of the nearest load balancer. The `dig` command queries the Domain Name System and returns the name and IP addresses of the Audience Manager [!UICONTROL Data Collection Servers (DCS)].

   ```
   dig dcs-beta.demdex.net
   ...
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 52.87.15.51
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 50.16.150.8
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 52.2.228.100
   ```

1. Using one of the addresses in the above table, add a static DNS entry in the [!DNL `/etc/hosts`] file.

   On Windows, modify [!DNL `c:\WINDOWS\system32\drivers\etc\hosts`].

   For example:

[!DNL `52.87.15.51 samplepartner.demdex.net`]

   >[!NOTE]
   >
   >The addresses change occasionally, so you must keep your [!DNL /etc/hosts] file up to date.

   Additionally, if you need to set up ID synchronization, you must add a similar entry for [!DNL dpm.demdex.net.]

[!DNL `52.87.15.51 dpm.demdex.net`] [!DNL]. 

1. Make a [!UICONTROL DCS] call, using the `curl` [command](https://curl.haxx.se/docs/manpage.html). Curl is a tool to transfer data from or to a server, using one of many supported protocols.

   For example:

[!DNL `https://<domain>/event?product=camera`] 

1. Verify that your request was served by the beta [!UICONTROL DCS] by looking for "sandbox" in the [!UICONTROL DCS] response header.

   For example:

   ```
   curl -v https://dcs-beta.demdex.net/?event
   [...]
   < DCS: va6-sandbox-dcs-3.sandbox.demdex.com <release_number>
   [...]
   ```
-->
