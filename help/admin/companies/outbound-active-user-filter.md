---
description: Siga estas instrucciones para generar un archivo de sincronización completo que incluya solo usuarios activos recientemente. Es posible que desee filtrar para que los usuarios activos inserten datos relevantes en un sistema de segmentación en el sitio o para limitar el tamaño de los archivos enviados a un DSP. No puede utilizar este filtro con sincronización incremental.
seo-description: Siga estas instrucciones para generar un archivo de sincronización completo que incluya solo usuarios activos recientemente. Es posible que desee filtrar para que los usuarios activos inserten datos relevantes en un sistema de segmentación en el sitio o para limitar el tamaño de los archivos enviados a un DSP. No puede utilizar este filtro con sincronización incremental.
seo-title: Filtrar datos de salida solo por usuarios activos
title: Filtrar datos de salida solo por usuarios activos
uuid: a2b4a385-eee3-458c-b978-09509cacb397
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 8%

---


# Filtrar datos de salida solo por usuarios activos {#filter-outbound-data-by-active-users-only}

Siga estas instrucciones para generar un archivo de sincronización completo que incluya solo usuarios activos recientemente. Es posible que desee filtrar para que los usuarios activos inserten datos relevantes en un sistema de segmentación en el sitio o para limitar el tamaño de los archivos enviados a un DSP. No puede utilizar este filtro con sincronización incremental.

>[!NOTE]
>
>No es necesario ver un visitante en un sitio de clientes seleccionado o en su tráfico de publicidad para calificar como &quot;activo&quot;. Cualquier cliente o [!DNL Audience Manager] socio puede considerarlos como &quot;activos&quot;.

Para filtrar solo por usuarios activos:

1. Haga clic **[!UICONTROL Companies]**.
1. Seleccione la compañía con la que desee trabajar y haga clic en **[!UICONTROL Destinations]**.
1. En la [!UICONTROL Batch Data] sección , establezca las siguientes opciones:

   * **[!UICONTROL Sync Type]**:: Seleccione **[!UICONTROL Customer]** o **[!UICONTROL Platform]**.
   * **[!UICONTROL Sync Type Lookback Period]**:: Este intervalo de tiempo define el intervalo del archivo de datos. Las opciones incluyen **[!UICONTROL 24 hours]**, **[!UICONTROL 7 days]**, **[!UICONTROL 30 days]**.
   * **[!UICONTROL Incremental Sync Scheduled Run]**: Select **[!UICONTROL Never]**. Recuerde que este filtro se aplica únicamente a los archivos de sincronización completa.
   * **[!UICONTROL Full Sync Scheduled Run]**:: Esto determina la frecuencia con la que desea recibir este archivo. Las opciones incluyen **[!UICONTROL 24 hours]**, **[!UICONTROL 7 days]**, **[!UICONTROL 30 days]** o **[!UICONTROL Never]** (para deshabilitar).

1. Haga clic **[!UICONTROL Save]**.
