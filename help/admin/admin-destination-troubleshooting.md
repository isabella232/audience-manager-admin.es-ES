---
description: Información para configurar destinos en Audience Manager y evitar problemas comunes.
seo-description: Information to help you set up destinations in Audience Manager and avoid common problems.
seo-title: Destination Setup Troubleshooting
title: Solución de problemas de configuración de destino
uuid: 04080fb9-6c7b-4de7-960e-54482be2de83
exl-id: 53c72b1a-f1a1-4266-a595-e4821c2640b2
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '1316'
ht-degree: 4%

---

# Solución de problemas de configuración de destino {#destination-setup-troubleshooting}

Información para configurar destinos en Audience Manager y evitar problemas comunes.

## He configurado un destino, pero no veo ningún archivo. ¿Dónde están? {#destination-no-files}

<!-- c_dest_tshooting.xml -->

Los problemas comunes de configuración de destino incluyen los siguientes:

### Destino mal configurado

* **Incorrecto [!UICONTROL UserID] Clave:** El [!UICONTROL UserID] La clave es [!UICONTROL MasterDPID] de este destino y es la base de los valores de ID que se eliminarán. Incluso si un [!UICONTROL UserID] se puede seleccionar mediante la lista desplegable; no significa necesariamente que haya ID, rasgos o segmentos asignados a este valor. Si la variable [!UICONTROL Outbound] El proceso de (que se ejecuta después de crear los destinos de ) no encuentra ningún usuario asignado a esto [!UICONTROL UserID] clave, no se saldrán datos.
* **No Se Ha Seleccionado Ningún Elemento En Las Fuentes De Datos De Archivo:** Al elegir cualquier tipo de destino distinto de [!UICONTROL S2S], aparecerá una sección en la parte inferior de la pantalla con la etiqueta [!UICONTROL Configure Data Sources]. Cuando aparece esta sección por primera vez, no se selecciona ningún valor. Si olvida hacer clic en [!UICONTROL All First Party] o seleccione individualmente las fuentes de datos de la [!UICONTROL Available Data Sources] ventana, no se saldrán datos.

### Formato mal configurado

Al seleccionar un formato para los datos salientes, es mejor, si es posible, reutilizar un formato existente. El uso de un formato ya comprobado garantiza que los datos salientes se generen correctamente. Para ver exactamente el formato de un formato existente, haga clic en [!UICONTROL Formats] opción de la barra de menús y busque el formato por nombre o por número de ID. Los formatos o macros mal formados utilizados en formatos proporcionarán resultados con formato incorrecto o evitarán que la información se emita completamente.

