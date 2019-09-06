---
description: Utilice la página Usuarios de integración para ver una lista de usuarios en la configuración de Audience Manager. Puede editar o eliminar usuarios existentes o crear nuevos usuarios siempre que tenga asignadas las funciones de usuario adecuadas.
seo-description: Utilice la página Usuarios de integración para ver una lista de usuarios en la configuración de Audience Manager. Puede editar o eliminar usuarios existentes o crear nuevos usuarios siempre que tenga asignadas las funciones de usuario adecuadas.
seo-title: Usuarios de integración
title: Usuarios de integración
uuid: 13 dcb 3 fb -4561-409 c -84 da -943 d 0 d 390 cf 3
translation-type: tm+mt
source-git-commit: 10adb6b06160f5a5c4068483b407e5798fc10150

---


# Usuarios de integración {#integration-users}

Utilice [!UICONTROL Integration Users] la página para ver una lista de usuarios en la configuración de Audience Manager. Puede editar o eliminar usuarios existentes o crear nuevos usuarios siempre que tenga asignadas las funciones de usuario adecuadas.

<!-- c_integration_users.xml -->

Puede ordenar cada columna en orden ascendente o descendente haciendo clic en el encabezado de la columna que desee.
Utilice [!UICONTROL Search] el cuadro o los controles de paginación en la parte inferior de la lista para encontrar al usuario que desee.

## Crear o editar un usuario {#create-edit-user}

Utilice [!UICONTROL Integration Users] la página de la herramienta Audience Manager [!UICONTROL Admin] para crear un nuevo usuario o editar una cuenta de usuario existente.

<!-- t_create_user.xml -->

>[!NOTE]
>
>Debe tener [!UICONTROL CREATE_USER] la función para crear nuevos usuarios. Debe tener [!UICONTROL EDIT_USER] la función para editar los usuarios existentes.

1. Para crear un nuevo usuario, haga clic **[!UICONTROL Integration Users]** en &gt; **[!UICONTROL Create a New User]**. Para editar un usuario existente, haga clic en el usuario que desee en **[!UICONTROL Username]** la columna.
2. Rellene los campos:
   * **[!UICONTROL First Name]**: (Obligatorio) Especifique el nombre del usuario.
   * **[!UICONTROL Last Name]**: (Obligatorio) Especifique el apellido del usuario.
   * **[!UICONTROL Username]**: (Obligatorio) Especifique el nombre de usuario del usuario.
   * **[!UICONTROL Email Address]**: (Requerido) Especifique la dirección de correo electrónico del usuario.
   * **[!UICONTROL Phone Number]**: Especifique el número de teléfono del usuario.
   * **[!UICONTROL IMS ID]**: Especifique [!UICONTROL Internet Messaging Service ID]los usuarios.
   * **[!UICONTROL User Roles]**: Seleccione las funciones de usuario que desee:
      * **[!UICONTROL DEXADMIN]**: Proporciona acceso de administrador para realizar tareas en [!UICONTROL Admin] la herramienta Audience Manager. Si no selecciona esta opción, puede elegir funciones individuales. Estas funciones permiten a los usuarios realizar tareas mediante [!DNL API] llamadas, pero no en la herramienta de administración.
      * **[!UICONTROL CREATE_USERS]**: Permite a los usuarios crear nuevos usuarios mediante [!DNL API] una llamada.
      * **[!UICONTROL DELETE_USERS]**: Permite que los usuarios eliminen usuarios existentes mediante [!DNL API] una llamada.
      * **[!UICONTROL EDIT_USERS]**: Permite a los usuarios editar usuarios existentes mediante [!DNL API] una llamada.
      * **[!UICONTROL VIEW_USERS]**: Permite que los usuarios vean otros usuarios en la configuración de Audience Manager mediante [!DNL API] una llamada.
      * **[!UICONTROL CREATE_PARTNERS]**: Permite a los usuarios crear socios de Audience Manager mediante [!DNL API] una llamada.
      * **[!UICONTROL DELETE_PARTNERS]**: Permite a los usuarios eliminar socios de Audience Manager mediante [!DNL API] una llamada.
      * **[!UICONTROL EDIT_PARTNERS]**: Permite a los usuarios editar los socios de Audience Manager mediante [!DNL API] una llamada.
      * **[!UICONTROL VIEW_PARNTERS]**: Permite a los usuarios ver los socios de Audience Manager mediante [!DNL API] una llamada.
   * **Estado:** Seleccione **[!UICONTROL Active]** esta opción para convertir a este usuario en un usuario de Audience Manager activado.
3. Haga clic en **[!UICONTROL Submit]**.

## Delete a User {#delete-user}

Utilice [!UICONTROL Integration Users] la página de la herramienta Audience Manager [!UICONTROL Admin] para eliminar un usuario existente.

<!-- t_delete_user.xml -->

>[!NOTE]
>
>Debe tener **[!UICONTROL DELETE_USER]** la función para crear nuevos usuarios.

1. Haga clic en **[!UICONTROL Integration Users]**.
2. Haga clic en ![](assets/icon_delete.png) la **[!UICONTROL Actions]** columna del usuario que desee.
3. Click **[!UICONTROL OK]** to confirm the deletion.