---
description: Crear, editar y eliminar destinos de Audience Manager.
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

Crear, editar y eliminar destinos de Audience Manager.

<!-- t_company_destinations.xml -->

Para obtener información detallada, consulte [Destinos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/destinations.html) en el *Guía del usuario de Audience Manager*.

## Crear o editar destinos de compañía {#create-edit-company-destinations}

Desplácese por las secciones para obtener instrucciones paso a paso sobre cómo crear nuevas páginas [!DNL Audience Manager] destinos o editar destinos existentes.

<!-- create-edit-company-destinations.xml -->

Visite la [página de integración de socios de Experience Cloud](https://wiki.corp.adobe.com/x/mPIMPw) antes de configurar destinos. La página contiene la información específica que debe rellenar para cada [!DNL Audience Manager] integración de partners.

Si su cliente desea utilizar [!DNL Adobe Media Optimizer] como destino en [!DNL Audience Manager] , debe configurar esto en [!DNL Adobe Media Optimizer].

## Vaya a la pestaña Destinos {#navigate-destinations}

1. Clic **[!UICONTROL Companies]**, luego busque y haga clic en la empresa deseada para mostrar su [!UICONTROL Profile] página. Puede usar el complemento [!UICONTROL Search] o los controles de paginación en la parte inferior de la lista para encontrar la empresa deseada. Puede ordenar cada columna en orden ascendente o descendente haciendo clic en el encabezado de la columna deseada.
1. Haga clic en **[!UICONTROL Destinations]** pestaña.
1. Para crear un nuevo destino, haga clic en **[!UICONTROL Add Destination]**. Para editar un destino existente, haga clic en el nombre del destino en la **[!UICONTROL Name]** columna.

## Configuración básica {#basic-settings}

Rellene los campos del **[!UICONTROL Basic Settings]** ventana.

* **[!UICONTROL Name]:** (Obligatorio) Especifique el nombre de este destino.
* **[!UICONTROL Description]:** Especifique información descriptiva sobre este destino.
* **[!UICONTROL Type]:** (Obligatorio) Seleccione el tipo de destino deseado:
   * **[!UICONTROL Bulk ID]**: ID de sincronización entre distintas plataformas.
   * **[!UICONTROL Bulk Trait]**: envía información de rasgos de forma masiva a diferentes plataformas.
   * **[!UICONTROL Bulk Segment]**: envía información de segmentos por lotes a diferentes plataformas.
   * **[!UICONTROL S2S]**: utilice destinos de servidor a servidor para enviar datos en tiempo real y por lotes a diferentes plataformas.
* **[!UICONTROL Auto-Fill Destination Mapping]:** ( [!UICONTROL S2S] Seleccione una opción:
   * **[!UICONTROL Segment ID]:** Si selecciona esta configuración, la asignación de valor de destino se rellena con la variable [!DNL Audience Manager] ID del segmento.
   * **[!UICONTROL Integration Code Value]:** Si selecciona esta configuración, la asignación de valor de destino se rellena con la variable [!DNL Audience Manager] Código de integración de segmentos.
* **[!UICONTROL User ID Key]:** (Obligatorio) Seleccione la clave de ID de usuario que desee para este destino en la lista desplegable.

Este ID se utiliza como ID de la fuente de datos maestra. Esto determina los ID de usuario que deben saltar en el archivo.

>[!NOTE]
>
>Para el [!UICONTROL Bulk ID] tipo de destino, no se puede utilizar el [!DNL Audience Manager] [!UICONTROL User ID] o el [!DNL Adobe Experience Cloud] ID.

Si su ID de fuente de datos ( [!UICONTROL DPID]) no aparece en la lista desplegable, debe seleccionar la opción **[!UICONTROL Outbound]** en el nivel de origen de datos en la [Página Configuración de fuente de datos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/manage-datasources.html).

* **[!UICONTROL Target Data Source]:** (Obligatorio) Seleccione la fuente de datos que desee para este destino en la lista desplegable. Esta configuración habilita el etiquetado de datos salientes, lo que permite la ingesta en sistemas independientes del lado del cliente.
* **[!UICONTROL Foreign Account ID]:** Especifique el ID de cuenta externa para este destino. Este es el valor de identificación en el sistema del destinatario para estos datos salientes.
* **[!UICONTROL Outbound Sample Rate Denominator]:** Cuando se desconoce la cantidad total de datos devueltos, utilice esta configuración para devolver solo una cantidad de datos de muestra, en lugar de la cantidad completa. Ajuste el número aquí para representar una fracción de los datos (por ejemplo, un valor de 100 devuelve 1/100 de la cantidad normal de datos, un valor de 10 devuelve 1/10 de la cantidad normal de datos). El valor predeterminado es &quot;1&quot;, que devuelve todos los datos.

## Datos en tiempo real (para destinos S2S) {#realtime-s2s}

Si está creando un [!UICONTROL S2S] destino, rellene los campos siguientes:

**[!UICONTROL Servers]**: Seleccione el `HTTP` servidor para este destino.
**[!UICONTROL Format]**: Seleccione el formato deseado para este destino de la lista desplegable: [!UICONTROL HTTP only].

>[!NOTE]
>
>Para [!DNL S2S] solo, puede habilitar o deshabilitar cualquiera de estas opciones [!UICONTROL Realtime] o [!UICONTROL Batch] destinos que utilizan los controles deslizantes de activación/desactivación en pantalla. No puede desactivar ambas opciones.

## Datos por lotes {#batch-data}

Para [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] o [!UICONTROL Bulk Segment] destinos, rellene los campos siguientes:

* **[!UICONTROL Protocol]**: (Obligatorio) Seleccione el protocolo deseado para este destino en la lista desplegable:
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**: (Obligatorio) Seleccione el servidor deseado para este destino de la lista desplegable.
* **[!UICONTROL Format]**: (Obligatorio) Seleccione el formato deseado para este destino en la lista desplegable: [!DNL HTTP] o tipo de archivo, según el protocolo elegido anteriormente.
* **[!UICONTROL Sync Type]**: (Obligatorio) Seleccione el tipo de sincronización deseado para este destino. Esto indica el nivel de actividades de usuario que los clientes desearían incluir en los pedidos salientes. Seleccionar **[!UICONTROL Customer]** si los clientes solo están interesados en analizar las clasificaciones de los segmentos a partir de sus propiedades. Seleccionar **[!UICONTROL Platform]** si desean incluir clasificaciones de segmentos de actividades fuera del sitio en todas las [!DNL Audience Manager] clientes.
* **[!UICONTROL Customer]**: el archivo contiene usuarios activos que tienen al menos 1 realización de características solo en las propiedades del cliente (asociadas con la propiedad del cliente) [!UICONTROL PID]) para el período de tiempo seleccionado. Los clientes deben utilizar esta opción para enviar sus *en tiempo real* cualificaciones de segmentos a destinos.
* **[!UICONTROL Platform]**: El archivo contiene usuarios activos que tienen al menos 1 interacción en tiempo real, ya sea sincronización de ID o realización de características, en cualquier lugar de todos los sitios [!DNL Audience Manager] las propiedades de los clientes (asociadas a todos los PID de cliente) durante el período de tiempo seleccionado. Los clientes deben utilizar esta opción para enviar sus *total* cualificaciones de segmentos a destinos.
* **[!UICONTROL Lifetime]**: el archivo contiene usuarios activos vistos en cualquier parte de todos los sitios [!DNL Audience Manager] propiedades de los clientes desde la creación del destino.
* **[!UICONTROL Sync Type Lookback Period]**: Si selecciona [!UICONTROL Customer] o [!UICONTROL Platform], seleccione un periodo de tiempo. Los archivos contienen usuarios activos para el período de tiempo seleccionado.
A continuación, seleccione el tipo de pedido. Esto indica la frecuencia y el ámbito de cada integración saliente con los socios. Seleccione entre pedidos incrementales y completos.
* **[!UICONTROL Incremental Scheduled Run]**: Con cada ejecución, [!DNL Audience Manager] solo sacará a los nuevos usuarios netos cualificados desde el pedido saliente anterior. Seleccione el período de tiempo deseado [!DNL Audience Manager] para realizar procesos de sincronización incrementales. Por ejemplo, puede seleccionar cada 24 horas, cada siete días, cada 30 días o nunca.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>El primer pedido incremental es equivalente a un pedido completo porque nunca se enviaron usuarios anteriores al destino.

* **[!UICONTROL Full Sync Scheduled Run]**: Con cada ejecución, [!DNL Audience Manager] saldrá de todos los usuarios activos desde que se configuró el destino por primera vez. Seleccione la programación que desee [!DNL Audience Manager] para utilizar para realizar procesos de sincronización completos. Por ejemplo, puede seleccionar cada 24 horas, cada siete días, cada 30 días o nunca.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>Se recomienda utilizar sincronizaciones incrementales con más frecuencia que sincronizaciones completas. Las sincronizaciones incrementales solo envían archivos que contienen nuevas realizaciones de rasgos o sincronizaciones de ID. Las sincronizaciones completas envían todos los archivos, independientemente de si incluyen nuevas realizaciones o sincronizaciones de ID. Utilice solo la variable [!UICONTROL Full Sync Scheduled Run] cuando los clientes necesitan una copia completa de todos sus usuarios, para reducir el volumen de datos saliente.

## Configuración de fuentes de datos {#configure-data-sources}

Para [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] o [!UICONTROL Bulk Segment] destinos, rellene los campos siguientes. Esta configuración le permite enviar todos los datos (características, segmentos o ID, según el tipo seleccionado) asociados a las fuentes de datos.

* **[!UICONTROL All Unrestricted First Party Data]**: seleccione esta opción para utilizar todas las fuentes de datos de origen. Si selecciona esta opción, la variable [!UICONTROL Available Data Sources] Las opciones de están desactivadas.
* **[!UICONTROL Available Data Sources]**: utilice las flechas para mover las fuentes de datos entre los **[!UICONTROL Available Data Sources]** y **[!UICONTROL In File Data Sources]** cajas.

## Guardar y finalizar {#save-and-finalize}

El **[!UICONTROL Save]** se activa después de rellenar todos los campos obligatorios. Clic **[!UICONTROL Save]** para finalizar el proceso crear destino.

## Eliminar destinos de empresa {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

Para eliminar un destino:

1. Clic **[!UICONTROL Companies]**, busque y haga clic en la empresa que quiera y luego haga clic en **[!UICONTROL Destinations]** pestaña.
1. Clic  ![](assets/icon_delete.png) en el **[!UICONTROL Actions]** del destino deseado.
1. Clic **[!UICONTROL OK]** para confirmar la eliminación.

>[!NOTE]
>
>No puede eliminar un destino si tiene segmentos asignados.