Para obtener más información sobre la configuración de formatos y el uso de macros, consulte [Macros de formato de archivo](formats/file-formats.md#) y [Macros de formato HTTP](formats/web-formats.md).

### Servidor mal configurado

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * No introduzca prefijos para nombres de host. Si se le da una cuenta [!DNL ftp://hello.com], simplemente introduzca [!DNL hello.com] en este campo.
   * **[!UICONTROL Port/Type Combination]**
      * Para un [!DNL FTP] transferencia, el tipo de transferencia preferido es [!DNL SFTP].
      * Al seleccionar la variable [!DNL SFTP] Tipo, el puerto es casi siempre 22.
      * Al seleccionar la variable [!DNL FTPs/TLS] Tipo, el puerto es casi siempre 21.
      * El [!DNL FTPs/TLS] el tipo no es lo mismo que un normal [!DNL FTP] transferencia. No se admiten los mensajes regulares (no seguros) [!DNL FTP] transferencias.
   * **[!UICONTROL Remote Path]**
      * Al elegir un subtrazado remoto, debe introducirse sin barra diagonal.
      * Si se supone que el archivo transferido debe colocarse en la [!DNL (root)/inbound] subcarpeta, simplemente añada [!DNL inbound] para la ruta remota, no [!DNL /inbound].
      * Si envía los archivos a varios directorios por la ruta, introduzca barras oblicuas entre cada directorio. Si se le da la ubicación de [!DNL /inbound/subdirectory1/subdirectory2], debe introducir [!DNL inbound/subdirectory1/subdirectory2] en este campo.
      * Si el archivo debe colocarse en el directorio al que el servidor externo dirige automáticamente, puede dejar este espacio en blanco. No introduzca ningún punto ( . ), barra diagonal ( / ) o cualquier otra cosa.

* **[!DNL S3]**
   * [!DNL S3] es el protocolo de transferencia preferido (antes de [!DNL FTP] o [!DNL HTTP]).
      * **[!UICONTROL Bucket]**
         * El nombre del contenedor debe aparecer sin barras diagonales, prefijos, sufijos, etc. Si te dan la dirección [!DNL s3://your-bucket] simplemente debe añadir [!DNL your-bucket] a este campo.
      * **[!UICONTROL Directory]**
         * Deje este campo en blanco a menos que se le proporcione específicamente un subdirectorio en el que se deben colocar los datos. Si te dan la dirección [!DNL s3://your-bucket/your-subdirectory], introduzca [!DNL your-bucket] en el [!UICONTROL Bucket] field y [!DNL your-subdirectory] debe añadirse a la [!UICONTROL Directory] field. No agregue las barras diagonales precedentes.
         * Si tiene que recorrer varios directorios por la ruta, solo entonces debe utilizar barras oblicuas como separadores. Así que una ubicación de [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] hubiera tenido [!DNL your-bucket] en el [!UICONTROL Bucket] field y [!DNL your-subdirectory1/your-subdirectory2] entró en la [!UICONTROL Directory] field.
      * **[!UICONTROL Access / Secret Keys]**
         * Cuándo [!DNL TechOps] crea un contenedor y proporciona claves de acceso/secretas a un consultor. Estas credenciales suelen ser `READ-ONLY` credenciales que están pensadas para entregarse al cliente. Estas credenciales no deben introducirse en la variable [!UICONTROL Access / Secret Key] porque esto provocará que la transferencia falle (porque esas credenciales son de solo lectura, no se pueden escribir). En el caso en que [!DNL TechOps] crea un contenedor y proporciona credenciales, el consultor también debe solicitar un par de claves de Adobe (QUE NO SE DEBE PROPORCIONAR AL CLIENTE) que permita escribir archivos en este contenedor. Esa clave debe añadirse a estos campos.

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * Especifique la información de prefijo para [!DNL HTTP] entradas. Si se le da una cuenta [!DNL https://superduper.com], introduzca [!DNL https://superduper.com] en este campo.
      * **[!UICONTROL URL Prefix]**
         * Al añadir un [!DNL URL] , deje la barra anterior desactivada. Una dirección de [!DNL https://hello.com/r/x/y/z] debería tener [!DNL https://hello.com] introducido en el [!UICONTROL Domain] field y [!DNL r/x/y/z] ingresado aquí en el [!UICONTROL URL Prefix] field.
         * Si un [!UICONTROL URL Prefix] no es necesario, deje este valor en blanco.
      * **[!UICONTROL Authentication - SSH Key]**
         * Introduzca el valor completo `SSH PRIVATE` valor de clave de este cuadro, incluidos encabezados, pies de página y saltos de línea para garantizar un cifrado y un almacenamiento de claves precisos.

### No hay tiempo suficiente para la generación saliente

El proceso saliente se ejecuta dos veces al día y varios procesos (saliente, publicación, transferencia a ubicaciones externas, etc.) debe ejecutarse antes de que un archivo se inserte en su destino final. Una buena regla general es que un destino debe estar completamente configurado al menos 24 horas antes de que pueda esperar que los datos se inserten en una ubicación externa.

### Tamaños de división de archivo demasiado grandes

Al enviar archivos salientes a destinos, puede dividir archivos salientes más grandes en fragmentos de archivo. Asegúrese de que los fragmentos de archivo individuales no superen los 10 GB. Consulte también. [Nombre del archivo de datos de salida: sintaxis y ejemplos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html?lang=en).


## Configuración de los destinos para exportar ID de Experience Cloud, ID de cliente o ID de Audience Manager en archivos de datos salientes {#set-up-destinations-export}

Esta página muestra cómo configurar destinos para exportar datos con claves del tipo de ID que desee en [!UICONTROL Outbound Data Files].

<!-- set-up-destinations-mcid-aamid.xml -->

Los destinos permiten a nuestros clientes activar sus datos en cualquier cantidad de canales digitales. Por ejemplo, pueden exportar datos de audiencia a otros [!DNL Adobe Experience Cloud] soluciones ([!DNL Target], [!DNL Campaign], etc.). O bien, pueden enviar datos a [!UICONTROL DSP]s, [!UICONTROL SSP]s o cualquier plataforma integrada con Audience Manager. Mantenemos una lista de socios con los que trabajamos en nuestro [Página Wiki de integraciones](https://wiki.corp.adobe.com/display/MCPI).

>[!NOTE]
>
>Para ver un tutorial detallado sobre la creación de destinos en la IU de administración, consulte la [Crear o editar destinos de compañía](companies/admin-manage-company-destinations.md#create-edit-company-destinations) artículo.

Los clientes desean exportar distintos tipos de ID según el destino. El gráfico de configuración siguiente muestra las opciones que debe seleccionar para exportar información de perfil relacionada con distintos tipos de ID. Le recomendamos que también consulte la [Índice de ID en el Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html?lang=en). Hay tres configuraciones importantes que hay que tener en cuenta: [!UICONTROL User ID Key], el [!UICONTROL Data Source Type] y el [!UICONTROL Format]. A continuación detallamos todos ellos.

* [!UICONTROL User ID Key]. En el [!UICONTROL Admin UI], vaya a **[!UICONTROL Companies]**. Busque la empresa del cliente y haga clic en ella. Busque la variable **[!UICONTROL Destinations]** y pulse **[!UICONTROL Add Destination]**. En el **[!UICONTROL Add Destination]** flujo de trabajo, seleccione [!UICONTROL User ID Key]. El [!UICONTROL User ID Key] filtrará los ID entrantes de la fuente de datos de destino y solo permitirá que se pasen los ID.

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]. Seleccione esta opción al crear un destino en la interfaz de usuario de Audience Manager. En primer lugar, seleccione [!UICONTROL Inbound]y, a continuación, seleccione el tipo de ID que desee. Las opciones son:

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]. Esta opción determina el formato de archivo que se va a exportar. En el **[!UICONTROL Add Destination]** flujo de trabajo, en **[!UICONTROL Batch Data]**, seleccione el formato.

Para inspeccionar un formato, vaya a **[!UICONTROL Admin UI > Formats]** y busque el [!UICONTROL Data Row] Elemento. Este elemento contiene una macro con el formato de archivo, &lt;mcid> en el ejemplo siguiente.

![](assets/data_row.PNG)

<table id="table_DAEE5BC75DCB4FC690C4BAE41F627DEC"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> Nº de configuración </th> 
   <th colname="col1" class="entry"> <p>Clave de usuario </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo de fuente de datos </p> </th> 
   <th colname="col3" class="entry"> <p>Formato </p> </th> 
   <th colname="col4" class="entry"> <p>Tipo de ID exportado </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> 1 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 2 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>UUID DE AUDIENCE MANAGER </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 3 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 4 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>ID de Audience Manager </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>UUID DE AUDIENCE MANAGER </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 5 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>ID de Audience Manager </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 6 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>ID de Audience Manager </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>UUID DE AUDIENCE MANAGER </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 7 </td> 
   <td colname="col1"> <p>DPID (cualquier fuente de datos a la que la compañía tenga acceso) </p> </td> 
   <td colname="col2"> <p>ID de cliente </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>ID del cliente (DPUUID) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 8 </td> 
   <td colname="col1"> <p>DPID (cualquier fuente de datos a la que la compañía tenga acceso) </p> </td> 
   <td colname="col2"> <p>ID de cliente </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 9 </td> 
   <td colname="col1"> <p>DPID (cualquier fuente de datos a la que la compañía tenga acceso) </p> </td> 
   <td colname="col2"> <p>ID de cliente </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>UUID DE AUDIENCE MANAGER </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 10 </td> 
   <td colname="col1"> <p>DPID (cualquier fuente de datos a la que la compañía tenga acceso) </p> </td> 
   <td colname="col2"> <p>ID de Audience Manager </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>UUID DE AUDIENCE MANAGER </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID (cualquier fuente de datos a la que la compañía tenga acceso) </p> </td> 
   <td colname="col2"> <p>ID de Audience Manager </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 12 </td> 
   <td colname="col1"> <p>DPID (cualquier fuente de datos a la que la compañía tenga acceso) </p> </td> 
   <td colname="col2"> <p>ID de Audience Manager </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>UUID DE AUDIENCE MANAGER </p> </td> 
  </tr> 
 </tbody> 
</table>

## Casos de uso

Digamos que usas Audience Manager y... [!DNL Campaign]. Para que los datos del cliente puedan procesarse en [!DNL Campaign], que desea exportar [!UICONTROL Experience Cloud IDs]. En este caso, debe utilizar el número de configuración 3.
