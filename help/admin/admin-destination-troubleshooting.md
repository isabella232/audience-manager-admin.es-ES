---
description: Información para configurar destinos en Audience Manager y evitar problemas comunes.
seo-description: Información para configurar destinos en Audience Manager y evitar problemas comunes.
seo-title: ' Solución de problemas de configuración de destino'
title: ' Solución de problemas de configuración de destino'
uuid: 04080fb9-6c7b-4de7-960e-54482be2de83
translation-type: tm+mt
source-git-commit: 118e8fa3f35bc77846c6518268448d57d779a2ee

---


# Solución de problemas de configuración de destino {#destination-setup-troubleshooting}

Información para configurar destinos en Audience Manager y evitar problemas comunes.

## Configuré un destino, pero no veo ningún archivo. ¿Dónde están? {#destination-no-files}

<!-- c_dest_tshooting.xml -->

Los problemas comunes de configuración de destino incluyen los siguientes:

### Destino mal configurado

* **[!UICONTROL UserID]Clave** incorrecta: La [!UICONTROL UserID] clave es la [!UICONTROL MasterDPID] de este destino y es la base para los valores de ID que se sobrepasarán. Aunque una [!UICONTROL UserID] clave se pueda seleccionar mediante la lista desplegable, no significa necesariamente que haya ID, características o segmentos asignados a este valor. Si el [!UICONTROL Outbound] proceso (que se ejecuta después de crear los destinos) no encuentra ningún usuario asignado a esta [!UICONTROL UserID] clave, no se devolverá ningún dato.
* **** No En Las Fuentes De Datos De Archivos Seleccionadas: Al elegir cualquier tipo de destino que no sea [!UICONTROL S2S], aparece una sección en la parte inferior de la pantalla con la etiqueta [!UICONTROL Configure Data Sources]. Cuando esta sección aparece por primera vez, no se seleccionan valores. Si olvida hacer clic en la casilla de verificación o seleccionar las fuentes de datos de forma individual desde la [!UICONTROL All First Party] [!UICONTROL Available Data Sources] ventana, no se devolverá ningún dato.

### Formato mal configurado

Al seleccionar un formato para los datos salientes, lo mejor es, si es posible, reutilizar un formato existente. El uso de un formato ya probado garantiza que los datos salientes se generarán correctamente. Para ver exactamente cómo se formatea un formato existente, haga clic en la [!UICONTROL Formats] opción de la barra de menús y busque el formato por nombre o por número de ID. Los formatos o macros con formato incorrecto utilizados en los formatos proporcionan una salida con formato incorrecto o evitan que la información se muestre por completo.

