---
description: Cree, edite y elimine destinos de Audience Manager.
seo-description: Cree, edite y elimine destinos de Audience Manager.
seo-title: Administrar destinos de empresa
title: Administrar destinos de empresa
uuid: d 9 a 6 bfb 1-7629-44 e 0-b 7 d 7-ece 44 f 65 ea 2 b
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# Administrar destinos de empresa {#manage-company-destinations}

Cree, edite y elimine destinos de Audience Manager.

<!-- t_company_destinations.xml -->

Para obtener más información, consulte [Destinos](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/destinations/destinations.html) en la Guía del usuario *de Audience Manager*.

## Crear o editar destinos de empresa {#create-edit-company-destinations}

Desplácese por las secciones para obtener instrucciones paso a paso sobre cómo crear [!DNL Audience Manager] destinos nuevos o editar destinos existentes.

<!-- create-edit-company-destinations.xml -->

Visite la página de integración de socios [de Experience Cloud](https://wiki.corp.adobe.com/x/mPIMPw) antes de configurar los destinos. La página contiene la información específica que debe rellenar para cada [!DNL Audience Manager] integración de socio.

Si su cliente desea utilizar [!DNL Adobe Media Optimizer] como destino en [!DNL Audience Manager] , debe configurarlo [!DNL Adobe Media Optimizer]en.

## Navigate to the Destinations Tab {#navigate-destinations}

1. Haga clic en **[!UICONTROL Companies]** y luego busque y haga clic en la empresa que desee para mostrar su [!UICONTROL Profile] página. Puede utilizar [!UICONTROL Search] el cuadro o los controles de paginación en la parte inferior de la lista para encontrar la empresa deseada. Puede ordenar cada columna en orden ascendente o descendente haciendo clic en el encabezado de la columna que desee.
1. Click the **[!UICONTROL Destinations]** tab.
1. Para crear un nuevo destino, haga clic **[!UICONTROL Add Destination]** en. To edit an existing destination, click the destination's name in the **[!UICONTROL Name]** column.

## Configuración básica {#basic-settings}

Fill in the fields in the **[!UICONTROL Basic Settings]** window.

* **[!UICONTROL Name]:** (Requerido) Especifique el nombre de este destino.
* **[!UICONTROL Description]:** Especifique información descriptiva sobre este destino.
* **[!UICONTROL Type]:** (Requerido) Seleccione el tipo de destino que desee:
   * **[!UICONTROL Bulk ID]**: Sincronizar ID entre distintas plataformas.
   * **[!UICONTROL Bulk Trait]**: Envíe información de características de forma masiva a diferentes plataformas.
   * **[!UICONTROL Bulk Segment]**: Envíe información de segmentos de forma masiva a diferentes plataformas.
   * **[!UICONTROL S2S]**: Utilice los destinos servidor a servidor para enviar datos en tiempo real y lotes a distintas plataformas.
* **[!UICONTROL Auto-Fill Destination Mapping]:** ( [!UICONTROL S2S] solo) Seleccione una opción:
   * **[!UICONTROL Segment ID]:** Si selecciona esta configuración, la asignación de valor de destino se rellena con el ID [!DNL Audience Manager] de segmento.
   * **[!UICONTROL Integration Code Value]:** Si selecciona esta configuración, la asignación de valores de destino se rellena con el código de integración [!DNL Audience Manager] de segmentos.
* **[!UICONTROL User ID Key]:** (Requerido) Seleccione la clave de ID de usuario que desee para este destino en la lista desplegable.

Este ID se utiliza como ID de fuente de datos principal. Esto determina la salida de los ID de usuario en el archivo.

>[!NOTE]
>
>Para el tipo [!UICONTROL Bulk ID] de destino, no puede utilizar el [!DNL Audience Manager][!UICONTROL User ID] ID o [!DNL Adobe Experience Cloud] la ID.

Si el ID de fuente de datos ( [!UICONTROL DPID]) no se muestra en la lista desplegable, debe seleccionar la **[!UICONTROL Outbound]** casilla en el nivel de fuente de datos en la [página Configuración de fuentes de datos](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/data-sources/manage-datasources.html).

* **[!UICONTROL Target Data Source]:** (Requerido) Seleccione la fuente de datos que desee para este destino en la lista desplegable. Esta configuración permite el etiquetado de datos salientes, lo que permite la ingesta en sistemas separados en el lado del cliente.
* **[!UICONTROL Foreign Account ID]:** Especifique el ID de cuenta externa para este destino. Es el valor de identificación en el sistema del destinatario para estos datos salientes.
* **[!UICONTROL Outbound Sample Rate Denominator]:** Cuando se desconoce la cantidad total de datos devueltos, utilice este valor para devolver solamente una cantidad de datos de muestra, en lugar de la cantidad completa. Ajuste el número aquí para representar una fracción de los datos (por ejemplo, un valor de ' 100 ' devuelve 1/100 a la cantidad regular de datos, un valor de ' 10 ' devuelve 1/10 la cantidad regular de datos). El valor predeterminado es ' 1 ', que devuelve todos los datos.

## Datos en tiempo real (para destinos S 2 S) {#realtime-s2s}

Si va a crear [!UICONTROL S2S] un destino, rellene los campos siguientes:

**[!UICONTROL Servers]**: Seleccione `HTTP` el servidor que desee para este destino.
**[!UICONTROL Format]**: Seleccione el formato deseado para este destino en la lista desplegable: [!UICONTROL HTTP only].

>[!NOTE]
>
>Solo es [!DNL S2S] posible habilitar o deshabilitar los controles [!UICONTROL Realtime] o [!UICONTROL Batch] los destinos con los controles deslizantes Desactivados/Activados en pantalla. No puede desactivar ambas opciones.

## Datos por lotes {#batch-data}

Para [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] o [!UICONTROL Bulk Segment] destinos, rellene los campos siguientes:

* **[!UICONTROL Protocol]**: (Necesario) Seleccione el protocolo deseado para este destino en la lista desplegable:
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**: (Necesario) Seleccione el servidor que desee para este destino en la lista desplegable.
* **[!UICONTROL Format]**: (Necesario) Seleccione el formato deseado para este destino desde la lista desplegable: [!DNL HTTP] o tipo de archivo, según el protocolo que haya elegido arriba.
* **[!UICONTROL Sync Type]**: (Requerido) Seleccione el tipo de sincronización deseado para este destino. Esto indica el nivel de actividades de usuario que los clientes desean incluir en los pedidos salientes. Seleccione **[!UICONTROL Customer]** si los clientes solo están interesados en analizar las calificaciones de segmentos desde sus propiedades. Seleccione **[!UICONTROL Platform]** si desea incluir las calificaciones de segmentos desde actividades fuera del sitio en todos [!DNL Audience Manager] los clientes.
* **[!UICONTROL Customer]**: El archivo contiene usuarios activos que tienen al menos 1 características solo en las propiedades del cliente (asociadas con el cliente [!UICONTROL PID]) durante el período de tiempo seleccionado. Sus clientes deben utilizar esta opción para superar *las calificaciones* de segmentos en tiempo real a destinos.
* **[!UICONTROL Platform]**: El archivo contiene usuarios activos que tienen al menos 1 interacción en tiempo real, ya sea sincronizaciones de ID o características de características, en cualquier lugar de las propiedades [!DNL Audience Manager] de los clientes (asociadas con todos los PIDS del cliente) durante el período de tiempo seleccionado. Sus clientes deben utilizar esta opción para superar *las calificaciones* totales de los segmentos a destinos.
* **[!UICONTROL Lifetime]**: El archivo contiene usuarios activos que se ven en cualquier lugar de las propiedades [!DNL Audience Manager] de todos los clientes desde la creación del destino.
* **[!UICONTROL Sync Type Lookback Period]**: Si selecciona [!UICONTROL Customer] o [!UICONTROL Platform], seleccione un período de tiempo. Los archivos contienen usuarios activos durante el período de tiempo seleccionado.
A continuación, seleccione el tipo de pedido. Esto indica la frecuencia y el ámbito de cada integración saliente con socios. Seleccione entre pedidos incrementales y completos.
* **[!UICONTROL Incremental Scheduled Run]**: Con cada ejecución, [!DNL Audience Manager] solo se outenlazarán los usuarios nuevos de la red calificados desde el orden saliente anterior. Seleccione el período de tiempo deseado para [!DNL Audience Manager] realizar procesos de sincronización incremental. Por ejemplo, puede seleccionar cada 24 horas, cada siete días, cada 30 días o nunca.

>[!NOTE] {important = "high"}
>
>El primer pedido incremental es equivalente a un pedido completo porque nunca se enviaron usuarios anteriores al destino.

* **[!UICONTROL Full Sync Scheduled Run]**: Con cada ejecución, [!DNL Audience Manager] se outenlazarán todos los usuarios activos desde la primera vez que se configuró el destino. Seleccione la programación que desee utilizar [!DNL Audience Manager] para realizar procesos de sincronización completos. Por ejemplo, puede seleccionar cada 24 horas, cada siete días, cada 30 días o nunca.

>[!NOTE] {important = "high"}
>
>Recomendamos el uso de sincronizaciones incrementales con mayor frecuencia que las sincronizaciones completas. Las sincronizaciones incrementales solo envían archivos que contengan nuevas características de características o sincronizaciones de ID. Las sincronizaciones completas envían todos los archivos, independientemente de si incluyen o no nuevas funciones o sincronizaciones de ID. Utilice únicamente la [!UICONTROL Full Sync Scheduled Run] configuración cuando los clientes necesiten una copia completa de todos los usuarios para reducir el volumen de datos salientes.

## Configurar fuentes de datos {#configure-data-sources}

Para [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] o [!UICONTROL Bulk Segment] destinos, rellene los campos a continuación. Esta configuración permite enviar todos los datos (características, segmentos o ID, según el tipo seleccionado) asociados con las fuentes de datos.

* **[!UICONTROL All Unrestricted First Party Data]**: Seleccione para utilizar todas las fuentes de datos de origen. Si selecciona esta opción, las [!UICONTROL Available Data Sources] opciones estarán desactivadas.
* **[!UICONTROL Available Data Sources]**: Utilice las flechas para mover las fuentes de datos entre los cuadros **[!UICONTROL Available Data Sources]** y **[!UICONTROL In File Data Sources]** las casillas.

## Guardar y finalizar {#save-and-finalize}

El **[!UICONTROL Save]** botón se activa después de rellenar todos los campos obligatorios. Haga clic en **[!UICONTROL Save]** para finalizar el proceso de destino.

## Eliminar destinos de empresa {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

Para eliminar un destino:

1. Haga clic en **[!UICONTROL Companies]**, busque y haga clic en la empresa que desee y, a continuación, haga clic **[!UICONTROL Destinations]** en la ficha.
1. Haga clic en ![](assets/icon_delete.png) la **[!UICONTROL Actions]** columna del destino deseado.
1. Click **[!UICONTROL OK]** to confirm the deletion.

>[!NOTE]
>
>No puede eliminar un destino si tiene segmentos asignados a él.