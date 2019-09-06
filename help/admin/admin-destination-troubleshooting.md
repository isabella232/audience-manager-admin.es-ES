---
description: Información para ayudarle a configurar destinos en Audience Manager y evitar problemas comunes.
seo-description: Información para ayudarle a configurar destinos en Audience Manager y evitar problemas comunes.
seo-title: Solución de problemas de configuración de destinos
title: Solución de problemas de configuración de destinos
uuid: 04080 fb 9-6 c 7 b -4 de 7-960 e -54482 be 2 de 83
translation-type: tm+mt
source-git-commit: 118e8fa3f35bc77846c6518268448d57d779a2ee

---


# Solución de problemas de configuración de destinos {#destination-setup-troubleshooting}

Información para ayudarle a configurar destinos en Audience Manager y evitar problemas comunes.

## Configuro un destino, pero no veo ningún archivo. ¿Dónde están? {#destination-no-files}

<!-- c_dest_tshooting.xml -->

Los problemas comunes de configuración de destino incluyen los siguientes problemas:

### Destino mal configurado

* **Clave incorrecta[!UICONTROL UserID]:** [!UICONTROL UserID] La clave es el [!UICONTROL MasterDPID] de este destino y es la base de los valores de ID que se van a filtrar. Aunque se pueda seleccionar una [!UICONTROL UserID] clave mediante la lista desplegable, no necesariamente significa que hay ID/características/segmentos asignados a este valor. Si [!UICONTROL Outbound] el proceso (que se ejecuta después de los destinos se crea) no encuentra ningún usuario asignado a esta [!UICONTROL UserID] clave, no se habrá ningún dato disponible.
* **No se seleccionaron las fuentes de datos de archivo:** Al elegir cualquier tipo de destino diferente [!UICONTROL S2S]de, aparece una sección en la parte inferior de la pantalla etiquetada [!UICONTROL Configure Data Sources]. Cuando aparece la primera sección, no se selecciona ningún valor. Si olvida hacer clic en [!UICONTROL All First Party] la casilla de verificación o selecciona fuentes de datos individuales desde [!UICONTROL Available Data Sources] la ventana, no habrá datos salientes.

### Formato mal configurado

Al seleccionar un formato para los datos salientes, es mejor, si es posible, volver a utilizar un formato existente. El uso de un formato ya comprobado garantiza que los datos salientes se generarán correctamente. Para ver exactamente cómo se aplica formato a un formato existente, haga clic [!UICONTROL Formats] en la opción de la barra de menús y busque su formato por nombre o por número de ID. Los formatos o macros incorrectos utilizados en formatos proporcionan resultados de formato incorrecto o evitarán que la información se muestre completamente.

