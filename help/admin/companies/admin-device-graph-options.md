---
description: Las Opciones de gráfico de dispositivos están disponibles para las empresas que participan en Adobe Experience Cloud Device Co-op. Si un cliente también tiene una relación contractual con un proveedor de gráficos de dispositivos de terceros integrado con Audience Manager, esta sección mostrará opciones para ese gráfico de dispositivos. Estas opciones se encuentran en Empresas > nombre de la empresa > Perfil > Opciones de gráfico de dispositivos.
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

El [!UICONTROL Device Graph Options] están disponibles para las empresas que participan en [!DNL Adobe Experience Cloud Device Co-op]. Si un cliente también tiene una relación contractual con un proveedor de gráficos de dispositivos de terceros integrado con Audience Manager, esta sección mostrará opciones para ese gráfico de dispositivos. Estas opciones se encuentran en [!UICONTROL Companies] > nombre de la empresa > [!UICONTROL Profile] > [!UICONTROL Device Graph Options].

![](assets/adminUIdataSource.png)

Esta ilustración utiliza nombres genéricos para las opciones de gráficos de dispositivos de terceros. En producción, estos nombres provienen del proveedor del gráfico del dispositivo y pueden variar de lo que se muestra aquí. Por ejemplo, la variable [!DNL LiveRamp] opciones normalmente (pero no siempre):

* Empiece por &quot;[!DNL LiveRamp]&quot;
* Contiene un segundo nombre que varía
* Finalizar con &quot;[!UICONTROL - Household]&quot; o &quot;[!UICONTROL -Person]&quot;

## Opciones del gráfico de dispositivos definidas {#device-graph-options-defined}

Las opciones del gráfico de dispositivos que seleccione aquí muestran u ocultan el [!UICONTROL Device Options] opciones disponibles para un [!DNL Audience Manager] cliente cuando crea un [!UICONTROL Profile Merge Rule].

### Gráfico de dispositivos de cooperación {#co-op-graph}

Clientes que participan en [Cooperación entre dispositivos de Adobe Experience Cloud](https://experienceleague.adobe.com/docs/device-co-op/using/about/overview.html?lang=en) utilice estas opciones para crear un [!UICONTROL Profile Merge Rule] con [datos determinísticos y probabilísticos](https://experienceleague.adobe.com/docs/device-co-op/using/device-graph/links.html?lang=en). El [!DNL Corporate Provisioning Team] activa y desactiva esta opción mediante un back-end [!DNL API] llamada. Estas casillas no se pueden activar ni desactivar en [!DNL Admin UI]. Además, la variable **[!UICONTROL Co-op Device Graph]** y **[!UICONTROL Company Device Graph]** Las opciones de se excluyen mutuamente. Los clientes pueden pedirnos que activemos uno o el otro, pero no ambos. Cuando se selecciona, se muestra el **[!UICONTROL Co-op Device Graph]** control en la [!UICONTROL Device Options] configuración de un [!UICONTROL Profile Merge Rule].

![](assets/adminUI1.png)

### Gráfico de dispositivos de la empresa {#company-graph}

Esta opción es para [!DNL Analytics] clientes que utilizan el [!UICONTROL People] métrica en su [!DNL Analytics] grupo de informes. El [!DNL Corporate Provisioning Team] activa y desactiva esta opción mediante un back-end [!DNL API] llamada. Estas casillas no se pueden activar ni desactivar en [!DNL Admin UI]. Además, la variable **[!UICONTROL Company Device Graph]** y **[!UICONTROL Co-op Device Graph]** Las opciones de se excluyen mutuamente. Los clientes pueden pedirnos que activemos uno o el otro, pero no ambos. Cuando está marcada:

* Este gráfico de dispositivos utiliza datos determinísticos que pertenecen a la empresa que está configurando (sin datos probabilísticos).
* [!DNL Audience Manager] crea automáticamente un [!UICONTROL Data Source] llamado `*`nombre del socio`*-Company Device Graph-Person`. En el [!UICONTROL Data Source] página de detalles, [!DNL Audience Manager] Los clientes de pueden cambiar el nombre del socio, la descripción y la aplicación [Controles de exportación de datos](https://experienceleague.adobe.com/docs/device-co-op/using/device-graph/links.html?lang=en) a esta fuente de datos.
* [!DNL Audience Manager] clientes *no* ver una nueva configuración en [!UICONTROL Device Options] sección para un [!UICONTROL Profile Merge Rule].

### Gráfico de dispositivos LiveRamp (persona o hogar) {#liveramp-device-graph}

Estas casillas están habilitadas en la variable [!DNL Admin UI] cuando un socio crea un [!UICONTROL Data Source] y selecciona **[!UICONTROL Use as an Authenticated Profile]** y/o **[!UICONTROL Use as a Device Graph]**. Los nombres de estas configuraciones están determinados por el proveedor de gráficos de dispositivos de terceros (por ejemplo, [!DNL LiveRamp], [!DNL TapAd], etc.). Cuando se selecciona, significa que la empresa que está configurando utilizará los datos proporcionados por estos gráficos de dispositivos.

![](assets/adminUI2.png)

>[!MORELIKETHIS]
>
>* [Definición de las opciones de las reglas de combinación de perfiles](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/merge-rule-definitions.html?lang=en).
>* [Configuración de fuentes de datos y opciones de menú](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html?lang=en)

