---
description: Utilice la página Formatos de la herramienta de administración de Audience Manager para crear un nuevo formato o editar uno existente.
seo-description: Use the Formats page in the Audience Manager Admin tool to create a new format or to edit an existing format.
seo-title: Create or Edit a Format
title: Crear o editar un formato
uuid: ca1b1feb-bcd3-4a41-b1e8-80565f6c23ae
exl-id: 3c97d1e9-8093-4181-a1fd-fb1816cdaa3d
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 3%

---

# Crear o editar un formato {#create-or-edit-a-format}

Utilice el [!UICONTROL Formats] en la herramienta de administración de Audience Manager para crear un nuevo formato o editar un formato existente.

<!-- t_create_format.xml -->

>[!TIP]
>
>Al seleccionar un formato para los datos salientes, es mejor, si es posible, reutilizar un formato existente. El uso de un formato ya comprobado garantiza que los datos salientes se generen correctamente. Para ver exactamente el formato de un formato existente, haga clic en [!UICONTROL Formats] opción de la barra de menús y busque el formato por nombre o por número de ID. Los formatos o macros mal formados utilizados en formatos proporcionarán resultados con formato incorrecto o evitarán que la información se emita completamente.

1. Para crear un nuevo formato, haga clic en **[!UICONTROL Formats]** > **[!UICONTROL Add Format]**. Para editar un formato existente, haga clic en el formato deseado en la **[!UICONTROL Name]** columna.

   ![](assets/create_format.png)

1. Rellene los campos:
   * **Nombre:** (Obligatorio) Proporcione un nombre descriptivo para el formato.
   * **Tipo:** (Obligatorio) Seleccione el formato que desee:
      * **[!UICONTROL File]**: envía datos mediante [!DNL FTP] archivos.
      * **[!UICONTROL HTTP]**: incluye datos en una [!DNL JSON] envoltorio.

1. (Condicional) Si elige **[!UICONTROL File]**, rellene los campos:

   >[!NOTE]
   >
   >Para ver una lista de las macros disponibles, consulte [Macros de formato de archivo](../formats/file-formats.md#concept_A867101505074418A58DE325949E5089) y [Macros de formato HTTP](../formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE).

   * **[!UICONTROL File Name]:** Especifique el nombre del archivo de transferencia de datos.
   * **Encabezado:** Especifique el texto que aparece en la primera fila del archivo de transferencia de datos.
   * **[!UICONTROL Data Row]:** Especifique el texto que aparece en cada fila saliente del archivo.
   * **[!UICONTROL Maximum File Size (In MB)]:** Especifique el tamaño máximo de archivo para los archivos de transferencia de datos. Los archivos comprimidos deben tener menos de 100 MB. No hay límite en el tamaño de archivo sin comprimir.
   * **[!UICONTROL Compression]:** Seleccione el tipo de compresión deseado: gz o zip para los archivos de datos. Para envío a [!UICONTROL AWS S3], debe utilizar archivos .gz o sin comprimir.
   * **[!UICONTROL .info Receipt]:** Especifica que un control de transferencia ([!DNL .info]) se genera el archivo. El [!DNL .info] proporciona información de metadatos sobre las transferencias de archivos para que los socios puedan comprobar que Audience Manager ha gestionado las transferencias de archivos correctamente. Para obtener más información, consulte [Archivos de transferencia y control para transferencias de archivos de registro](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/transfer-control-files.html?lang=en).
   * **[!UICONTROL MD5 Checksum Receipt]:** Especifica que una [!DNL MD5] se genera el cobro de suma de comprobación. El [!DNL MD5] recibo de suma de comprobación para que los socios puedan comprobar que el Audience Manager ha gestionado correctamente la transferencia completa.

1. (Condicional) Si elige **[!UICONTROL HTTP]**, rellene los campos:

   * **[!UICONTROL Method]:** Elija la [!DNL API] método que desea utilizar para el proceso de transferencia:
      * **[!UICONTROL POST]:** Si selecciona [!DNL POST], seleccione el tipo de contenido ([!DNL XML] o [!DNL JSON]) y, a continuación, especifique el cuerpo de la solicitud.
      * **[!UICONTROL GET]:** Si selecciona [!DNL GET], especifique los parámetros de consulta.

1. Clic **[!UICONTROL Create]** si está creando un nuevo formato, o haga clic en **[!UICONTROL Save Updates]** si está editando un formato existente.

## Eliminar un formato {#delete-format}

1. Haga clic **[!UICONTROL Formats]**.
2. Clic  ![](assets/icon_delete.png) en el **[!UICONTROL Actions]** del formato deseado.
3. Clic **[!UICONTROL OK]** para confirmar la eliminación.
