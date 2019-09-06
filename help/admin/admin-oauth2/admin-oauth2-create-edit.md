---
description: Utilice la página Clientes oauth 2 para ver una lista de clientes oauth 2 en la configuración de Audience Manager. Puede editar o eliminar clientes existentes o crear nuevos clientes, siempre y cuando tenga asignadas las funciones de usuario adecuadas.
seo-description: Utilice la página Clientes oauth 2 para ver una lista de clientes oauth 2 en la configuración de Audience Manager. Puede editar o eliminar clientes existentes o crear nuevos clientes, siempre y cuando tenga asignadas las funciones de usuario adecuadas.
seo-title: Clientes oauth 2
title: Clientes oauth 2
uuid: 3 e 654053-fb 2 f -4 d 8 f-a 53 c-b 5 c 3 b 8 dbdaaa
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# Clientes oauth 2 {#oauth-clients}

Utilice [!UICONTROL OAuth2 Clients] la página para ver una lista [!UICONTROL OAuth2] de clientes en [!DNL Audience Manager] su configuración. Puede editar o eliminar clientes existentes o crear nuevos clientes, siempre y cuando tenga asignadas las funciones de usuario adecuadas.

## Información general {#overview}

<!-- c_oauth.xml -->

>[!NOTE]
>
>Asegúrese de que el cliente lee la documentación [oauth 2](https://docs.adobe.com/content/help/en/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html#oauth) en el [! Guía del usuario de Audience Manager DNL.

[!DNL OAuth2] es un estándar abierto para autorizar el acceso delegado asegurado a [!DNL Audience Manager] los recursos en nombre del propietario del recurso.

![](assets/oauth.png)

Puede ordenar cada columna en orden ascendente o descendente haciendo clic en el encabezado de la columna que desee.

Utilice [!UICONTROL Search] el cuadro o los controles de paginación en la parte inferior de la lista para encontrar el cliente que desee.

## Crear o editar un cliente oauth 2 {#create-edit-client}

<!-- t_create_edit_auth.xml -->

Utilice [!UICONTROL OAuth2 Clients] la página de la herramienta Audience Manager [!UICONTROL Admin] para crear un [!UICONTROL Oauth2] cliente nuevo o editar un cliente existente.

1. Para crear un [!UICONTROL OAuth2] nuevo cliente, haga clic **[!UICONTROL OAuth2 Clients]** en &gt; **[!UICONTROL Add OAuth2 Client]**. Para editar un [!UICONTROL OAuth2] cliente existente, haga clic en el cliente que desee en **[!UICONTROL Client ID]** la columna.
1. Especifique el nombre que desee para este [!UICONTROL OAuth2] cliente. Tenga en cuenta que solo es un nombre para el registro.
1. Especifique la dirección de correo electrónico [!UICONTROL OAuth2] del cliente. Existe un límite de una dirección de correo electrónico.
1. En la lista **[!UICONTROL Partner]** desplegable, seleccione el socio que desee.
1. En **[!UICONTROL Client ID]** el cuadro, especifique el ID que desee. Este es el valor utilizado al enviar [!DNL API] solicitudes. El prefijo se rellena automáticamente cuando se empieza a escribir después de elegir una [!UICONTROL Partner] en la lista desplegable del paso anterior. El formato correcto es &lt; *`partner subdomain`*&gt; - &lt; *`Audience Manager username`*&gt;.
1. Seleccione o anule la selección de **[!UICONTROL Restrict to Partner Users]** la casilla de verificación, según desee. Si se selecciona esta casilla de verificación, el usuario debe ser [!DNL Audience Manager] un usuario enumerado para el socio seleccionado. Se recomienda seleccionar esta opción.
1. En **[!UICONTROL Scope]** la sección, seleccione o anule la selección de las casillas **[!UICONTROL Read]** y **[!UICONTROL Write]** casillas de verificación, según desee.
1. En **[!UICONTROL Grant Type]** la sección, seleccione los medios que desee autorizar. Le recomendamos que utilice la configuración y [!UICONTROL Password][!UICONTROL Refresh-token] las opciones predeterminadas.

   * **[!UICONTROL Implicit]**: Si selecciona esta opción, el [!UICONTROL Redirect URI] cuadro estará habilitado. Al usuario se le asigna un autentificador de acceso automático tras autenticarse y se envía inmediatamente a la redirección [!DNL URI].
   * **[!UICONTROL Authorization Code]**: Si selecciona esta opción, el [!UICONTROL Redirect URI] cuadro estará habilitado. Tras autenticarse, el usuario regresa al cliente y después se envía al redireccionamiento [!DNL URI].
   * **[!UICONTROL Password]**: El usuario se autentica con una contraseña introducida por el usuario, en lugar de un intento de validación automático a través de un servidor de autorización.
   * **[!UICONTROL Refresh_token]**: Se utiliza para actualizar un token de acceso caducado durante un período de tiempo prolongado.

1. En **[!UICONTROL Redirect URI]** el cuadro, especifique el [!DNL URI]. Esta opción solo se activa si se seleccionan los **[!UICONTROL Implicit]** tipos **[!UICONTROL Authorization_code]** y los tipos de becas. El **[!UICONTROL Redirect URI]** cuadro permite especificar un valor separado por comas de [!DNL URI] valores aceptables. Es el [!DNL URI] usuario de un cliente al que se redirige después de aprobar al cliente para [!DNL API] obtener acceso.
1. Especifique el tiempo de caducidad deseado (en segundos) para el acceso y la caducidad del autentificador.

   * **[!UICONTROL Access Token Expiration Time]**: Número de segundos que un token de acceso es válido después de emitirse. Puede ser nulo para utilizar la plataforma predeterminada (12 horas). También puede ser -1 para indicar que el autentificador de acceso no caduca.
   * **[!UICONTROL Refresh Token Expiration Time]**: Número de segundos que un token de actualización es válido después de emitirse. Puede ser nulo para utilizar la plataforma predeterminada (30 días).

1. Haga clic en **[!UICONTROL Save]**.

Para eliminar un [!UICONTROL OAuth2] cliente, haga clic en **[!UICONTROL OAuth2 Clients]** y luego en ![](assets/icon_delete.png) la **[!UICONTROL Actions]** columna del cliente que desee.

>[!MORE_ LIKE_ THIS]
>
>* [Requisitos de API y Recomendaciones](../admin-oauth2/aam-admin-api-requirements.md)

