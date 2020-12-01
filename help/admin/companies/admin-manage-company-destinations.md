---
description: Cree, edite y elimine destinos de Audience Manager.
seo-description: Cree, edite y elimine destinos de Audience Manager.
seo-title: Administrar destinos de la compañía
title: Administrar destinos de la compañía
uuid: d9a6bfb1-7629-44e0-b7d7-ece44f65ea2b
translation-type: tm+mt
source-git-commit: f247457004a624297ddc8847dd256dbb7d8da418
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 1%

---


# Administrar destinos de la compañía {#manage-company-destinations}

Cree, edite y elimine destinos de Audience Manager.

<!-- t_company_destinations.xml -->

Para obtener información detallada, consulte [Destinations](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/destinations/destinations.html) en la *Guía del usuario del Audience Manager*.

## Crear o editar destinos de compañía {#create-edit-company-destinations}

Desplácese por las secciones para obtener instrucciones paso a paso sobre cómo crear nuevos destinos [!DNL Audience Manager] o editar los existentes.

<!-- create-edit-company-destinations.xml -->

Visite la [página de integración de socios de Experience Cloud](https://wiki.corp.adobe.com/x/mPIMPw) antes de configurar los destinos. La página contiene la información específica que debe completar para cada integración de [!DNL Audience Manager] socio.

Si su cliente desea utilizar [!DNL Adobe Media Optimizer] como destino en [!DNL Audience Manager], debe configurarlo en [!DNL Adobe Media Optimizer].

## Vaya a la ficha Destinos {#navigate-destinations}

1. Haga clic en **[!UICONTROL Companies]**, luego localice y haga clic en la compañía deseada para mostrar su [!UICONTROL Profile] página. Puede utilizar el cuadro [!UICONTROL Search] o los controles de paginación en la parte inferior de la lista para encontrar la compañía deseada. Puede ordenar cada columna en orden ascendente o descendente haciendo clic en el encabezado de la columna deseada.
1. Haga clic en la ficha **[!UICONTROL Destinations]**.
1. Para crear un nuevo destino, haga clic en **[!UICONTROL Add Destination]**. Para editar un destino existente, haga clic en el nombre del destino en la columna **[!UICONTROL Name]**.

## Configuración básica {#basic-settings}

Rellene los campos de la ventana **[!UICONTROL Basic Settings]**.

* **[!UICONTROL Name]:** (Obligatorio) Especifique el nombre de este destino.
* **[!UICONTROL Description]:** Especifique información descriptiva sobre este destino.
* **[!UICONTROL Type]:** (Obligatorio) Seleccione el tipo de destino que desee:
   * **[!UICONTROL Bulk ID]**:: Sincronizar ID entre distintas plataformas.
   * **[!UICONTROL Bulk Trait]**:: Enviar información de características de forma masiva a diferentes plataformas.
   * **[!UICONTROL Bulk Segment]**:: Enviar información de segmentos de forma masiva a diferentes plataformas.
   * **[!UICONTROL S2S]**:: Utilice destinos de servidor a servidor para enviar datos en tiempo real y por lotes a distintas plataformas.
* **[!UICONTROL Auto-Fill Destination Mapping]:** ( [!UICONTROL S2S] solamente) Seleccione una opción:
   * **[!UICONTROL Segment ID]:** Si selecciona esta configuración, la asignación de valores de destino se rellena con la ID  [!DNL Audience Manager] del segmento.
   * **[!UICONTROL Integration Code Value]:** Si selecciona esta configuración, la asignación de valores de destino se rellena con el código de integración de  [!DNL Audience Manager] segmentos.
* **[!UICONTROL User ID Key]:** (Obligatorio) Seleccione la clave de ID de usuario que desee para este destino en la lista desplegable.

Este ID se utiliza como ID de origen de datos principal. Esto determina los ID de usuario que se van a superar en el archivo.

>[!NOTE]
>
>Para el tipo de destino [!UICONTROL Bulk ID], no puede utilizar el [!DNL Audience Manager] [!UICONTROL User ID] ni el [!DNL Adobe Experience Cloud] ID.

Si el ID de fuente de datos ( [!UICONTROL DPID]) no se muestra en la lista desplegable, debe seleccionar la casilla **[!UICONTROL Outbound]** en el nivel de fuente de datos en la [página Configuración de fuente de datos](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/data-sources/manage-datasources.html).

* **[!UICONTROL Target Data Source]:** (Obligatorio) Seleccione el origen de datos deseado para este destino en la lista desplegable. Esta configuración permite el etiquetado de datos salientes, lo que permite la ingestión en sistemas separados del cliente.
* **[!UICONTROL Foreign Account ID]:** Especifique el ID de cuenta externa de este destino. Este es el valor de identificación en el sistema del destinatario para estos datos devueltos.
* **[!UICONTROL Outbound Sample Rate Denominator]:** Cuando se desconozca la cantidad total de datos devueltos, utilice esta configuración para devolver solo una cantidad de datos de muestra, en lugar de la cantidad total. Ajuste el número aquí para representar una fracción de los datos (p. ej., un valor de &#39;100&#39; devuelve 1/100 de la cantidad regular de datos, un valor de &#39;10&#39; devuelve 1/10 de la cantidad regular de datos). El valor predeterminado es &#39;1&#39;, que devuelve todos los datos.

## Datos en tiempo real (para destinos S2S) {#realtime-s2s}

Si va a crear un destino [!UICONTROL S2S], rellene los campos siguientes:

**[!UICONTROL Servers]**:: Seleccione el  `HTTP` servidor que desee para este destino.
**[!UICONTROL Format]**:: Seleccione el formato deseado para este destino en la lista desplegable:  [!UICONTROL HTTP only].

>[!NOTE]
>
>Sólo para [!DNL S2S], puede habilitar o deshabilitar destinos [!UICONTROL Realtime] o [!UICONTROL Batch] mediante los deslizadores Desactivado/Activado en pantalla. No puede desactivar ambas opciones.

## Datos por lotes {#batch-data}

Para destinos [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] o [!UICONTROL Bulk Segment], rellene los campos siguientes:

* **[!UICONTROL Protocol]**:: (Requerido) Seleccione el protocolo deseado para este destino en la lista desplegable:
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**:: (Requerido) Seleccione el servidor que desee para este destino en la lista desplegable.
* **[!UICONTROL Format]**:: (Requerido) Seleccione el formato deseado para este destino en la lista desplegable:  [!DNL HTTP] o tipo de archivo, según el protocolo que haya elegido anteriormente.
* **[!UICONTROL Sync Type]**:: (Requerido) Seleccione el tipo de sincronización que desee para este destino. Esto indica el nivel de actividades de usuario que los clientes desean incluir en los pedidos salientes. Seleccione **[!UICONTROL Customer]** si los clientes solo están interesados en analizar las cualificaciones de los segmentos desde sus propiedades. Seleccione **[!UICONTROL Platform]** si desea incluir cualificaciones de segmentos de actividades fuera del sitio en todos los clientes [!DNL Audience Manager].
* **[!UICONTROL Customer]**:: El archivo contiene usuarios activos que tienen al menos 1 realización de características solo en las propiedades del cliente (asociadas con la del cliente  [!UICONTROL PID]) durante el período de tiempo seleccionado. Los clientes deben utilizar esta opción para exportar sus *calificaciones de segmento en tiempo real* a destinos.
* **[!UICONTROL Platform]**:: El archivo contiene usuarios activos que tienen al menos una interacción en tiempo real, ya sea la sincronización de ID o la realización de características, en cualquier parte de las propiedades de todos los  [!DNL Audience Manager] clientes (asociadas con todos los PID de cliente) para el período de tiempo seleccionado. Los clientes deben utilizar esta opción para exportar sus *calificaciones de segmento totales* a destinos.
* **[!UICONTROL Lifetime]**:: El archivo contiene los usuarios activos vistos en cualquier parte de las propiedades de todos los  [!DNL Audience Manager] clientes desde la creación del destino.
* **[!UICONTROL Sync Type Lookback Period]**:: Si selecciona  [!UICONTROL Customer] o  [!UICONTROL Platform], seleccione un período de tiempo. Los archivos contienen usuarios activos para el período de tiempo seleccionado.
A continuación, seleccione el tipo de pedido. Esto indica la frecuencia y el alcance de cada integración saliente con los socios. Seleccione entre pedidos incrementales y completos.
* **[!UICONTROL Incremental Scheduled Run]**:: Con cada ejecución, solo  [!DNL Audience Manager] salirán los nuevos usuarios netos cualificados desde el pedido saliente anterior. Seleccione el período de tiempo que desee que [!DNL Audience Manager] realice procesos de sincronización incremental. Por ejemplo, puede seleccionar cada 24 horas, cada siete días, cada 30 días o nunca.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>El primer pedido incremental equivale a un pedido completo porque nunca se envió a los usuarios anteriores al destino.

* **[!UICONTROL Full Sync Scheduled Run]**:: Con cada ejecución,  [!DNL Audience Manager] saldrá de todos los usuarios activos desde la primera configuración del destino. Seleccione la programación que desee que [!DNL Audience Manager] utilice para realizar procesos de sincronización completos. Por ejemplo, puede seleccionar cada 24 horas, cada siete días, cada 30 días o nunca.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>Se recomienda utilizar sincronizaciones incrementales con más frecuencia que sincronizaciones completas. Las sincronizaciones incrementales sólo envían archivos que contienen nuevas realizaciones de características o sincronizaciones de ID. Las sincronizaciones completas envían todos los archivos, tanto si incluyen nuevas realizaciones como sincronizaciones de ID. Utilice sólo la configuración [!UICONTROL Full Sync Scheduled Run] cuando los clientes necesiten una copia completa de todos sus usuarios para reducir el volumen de datos de salida.

## Configurar fuentes de datos {#configure-data-sources}

Para destinos [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] o [!UICONTROL Bulk Segment], rellene los campos siguientes. Esta configuración le permite enviar todos los datos (características, segmentos o ID, según el tipo seleccionado) asociados a las fuentes de datos.

* **[!UICONTROL All Unrestricted First Party Data]**:: Seleccione esta opción para utilizar todas las fuentes de datos de origen. Si selecciona esta opción, las opciones [!UICONTROL Available Data Sources] están desactivadas.
* **[!UICONTROL Available Data Sources]**:: Utilice las flechas para mover los orígenes de datos entre los  **[!UICONTROL Available Data Sources]** y  **[!UICONTROL In File Data Sources]** cuadros.

## Guardar y finalizar {#save-and-finalize}

El botón **[!UICONTROL Save]** se activa después de rellenar todos los campos obligatorios. Haga clic en **[!UICONTROL Save]** para finalizar el proceso de creación de destino.

## Eliminar destinos de Compañía {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

Para eliminar un destino:

1. Haga clic en **[!UICONTROL Companies]**, localice y haga clic en la compañía deseada y, a continuación, haga clic en la ficha **[!UICONTROL Destinations]**.
1. Haga clic ![](assets/icon_delete.png) en la columna **[!UICONTROL Actions]** del destino deseado.
1. Haga clic en **[!UICONTROL OK]** para confirmar la eliminación.

>[!NOTE]
>
>No puede eliminar un destino si tiene segmentos asignados a él.