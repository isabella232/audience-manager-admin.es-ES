---
description: Las opciones de Device Graph están disponibles para las empresas que participan en Adobe Experience Cloud Device Co-op. Si un cliente también tiene una relación contractual con un proveedor de gráficos de dispositivos de terceros que está integrado con Audience Manager, esta sección mostrará las opciones para ese gráfico de dispositivos. Estas opciones se encuentran en Empresas > nombre de la empresa > Perfil > Opciones de Device Graph.
seo-description: Las opciones de Device Graph están disponibles para las empresas que participan en Adobe Experience Cloud Device Co-op. Si un cliente también tiene una relación contractual con un proveedor de gráficos de dispositivos de terceros que está integrado con Audience Manager, esta sección mostrará las opciones para ese gráfico de dispositivos. Estas opciones se encuentran en Empresas > nombre de la empresa > Perfil > Opciones de Device Graph.
seo-title: Opciones de Device Graph para empresas
title: Opciones de Device Graph para empresas
uuid: a8ced843-710c-4a8f-a0d7-ea89d010a7a5
translation-type: tm+mt
source-git-commit: 2998dc049971b2fac8c45ca6e3118ea607ae3f92

---


# Opciones de Device Graph para empresas {#device-graph-options-for-companies}

Los [!UICONTROL Device Graph Options] están disponibles para las empresas que participan en la [!DNL Adobe Experience Cloud Device Co-op]. Si un cliente también tiene una relación contractual con un proveedor de gráficos de dispositivos de terceros que está integrado con Audience Manager, esta sección mostrará las opciones para ese gráfico de dispositivos. Estas opciones se encuentran en [!UICONTROL Companies] &gt; nombre de la empresa &gt; [!UICONTROL Profile] &gt; [!UICONTROL Device Graph Options].

![](assets/adminUIdataSource.png)

En esta ilustración se utilizan nombres genéricos para las opciones de gráficos de dispositivos de terceros. En producción, estos nombres provienen del proveedor de gráficos de dispositivos y pueden variar de lo que se muestra aquí. Por ejemplo, las [!DNL LiveRamp] opciones suelen (pero no siempre):

* Empiece por "[!DNL LiveRamp]"
* Contener un nombre medio que varía
* Finalizar con "[!UICONTROL - Household]" o "[!UICONTROL -Person]"

## Opciones de Device Graph definidas {#device-graph-options-defined}

Las opciones de gráficos de dispositivos que seleccione aquí exponen u ocultan las [!UICONTROL Device Options] opciones disponibles para un [!DNL Audience Manager] cliente cuando crea un [!UICONTROL Profile Merge Rule].

### Gráfico de dispositivos de cooperación {#co-op-graph}

Los clientes que participan en Device Co-op [de](https://marketing.adobe.com/resources/help/en_US/mcdc/) Adobe Experience Cloud utilizan estas opciones para crear un [!UICONTROL Profile Merge Rule] evento con datos [determinísticos y probabilísticos](https://marketing.adobe.com/resources/help/en_US/mcdc/mcdc-links.html). La [!DNL Corporate Provisioning Team] activa y desactiva esta opción mediante una [!DNL API] llamada back-end. Estas casillas no se pueden marcar ni borrar en la [!DNL Admin UI]. Además, las opciones **[!UICONTROL Co-op Device Graph]** y **[!UICONTROL Company Device Graph]** son mutuamente excluyentes. Los clientes pueden solicitarnos que activemos uno u otro, pero no ambos. Cuando se selecciona, se expone el **[!UICONTROL Co-op Device Graph]** control en la [!UICONTROL Device Options] configuración de un [!UICONTROL Profile Merge Rule].

![](assets/adminUI1.png)

### Gráfico de dispositivos de la empresa {#company-graph}

Esta opción es para [!DNL Analytics] los clientes que utilizan la [!UICONTROL People] métrica en su grupo [!DNL Analytics] de informes. La [!DNL Corporate Provisioning Team] activa y desactiva esta opción mediante una [!DNL API] llamada back-end. Estas casillas no se pueden marcar ni borrar en la [!DNL Admin UI]. Además, las opciones **[!UICONTROL Company Device Graph]** y **[!UICONTROL Co-op Device Graph]** son mutuamente excluyentes. Los clientes pueden solicitarnos que activemos uno u otro, pero no ambos. Cuando está marcado:

* Este gráfico de dispositivos utiliza datos determinísticos que pertenecen a la empresa que está configurando (sin datos probabilísticos).
* [!DNL Audience Manager] crea automáticamente un [!UICONTROL Data Source] nombre de `*`socio`*-Company Device Graph-Person`. En la página [!UICONTROL Data Source] de detalles, [!DNL Audience Manager] los clientes pueden cambiar el nombre del socio, la descripción y aplicar controles [de exportación](https://marketing.adobe.com/resources/help/en_US/aam/c_dec.html) de datos a esta fuente de datos.
* [!DNL Audience Manager] los clientes *no* ven una nueva configuración en la [!UICONTROL Device Options] sección para una [!UICONTROL Profile Merge Rule].

### LiveRamp Device Graph (persona o hogar) {#liveramp-device-graph}

Estas casillas de verificación se activan en el [!DNL Admin UI] momento en que un socio crea un [!UICONTROL Data Source] y selecciona **[!UICONTROL Use as an Authenticated Profile]** y/o **[!UICONTROL Use as a Device Graph]**. Los nombres de esta configuración los determina el proveedor de gráficos de dispositivos de terceros (por ejemplo, [!DNL LiveRamp], [!DNL TapAd], etc.). Cuando se selecciona, esto significa que la empresa que está configurando va a utilizar los datos proporcionados por estos gráficos de dispositivos.

![](assets/adminUI2.png)

>[!MORELIKETHIS]
>
>* [Opciones de regla de combinación de perfiles definidas](https://marketing.adobe.com/resources/help/en_US/aam/merge-rule-definitions.html)
>* [Configuración y opciones de menú de la fuente de datos](https://marketing.adobe.com/resources/help/en_US/aam/datasource-settings-definitions.html)

