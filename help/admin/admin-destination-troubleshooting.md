---
description: Información para configurar destinos en Audience Manager y evitar problemas comunes.
seo-description: Information to help you set up destinations in Audience Manager and avoid common problems.
seo-title: Destination Setup Troubleshooting
title: Solución de problemas de configuración de destino
uuid: 04080fb9-6c7b-4de7-960e-54482be2de83
exl-id: 53c72b1a-f1a1-4266-a595-e4821c2640b2
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '1316'
ht-degree: 4%

---

# Solución de problemas de configuración de destino {#destination-setup-troubleshooting}

Información para configurar destinos en Audience Manager y evitar problemas comunes.

## Configuré un destino, pero no veo ningún archivo. ¿Dónde están? {#destination-no-files}

<!-- c_dest_tshooting.xml -->

Los problemas comunes de configuración de destino incluyen los siguientes problemas:

### Destino no configurado

* **Clave  [!UICONTROL UserID] incorrecta:** la  [!UICONTROL UserID] clave es la  [!UICONTROL MasterDPID] de este destino y es la base de los valores de ID que se van a superar. Aunque se pueda seleccionar una clave [!UICONTROL UserID] a través de la lista desplegable, no significa necesariamente que haya ID, rasgos o segmentos asignados a este valor. Si el proceso [!UICONTROL Outbound] (que se ejecuta después de crear los destinos) no encuentra ningún usuario asignado a esta clave [!UICONTROL UserID], no se devolverá ningún dato.
* **No en las fuentes de datos de archivo seleccionadas:** al elegir cualquier tipo de destino que no sea  [!UICONTROL S2S], aparece una sección en la parte inferior de la pantalla etiquetada  [!UICONTROL Configure Data Sources]. Cuando esta sección aparece por primera vez, no se selecciona ningún valor. Si olvidó hacer clic en la casilla de verificación [!UICONTROL All First Party] o seleccionar individualmente las fuentes de datos de la ventana [!UICONTROL Available Data Sources] , no se devolverá ningún dato.

### Formato mal configurado

Al seleccionar un formato para los datos salientes, es mejor, si es posible, reutilizar un formato existente. El uso de un formato ya probado garantiza que los datos salientes se generarán correctamente. Para ver exactamente cómo se formatea un formato existente, haga clic en la opción [!UICONTROL Formats] de la barra de menús y busque el formato por nombre o por número de ID. Los formatos o macros mal formateados utilizados en formatos proporcionan una salida con formato incorrecto o evitan que la información se emita por completo.