Para obtener más información sobre la configuración de formatos y el uso de macros, consulte Macros [de formato](formats/file-formats.md#) de archivo y Macros [de formato](formats/web-formats.md)HTTP.

### Servidor no configurado

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * No introduzca prefijos para nombres de host. Si tiene una cuenta [!DNL ftp://hello.com], simplemente ingrese [!DNL hello.com] en este campo.
   * **[!UICONTROL Port/Type Combination]**
      * Para una [!DNL FTP] transferencia, el tipo de transferencia preferido es [!DNL SFTP].
      * Al seleccionar el [!DNL SFTP] tipo, el puerto es casi siempre 22.
      * Al seleccionar el [!DNL FTPs/TLS] tipo, el puerto es casi siempre 21.
      * El [!DNL FTPs/TLS] tipo no es el mismo que una [!DNL FTP] transferencia normal. No apoyamos transferencias regulares (no seguras) [!DNL FTP] .
   * **[!UICONTROL Remote Path]**
      * Al elegir una subruta remota, debe introducirse sin barra diagonal inicial.
      * Si se supone que el archivo transferido se debe colocar en la [!DNL (root)/inbound] subcarpeta, simplemente agregue [!DNL inbound] la ruta remota, no [!DNL /inbound].
      * Si envía los archivos a varios directorios por la ruta, introduzca barras entre cada directorio. Si tiene la ubicación de [!DNL /inbound/subdirectory1/subdirectory2], debe introducir [!DNL inbound/subdirectory1/subdirectory2] en este campo.
      * Si el servidor externo debe colocar el archivo en el directorio al que se enruta automáticamente, puede dejar este espacio en blanco. No escriba un punto ( . ), barra ( / ) o cualquier otra cosa.

* **[!DNL S3]**
   * [!DNL S3] es el protocolo de transferencia preferido (sobre [!DNL FTP] o [!DNL HTTP]).
      * **[!UICONTROL Bucket]**
         * El nombre del bloque debe aparecer sin barras, prefijos, sufijos, etc. Si se le da la dirección [!DNL s3://your-bucket] debe simplemente agregarla [!DNL your-bucket] a este campo.
      * **[!UICONTROL Directory]**
         * Deje este campo en blanco a menos que se le proporcione específicamente un subdirectorio en el cual se deben colocar los datos. Si se le da la dirección [!DNL s3://your-bucket/your-subdirectory], introduzca [!DNL your-bucket] en el [!UICONTROL Bucket] campo y [!DNL your-subdirectory] debe agregarse al [!UICONTROL Directory] . No agregue barras inclinadas anteriores.
         * Si tiene que recorrer varios directorios por la ruta, sólo entonces debe utilizar barras diagonales como separadores. Entonces una ubicación de [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] habría [!DNL your-bucket] en el [!UICONTROL Bucket] campo y [!DNL your-subdirectory1/your-subdirectory2] entraría en el [!UICONTROL Directory] campo.
      * **[!UICONTROL Access / Secret Keys]**
         * Cuando [!DNL TechOps] crea un bloque y proporciona claves de acceso/secreto a un consultor, estas credenciales suelen ser `READ-ONLY` credenciales que deben entregarse al cliente. Estas credenciales no se deben introducir en los [!UICONTROL Access / Secret Key] campos, ya que esto provocará que la transferencia falle (porque esas credenciales son de sólo lectura, no se pueden escribir). En el caso de que [!DNL TechOps] cree un bucket y proporcione credenciales, el consultor también debe solicitar un par de claves de Adobe (NO SE LE DEBE DAR AL CLIENTE) que permita escribir archivos en este bucket. Esa clave debe agregarse a estos campos.

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * Escriba la información de prefijo de [!DNL HTTP] las entradas. Si tiene una cuenta [!DNL https://superduper.com], escriba [!DNL https://superduper.com] en este campo.
      * **[!UICONTROL URL Prefix]**
         * Al agregar un [!DNL URL] prefijo, deje la barra anterior desactivada. Una dirección de [!DNL https://hello.com/r/x/y/z] debe haber [!DNL https://hello.com] ingresado en el [!UICONTROL Domain] campo y [!DNL r/x/y/z] ingresado aquí en el [!UICONTROL URL Prefix] campo.
         * Si no [!UICONTROL URL Prefix] es necesario, deje este valor en blanco.
      * **[!UICONTROL Authentication - SSH Key]**
         * Escriba el valor `SSH PRIVATE` clave completo en este cuadro, incluidos los encabezados, pies de página y saltos de línea, para garantizar un cifrado y almacenamiento de claves precisos.

### Tiempo insuficiente para la generación saliente

El proceso de salida se ejecuta dos veces al día y varios procesos (salida, publicación, inserción a ubicaciones externas, etc.) debe ejecutarse antes de que se envíe un archivo a su destino final. Una buena regla general es que un destino debe configurarse completamente al menos 24 horas antes de que pueda esperar que los datos se inserten en una ubicación externa.

### Los tamaños de división de archivos son demasiado grandes

Al exportar archivos a destinos, puede dividir archivos salientes más grandes en fragmentos de archivos. Asegúrese de que los fragmentos de archivos individuales no superen los 10 GB. Consulte también Nombre del archivo de datos [de salida: Sintaxis y ejemplos](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html).


## Cómo configurar sus destinos para exportar ID de Experience Cloud, ID de cliente o ID de Audience Manager en archivos de datos de salida {#set-up-destinations-export}

En esta página se muestra cómo configurar destinos para exportar datos con claves del tipo de ID que desee [!UICONTROL Outbound Data Files].

<!-- set-up-destinations-mcid-aamid.xml -->

Los destinos permiten a nuestros clientes activar sus datos en cualquier número de canales digitales. Por ejemplo, pueden exportar datos de audiencia a otras [!DNL Adobe Experience Cloud] soluciones ([!DNL Target], [!DNL Campaign], etc.). O bien, podrían enviar datos a [!UICONTROL DSP]s, [!UICONTROL SSP]s o cualquier plataforma integrada con Audience Manager. Mantenemos una lista de socios con los que trabajamos en nuestra página [Wiki de](https://wiki.corp.adobe.com/display/MCPI)Integraciones.

>[!NOTE]
>
>Para obtener un tutorial detallado sobre la creación de destinos en la interfaz de usuario del administrador, consulte el artículo [Crear o editar destinos](companies/admin-manage-company-destinations.md#create-edit-company-destinations) de empresa.

Los clientes desean exportar distintos tipos de ID, según el destino. El gráfico de configuración siguiente muestra las opciones que debe seleccionar para exportar la información de perfil relacionada con diferentes tipos de ID. También le recomendamos que consulte el [índice de ID en Audience Manager](https://marketing.adobe.com/resources/help/en_US/aam/ids-in-aam.html). Hay tres configuraciones importantes que considerar: la [!UICONTROL User ID Key], la [!UICONTROL Data Source Type] y la [!UICONTROL Format]. Los detallamos a continuación.

* [!UICONTROL User ID Key]. En el [!UICONTROL Admin UI], vaya a **[!UICONTROL Companies]**. Busque la empresa de su cliente y haga clic en ella. Busque la **[!UICONTROL Destinations]** ficha y presione **[!UICONTROL Add Destination]**. En el **[!UICONTROL Add Destination]** flujo de trabajo, seleccione el [!UICONTROL User ID Key]. El [!UICONTROL User ID Key] filtro filtrará los ID entrantes del origen de datos de destino y solo permitirá que los ID se pasen.

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]. Seleccione esta opción al crear un destino en la interfaz de usuario de Audience Manager. En primer lugar, seleccione [!UICONTROL Inbound]y luego el tipo de ID que desee. Las opciones son:

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]. Esta opción determina el formato de archivo que se va a exportar. En el **[!UICONTROL Add Destination]** flujo de trabajo, en **[!UICONTROL Batch Data]**, seleccione el formato.

Para inspeccionar un formato, vaya a **[!UICONTROL Admin UI > Formats]** y busque el [!UICONTROL Data Row] elemento. Este elemento contiene una macro del formato de archivo, &lt;MCID&gt; en el ejemplo siguiente.

![](assets/data_row.PNG)

<table id="table_DAEE5BC75DCB4FC690C4BAE41F627DEC"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> Nº configuración </th> 
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
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
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
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>ID del cliente (DPUUID) </p> </td> 
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
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
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

Supongamos que utiliza Audience Manager y [!DNL Campaign]. Para que los datos del cliente sean procesables en [!DNL Campaign], debe exportar [!UICONTROL Experience Cloud IDs]. En este caso, debe utilizar el número de configuración 3.