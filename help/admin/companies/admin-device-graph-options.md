---
description: Las opciones de gráfico de dispositivos están disponibles para las empresas que participan en Device Co-op de Adobe Experience Cloud. Si un cliente también tiene una relación contractual con un proveedor de gráficos de dispositivos de terceros que esté integrado con el Audience Manager, esta sección mostrará las opciones para ese gráfico de dispositivos. Estas opciones se encuentran en Companies > company name > Profile > Device Graph Options.
seo-description: The Device Graph Options are available to companies that participate in the Adobe Experience Cloud Device Co-op. If a customer also has a contractual relationship with a third-party device graph provider that is integrated with Audience Manager, this section will show options for that device graph. These options are located in Companies > company name > Profile > Device Graph Options.
seo-title: Device Graph Options for Companies
title: Opciones de gráfico de dispositivos para compañías
uuid: a8ced843-710c-4a8f-a0d7-ea89d010a7a5
exl-id: 2502f3d2-b43c-410c-acb6-03c2a2ba2c1d
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 3%

---

# Opciones de gráfico de dispositivos para compañías {#device-graph-options-for-companies}

Los [!UICONTROL Device Graph Options] están disponibles para las empresas que participan en [!DNL Adobe Experience Cloud Device Co-op]. Si un cliente también tiene una relación contractual con un proveedor de gráficos de dispositivos de terceros que esté integrado con el Audience Manager, esta sección mostrará las opciones para ese gráfico de dispositivos. Estas opciones se encuentran en [!UICONTROL Companies] > nombre de la empresa > [!UICONTROL Profile] > [!UICONTROL Device Graph Options].

![](assets/adminUIdataSource.png)

Esta ilustración utiliza nombres genéricos para las opciones de gráficos de dispositivos de terceros. En producción, estos nombres provienen del proveedor de gráficos de dispositivos y pueden variar con respecto a lo que se muestra aquí. Por ejemplo, las opciones de [!DNL LiveRamp] generalmente (pero no siempre):

* Empiece por &quot;[!DNL LiveRamp]&quot;
* Contienen un nombre intermedio que varía
* Finalizar con &quot;[!UICONTROL - Household]&quot; o &quot;[!UICONTROL -Person]&quot;

## Opciones definidas de Device Graph {#device-graph-options-defined}

Las opciones de gráfico de dispositivos que seleccione aquí exponen u ocultan las [!UICONTROL Device Options] opciones disponibles para un cliente [!DNL Audience Manager] cuando crean un [!UICONTROL Profile Merge Rule].

### Gráfico de dispositivos de cooperación {#co-op-graph}

Los clientes que participan en [Adobe Experience Cloud Device Co-op](https://experienceleague.adobe.com/docs/device-co-op/using/about/overview.html?lang=en) utilizan estas opciones para crear un [!UICONTROL Profile Merge Rule] con [datos determinísticos y probabilísticos](https://experienceleague.adobe.com/docs/device-co-op/using/device-graph/links.html?lang=en). El [!DNL Corporate Provisioning Team] activa y desactiva esta opción mediante una llamada back-end [!DNL API]. No puede marcar ni borrar estas casillas en [!DNL Admin UI]. Además, las opciones **[!UICONTROL Co-op Device Graph]** y **[!UICONTROL Company Device Graph]** se excluyen mutuamente. Los clientes pueden pedirnos que activemos uno o el otro, pero no ambos. Cuando se selecciona, esto expone el control **[!UICONTROL Co-op Device Graph]** en la configuración [!UICONTROL Device Options] de un [!UICONTROL Profile Merge Rule].

![](assets/adminUI1.png)

### Gráfico de dispositivos de la empresa {#company-graph}

Esta opción es para clientes [!DNL Analytics] que usan la métrica [!UICONTROL People] en su grupo de informes [!DNL Analytics]. El [!DNL Corporate Provisioning Team] activa y desactiva esta opción mediante una llamada back-end [!DNL API]. No puede marcar ni borrar estas casillas en [!DNL Admin UI]. Además, las opciones **[!UICONTROL Company Device Graph]** y **[!UICONTROL Co-op Device Graph]** se excluyen mutuamente. Los clientes pueden pedirnos que activemos uno o el otro, pero no ambos. Cuando está marcado:

* Este gráfico de dispositivos utiliza datos determinísticos que pertenecen a la empresa que está configurando (sin datos probabilísticos).
* [!DNL Audience Manager] crea automáticamente un  [!UICONTROL Data Source] nombre de  `*`socio`*-Company Device Graph-Person`. En la página de detalles [!UICONTROL Data Source] , los clientes [!DNL Audience Manager] pueden cambiar el nombre del socio, la descripción y aplicar [Controles de exportación de datos](https://experienceleague.adobe.com/docs/device-co-op/using/device-graph/links.html?lang=en) a esta fuente de datos.
* [!DNL Audience Manager] los clientes de  *no* ven una nueva configuración en la  [!UICONTROL Device Options] sección para  [!UICONTROL Profile Merge Rule].

### LiveRamp Device Graph (persona o hogar) {#liveramp-device-graph}

Estas casillas de verificación están habilitadas en el [!DNL Admin UI] cuando un socio crea un [!UICONTROL Data Source] y selecciona **[!UICONTROL Use as an Authenticated Profile]** o **[!UICONTROL Use as a Device Graph]**. Los nombres de estos ajustes los determina el proveedor de gráficos de dispositivos de terceros (por ejemplo, [!DNL LiveRamp], [!DNL TapAd], etc.). Cuando se selecciona, esto significa que la empresa que está configurando va a utilizar los datos proporcionados por estos gráficos de dispositivos.

![](assets/adminUI2.png)

>[!MORELIKETHIS]
>
>* [Definición de las opciones de las reglas de combinación de perfiles](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/merge-rule-definitions.html?lang=en).
>* [Configuración y opciones de menú de fuentes de datos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html?lang=en)

