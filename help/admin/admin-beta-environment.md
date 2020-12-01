---
description: El entorno beta es para probar las implementaciones de Audience Manager. Los cambios realizados en la versión beta no afectan a los datos de producción. El entorno beta Audience Manager es una versión independiente de menor escala del entorno de producción. Todos los datos que desee probar deben introducirse y recopilarse en este entorno.
seo-description: El entorno beta es para probar las implementaciones de Audience Manager. Los cambios realizados en la versión beta no afectan a los datos de producción. El entorno beta Audience Manager es una versión independiente de menor escala del entorno de producción. Todos los datos que desee probar deben introducirse y recopilarse en este entorno.
seo-title: Entorno beta
solution: Audience Manager
title: Entorno beta
uuid: 6a253f4e-96e7-4395-a783-a8eb213b7daf
translation-type: tm+mt
source-git-commit: 7765dbf79c2fb6ca8c4b52fe8090c1fd11f9db27
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 3%

---


# Entorno beta {#beta-environment}

El entorno beta es para probar las implementaciones de Audience Manager. Los cambios realizados en la versión beta no afectan a los datos de producción. El entorno beta Audience Manager es una versión independiente de menor escala del entorno de producción. Todos los datos que desee probar deben introducirse y recopilarse en este entorno.

## Información general {#overview}

<!-- beta_environment_admin.xml -->

| Servicio | URL/nombre de host | Pasos para aprovisionar |
|--- |--- |--- |
| S3 |  | Consulte [Provisión de cubos Amazon S3](admin-beta-environment.md#provision-s3-buckets). |
| DCS | https&amp;dos puntos;//dcs-beta.demdex.net/... | No necesitamos pasos adicionales de nuestro lado. Consulte [Acceso al DCS en el Entorno Beta](admin-beta-environment.md#access-dcs-beta-environment). |
| IU | https&amp;dos puntos;//bank-beta.demdex.com | Los datos se copian de la producción al entorno beta mensualmente. Las credenciales de producción son válidas para la versión beta. |
| API | https&amp;dos puntos;//api-beta.demdex.com/... | Los datos se copian de la producción al entorno beta mensualmente. Las credenciales de producción son válidas para la versión beta. |

## Aprovisionamiento de cubos Amazon S3 {#provision-s3-buckets}

>[!NOTE]
>
>Nos estamos alejando del uso de [!DNL FTP/SFTP]. Además, tenga en cuenta que las transferencias de datos salientes no funcionan para el entorno beta.

Para aprovisionar bloques [!DNL S3] para datos de entrada:

1. Utilice la función [**Ayuda de TechOps de solicitud SKMS**](https://skms.adobe.com/).
1. Vaya a **[!UICONTROL Request TechOps Help]** en el carril de navegación izquierdo.
1. En **[!UICONTROL Request Search]**, escriba Audience Manager en el campo de búsqueda.
1. Desplácese hacia abajo en los resultados de la búsqueda y haga clic en **Audience Manager - S3 Entrante / Aprovisionamiento de cuentas de salida**.
1. Rellene los campos de la ventana de aprovisionamiento y especifique **entorno de Simulador para pruebas** en el campo **[!UICONTROL Environment]**.

>[!NOTE]
>
>Desalentamos el uso de [!DNL FTP/SFTP] y alentamos el uso de [!UICONTROL Amazon S3]. Las razones por las que alentamos el uso de [!UICONTROL Amazon S3] se enumeran en [Amazon S3:About](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html).

## Acceda al DCS en el Entorno Beta {#access-dcs-beta-environment}

Para acceder a [!UICONTROL DCS] en el entorno beta:

1. Realice una llamada [!UICONTROL DCS] mediante el comando [!DNL curl] [](https://curl.haxx.se/docs/manpage.html). [!DNL Curl] es una herramienta para transferir datos desde o hacia un servidor, utilizando uno de los muchos protocolos admitidos.

   Por ejemplo: `curl -v https://dcs-beta.demdex.net/event`

1. Compruebe que la solicitud la haya enviado la versión beta [!UICONTROL DCS] buscando &quot;[!DNL sandbox]&quot; en el encabezado de respuesta [!UICONTROL DCS].

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