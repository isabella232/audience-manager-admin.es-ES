---
description: Cree, edite y elimine destinos de Audience Manager.
seo-description: Create, edit, and delete Audience Manager destinations.
seo-title: Manage Company Destinations
title: Administrar destinos de la compañía
uuid: d9a6bfb1-7629-44e0-b7d7-ece44f65ea2b
exl-id: a2e73613-07cd-4ab8-8c6e-be451ed50bfc
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '1068'
ht-degree: 1%

---

# Administrar destinos de la compañía {#manage-company-destinations}

Cree, edite y elimine destinos de Audience Manager.

<!-- t_company_destinations.xml -->

Para obtener información detallada, consulte [Destinations](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/destinations.html) en la *Guía del usuario del Audience Manager*.

## Crear o editar destinos de compañía {#create-edit-company-destinations}

Desplácese por las secciones para obtener instrucciones paso a paso sobre cómo crear nuevos destinos [!DNL Audience Manager] o editar los existentes.

<!-- create-edit-company-destinations.xml -->

Visite la [página de integración del socio de Experience Cloud](https://wiki.corp.adobe.com/x/mPIMPw) antes de configurar los destinos. La página contiene la información específica que debe completar para cada integración de socio [!DNL Audience Manager].

Si su cliente desea utilizar [!DNL Adobe Media Optimizer] como destino en [!DNL Audience Manager] , debe configurarlo en [!DNL Adobe Media Optimizer].

## Vaya a la pestaña Destinos {#navigate-destinations}

1. Haga clic en **[!UICONTROL Companies]**, luego localice y haga clic en la empresa que desee para mostrar su página [!UICONTROL Profile]. Puede utilizar el cuadro [!UICONTROL Search] o los controles de paginación situados en la parte inferior de la lista para encontrar la empresa que desee. Para ordenar cada columna en orden ascendente o descendente, haga clic en el encabezado de la columna que desee.
1. Haga clic en la pestaña **[!UICONTROL Destinations]**.
1. Para crear un nuevo destino, haga clic en **[!UICONTROL Add Destination]**. Para editar un destino existente, haga clic en el nombre del destino en la columna **[!UICONTROL Name]**.

## Configuración básica {#basic-settings}

Rellene los campos de la ventana **[!UICONTROL Basic Settings]** .

* **[!UICONTROL Name]:**  (Obligatorio) Especifique el nombre de este destino.
* **[!UICONTROL Description]:** especifique información descriptiva sobre este destino.
* **[!UICONTROL Type]:** (obligatorio) seleccione el tipo de destino deseado:
   * **[!UICONTROL Bulk ID]**: Sincronizar ID entre distintas plataformas.
   * **[!UICONTROL Bulk Trait]**: Envíe información de características de forma masiva a diferentes plataformas.
   * **[!UICONTROL Bulk Segment]**: Envíe información de segmentos de forma masiva a diferentes plataformas.
   * **[!UICONTROL S2S]**: Utilice destinos de servidor a servidor para enviar datos en tiempo real y por lotes a distintas plataformas.
* **[!UICONTROL Auto-Fill Destination Mapping]:**  ( [!UICONTROL S2S] solo) Seleccione una opción:
   * **[!UICONTROL Segment ID]:** Si selecciona esta configuración, la asignación de valor de destino se rellena con el ID de  [!DNL Audience Manager] segmento.
   * **[!UICONTROL Integration Code Value]:** Si selecciona esta configuración, la asignación de valor de destino se rellena con el código de integración del  [!DNL Audience Manager] segmento.
* **[!UICONTROL User ID Key]:** (obligatorio) seleccione la clave de ID de usuario que desee para este destino en la lista desplegable.

Este ID se utiliza como ID de fuente de datos principal. Esto determina los ID de usuario que se van a superar en el archivo.

>[!NOTE]
>
>Para el tipo de destino [!UICONTROL Bulk ID] no se puede usar el [!DNL Audience Manager] [!UICONTROL User ID] ni el [!DNL Adobe Experience Cloud] ID.

Si el ID de fuente de datos ( [!UICONTROL DPID]) no se muestra en la lista desplegable, debe seleccionar la casilla **[!UICONTROL Outbound]** en el nivel de fuente de datos de la [página Configuración de fuente de datos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/manage-datasources.html).

* **[!UICONTROL Target Data Source]:**  (Obligatorio) Seleccione la fuente de datos que desee para este destino en la lista desplegable. Esta configuración permite el etiquetado de los datos salientes, lo que permite su incorporación en sistemas independientes en el lado del cliente.
* **[!UICONTROL Foreign Account ID]:** especifique el ID de cuenta externa para este destino. Este es el valor de identificación en el sistema del destinatario para estos datos salientes.
* **[!UICONTROL Outbound Sample Rate Denominator]:** Cuando se desconozca la cantidad total de datos devueltos, utilice esta configuración para devolver solo una cantidad de datos de muestra, en lugar de la cantidad completa. Ajuste el número aquí para representar una fracción de los datos (por ejemplo, un valor de &quot;100&quot; devuelve 1/100 de la cantidad normal de datos, un valor de &quot;10&quot; devuelve 1/10 de la cantidad normal de datos). El valor predeterminado es &quot;1&quot;, que devuelve todos los datos.

## Datos en tiempo real (para destinos S2S) {#realtime-s2s}

Si está creando un destino [!UICONTROL S2S], rellene los campos siguientes:

**[!UICONTROL Servers]**: Seleccione el  `HTTP` servidor que desee para este destino.
**[!UICONTROL Format]**: Seleccione el formato deseado para este destino en la lista desplegable:  [!UICONTROL HTTP only].

>[!NOTE]
>
>Solo para [!DNL S2S], puede habilitar o deshabilitar destinos [!UICONTROL Realtime] o [!UICONTROL Batch] mediante los deslizadores Desactivado/Activado en pantalla. No puede desactivar ambas opciones.

## Datos por lotes {#batch-data}

Para destinos [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] o [!UICONTROL Bulk Segment] , rellene los campos siguientes:

* **[!UICONTROL Protocol]**: (Obligatorio) Seleccione el protocolo deseado para este destino en la lista desplegable:
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**: (Obligatorio) Seleccione el servidor que desee para este destino en la lista desplegable.
* **[!UICONTROL Format]**: (Obligatorio) Seleccione el formato deseado para este destino en la lista desplegable:  [!DNL HTTP] o tipo de archivo, según el protocolo que haya elegido anteriormente.
* **[!UICONTROL Sync Type]**: (Obligatorio) Seleccione el tipo de sincronización deseado para este destino. Esto indica el nivel de actividades de usuario que los clientes querrían incluir en los pedidos salientes. Seleccione **[!UICONTROL Customer]** si los clientes solo están interesados en analizar las cualificaciones de los segmentos desde sus propiedades. Seleccione **[!UICONTROL Platform]** si desea incluir cualificaciones de segmentos de actividades fuera del sitio en todos los clientes [!DNL Audience Manager].
* **[!UICONTROL Customer]**: El archivo contiene usuarios activos que tienen al menos 1 realización de rasgos solo en las propiedades del cliente (asociadas con las del cliente  [!UICONTROL PID]) durante el período de tiempo seleccionado. Sus clientes deben utilizar esta opción para exportar sus *cualificaciones de segmento en tiempo real* a los destinos.
* **[!UICONTROL Platform]**: El archivo contiene usuarios activos que tienen al menos 1 interacción en tiempo real, ya sea la sincronización de ID o la realización de rasgos, en cualquier parte de las propiedades de todos los  [!DNL Audience Manager] clientes (asociadas con todos los PID de clientes) durante el período de tiempo seleccionado. Sus clientes deben utilizar esta opción para exportar sus *totales* clasificaciones de segmento a los destinos.
* **[!UICONTROL Lifetime]**: El archivo contiene los usuarios activos vistos en cualquier parte en las propiedades de todos los  [!DNL Audience Manager] clientes desde la creación del destino.
* **[!UICONTROL Sync Type Lookback Period]**: Si selecciona  [!UICONTROL Customer] o  [!UICONTROL Platform], seleccione un período de tiempo. Los archivos contienen usuarios activos durante el período de tiempo seleccionado.
A continuación, seleccione el tipo de orden. Esto indica la frecuencia y el alcance de cada integración saliente con los socios. Seleccione entre pedidos incrementales y completos.
* **[!UICONTROL Incremental Scheduled Run]**: Con cada ejecución, solo  [!DNL Audience Manager] salirán los nuevos usuarios netos cualificados desde el orden saliente anterior. Seleccione el período de tiempo deseado que desea que [!DNL Audience Manager] realice procesos de sincronización incrementales. Por ejemplo, puede seleccionar cada 24 horas, cada siete días, cada 30 días o nunca.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>El primer orden incremental equivale a un pedido completo porque nunca se envió a los usuarios anteriores al destino.

* **[!UICONTROL Full Sync Scheduled Run]**: Con cada ejecución,  [!DNL Audience Manager] salirá de todos los usuarios activos desde que se configuró por primera vez el destino. Seleccione la programación que desee utilizar [!DNL Audience Manager] para realizar procesos de sincronización completos. Por ejemplo, puede seleccionar cada 24 horas, cada siete días, cada 30 días o nunca.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>Se recomienda utilizar sincronizaciones incrementales con más frecuencia que sincronizaciones completas. Las sincronizaciones incrementales solo envían archivos que contienen nuevas realizaciones de características o sincronizaciones de ID. Las sincronizaciones completas envían todos los archivos, tanto si incluyen nuevas realizaciones como si no sincronizaciones de ID. Utilice únicamente la configuración [!UICONTROL Full Sync Scheduled Run] cuando los clientes necesiten una copia completa de todos sus usuarios, para reducir el volumen de datos salientes.

## Configuración de fuentes de datos {#configure-data-sources}

Para destinos [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] o [!UICONTROL Bulk Segment], rellene los campos siguientes. Esta configuración le permite enviar todos los datos (características, segmentos o ID, según el tipo seleccionado) asociados a las fuentes de datos.

* **[!UICONTROL All Unrestricted First Party Data]**: Seleccione esta opción para utilizar todas las fuentes de datos de origen. Si selecciona esta opción, las opciones [!UICONTROL Available Data Sources] están desactivadas.
* **[!UICONTROL Available Data Sources]**: Utilice las flechas para mover los orígenes de datos entre  **[!UICONTROL Available Data Sources]** los  **[!UICONTROL In File Data Sources]** cuadros y .

## Guardar y finalizar {#save-and-finalize}

El botón **[!UICONTROL Save]** se activa después de rellenar todos los campos obligatorios. Haga clic en **[!UICONTROL Save]** para finalizar el proceso de creación de destino.

## Eliminar destinos de compañía {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

Para eliminar un destino:

1. Haga clic en **[!UICONTROL Companies]**, busque y haga clic en la empresa que desee y, a continuación, haga clic en la pestaña **[!UICONTROL Destinations]**.
1. Haga clic ![](assets/icon_delete.png) en la columna **[!UICONTROL Actions]** del destino deseado.
1. Haga clic en **[!UICONTROL OK]** para confirmar la eliminación.

>[!NOTE]
>
>No puede eliminar un destino si tiene segmentos asignados a él.
