---
description: Utilice la página Empresas de la herramienta Administración de Audience Manager para crear una nueva empresa.
seo-description: Use the Companies page in the Audience Manager Admin tool to create a new company.
seo-title: Create a Company Profile
title: Crear un perfil de compañía
uuid: 55de18f8-883d-43fe-b37f-e8805bb92f7a
exl-id: 80bb8a89-0207-4645-ac42-e73cd10561de
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 4%

---

# Crear un perfil de compañía {#create-a-company-profile}

Utilice la página [!UICONTROL Companies] de la herramienta Administración de Audience Manager para crear una nueva empresa.

<!-- t_create_company.xml -->

>[!NOTE]
>
>Debe tener la función **[!UICONTROL DEXADMIN]** para crear nuevas empresas.

1. Haga clic **[!UICONTROL Companies]** > **[!UICONTROL Add Company]**.
1. Rellene los campos:

   * **[!UICONTROL Name]**: (Obligatorio) Especifique el nombre de la empresa.
   * **[!UICONTROL Description]**: (Obligatorio) Proporcione información descriptiva sobre la empresa, como la industria o su nombre completo.
   * **[!UICONTROL Subdomain]**: (Obligatorio) Especifique el subdominio de la empresa. El texto que introduzca es lo que se muestra como el subdominio de la llamada de evento. Esto no se puede cambiar. Debe ser una cadena de caracteres [!DNL URL] válidos.

      Por ejemplo, si su empresa se llama [!DNL AcmeCorp], el subdominio será [!DNL acmecorp].

      Audience Manager utiliza el subdominio para el [!UICONTROL Data Collection Server] (DCS). En el ejemplo anterior, si el [!DNL URL] completo de su empresa en [!UICONTROL DCS] sería [!DNL acmecorp.demdex.net].

   * **[!UICONTROL Lifecyle]**: Especifique el escenario deseado para la empresa:
      * **[!UICONTROL Active]**: Especifique que la empresa será un cliente Audience Manager activo. Una cuenta [!UICONTROL Active] significa que un cliente paga, no solo por consultoría, sino por el SKU del Audience Manager.
      * **[!UICONTROL Demo]**: Especifique que la empresa solo será para fines de demostración. Los datos de los informes se falsificarán automáticamente.
      * **[!UICONTROL Prospect]**: Especifique que la empresa es un cliente Audience Manager potencial, como que una empresa recibe una configuración gratuita  [!DNL POC] o de cuenta para una demostración de ventas.
      * **[!UICONTROL Test]**: Especifique que la empresa solo se utilizará para pruebas internas.
   * **[!UICONTROL Account Types]**: Especifique el conjunto completo de tipos de cuenta para esta empresa. Ningún tipo de cuenta se excluye mutuamente con ningún otro tipo.
      * **[!UICONTROL Full AAM]**: Especifique que la empresa tendrá una cuenta completa de Adobe Audience Manager y que los usuarios tendrán acceso de inicio de sesión.
      * **[!UICONTROL MMP]**: Especifique que la empresa ha sido habilitada para utilizar las capacidades  [!UICONTROL Master Marketing Profile] ([!UICONTROL MMP]). El [!UICONTROL MMP] permite compartir audiencias en el Experience Cloud mediante un [!UICONTROL Experience Cloud ID] ([!DNL MCID]) asignado a cada visitante y luego utilizado por el Audience Manager. Si selecciona este tipo de cuenta, el [!UICONTROL Experience Cloud ID Service] también se selecciona automáticamente.

         Para obtener más información, consulte [Audiencias de Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/services/audiences/audience-library.html?lang=en).
   * **[!UICONTROL Data Source]**: Especifique que la empresa es un proveedor de datos de terceros dentro del Audience Manager.
   * **[!UICONTROL Targeting Partner]**: Especifique que la empresa actúa como plataforma de segmentación para los clientes Audience Manager.
   * **[!UICONTROL Visitor ID Service]**: Especifique que la empresa ha sido habilitada para utilizar  [!UICONTROL Experience Cloud Visitor ID Service].

      El [!UICONTROL Experience Cloud Visitor ID Service] proporciona un ID de visitante universal para las soluciones de Experience Cloud. Para obtener más información, consulte la [guía del usuario del servicio de ID de visitante de Experience Cloud](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=en).

   * **[!UICONTROL Agency]**: Especifique que la empresa tendrá una  [!UICONTROL Agency] cuenta.



