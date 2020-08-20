---
description: Utilice la página Clientes de OAuth2 para la vista de una lista de clientes de OAuth2 en la configuración del Audience Manager. Puede editar o eliminar clientes existentes o crear nuevos clientes, siempre que tenga asignadas las funciones de usuario correspondientes.
seo-description: Utilice la página Clientes de OAuth2 para la vista de una lista de clientes de OAuth2 en la configuración del Audience Manager. Puede editar o eliminar clientes existentes o crear nuevos clientes, siempre que tenga asignadas las funciones de usuario correspondientes.
seo-title: Clientes de OAuth2
title: Clientes de OAuth2
uuid: 3e654053-fb2f-4d8f-a53c-b5c3b8dbdaaa
translation-type: tm+mt
source-git-commit: 0ee7aa9c13f1b9b8fd64dddff4e52d101055e77c
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 2%

---


# Clientes de OAuth2 {#oauth-clients}

Utilice la [!UICONTROL OAuth2 Clients] página para vista de una lista de [!UICONTROL OAuth2] clientes en su [!DNL Audience Manager] configuración. Puede editar o eliminar clientes existentes o crear nuevos clientes, siempre que tenga asignadas las funciones de usuario correspondientes.

## Información general {#overview}

<!-- c_oauth.xml -->

>[!NOTE]
>
>Asegúrese de que el cliente lea la documentación de [OAuth2](https://docs.adobe.com/content/help/en/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html#oauth) en la Guía del usuario del Audience Manager.

[!DNL OAuth2] es una norma abierta para la autorización de proporcionar acceso delegado seguro a los recursos en nombre de un propietario de [!DNL Audience Manager] recursos.

![](assets/oauth.png)

Puede ordenar cada columna en orden ascendente o descendente haciendo clic en el encabezado de la columna deseada.

Use el [!UICONTROL Search] cuadro o los controles de paginación en la parte inferior de la lista para encontrar el cliente deseado.

## Crear o editar un cliente OAuth2 {#create-edit-client}

<!-- t_create_edit_auth.xml -->

Utilice la [!UICONTROL OAuth2 Clients] página de la herramienta Audience Manager [!UICONTROL Admin] para crear un nuevo [!UICONTROL Oauth2] cliente o editar un cliente existente.

1. Para crear un nuevo [!UICONTROL OAuth2] cliente, haga clic en **[!UICONTROL OAuth2 Clients]** > **[!UICONTROL Add OAuth2 Client]**. Para editar un cliente existente, haga clic en el cliente que desee en la [!UICONTROL OAuth2] **[!UICONTROL Client ID]** columna.
1. Especifique el nombre que desee para este [!UICONTROL OAuth2] cliente. Tenga en cuenta que este es un nombre sólo para el registro.
1. Especifique la dirección de correo electrónico del [!UICONTROL OAuth2] cliente. Hay un límite de una dirección de correo electrónico.
1. En la lista **[!UICONTROL Partner]** desplegable, seleccione el socio que desee.
1. En el **[!UICONTROL Client ID]** cuadro, especifique el ID que desee. Es el valor que se utiliza al enviar [!DNL API] solicitudes. El prefijo se rellena automáticamente cuando se escribe con inicio después de haber seleccionado un elemento [!UICONTROL Partner] de la lista desplegable del paso anterior. El formato correcto es &lt; *`partner subdomain`*> - &lt; *`Audience Manager username`*>.
1. Seleccione o anule la selección de la **[!UICONTROL Restrict to Partner Users]** casilla de verificación que desee. Si esta casilla de verificación está activada, el usuario debe ser un [!DNL Audience Manager] usuario de la lista del socio seleccionado. Se recomienda seleccionar esta opción como práctica recomendada.
1. En la **[!UICONTROL Scope]** sección, seleccione o anule la selección de las casillas de verificación **[!UICONTROL Read]** y **[!UICONTROL Write]** , según desee.
1. En la **[!UICONTROL Grant Type]** sección , seleccione los medios deseados para la autorización. Le recomendamos que utilice la configuración predeterminada de [!UICONTROL Password] y las [!UICONTROL Refresh-token] opciones.

   * **[!UICONTROL Implicit]**:: Si selecciona esta opción, el [!UICONTROL Redirect URI] cuadro estará habilitado. El usuario recibe un token de acceso automático tras la autenticación y se envía inmediatamente al redireccionamiento [!DNL URI].
   * **[!UICONTROL Authorization Code]**:: Si selecciona esta opción, el [!UICONTROL Redirect URI] cuadro estará habilitado. El usuario se devuelve al cliente después de autenticarse y se envía a la redirección [!DNL URI].
   * **[!UICONTROL Password]**:: El usuario se autentica con una contraseña introducida por el usuario en lugar de un intento de validación automática a través de un servidor de autorización.
   * **[!UICONTROL Refresh_token]**:: Se utiliza para actualizar un token de acceso caducado durante un período de tiempo prolongado.

1. En el **[!UICONTROL Redirect URI]** cuadro, especifique el [!DNL URI]. Esta opción solo está habilitada si selecciona los tipos **[!UICONTROL Implicit]** y **[!UICONTROL Authorization_code]** beca. El **[!UICONTROL Redirect URI]** cuadro permite especificar un valor separado por comas de [!DNL URI] valores aceptables. Se redirige a [!DNL URI] un usuario de un cliente después de aprobar el [!DNL API] acceso del cliente.
1. Especifique el tiempo de caducidad (en segundos) que desee para el acceso y la caducidad del token de actualización.

   * **[!UICONTROL Access Token Expiration Time]**:: El número de segundos que un token de acceso es válido después de emitirse. Puede ser nulo para utilizar la plataforma predeterminada (12 horas). También puede ser -1 para indicar que el token de acceso no caduca.
   * **[!UICONTROL Refresh Token Expiration Time]**:: El número de segundos que un token de actualización es válido después de emitirse. Puede ser nulo para usar la plataforma predeterminada (30 días).

1. Haga clic **[!UICONTROL Save]**.

Para eliminar un [!UICONTROL OAuth2] cliente, haga clic en **[!UICONTROL OAuth2 Clients]**, luego haga clic ![](assets/icon_delete.png) en la **[!UICONTROL Actions]** columna del cliente deseado.

>[!MORELIKETHIS]
>
>* [Requisitos y recomendaciones de API](../admin-oauth2/aam-admin-api-requirements.md)

