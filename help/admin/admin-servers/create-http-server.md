---
description: Utilice la página Servidores de la herramienta Administración de Audience Manager para crear un nuevo servidor HTTP o editar un servidor existente.
seo-description: Utilice la página Servidores de la herramienta Administración de Audience Manager para crear un nuevo servidor HTTP o editar un servidor existente.
seo-title: Creación o edición de un servidor HTTP
title: Creación o edición de un servidor HTTP
uuid: 1 ef 0 e 751-e 239-4 dc 6-a 4 f 6-73 cc 05686807
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# Creación o edición de un servidor HTTP {#create-or-edit-an-http-server}

Utilice [!UICONTROL Servers] la página de la herramienta de administración de Audience Manager para crear un nuevo servidor HTTP o editar un servidor existente.

>[!NOTE]
>
>Debe tener [!UICONTROL DEXADMIN] la función para crear nuevos servidores o editar los servidores existentes.

1. Para crear un nuevo servidor, vaya **[!UICONTROL Servers]** a &gt; **[!UICONTROL Create Server]**. Para editar un servidor existente, haga clic en el servidor que desee en **[!UICONTROL Label]** la columna.
1. Especifique la etiqueta que desee para este servidor.
1. En la lista **[!UICONTROL Protocol]** desplegable, seleccione el protocolo que desee: [!DNL HTTP].
1. Rellene los campos:

   * **[!UICONTROL Domain]:** Especifique el dominio (host) deseado para este servidor.
   * **[!UICONTROL Port]:** Especifique el puerto deseado para este servidor. Se muestra el puerto predeterminado para cada tipo de codificación. Puede cambiar el puerto predeterminado, si es necesario
   * **[!UICONTROL Maximum Users Per Request]:** Especifique el número máximo de usuarios por solicitud permitida para este servidor.
   * **[!UICONTROL URL Prefix]:** Especifique el [!DNL URL] prefijo que debe utilizarse para este servidor.
   * **[!UICONTROL Authentication URL]:** Especifique la [!UICONTROL Authentication URL] para este `HTTP` servidor.
   * **[!UICONTROL Authentication]:** Especifique el método de autenticación que desee: **[!UICONTROL None]**, **[!UICONTROL Username/Password]** o **[!UICONTROL SSH Key]**.
   * **[!UICONTROL HTTP Signature Header]:** Nombre del [!DNL HTTP] encabezado proporcionado por el cliente que contiene la clave [!DNL HTTP] de firma. El valor predeterminado es [!UICONTROL X-Signature], como se muestra en el ejemplo siguiente:

      ```
      * Connected to partner.website.com (127.0.0.1) port 80 (#0)
      > POST /webpage HTTP/1.1
      > Host: partner.host.com
      > Accept: */*
      > Content-Type: application/json
      > Content-Length: 20
      > X-Signature: wxa2ByMWhhP328EvHQsVlOD5jTc=
      POST message content
      ```

   * **[!UICONTROL HTTP Signature Key]:** Clave utilizada para firmar [!DNL HTTP] la solicitud, proporcionada por el cliente.
   * **[!UICONTROL Show Signature Key]:** Alternar si se muestra o no la firma en el navegador.
   * **[!UICONTROL HTTP Signature Encryption Method]:** Especifique el método que utilizamos para cifrar la firma. Se utiliza [!UICONTROL SHA1] a menos que el cliente prefiera.
   >[!NOTE]
   >
   >Si desea habilitar [la autenticación oauth 2.0 para transferencias de datos en tiempo real](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html) para un socio, rellene los campos como se muestra en la siguiente tabla. Los campos en *cursiva* deben rellenarse exactamente como en la tabla.

   | Nombre  | Valor |
   |---|---|
   | [!UICONTROL Label] | [!UICONTROL Server with OAuth 2.0 enabled] |
   | [!UICONTROL Protocol] | [!UICONTROL HTTP] |
   | [!UICONTROL Domain] | [!UICONTROL api.partner.com] |
   | [!UICONTROL Port] | [!UICONTROL 443] |
   | [!UICONTROL Maximum Users per Request] | [!UICONTROL 10] |
   | [!UICONTROL URL Prefix] | [!UICONTROL /segments/aam] |
   | [!UICONTROL Authentication URL] | [!UICONTROL api.partner.com/oauth2/token] |
   | [!UICONTROL Authentication] | [!UICONTROL Username/Password] |
   | [!UICONTROL Username] | [!UICONTROL *Autorización *] |
   | [!UICONTROL Password] | your_ password_ here |
   | [!UICONTROL HTTP Signature Header] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Key] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Encryption Method] | [!UICONTROL None] |

1. Haga clic **[!UICONTROL Create]** en si está creando un servidor nuevo o si está **[!UICONTROL Update]** editando un servidor existente.