Para obtener más información sobre la configuración de formatos y el uso de macros, consulte [Macros de formato de archivo](formats/file-formats.md#) y [Macros de formato HTTP](formats/web-formats.md).

### Servidor mal configurado

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * No introduzca prefijos para los nombres de host. Si tiene una cuenta [!DNL ftp://hello.com], simplemente ingrese [!DNL hello.com] en este campo.
   * **[!UICONTROL Port/Type Combination]**
      * Para una [!DNL FTP] transferencia, el tipo de transferencia preferido [!DNL SFTP]es.
      * Al seleccionar el [!DNL SFTP] tipo, el puerto es casi siempre 22.
      * Al seleccionar el [!DNL FTPs/TLS] tipo, el puerto es casi siempre 21.
      * [!DNL FTPs/TLS] El tipo no es lo mismo que [!DNL FTP] una transferencia regular. No admitimos [!DNL FTP] transferencias regulares (no seguras).
   * **[!UICONTROL Remote Path]**
      * Al elegir una subruta remota, debe introducirse sin barra diagonal inicial.
      * Si el archivo transferido debe colocarse en la [!DNL (root)/inbound] subcarpeta, simplemente agregue [!DNL inbound] para la ruta remota, no [!DNL /inbound].
      * Si envía varios directorios a través de la ruta, introduzca barras diagonales entre cada directorio. Si tiene la ubicación de [!DNL /inbound/subdirectory1/subdirectory2], debe ingresar [!DNL inbound/subdirectory1/subdirectory2] en este campo.
      * Si el archivo debe colocarse en el directorio automáticamente enrutado por el servidor externo, puede dejar este espacio en blanco. No introduzca un punto (. ), barra inclinada (/) o cualquier otra cosa.

* **[!DNL S3]**
   * [!DNL S3] es el protocolo de transferencia preferido (sobre [!DNL FTP] o [!DNL HTTP]).
      * **[!UICONTROL Bucket]**
         * El nombre del bucket debe aparecer sin barras, prefijos, sufijos, etc. Si tiene la dirección [!DNL s3://your-bucket] , simplemente debe agregar [!DNL your-bucket] a este campo.
      * **[!UICONTROL Directory]**
         * Deje este campo en blanco a menos que se le asigne específicamente un subdirectorio en el que se deben colocar los datos. Si tiene la dirección [!DNL s3://your-bucket/your-subdirectory], introduzca [!DNL your-bucket] en [!UICONTROL Bucket] el campo y [!DNL your-subdirectory] debe agregarse al [!UICONTROL Directory] campo. No agregue barras anteriores.
         * Si tiene que recorrer varios directorios por la ruta, solo debería utilizar barras diagonales como separadores. Así, una ubicación tendría [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2][!DNL your-bucket] en [!UICONTROL Bucket] el campo y [!DNL your-subdirectory1/your-subdirectory2] se introduciría en [!UICONTROL Directory] el campo.
      * **[!UICONTROL Access / Secret Keys]**
         * Cuando [!DNL TechOps] crea un bloque y proporciona claves de acceso/secreto a un asesor, dichas credenciales suelen `READ-ONLY` ser credenciales que se han diseñado para enviarse al cliente. Estas credenciales no deben ingresarse en [!UICONTROL Access / Secret Key] los campos porque esto provocará que la transferencia falle (ya que dichas credenciales son de solo lectura, no de escritura). En caso de [!DNL TechOps] crear un bloque y proporcionar credenciales, el asesor también debe solicitar un par de claves de Adobe (NO DEBE PROPORCIONARSE AL CLIENTE) que permita escribir archivos en este bucket. Dicha clave debe agregarse a estos campos.

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * Introduzca la información de prefijo para [!DNL HTTP] entradas. Si tiene una cuenta [!DNL https://superduper.com], introduzca [!DNL https://superduper.com] en este campo.
      * **[!UICONTROL URL Prefix]**
         * Al agregar [!DNL URL] un prefijo, deje desactivada la barra diagonal anterior. Una dirección de [!DNL https://hello.com/r/x/y/z] should have [!DNL https://hello.com] entered in the [!UICONTROL Domain] field and [!DNL r/x/y/z] entered here in the [!UICONTROL URL Prefix] field.
         * Si no [!UICONTROL URL Prefix] se necesita, deje este valor en blanco.
      * **[!UICONTROL Authentication - SSH Key]**
         * Introduzca el valor `SSH PRIVATE` de clave completa en este cuadro, incluidos encabezados, pies de página y saltos de línea para garantizar un almacenamiento preciso o clave.

### Tiempo insuficiente para la generación saliente

El proceso de salida hacia otro sitio se ejecuta dos veces al día y varios procesos (outbounding, publishing, push to external locations, etc.) debe ejecutarse antes de que se inserte un archivo en su destino final. Una buena regla es que un destino debe configurarse completamente al menos 24 horas antes de que se espere que los datos se inserten en una ubicación externa.

### Tamaños de división de archivos demasiado grandes

Cuando se outbounding to destinations, you can split major outbound files in file chunks. Asegúrese de que los fragmentos de archivo individuales no excedan los 10 GB. Consulte también Nombre del archivo de datos [saliente: Sintaxis y ejemplos](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html).


## Cómo configurar los destinos para exportar ID de Experience Cloud, ID de cliente o ID de Audience Manager en archivos de datos salientes {#set-up-destinations-export}

Esta página muestra cómo configurar los destinos para exportar los datos con el tipo de ID que desee.[!UICONTROL Outbound Data Files]

<!-- set-up-destinations-mcid-aamid.xml -->

Los destinos permiten a nuestros clientes activar sus datos en cualquier número de canales digitales. Por ejemplo, pueden exportar datos de audiencia a otras [!DNL Adobe Experience Cloud] soluciones ([!DNL Target], [!DNL Campaign]etc.). O bien, pueden enviar datos a [!UICONTROL DSP]s, [!UICONTROL SSP]s o cualquier plataforma que esté integrada con Audience Manager. Mantenemos una lista de socios con los que trabajamos en nuestra [página de Integraciones Wiki](https://wiki.corp.adobe.com/display/MCPI).

>[!NOTE]
>
>Para obtener una descripción detallada sobre la creación de destinos en la interfaz de usuario de administración, consulte [el artículo Crear o editar destinos](companies/admin-manage-company-destinations.md#create-edit-company-destinations) de empresa.

Los clientes desean exportar distintos tipos de ID según el destino. El gráfico de configuración siguiente muestra las opciones que debe seleccionar para exportar información de perfil relacionada con distintos tipos de ID. También le recomendamos que consulte [el índice de ID de Audience Manager](https://marketing.adobe.com/resources/help/en_US/aam/ids-in-aam.html). Hay tres opciones importantes que considerar: la [!UICONTROL User ID Key], la [!UICONTROL Data Source Type] , la y [!UICONTROL Format]la. A continuación se detallan todos los detalles.

* [!UICONTROL User ID Key]. En [!UICONTROL Admin UI], vaya **[!UICONTROL Companies]** a. Busque la empresa de su cliente y haga clic en ella. Busque **[!UICONTROL Destinations]** la ficha y pulse **[!UICONTROL Add Destination]**. En **[!UICONTROL Add Destination]** el flujo de trabajo, seleccione la [!UICONTROL User ID Key]. El filtro filtrará [!UICONTROL User ID Key] los ID entrantes del origen de datos objetivo y solo permitirá que se pasen los ID.

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]. Seleccione esta opción al crear un destino en la interfaz de usuario de Audience Manager. Primero, seleccione [!UICONTROL Inbound]y seleccione el tipo de ID que desee. Las opciones son:

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]. Esta opción determina el formato de archivo que va a exportar. En **[!UICONTROL Add Destination]** el flujo de trabajo, en **[!UICONTROL Batch Data]**, seleccione el formato.

Para inspeccionar un formato, vaya **[!UICONTROL Admin UI > Formats]** y busque [!UICONTROL Data Row] el elemento. Este elemento contiene una macro del formato de archivo, &lt; MCID &gt; en el ejemplo siguiente.

![](assets/data_row.PNG)

<table id="table_DAEE5BC75DCB4FC690C4BAE41F627DEC"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> Configuración No. </th> 
   <th colname="col1" class="entry"> <p>Clave del usuario </p> </th> 
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
   <td colname="col3"> <p>&lt; DP_ UUID &gt; </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 2 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>UUID de Audience Manager </p> </td> 
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
   <td colname="col3"> <p>&lt; DP_ UUID &gt; </p> </td> 
   <td colname="col4"> <p>UUID de Audience Manager </p> </td> 
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
   <td colname="col4"> <p>UUID de Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 7 </td> 
   <td colname="col1"> <p>DPID (cualquier fuente de datos a la que la empresa tenga acceso) </p> </td> 
   <td colname="col2"> <p>Customer ID </p> </td> 
   <td colname="col3"> <p>&lt; DP_ UUID &gt; </p> </td> 
   <td colname="col4"> <p>ID de cliente (DPUUID) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 8 </td> 
   <td colname="col1"> <p>DPID (cualquier fuente de datos a la que la empresa tenga acceso) </p> </td> 
   <td colname="col2"> <p>Customer ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 9 </td> 
   <td colname="col1"> <p>DPID (cualquier fuente de datos a la que la empresa tenga acceso) </p> </td> 
   <td colname="col2"> <p>Customer ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>UUID de Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 10 </td> 
   <td colname="col1"> <p>DPID (cualquier fuente de datos a la que la empresa tenga acceso) </p> </td> 
   <td colname="col2"> <p>ID de Audience Manager </p> </td> 
   <td colname="col3"> <p>&lt; DP_ UUID &gt; </p> </td> 
   <td colname="col4"> <p>UUID de Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID (cualquier fuente de datos a la que la empresa tenga acceso) </p> </td> 
   <td colname="col2"> <p>ID de Audience Manager </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 12 </td> 
   <td colname="col1"> <p>DPID (cualquier fuente de datos a la que la empresa tenga acceso) </p> </td> 
   <td colname="col2"> <p>ID de Audience Manager </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>UUID de Audience Manager </p> </td> 
  </tr> 
 </tbody> 
</table>

## Casos de uso

Supongamos que usa Audience Manager y [!DNL Campaign]. Para hacer que los datos del cliente sean procesables, [!DNL Campaign]quiere exportar [!UICONTROL Experience Cloud IDs]. En este caso, debe utilizar el número 3 de configuración.