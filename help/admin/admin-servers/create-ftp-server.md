---
description: Utilice la página Servidores de la herramienta Administración de Audience Manager para crear un nuevo servidor FTP o editar un servidor existente.
seo-description: Utilice la página Servidores de la herramienta Administración de Audience Manager para crear un nuevo servidor FTP o editar un servidor existente.
seo-title: Creación o edición de un servidor FTP
title: Creación o edición de un servidor FTP
uuid: 9273 abb 2-963 d -4 d 83-bf 5 a-b 3817 f 0 b 90 e 6
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# Creación o edición de un servidor FTP {#create-or-edit-an-ftp-server}

Utilice [!UICONTROL Servers] la página de la herramienta de administración de Audience Manager para crear un nuevo servidor FTP o editar un servidor existente.

>[!NOTE]
>
>Debe tener [!UICONTROL DEXADMIN] la función para crear nuevos servidores o editar los servidores existentes.

1. Para crear un nuevo servidor, haga clic **[!UICONTROL Servers]** en &gt; **[!UICONTROL Create Server]**. Para editar un servidor existente, haga clic en el servidor que desee en **[!UICONTROL Label]** la columna.
1. Especifique la etiqueta que desee para este servidor.
1. En la lista **[!UICONTROL Protocol]** desplegable, seleccione el protocolo que desee: **FTP**.

   >[!NOTE]
   >
   >Se recomienda utilizar [!DNL Amazon S3] como método para obtener archivos y enviar archivos a socios. [!DNL Amazon S3] proporciona una interfaz de servicios Web sencilla que se puede utilizar para almacenar y recuperar cualquier cantidad de datos, en cualquier momento, desde cualquier lugar de la Web. Para obtener más información, consulte [Acerca de Amazon S 3](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html) en la Guía del usuario de *Audience Manager*.

1. Rellene los campos:

   * **[!UICONTROL Type]:** Seleccione el tipo de codificación que desee: **[!UICONTROL SFTP]** o **[!UICONTROL FTPs/TLS]**.
   * **[!UICONTROL Domain]:** Especifique el dominio (host) deseado para este servidor.
   * **[!UICONTROL Port]:** Especifique el puerto deseado para este servidor. Se muestra el puerto predeterminado para cada tipo de codificación. Si es necesario, puede cambiar el puerto predeterminado.
   * **[!UICONTROL Remote Path]:** Especifique la ruta remota que desee para este servidor. Si deja este campo vacío, Audience Manager coloca los archivos en el directorio predeterminado.
   * **[!UICONTROL .tmp File Rename on Completion]:** Active esta opción para cambiar el nombre del `.tmp` archivo al finalizar.
   * **[!UICONTROL Filename Suffix]:** Especifique el texto que desee anexar para transferir archivos.
   * **[!UICONTROL Moved to When Finished]:** Especifique la ruta a la ubicación donde desee mover el archivo de transferencia.
   * **[!UICONTROL Authentication]:** Especifique el método de autenticación del servidor que desee: **[!UICONTROL Username/Password]** o **[!UICONTROL SSH Key]**.
   >[!NOTE]
   >
   >Recuerde incluir nuestra marca [!DNL FTP][!DNL IP]: **52.44.29.204**.

1. Para **[!UICONTROL SSH Key]** autenticación:
   1. Genere el par de clave pública/privada desde cualquier [!DNL Linux] equipo o [!DNL Mac] equipo.
   1. Proporcione la clave **pública** al cliente para que se actualice en su [!DNL SFTP] servidor. Deben incluir todo el texto desde la clave pública de su servidor, incluyendo `-----BEGIN RSA PRIVATE KEY-----` y `-----END RSA PRIVATE KEY-----` . A cambio, deben proporcionar el nombre de usuario bajo el cual están instalando la clave.
   1. Actualice el campo de nombre de usuario con el proporcionado por el cliente y el campo clave con la clave **privada**.
1. Haga clic **[!UICONTROL Create]** en si está creando un servidor nuevo o si está **[!UICONTROL Update]** editando un servidor existente.