1. Haga clic **[!UICONTROL Create]**. Continúe con las instrucciones de [Editar un perfil de empresa](../companies/admin-manage-company-profiles.md#edit-company-profile).

   ![Resultado de los pasos](assets/add_company.png)

## Editar un perfil de compañía {#edit-company-profile}

Edite el perfil de una empresa, incluido su nombre, descripción, subdominio, ciclo vital, etc.

<!-- t_edit_company_profile.xml -->

1. Haga clic en **[!UICONTROL Companies]**, luego localice y haga clic en la empresa que desee para mostrar su página [!UICONTROL Profile].

   Utilice el cuadro [!UICONTROL Search] o los controles de paginación situados en la parte inferior de la lista para encontrar la empresa que desee. Para ordenar cada columna en orden ascendente o descendente, haga clic en el encabezado de la columna que desee.

   ![Resultado de los pasos](assets/profile_company.png)

1. Edite los campos como sea necesario:

   * **[!UICONTROL Name]**: Edite el nombre de la empresa. Se trata de un campo obligatorio.
   * **[!UICONTROL Description]**: Edite la descripción de la empresa. Se trata de un campo obligatorio.
   * **[!UICONTROL Subdomain]**: (Obligatorio) Especifique el subdominio de la empresa. El texto que introduzca es lo que se muestra como el subdominio de la llamada de evento. Esto no se puede cambiar. Debe ser una cadena de caracteres [!DNL URL] válidos.

      Por ejemplo, si su empresa se llama [!DNL AcmeCorp], el subdominio será [!DNL acmecorp].

      Audience Manager utiliza el subdominio para el [!UICONTROL Data Collection Server] (DCS). En el ejemplo anterior, si el [!DNL URL] completo de su empresa en [!UICONTROL DCS] sería [!DNL acmecorp.demdex.net].

   * **[!UICONTROL imsOrgld]**: ([!UICONTROL Identity Management System Organization ID]) Este ID le permite conectar su empresa con Adobe Experience Cloud.
   * **[!UICONTROL Lifecyle]**: Especifique el escenario deseado para la empresa:
      * **[!UICONTROL Active]**: Especifique que la empresa será un cliente Audience Manager activo. Una cuenta activa significa un cliente de pago, no solo para consultoría, sino para el SKU del Audience Manager.
      * **[!UICONTROL Demo]**: Especifique que la empresa solo será para fines de demostración. Los datos de los informes se falsificarán automáticamente.
      * **[!UICONTROL Prospect]**: Especifique que la empresa es un cliente Audience Manager potencial, como que una empresa recibe una configuración gratuita  [!DNL POC] o de cuenta para una demostración de ventas.
      * **[!UICONTROL Test]**: Especifique que la empresa solo se utilizará para pruebas internas.
   * **[!UICONTROL Account Types]**: Especifique el conjunto completo de tipos de cuenta para esta empresa. Ningún tipo de cuenta se excluye mutuamente con ningún otro tipo.
      * **[!UICONTROL Full AAM]**: Especifique que la empresa tendrá una cuenta completa de Adobe Audience Manager y que los usuarios tendrán acceso de inicio de sesión.
      * **[!UICONTROL MMP]**: Especifique que la empresa ha sido habilitada para utilizar las capacidades del perfil de marketing maestro ([!UICONTROL MMP]).

         Si selecciona este tipo de cuenta, **[!UICONTROL Visitor ID Service]** también se selecciona automáticamente.
Para obtener más información, consulte [Audiencias de Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/services/audiences/audience-library.html?lang=en).
   * **[!UICONTROL Data Source]**: Especifique que la empresa es un proveedor de datos de terceros dentro del Audience Manager.
   * **[!UICONTROL Targeting Partner]**: Especifique que la empresa actúa como plataforma de segmentación para los clientes Audience Manager.
   * **[!UICONTROL Visitor ID Service]**: Especifique que la empresa ha sido habilitada para utilizar el servicio de ID de visitante de Experience Cloud.

      El servicio de identificación de visitantes de Experience Cloud proporciona un ID de visitante universal en las soluciones de Experience Cloud. Para obtener más información, consulte la [guía del usuario del servicio de ID de Experience Cloud](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en).

   * **[!UICONTROL Agency]**: Especifique que la empresa tendrá una cuenta de Agencia.
   * **[!UICONTROL Features]**: Seleccione las opciones que desee:
      * **[!UICONTROL Password Expiration]**: Establece que todas las contraseñas de usuario de esta empresa caduquen después de 90 días para aumentar la seguridad del Audience Manager.
      * **[!UICONTROL Reporting]**: Habilita los informes de Audience Manager para esta empresa.
      * **[!UICONTROL Role Based Access Controls]**: Habilite los controles de acceso basados en roles para esta empresa. Los controles de acceso basados en funciones le permiten crear grupos de usuarios con diferentes permisos de acceso. Los usuarios individuales de estos grupos pueden acceder solo a las funciones específicas del Audience Manager.


1. Haga clic **[!UICONTROL Submit Updates]**.

## Eliminar un perfil de compañía {#delete-company-profile}

Utilice la página [!UICONTROL Companies] de la herramienta [!UICONTROL Admin] Audience Manager para eliminar una empresa existente.

<!-- t_delete_company.xml -->

>[!NOTE]
>
>Debe tener la función [!UICONTROL DEXADMIN] para eliminar las empresas existentes.

1. Para eliminar una empresa existente, haga clic en **[!UICONTROL Companies]**.

   ![Resultado de los pasos](assets/companies.png)

1. Haga clic ![](assets/icon_delete.png) en la columna **[!UICONTROL Actions]** de la empresa deseada.
1. Haga clic en **[!UICONTROL OK]** para confirmar la eliminación.
