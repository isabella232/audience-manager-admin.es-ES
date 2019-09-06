---
description: Utilice la página Formatos de la herramienta Administración de Audience Manager para crear un nuevo formato o editar un formato existente.
seo-description: Utilice la página Formatos de la herramienta Administración de Audience Manager para crear un nuevo formato o editar un formato existente.
seo-title: Creación o edición de un formato
title: Creación o edición de un formato
uuid: ca 1 b 1 feb-bcd 3-4 a 41-b 1 e 8-80565 f 6 c 23 ae
translation-type: tm+mt
source-git-commit: 71bf4cec222428686c1eab0998f66887db06da68

---


# Creación o edición de un formato {#create-or-edit-a-format}

Utilice [!UICONTROL Formats] la página de la herramienta de administración de Audience Manager para crear un nuevo formato o editar un formato existente.

<!-- t_create_format.xml -->

>[!TIP]
>
>Al seleccionar un formato para los datos salientes, es mejor, si es posible, volver a utilizar un formato existente. El uso de un formato ya comprobado garantiza que los datos salientes se generarán correctamente. Para ver exactamente cómo se aplica formato a un formato existente, haga clic [!UICONTROL Formats] en la opción de la barra de menús y busque su formato por nombre o por número de ID. Los formatos o macros incorrectos utilizados en formatos proporcionan resultados de formato incorrecto o evitarán que la información se muestre completamente.

1. Para crear un nuevo formato, haga clic **[!UICONTROL Formats]** en &gt; **[!UICONTROL Add Format]**. Para editar un formato existente, haga clic en el formato que desee en **[!UICONTROL Name]** la columna.

   ![](assets/create_format.png)

1. Rellene los campos:
   * **Nombre:** (Obligatorio) Proporcione un nombre descriptivo para el formato.
   * **Tipo:** (Obligatorio) Seleccione el formato que desee:
      * **[!UICONTROL File]**: Envía datos a través [!DNL FTP] de archivos.
      * **[!UICONTROL HTTP]**: Incluye datos en [!DNL JSON] un envoltorio.

1. (Condicional) Si elige **[!UICONTROL File]**, rellene los campos:

   >[!NOTE]
   >
   >Para obtener una lista de macros disponibles, consulte [Macros de formato de archivo](../formats/file-formats.md#concept_A867101505074418A58DE325949E5089) y [Macros de formato HTTP](../formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE).

   * **[!UICONTROL File Name]:** Especifique el nombre de archivo del archivo de transferencia de datos.
   * **Encabezado:** Especifique el texto que aparece en la primera fila del archivo de transferencia de datos.
   * **[!UICONTROL Data Row]:** Especifique el texto que aparece en cada fila saliente del archivo.
   * **[!UICONTROL Maximum File Size (In MB)]:** Especifique el tamaño máximo de archivo para los archivos de transferencia de datos. Los archivos comprimidos deben ser menores que 100 MB. No hay límite en el tamaño de archivo sin comprimir.
   * **[!UICONTROL Compression]:** Seleccione el tipo de compresión que desee: gz o zip para los archivos de datos. Para la entrega a [!UICONTROL AWS S3], debe utilizar archivos.gz o no comprimidos.
   * **[!UICONTROL .info Receipt]:** Especifica que se genera un archivo transfer-control ([!DNL .info]). [!DNL .info] El archivo proporciona información de metadatos sobre las transferencias de archivos para que los socios puedan comprobar que Audience Manager gestiona las transferencias de archivos correctamente. Para obtener más información, consulte [Transferir archivos de control para transferencias de archivos de registro](https://marketing.adobe.com/resources/help/en_US/aam/c_s2s_add_transfer_control_files.html).
   * **[!UICONTROL MD5 Checksum Receipt]:** Especifica que se genera un recibo [!DNL MD5] de suma de comprobación. Recibo [!DNL MD5] de suma de comprobación para que los socios puedan verificar que Audience Manager gestione la transferencia completa correctamente.

1. (Condicional) Si elige **[!UICONTROL HTTP]**, rellene los campos:

   * **[!UICONTROL Method]:** Elija [!DNL API] el método que desee utilizar para el proceso de transferencia:
      * **[!UICONTROL POST]:** Si selecciona [!DNL POST], seleccione el tipo de contenido ([!DNL XML] o [!DNL JSON]) y, a continuación, especifique el cuerpo de la solicitud.
      * **[!UICONTROL GET]:** Si selecciona [!DNL GET], especifique los parámetros de consulta.

1. Haga clic **[!UICONTROL Create]** en si está creando un nuevo formato o si está **[!UICONTROL Save Updates]** editando un formato existente.

## Eliminar un formato {#delete-format}

1. Haga clic en **[!UICONTROL Formats]**.
2. Haga clic en ![](assets/icon_delete.png) la **[!UICONTROL Actions]** columna del formato deseado.
3. Click **[!UICONTROL OK]** to confirm the deletion.
