---
description: Cree, edite y elimine destinos de Audience Manager.
seo-description: Cree, edite y elimine destinos de Audience Manager.
seo-title: Administrar destinos de empresa
title: Administrar destinos de empresa
uuid: d9a6bfb1-7629-44e0-b7d7-ece44f65ea2b
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# Administrar destinos de empresa {#manage-company-destinations}

Cree, edite y elimine destinos de Audience Manager.

<!-- t_company_destinations.xml -->

Para obtener información detallada, consulte [Destinos](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/destinations/destinations.html) en la Guía *del usuario de* Audience Manager.

## Crear o editar destinos de empresa {#create-edit-company-destinations}

Desplácese por las secciones para obtener instrucciones paso a paso sobre cómo crear nuevos [!DNL Audience Manager] destinos o editar los existentes.

<!-- create-edit-company-destinations.xml -->

Visite la página [de integración de socios de](https://wiki.corp.adobe.com/x/mPIMPw) Experience Cloud antes de configurar los destinos. La página contiene la información específica que debe completar para cada integración de [!DNL Audience Manager] socio.

Si su cliente desea usar [!DNL Adobe Media Optimizer] como destino en [!DNL Audience Manager] , debe configurarlo en [!DNL Adobe Media Optimizer].

## Navigate to the Destinations Tab {#navigate-destinations}

1. Haga clic en **[!UICONTROL Companies]**, luego busque y haga clic en la empresa que desee para mostrar su [!UICONTROL Profile] página. Puede utilizar el [!UICONTROL Search] cuadro o los controles de paginación en la parte inferior de la lista para encontrar la empresa deseada. Puede ordenar cada columna en orden ascendente o descendente haciendo clic en el encabezado de la columna deseada.
1. Click the **[!UICONTROL Destinations]** tab.
1. Para crear un nuevo destino, haga clic en **[!UICONTROL Add Destination]**. To edit an existing destination, click the destination's name in the **[!UICONTROL Name]** column.

## Configuración básica {#basic-settings}

Fill in the fields in the **[!UICONTROL Basic Settings]** window.

* **[!UICONTROL Name]** :: (Requerido) Especifique el nombre de este destino.
* **[!UICONTROL Description]** :: Especifique información descriptiva sobre este destino.
* **[!UICONTROL Type]** :: (Requerido) Seleccione el tipo de destino deseado:
   * **[!UICONTROL Bulk ID]**:: Sincronizar ID entre distintas plataformas.
   * **[!UICONTROL Bulk Trait]**:: Enviar información de características de forma masiva a diferentes plataformas.
   * **[!UICONTROL Bulk Segment]**:: Enviar información de segmentos de forma masiva a diferentes plataformas.
   * **[!UICONTROL S2S]**:: Utilice destinos de servidor a servidor para enviar datos en tiempo real y por lotes a distintas plataformas.
* **[!UICONTROL Auto-Fill Destination Mapping]** :: ( [!UICONTROL S2S] solo) Seleccione una opción:
   * **[!UICONTROL Segment ID]** :: Si selecciona esta configuración, la asignación de valores de destino se rellena con la ID del [!DNL Audience Manager] segmento.
   * **[!UICONTROL Integration Code Value]** :: Si selecciona esta configuración, la asignación de valores de destino se rellena con el código de integración de [!DNL Audience Manager] segmentos.
* **[!UICONTROL User ID Key]** :: (Requerido) Seleccione la clave de ID de usuario que desee para este destino en la lista desplegable.

Este ID se utiliza como ID de origen de datos principal. Esto determina los ID de usuario que se van a superar en el archivo.

>[!NOTE]
>
>Para el tipo de [!UICONTROL Bulk ID] destino, no puede utilizar el [!DNL Audience Manager] o el [!UICONTROL User ID] ID [!DNL Adobe Experience Cloud] .

Si el ID de fuente de datos ( [!UICONTROL DPID]) no se muestra en la lista desplegable, debe seleccionar la **[!UICONTROL Outbound]** casilla de verificación en el nivel de fuente de datos en la página [Configuración de fuente de](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/data-sources/manage-datasources.html)datos.

* **[!UICONTROL Target Data Source]** :: (Requerido) Seleccione el origen de datos deseado para este destino en la lista desplegable. Esta configuración permite el etiquetado de datos salientes, lo que permite la ingestión en sistemas separados del cliente.
* **[!UICONTROL Foreign Account ID]** :: Especifique el ID de cuenta externa para este destino. Es el valor de identificación en el sistema del destinatario para estos datos salientes.
* **[!UICONTROL Outbound Sample Rate Denominator]** :: Cuando se desconozca la cantidad total de datos devueltos, utilice esta configuración para devolver solo una cantidad de datos de muestra en lugar de la cantidad total. Ajuste el número aquí para representar una fracción de los datos (por ejemplo, un valor de '100' devuelve 1/100 de la cantidad regular de datos, un valor de '10' devuelve 1/10 de la cantidad regular de datos). El valor predeterminado es '1', que devuelve todos los datos.

## Datos en tiempo real (para destinos S2S) {#realtime-s2s}

Si va a crear un [!UICONTROL S2S] destino, rellene los campos siguientes:

**[!UICONTROL Servers]**:: Seleccione el servidor que desee `HTTP` para este destino.
**[!UICONTROL Format]**:: Seleccione el formato deseado para este destino en la lista desplegable: [!UICONTROL HTTP only].

>[!NOTE]
>
>Por [!DNL S2S] lo menos, puede activar o desactivar [!UICONTROL Realtime] o [!UICONTROL Batch] destinos mediante los controles deslizantes Desactivado/Activado en pantalla. No puede desactivar ambas opciones.

## Datos por lotes {#batch-data}

Para [!UICONTROL Bulk ID]destinos [!UICONTROL Bulk Trait] o [!UICONTROL Bulk Segment] , rellene los campos siguientes:

* **[!UICONTROL Protocol]**:: (Requerido) Seleccione el protocolo deseado para este destino en la lista desplegable:
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**:: (Requerido) Seleccione el servidor que desee para este destino en la lista desplegable.
* **[!UICONTROL Format]**:: (Requerido) Seleccione el formato deseado para este destino en la lista desplegable: [!DNL HTTP] o tipo de archivo, según el protocolo elegido anteriormente.
* **[!UICONTROL Sync Type]**:: (Requerido) Seleccione el tipo de sincronización deseado para este destino. Esto indica el nivel de actividades de usuario que los clientes desean incluir en los pedidos salientes. Seleccione **[!UICONTROL Customer]** si los clientes solo están interesados en analizar las cualificaciones de los segmentos desde sus propiedades. Seleccione **[!UICONTROL Platform]** si desea incluir cualificaciones de segmentos de actividades fuera del sitio en todos los [!DNL Audience Manager] clientes.
* **[!UICONTROL Customer]**:: El archivo contiene usuarios activos que tienen al menos 1 realización de características solo en las propiedades del cliente (asociadas con la del cliente [!UICONTROL PID]) durante el período de tiempo seleccionado. Los clientes deben utilizar esta opción para exportar sus cualificaciones de segmentos en tiempo *real* a destinos.
* **[!UICONTROL Platform]**:: El archivo contiene usuarios activos que tienen al menos una interacción en tiempo real, ya sea la sincronización de ID o la realización de características, en cualquier parte de las propiedades de todos [!DNL Audience Manager] los clientes (asociadas con todos los PID de cliente) durante el período de tiempo seleccionado. Los clientes deben utilizar esta opción para exportar sus cualificaciones de segmentos *totales* a destinos.
* **[!UICONTROL Lifetime]**:: El archivo contiene los usuarios activos vistos en cualquier parte de las propiedades de todos los [!DNL Audience Manager] clientes desde la creación del destino.
* **[!UICONTROL Sync Type Lookback Period]**:: Si selecciona [!UICONTROL Customer] o [!UICONTROL Platform], seleccione un período de tiempo. Los archivos contienen usuarios activos para el período de tiempo seleccionado.
A continuación, seleccione el tipo de pedido. Esto indica la frecuencia y el alcance de cada integración saliente con los socios. Seleccione entre pedidos incrementales y completos.
* **[!UICONTROL Incremental Scheduled Run]**:: Con cada ejecución, [!DNL Audience Manager] solo salirán los nuevos usuarios netos cualificados desde el pedido saliente anterior. Seleccione el período de tiempo que desee [!DNL Audience Manager] para realizar procesos de sincronización incremental. Por ejemplo, puede seleccionar cada 24 horas, cada siete días, cada 30 días o nunca.

>[!NOTE] {important="high"}
>
>El primer pedido incremental equivale a un pedido completo porque nunca se envió a los usuarios anteriores al destino.

* **[!UICONTROL Full Sync Scheduled Run]**:: Con cada ejecución, [!DNL Audience Manager] salirá de todos los usuarios activos desde la primera configuración del destino. Seleccione la programación que desee utilizar [!DNL Audience Manager] para realizar procesos de sincronización completos. Por ejemplo, puede seleccionar cada 24 horas, cada siete días, cada 30 días o nunca.

>[!NOTE] {important="high"}
>
>Se recomienda utilizar sincronizaciones incrementales con más frecuencia que sincronizaciones completas. Las sincronizaciones incrementales sólo envían archivos que contienen nuevas realizaciones de características o sincronizaciones de ID. Las sincronizaciones completas envían todos los archivos, tanto si incluyen nuevas realizaciones como sincronizaciones de ID. Utilice la configuración únicamente cuando los clientes necesiten una copia completa de todos sus usuarios para reducir el volumen de datos de salida. [!UICONTROL Full Sync Scheduled Run]

## Configurar fuentes de datos {#configure-data-sources}

Para [!UICONTROL Bulk ID]destinos [!UICONTROL Bulk Trait] o [!UICONTROL Bulk Segment] , rellene los campos siguientes. Esta configuración le permite enviar todos los datos (características, segmentos o ID, según el tipo seleccionado) asociados a las fuentes de datos.

* **[!UICONTROL All Unrestricted First Party Data]**:: Seleccione esta opción para utilizar todas las fuentes de datos de origen. Si selecciona esta opción, las [!UICONTROL Available Data Sources] opciones estarán desactivadas.
* **[!UICONTROL Available Data Sources]**:: Utilice las flechas para mover los orígenes de datos entre los **[!UICONTROL Available Data Sources]** cuadros y **[!UICONTROL In File Data Sources]** .

## Guardar y finalizar {#save-and-finalize}

El **[!UICONTROL Save]** botón se activa después de rellenar todos los campos obligatorios. Haga clic en **[!UICONTROL Save]** para finalizar el proceso de creación de destino.

## Eliminar destinos de empresa {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

Para eliminar un destino:

1. Haga clic en **[!UICONTROL Companies]**, localice y haga clic en la empresa que desee y, a continuación, haga clic en la **[!UICONTROL Destinations]** ficha.
1. Haga clic ![](assets/icon_delete.png) en la **[!UICONTROL Actions]** columna del destino deseado.
1. Click **[!UICONTROL OK]** to confirm the deletion.

>[!NOTE]
>
>No puede eliminar un destino si tiene segmentos asignados a él.