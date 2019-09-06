---
description: Siga estas instrucciones para generar un archivo de sincronización completo que incluya solo a los usuarios activos recientemente. Es posible que desee filtrar los usuarios activos para que inserten datos relevantes en un sistema de segmentación en el sitio o para limitar el tamaño de los archivos enviados a un DSP. No puede utilizar este filtro con una sincronización incremental.
seo-description: Siga estas instrucciones para generar un archivo de sincronización completo que incluya solo a los usuarios activos recientemente. Es posible que desee filtrar los usuarios activos para que inserten datos relevantes en un sistema de segmentación en el sitio o para limitar el tamaño de los archivos enviados a un DSP. No puede utilizar este filtro con una sincronización incremental.
seo-title: Filtrar datos salientes únicamente por usuarios activos
title: Filtrar datos salientes únicamente por usuarios activos
uuid: a 2 b 4 a 385-eee 3-458 c-b 978-09509 cacb 397
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# Filtrar datos salientes únicamente por usuarios activos {#filter-outbound-data-by-active-users-only}

Siga estas instrucciones para generar un archivo de sincronización completo que incluya solo a los usuarios activos recientemente. Es posible que desee filtrar los usuarios activos para que inserten datos relevantes en un sistema de segmentación en el sitio o para limitar el tamaño de los archivos enviados a un DSP. No puede utilizar este filtro con una sincronización incremental.

>[!NOTE]
>
>No es necesario que un visitante se vea en un sitio de cliente seleccionado o en su tráfico publicitario para calificarlo como "activo". Cualquier [!DNL Audience Manager] cliente o socio puede verlos para calificar como "activo".

Para filtrar únicamente por usuarios activos:

1. Haga clic en **[!UICONTROL Companies]**.
1. Seleccione la empresa con la que desee trabajar y haga clic **[!UICONTROL Destinations]** en.
1. En [!UICONTROL Batch Data] la sección, establezca las siguientes opciones:

   * **[!UICONTROL Sync Type]**: Seleccione **[!UICONTROL Customer]** o **[!UICONTROL Platform]**.
   * **[!UICONTROL Sync Type Lookback Period]**: Este intervalo de tiempo define el intervalo del archivo de datos. Las opciones incluyen **[!UICONTROL 24 hours]****[!UICONTROL 7 days]****[!UICONTROL 30 days]**.
   * **[!UICONTROL Incremental Sync Scheduled Run]**: Seleccione **[!UICONTROL Never]**. Recuerde, este filtro se aplica sólo a archivos de sincronización completos.
   * **[!UICONTROL Full Sync Scheduled Run]**: Esto determina la frecuencia con la que desea recibir este archivo. Las opciones incluyen **[!UICONTROL 24 hours]**, **[!UICONTROL 7 days]****[!UICONTROL 30 days]** o **[!UICONTROL Never]** (para deshabilitar).

1. Haga clic en **[!UICONTROL Save]**.
