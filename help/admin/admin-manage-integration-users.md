---
description: Utilice la página Usuarios de integración para ver una lista de usuarios en la configuración de Audience Manager. Puede editar o eliminar usuarios existentes o crear nuevos usuarios, siempre que tenga asignadas las funciones de usuario correspondientes.
seo-description: Utilice la página Usuarios de integración para ver una lista de usuarios en la configuración de Audience Manager. Puede editar o eliminar usuarios existentes o crear nuevos usuarios, siempre que tenga asignadas las funciones de usuario correspondientes.
seo-title: Usuarios de integración
title: Usuarios de integración
uuid: 13dcb3fb-4561-409c-84da-943d0d390cf3
translation-type: tm+mt
source-git-commit: 10adb6b06160f5a5c4068483b407e5798fc10150

---


# Usuarios de integración {#integration-users}

Utilice la [!UICONTROL Integration Users] página para ver una lista de usuarios en la configuración de Audience Manager. Puede editar o eliminar usuarios existentes o crear nuevos usuarios, siempre que tenga asignadas las funciones de usuario correspondientes.

<!-- c_integration_users.xml -->

Puede ordenar cada columna en orden ascendente o descendente haciendo clic en el encabezado de la columna deseada.
Use el [!UICONTROL Search] cuadro o los controles de paginación en la parte inferior de la lista para encontrar el usuario deseado.

## Crear o editar un usuario {#create-edit-user}

Utilice la página [!UICONTROL Integration Users] de la herramienta Audience Manager [!UICONTROL Admin] para crear un usuario nuevo o editar una cuenta de usuario existente.

<!-- t_create_user.xml -->

>[!NOTE]
>
>Debe tener la [!UICONTROL CREATE_USER] función para crear nuevos usuarios. Debe tener la [!UICONTROL EDIT_USER] función para editar los usuarios existentes.

1. Para crear un nuevo usuario, haga clic en **[!UICONTROL Integration Users]** &gt; **[!UICONTROL Create a New User]**. Para editar un usuario existente, haga clic en el usuario que desee en la **[!UICONTROL Username]** columna.
2. Rellene los campos:
   * **[!UICONTROL First Name]**:: (Requerido) Especifique el nombre del usuario.
   * **[!UICONTROL Last Name]**:: (Requerido) Especifique los apellidos del usuario.
   * **[!UICONTROL Username]**:: (Requerido) Especifique el nombre de usuario del usuario.
   * **[!UICONTROL Email Address]**:: (Requerido) Especifique la dirección de correo electrónico del usuario.
   * **[!UICONTROL Phone Number]**:: Especifique el número de teléfono del usuario.
   * **[!UICONTROL IMS ID]**:: Especifique la del usuario [!UICONTROL Internet Messaging Service ID].
   * **[!UICONTROL User Roles]**:: Seleccione las funciones de usuario que desee:
      * **[!UICONTROL DEXADMIN]**:: Proporciona acceso de administrador para realizar tareas en la herramienta Audience Manager [!UICONTROL Admin] . Si no selecciona esta opción, puede elegir funciones individuales. Estas funciones permiten a los usuarios realizar tareas mediante [!DNL API] llamadas, pero no en la herramienta Administración.
      * **[!UICONTROL CREATE_USERS]**:: Permite a los usuarios crear nuevos usuarios mediante una [!DNL API] llamada.
      * **[!UICONTROL DELETE_USERS]**:: Permite a los usuarios eliminar usuarios existentes mediante una [!DNL API] llamada.
      * **[!UICONTROL EDIT_USERS]**:: Permite a los usuarios editar usuarios existentes mediante una [!DNL API] llamada.
      * **[!UICONTROL VIEW_USERS]**:: Permite a los usuarios ver otros usuarios en la configuración de Audience Manager mediante una [!DNL API] llamada.
      * **[!UICONTROL CREATE_PARTNERS]**:: Permite a los usuarios crear socios de Audience Manager mediante una [!DNL API] llamada.
      * **[!UICONTROL DELETE_PARTNERS]**:: Permite a los usuarios eliminar socios de Audience Manager mediante una [!DNL API] llamada.
      * **[!UICONTROL EDIT_PARTNERS]**:: Permite a los usuarios editar socios de Audience Manager mediante una [!DNL API] llamada.
      * **[!UICONTROL VIEW_PARNTERS]**:: Permite a los usuarios ver socios de Audience Manager mediante una [!DNL API] llamada.
   * **** Estado: Seleccione **[!UICONTROL Active]** para que este usuario sea un usuario activado de Audience Manager.
3. Haga clic en **[!UICONTROL Submit]**.

## Delete a User {#delete-user}

Utilice la [!UICONTROL Integration Users] página de la herramienta Audience Manager [!UICONTROL Admin] para eliminar un usuario existente.

<!-- t_delete_user.xml -->

>[!NOTE]
>
>Debe tener la **[!UICONTROL DELETE_USER]** función para crear nuevos usuarios.

1. Haga clic en **[!UICONTROL Integration Users]**.
2. Haga clic ![](assets/icon_delete.png) en la **[!UICONTROL Actions]** columna del usuario deseado.
3. Click **[!UICONTROL OK]** to confirm the deletion.