Para obtener más información sobre la configuración de formatos y el uso de macros, consulte [Macros de formato de archivo](formats/file-formats.md#) y [Macros de formato HTTP](formats/web-formats.md).

### Servidor no configurado

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * No escriba prefijos para nombres de host. Si se le da una cuenta [!DNL ftp://hello.com], simplemente escriba [!DNL hello.com] en este campo.
   * **[!UICONTROL Port/Type Combination]**
      * Para una transferencia [!DNL FTP], el tipo de transferencia preferido es [!DNL SFTP].
      * Al seleccionar el tipo [!DNL SFTP], el puerto es casi siempre 22.
      * Al seleccionar el tipo [!DNL FTPs/TLS], el puerto es casi siempre 21.
      * El tipo [!DNL FTPs/TLS] no es lo mismo que una transferencia regular [!DNL FTP]. No se admiten transferencias [!DNL FTP] regulares (no seguras).
   * **[!UICONTROL Remote Path]**
      * Al elegir una subruta remota, debe introducirse sin barra diagonal.
      * Si se supone que el archivo transferido debe colocarse en la subcarpeta [!DNL (root)/inbound], simplemente agregue [!DNL inbound] para la ruta remota, no [!DNL /inbound].
      * Si envía sus archivos a varios directorios por la ruta, introduzca barras entre cada directorio. Si se le asigna la ubicación [!DNL /inbound/subdirectory1/subdirectory2], debe introducir [!DNL inbound/subdirectory1/subdirectory2] en este campo.
      * Si el servidor externo debe colocar el archivo en el directorio al que enrute automáticamente el archivo, puede dejar este espacio en blanco. No introduzca un punto ( . ), barra diagonal ( / ) o cualquier otra cosa.

* **[!DNL S3]**
   * [!DNL S3] es el protocolo de transferencia preferido (sobre  [!DNL FTP] o  [!DNL HTTP]).
      * **[!UICONTROL Bucket]**
         * El nombre del contenedor debe aparecer en la lista sin barras, prefijos, sufijos, etc. Si se le da la dirección [!DNL s3://your-bucket] simplemente debe agregar [!DNL your-bucket] a este campo.
      * **[!UICONTROL Directory]**
         * Deje este campo vacío a menos que se le asigne específicamente un subdirectorio en el que se deben colocar los datos. Si se le da la dirección [!DNL s3://your-bucket/your-subdirectory], introduzca [!DNL your-bucket] en el campo [!UICONTROL Bucket] y [!DNL your-subdirectory] debe agregarse al campo [!UICONTROL Directory]. No agregue barras anteriores.
         * Si tiene que desplazar varios directorios por la ruta, solo entonces debería usar barras como separadores. Por lo tanto, una ubicación de [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] tendría [!DNL your-bucket] en el campo [!UICONTROL Bucket] y [!DNL your-subdirectory1/your-subdirectory2] se introduciría en el campo [!UICONTROL Directory].
      * **[!UICONTROL Access / Secret Keys]**
         * Cuando [!DNL TechOps] crea un bucket y proporciona claves de acceso/secreto a un consultor, esas credenciales generalmente son `READ-ONLY` credenciales que deben entregarse al cliente. Estas credenciales no deben introducirse en los campos [!UICONTROL Access / Secret Key] porque esto provocará que la transferencia falle (porque son de solo lectura, no de escritura). En el caso de que [!DNL TechOps] cree un bucket y proporcione credenciales, el consultor también debería solicitar un par de claves de Adobe (NO SE LE DEBE DAR AL CLIENTE) que permita escribir archivos en este bucket. Esa clave debe agregarse a estos campos.

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * Introduzca la información de prefijo de las entradas [!DNL HTTP]. Si tiene una cuenta [!DNL https://superduper.com], escriba [!DNL https://superduper.com] en este campo.
      * **[!UICONTROL URL Prefix]**
         * Al añadir un prefijo [!DNL URL], deje la barra diagonal anterior desactivada. Una dirección de [!DNL https://hello.com/r/x/y/z] debe tener [!DNL https://hello.com] introducido en el campo [!UICONTROL Domain] y [!DNL r/x/y/z] introducido aquí en el campo [!UICONTROL URL Prefix].
         * Si no se necesita un [!UICONTROL URL Prefix], deje este valor en blanco.
      * **[!UICONTROL Authentication - SSH Key]**
         * Introduzca el valor de clave `SSH PRIVATE` completo en este cuadro, incluidos encabezados, pies de página y saltos de línea para garantizar un cifrado y un almacenamiento de claves precisos.

### No hay tiempo suficiente para la generación saliente

El proceso de salida se ejecuta dos veces al día y varios procesos (salida, publicación, inserción en ubicaciones externas, etc.) debe ejecutarse antes de que un archivo se inserte en su destino final. Una buena regla general es que un destino debe configurarse completamente al menos 24 horas antes de esperar que los datos se inserten en una ubicación externa.

### Tamaños de división de archivos demasiado grandes

Cuando se envían archivos a destinos, se pueden dividir los archivos salientes más grandes en fragmentos de archivos. Asegúrese de que los fragmentos de archivos individuales no superen los 10 GB. Consulte también [Nombre del archivo de datos de salida: Sintaxis y ejemplos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html?lang=en).


## Cómo configurar sus destinos para exportar ID de Experience Cloud, ID de cliente o ID de Audience Manager en archivos de datos de salida {#set-up-destinations-export}

Esta página muestra cómo configurar destinos para exportar datos con claves del tipo de ID que desee en [!UICONTROL Outbound Data Files].

<!-- set-up-destinations-mcid-aamid.xml -->

Los destinos permiten a nuestros clientes activar sus datos en cualquier cantidad de canales digitales. Por ejemplo, pueden exportar datos de audiencia a otras [!DNL Adobe Experience Cloud] soluciones ([!DNL Target], [!DNL Campaign], etc.). O bien, podrían enviar datos a [!UICONTROL DSP]s, [!UICONTROL SSP]s o a cualquier plataforma que esté integrada con Audience Manager. Mantenemos una lista de socios con los que trabajamos en nuestra [página de wiki de integraciones](https://wiki.corp.adobe.com/display/MCPI).

>[!NOTE]
>
>Para obtener un tutorial detallado sobre la creación de destinos en la interfaz de usuario de administración, consulte el artículo [Crear o editar destinos de la empresa](companies/admin-manage-company-destinations.md#create-edit-company-destinations) .

Sus clientes desean exportar diferentes tipos de ID, según el destino. El gráfico de configuración siguiente muestra las opciones que debe seleccionar para exportar información de perfil relacionada con distintos tipos de ID. También le recomendamos que consulte el [Índice de ID en Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html?lang=en). Hay tres configuraciones importantes que considerar: [!UICONTROL User ID Key], [!UICONTROL Data Source Type] y [!UICONTROL Format]. A continuación detallamos todos ellos.

* [!UICONTROL User ID Key]. En [!UICONTROL Admin UI], vaya a **[!UICONTROL Companies]**. Busque la empresa de su cliente y haga clic en ella. Busque la pestaña **[!UICONTROL Destinations]** y presione **[!UICONTROL Add Destination]**. En el flujo de trabajo **[!UICONTROL Add Destination]**, seleccione [!UICONTROL User ID Key]. El [!UICONTROL User ID Key] filtrará los ID entrantes de la fuente de datos de destino y solo permitirá que pasen los ID.

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]. Seleccione esta opción al crear un destino en la interfaz de usuario del Audience Manager. En primer lugar, seleccione [!UICONTROL Inbound] y luego seleccione el tipo de ID que desee. Las opciones son:

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]. Esta opción determina el formato de archivo que se va a exportar. En el flujo de trabajo **[!UICONTROL Add Destination]**, en **[!UICONTROL Batch Data]**, seleccione el formato .

Para inspeccionar un formato, vaya a **[!UICONTROL Admin UI > Formats]** y busque el elemento [!UICONTROL Data Row]. Este elemento contiene una macro del formato de archivo, &lt;MCID> en el ejemplo siguiente.

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
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p>ID de Experience Cloud </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 2 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>ID de Experience Cloud </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>UUID de Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 3 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>ID de Experience Cloud </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>ID de Experience Cloud </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 4 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>ID de Audience Manager </p> </td> 
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p>UUID de Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 5 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>ID de Audience Manager </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>ID de Experience Cloud </p> </td> 
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
   <td colname="col2"> <p>ID de cliente </p> </td> 
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p>ID de cliente (DPUUID) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 8 </td> 
   <td colname="col1"> <p>DPID (cualquier fuente de datos a la que la empresa tenga acceso) </p> </td> 
   <td colname="col2"> <p>ID de cliente </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>ID de Experience Cloud </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 9 </td> 
   <td colname="col1"> <p>DPID (cualquier fuente de datos a la que la empresa tenga acceso) </p> </td> 
   <td colname="col2"> <p>ID de cliente </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>UUID de Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 10 </td> 
   <td colname="col1"> <p>DPID (cualquier fuente de datos a la que la empresa tenga acceso) </p> </td> 
   <td colname="col2"> <p>ID de Audience Manager </p> </td> 
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p>UUID de Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID (cualquier fuente de datos a la que la empresa tenga acceso) </p> </td> 
   <td colname="col2"> <p>ID de Audience Manager </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>ID de Experience Cloud </p> </td> 
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

Supongamos que utiliza Audience Manager y [!DNL Campaign]. Para que los datos del cliente puedan procesarse en [!DNL Campaign], debe exportar [!UICONTROL Experience Cloud IDs]. En este caso, debe utilizar el número de configuración 3.
