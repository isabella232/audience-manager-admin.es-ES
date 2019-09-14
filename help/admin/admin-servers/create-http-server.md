---
description: Utilice la página Servidores de la herramienta de administración de Audience Manager para crear un nuevo servidor HTTP o editar un servidor existente.
seo-description: Utilice la página Servidores de la herramienta de administración de Audience Manager para crear un nuevo servidor HTTP o editar un servidor existente.
seo-title: Crear o editar un servidor HTTP
title: Crear o editar un servidor HTTP
uuid: 1ef0e751-e239-4dc6-a4f6-73cc05686807
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# Crear o editar un servidor HTTP {#create-or-edit-an-http-server}

Utilice la página de la herramienta de administración de Audience Manager para crear un nuevo servidor HTTP o editar un servidor existente. [!UICONTROL Servers]

>[!NOTE]
>
>Debe tener la [!UICONTROL DEXADMIN] función para crear nuevos servidores o editar los existentes.

1. Para crear un nuevo servidor, vaya a **[!UICONTROL Servers]** &gt; **[!UICONTROL Create Server]**. Para editar un servidor existente, haga clic en el servidor que desee en la **[!UICONTROL Label]** columna.
1. Especifique la etiqueta que desee para este servidor.
1. En la lista **[!UICONTROL Protocol]** desplegable, seleccione el protocolo que desee: [!DNL HTTP].
1. Rellene los campos:

   * **[!UICONTROL Domain]** :: Especifique el dominio (host) deseado para este servidor.
   * **[!UICONTROL Port]** :: Especifique el puerto deseado para este servidor. Se muestra el puerto predeterminado para cada tipo de codificación. Si es necesario, puede cambiar el puerto predeterminado
   * **[!UICONTROL Maximum Users Per Request]** :: Especifique el número máximo de usuarios por solicitud permitida para este servidor.
   * **[!UICONTROL URL Prefix]** :: Especifique el [!DNL URL] prefijo que se usará para este servidor.
   * **[!UICONTROL Authentication URL]** :: Especifique el [!UICONTROL Authentication URL] para este `HTTP` servidor.
   * **[!UICONTROL Authentication]** :: Especifique el método de autenticación deseado: **[!UICONTROL None]**, **[!UICONTROL Username/Password]** o **[!UICONTROL SSH Key]**.
   * **[!UICONTROL HTTP Signature Header]** :: El nombre del [!DNL HTTP] encabezado, proporcionado por el cliente, que contiene la clave de [!DNL HTTP] firma. El valor predeterminado es [!UICONTROL X-Signature], como se muestra en el ejemplo siguiente:

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

   * **[!UICONTROL HTTP Signature Key]** :: Clave utilizada para firmar la [!DNL HTTP] solicitud, proporcionada por el cliente.
   * **[!UICONTROL Show Signature Key]** :: Alterne si desea o no mostrar la firma en el explorador.
   * **[!UICONTROL HTTP Signature Encryption Method]** :: Especifique el método que usamos para cifrar la firma. Utilícelo [!UICONTROL SHA1] a menos que el cliente prefiera lo contrario.
   >[!NOTE]
   >
   >Si desea habilitar la autenticación [OAuth 2.0 para transferencias](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html) de datos en tiempo real para un socio, rellene los campos como se muestra en la tabla siguiente. Los campos en *cursiva* deben rellenarse exactamente como en la tabla.

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
   | [!UICONTROL Password] | your_password_here |
   | [!UICONTROL HTTP Signature Header] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Key] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Encryption Method] | [!UICONTROL None] |

1. Haga clic **[!UICONTROL Create]** si está creando un nuevo servidor o haga clic en **[!UICONTROL Update]** si está editando un servidor existente.