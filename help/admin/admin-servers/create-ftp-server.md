---
description: Utilice la página Servidores de la herramienta de administración de Audience Manager para crear un nuevo servidor FTP o editar un servidor existente.
seo-description: Utilice la página Servidores de la herramienta de administración de Audience Manager para crear un nuevo servidor FTP o editar un servidor existente.
seo-title: Crear o editar un servidor FTP
title: Crear o editar un servidor FTP
uuid: 9273abb2-963d-4d83-bf5a-b3817f0b90e6
translation-type: tm+mt
source-git-commit: e0dc190f8765ec91431a2c02a62c6bf5458c7e3d
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 5%

---


# Crear o editar un servidor FTP {#create-or-edit-an-ftp-server}

Utilice la [!UICONTROL Servers] página de la herramienta de administración de Audience Manager para crear un nuevo servidor FTP o editar un servidor existente.

>[!NOTE]
>
>Debe tener la [!UICONTROL DEXADMIN] función para crear nuevos servidores o editar los existentes.

1. Para crear un nuevo servidor, haga clic en **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. Para editar un servidor existente, haga clic en el servidor que desee en la **[!UICONTROL Label]** columna.
1. Especifique la etiqueta que desee para este servidor.
1. En la lista **[!UICONTROL Protocol]** desplegable, seleccione el protocolo que desee: **FTP**.

   >[!NOTE]
   >
   >Se recomienda utilizar [!DNL Amazon S3] como método para obtener archivos de los socios y enviarlos. [!DNL Amazon S3] proporciona una interfaz de servicios Web sencilla que puede utilizarse para almacenar y recuperar cualquier cantidad de datos, en cualquier momento y desde cualquier lugar de la web. Para obtener más información, consulte [Acerca de Amazon S3](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html) en la Guía *del usuario de* Audience Manager.

1. Rellene los campos:

   * **[!UICONTROL Type]::**Seleccione el tipo de codificación que desee:**[!UICONTROL SFTP]**o **[!UICONTROL FTPs/TLS]**.
   * **[!UICONTROL Domain]::**Especifique el dominio (host) deseado para este servidor.
   * **[!UICONTROL Port]::**Especifique el puerto deseado para este servidor. Se muestra el puerto predeterminado para cada tipo de codificación. Si es necesario, puede cambiar el puerto predeterminado.
   * **[!UICONTROL Remote Path]::**Especifique la ruta de acceso remota que desee para este servidor. Si deja este campo vacío, Audience Manager coloca los archivos en el directorio predeterminado.
   * **[!UICONTROL .tmp File Rename on Completion]::**Active esta opción para cambiar el nombre del`.tmp`archivo una vez finalizado.
   * **[!UICONTROL Filename Suffix]::**Especifique el texto que desee anexar para transferir archivos.
   * **[!UICONTROL Moved to When Finished]::**Especifique la ruta de la ubicación en la que desea que se mueva el archivo de transferencia al finalizar.
   * **[!UICONTROL Authentication]::**Especifique el método de autenticación del servidor que desee:**[!UICONTROL Username/Password]**o **[!UICONTROL SSH Key]**.
   >[!NOTE]
   >
   >Recuerde agregar nuestra salida [!DNL FTP] [!DNL IP] a su lista de IP permitidas: **52.44.29.204**.

1. Para **[!UICONTROL SSH Key]** autenticación:
   1. Genere el par de claves pública/privada desde cualquier [!DNL Linux] o [!DNL Mac] máquina.
   1. Proporcione la clave **** pública al cliente para que la actualice en su [!DNL SFTP] servidor. Deben incluir todo el texto de la clave pública en su servidor, incluyendo `-----BEGIN RSA PRIVATE KEY-----` y `-----END RSA PRIVATE KEY-----` . A cambio, deben proporcionar el nombre de usuario en el que instalan la clave.
   1. Actualice el campo de nombre de usuario con el proporcionado por el cliente y el campo de clave con la clave **privada**.
1. Haga clic **[!UICONTROL Create]** si está creando un nuevo servidor o haga clic en **[!UICONTROL Update]** si está editando un servidor existente.
