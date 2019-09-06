---
description: El entorno beta sirve para probar implementaciones de Audience Manager. Los cambios realizados en beta no afectan a los datos de producción. El entorno beta de Audience Manager es una versión independiente y en escala más pequeña del entorno de producción. Todos los datos que desee probar deben ingresarse y recopilarse en este entorno.
seo-description: El entorno beta sirve para probar implementaciones de Audience Manager. Los cambios realizados en beta no afectan a los datos de producción. El entorno beta de Audience Manager es una versión independiente y en escala más pequeña del entorno de producción. Todos los datos que desee probar deben ingresarse y recopilarse en este entorno.
seo-title: Entorno beta
solution: Audience Manager
title: Entorno beta
uuid: 6 a 253 f 4 e -96 e 7-4395-a 783-a 8 eb 213 b 7 daf
translation-type: tm+mt
source-git-commit: 7765dbf79c2fb6ca8c4b52fe8090c1fd11f9db27

---


# Entorno beta {#beta-environment}

El entorno beta sirve para probar implementaciones de Audience Manager. Los cambios realizados en beta no afectan a los datos de producción. El entorno beta de Audience Manager es una versión independiente y en escala más pequeña del entorno de producción. Todos los datos que desee probar deben ingresarse y recopilarse en este entorno.

## Información general {#overview}

<!-- beta_environment_admin.xml -->

| Servicio | URL/Nombre de host | Pasos a suministrar |
|--- |--- |--- |
| S3 |  | Consulte [Suministro de contenedores Amazon S 3](admin-beta-environment.md#provision-s3-buckets). |
| DCS | https &amp; amp; dos puntos; dcs-beta.demdex.net/./. | No se necesitan pasos adicionales de nuestro lado. Consulte [Acceso al DCS en el entorno beta](admin-beta-environment.md#access-dcs-beta-environment). |
| IU | https &amp; amp; dos puntos; //bank-beta.demdex.com | Los datos se copian de la producción al entorno beta mensualmente. Las credenciales de producción son válidas para la versión beta. |
| API | https &amp; amp; dos puntos; api-beta.demdex.com/./. | Los datos se copian de la producción al entorno beta mensualmente. Las credenciales de producción son válidas para la versión beta. |

## Suministro de contenedores Amazon S 3 {#provision-s3-buckets}

>[!NOTE]
>
>Estamos dejando de utilizar [!DNL FTP/SFTP]. Además, tenga en cuenta que las transferencias de datos salientes no funcionan para el entorno beta.

Para aprovisionar [!DNL S3] bloques para datos de entrada:

1. Utilice [**la función de ayuda**](https://skms.adobe.com/) de SKMS Request techops.
1. Vaya a **[!UICONTROL Request TechOps Help]** la barra de navegación izquierda.
1. En **[!UICONTROL Request Search]**, escriba Audience Manager en el campo de búsqueda.
1. Desplácese hacia abajo en los resultados de búsqueda y haga clic en **Audience Manager - Aprovisionamiento de cuenta de entrada/saliente S 3**.
1. Complete los campos de la ventana de aprovisionamiento y especifique **el entorno Simulador para pruebas** en **[!UICONTROL Environment]** el campo.

>[!NOTE]
>
>Desincentivamos el uso [!DNL FTP/SFTP] y alentamos el uso [!UICONTROL Amazon S3]de. Las razones por las cuales alentamos el uso [!UICONTROL Amazon S3] de se enumeran en [Amazon S 3: Acerca](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html)de.

## Acceder al DCS en el entorno Beta {#access-dcs-beta-environment}

Para acceder al [!UICONTROL DCS] entorno beta:

1. Realice [!UICONTROL DCS] una llamada mediante [!DNL curl][el comando](https://curl.haxx.se/docs/manpage.html). [!DNL Curl] es una herramienta para transferir datos desde o hacia un servidor utilizando uno de los muchos protocolos admitidos.

   Por ejemplo: `curl -v https://dcs-beta.demdex.net/event`

1. Verifique que la versión beta [!UICONTROL DCS] ofrezca su solicitud buscando "[!DNL sandbox]en el encabezado [!UICONTROL DCS] de respuesta.

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