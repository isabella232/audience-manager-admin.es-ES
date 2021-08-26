---
description: Utilice la página Servidores de la herramienta Administración de Audience Manager para crear un nuevo servidor FTP o editar uno existente.
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new FTP server or to edit an existing server.
seo-title: Create or Edit an FTP Server
title: Crear o editar un servidor FTP
uuid: 9273abb2-963d-4d83-bf5a-b3817f0b90e6
exl-id: 9eae4ecf-ccde-483a-ae53-1cbac033d8d6
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 4%

---

# Crear o editar un servidor FTP {#create-or-edit-an-ftp-server}

Utilice la página [!UICONTROL Servers] de la herramienta de administración del Audience Manager para crear un nuevo servidor FTP o editar un servidor existente.

>[!NOTE]
>
>Debe tener la función [!UICONTROL DEXADMIN] para crear nuevos servidores o editar los existentes.

1. Para crear un nuevo servidor, haga clic en **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. Para editar un servidor existente, haga clic en el servidor que desee en la columna **[!UICONTROL Label]** .
1. Especifique la etiqueta que desee para este servidor.
1. En la lista desplegable **[!UICONTROL Protocol]** , seleccione el protocolo deseado: **FTP**.

   >[!NOTE]
   >
   >Se recomienda utilizar [!DNL Amazon S3] como método para obtener archivos de y enviar archivos a los socios. [!DNL Amazon S3] proporciona una interfaz de servicios web sencilla que se puede utilizar para almacenar y recuperar cualquier cantidad de datos, en cualquier momento y desde cualquier lugar de la web. Para obtener más información, consulte [Acerca de Amazon S3](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html) en la *Guía del usuario Audience Manager*.

1. Rellene los campos:

   * **[!UICONTROL Type]:** seleccione el tipo de cifrado deseado:  **[!UICONTROL SFTP]** o  **[!UICONTROL FTPs/TLS]**.
   * **[!UICONTROL Domain]:** especifique el dominio (host) deseado para este servidor.
   * **[!UICONTROL Port]:** especifique el puerto deseado para este servidor. El puerto predeterminado se muestra para cada tipo de cifrado. Si es necesario, puede cambiar el puerto predeterminado.
   * **[!UICONTROL Remote Path]:** especifique la ruta remota que desee para este servidor. Si deja este campo vacío, el Audience Manager coloca los archivos en el directorio predeterminado.
   * **[!UICONTROL .tmp File Rename on Completion]:** Active esta opción para cambiar el nombre del  `.tmp` archivo una vez finalizado.
   * **[!UICONTROL Filename Suffix]:** especifique el texto que desea anexar para transferir archivos.
   * **[!UICONTROL Moved to When Finished]:** especifique la ruta a la ubicación en la que desea que se mueva el archivo de transferencia al completarse.
   * **[!UICONTROL Authentication]:** Especifique el método de autenticación de servidor deseado:  **[!UICONTROL Username/Password]** o  **[!UICONTROL SSH Key]**.

   >[!NOTE]
   >
   >Recuerde agregar nuestra salida [!DNL FTP] [!DNL IP] a su lista de IP permitidas : **52.44.29.204**.

1. Para la autenticación **[!UICONTROL SSH Key]**:
   >[!NOTE]
   >
   >Al configurar la autenticación de clave SSH, asegúrese de generar siempre las claves pública y privada solo en formato OpenSSH.
   1. Genere el par de clave pública/privada desde cualquier equipo [!DNL Linux] o [!DNL Mac].
   1. Asigne la **clave pública** al cliente para actualizar en su servidor [!DNL SFTP]. Deben incluir todo el texto de la clave pública de su servidor, incluidos `-----BEGIN RSA PRIVATE KEY-----` y `-----END RSA PRIVATE KEY-----` . A cambio, deben proporcionar el nombre de usuario bajo el cual están instalando la clave.
   1. Actualice el campo de nombre de usuario con el proporcionado por el cliente y el campo de clave con la **clave privada**.
1. Haga clic en **[!UICONTROL Create]** si está creando un nuevo servidor o haga clic en **[!UICONTROL Update]** si está editando un servidor existente.
