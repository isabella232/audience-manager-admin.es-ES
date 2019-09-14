---
description: Utilice la página Empresas de la herramienta de administración de Audience Manager para crear una nueva empresa.
seo-description: Utilice la página Empresas de la herramienta de administración de Audience Manager para crear una nueva empresa.
seo-title: Crear un perfil de empresa
title: Crear un perfil de empresa
uuid: 55de18f8-883d-43fe-b37f-e8805bb92f7a
translation-type: tm+mt
source-git-commit: 71bf4cec222428686c1eab0998f66887db06da68

---


# Crear un perfil de empresa {#create-a-company-profile}

Utilice la página [!UICONTROL Companies] de la herramienta de administración de Audience Manager para crear una nueva empresa.

<!-- t_create_company.xml -->

>[!NOTE]
>
>Debe tener la **[!UICONTROL DEXADMIN]** función de crear nuevas empresas.

1. Click **[!UICONTROL Companies]** &gt; **[!UICONTROL Add Company]**.
1. Rellene los campos:

   * **[!UICONTROL Name]**:: (Requerido) Especifique el nombre de la empresa.
   * **[!UICONTROL Description]**:: (Requerido) Proporcione información descriptiva sobre la empresa, como la industria o su nombre completo.
   * **[!UICONTROL Subdomain]**:: (Requerido) Especifique el subdominio de la empresa. El texto que se introduce es lo que se muestra como subdominio de la llamada al evento. Esto no se puede cambiar. Debe ser una cadena de caracteres [!DNL URL]-válidos.

      Por ejemplo, si se nombrara a su empresa [!DNL AcmeCorp], el subdominio sería [!DNL acmecorp].

      Audience Manager utiliza el subdominio para [!UICONTROL Data Collection Server]([!UICONTROL DCS]). En el ejemplo anterior, si la empresa está llena [!DNL URL] en [!UICONTROL DCS] sería [!DNL acmecorp.demdex.net].

   * **[!UICONTROL Lifecyle]**:: Especifique la etapa deseada para la empresa:
      * **[!UICONTROL Active]**:: Especifique que la empresa será un cliente activo de Audience Manager. Una [!UICONTROL Active] cuenta significa un cliente de pago, no solo para consultar, sino también para el SKU de Audience Manager.
      * **[!UICONTROL Demo]**:: Especifique que la empresa será solo para fines de demostración. Los datos de informes se falsificarán automáticamente.
      * **[!UICONTROL Prospect]**:: Especifique que la empresa es un cliente potencial de Audience Manager, como una empresa a la que se le ha dado una configuración gratuita [!DNL POC] o de cuenta para una demostración de ventas.
      * **[!UICONTROL Test]**:: Especifique que la empresa será solo para pruebas internas.
   * **[!UICONTROL Account Types]**:: Especifique el conjunto completo de tipos de cuenta para esta empresa. Ningún tipo de cuenta se excluye mutuamente con ningún otro tipo.
      * **[!UICONTROL Full AAM]**:: Especifique que la empresa tendrá una cuenta completa de Adobe Audience Manager y que los usuarios tendrán acceso de inicio de sesión.
      * **[!UICONTROL MMP]**:: Especifique que la empresa ha sido habilitada para usar las capacidades [!UICONTROL Master Marketing Profile] ([!UICONTROL MMP]). El [!UICONTROL MMP] permite compartir audiencias en Experience Cloud mediante un [!UICONTROL Experience Cloud ID] ([!DNL MCID]) asignado a cada visitante y, a continuación, utilizado por Audience Manager. Si selecciona este tipo de cuenta, también [!UICONTROL Experience Cloud ID Service] se selecciona automáticamente.

         Para obtener más información, consulte [Servicios de audiencias - Perfil](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html)de marketing principal.
   * **[!UICONTROL Data Source]**:: Especifique que la empresa es un proveedor de datos de terceros dentro de Audience Manager.
   * **[!UICONTROL Targeting Partner]**:: Especifique que la empresa actúa como plataforma de segmentación para los clientes de Audience Manager.
   * **[!UICONTROL Visitor ID Service]**:: Especifique que la empresa se ha habilitado para usar el [!UICONTROL Experience Cloud Visitor ID Service].

      El [!UICONTROL Experience Cloud Visitor ID Service] proporciona un ID de visitante universal en todas las soluciones de Experience Cloud. For more information, see the [Experience Cloud Visitor ID Service user guide](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-overview.html).

   * **[!UICONTROL Agency]**:: Especifique que la empresa tendrá una [!UICONTROL Agency] cuenta.



1. Haga clic en **[!UICONTROL Create]**. Continúe con las instrucciones de [Editar un perfil](../companies/admin-manage-company-profiles.md#edit-company-profile)de empresa.

   ![Resultado del paso](assets/add_company.png)

## Editar un perfil de empresa {#edit-company-profile}

Edite el perfil de una empresa, incluido su nombre, descripción, subdominio, ciclo vital, etc.

<!-- t_edit_company_profile.xml -->

1. Haga clic en **[!UICONTROL Companies]**, luego busque y haga clic en la empresa que desee para mostrar su [!UICONTROL Profile] página.

   Use el [!UICONTROL Search] cuadro o los controles de paginación en la parte inferior de la lista para encontrar la empresa deseada. Puede ordenar cada columna en orden ascendente o descendente haciendo clic en el encabezado de la columna deseada.

   ![Resultado del paso](assets/profile_company.png)

1. Edite los campos como sea necesario:

   * **[!UICONTROL Name]**:: Edite el nombre de la empresa. Este campo es obligatorio.
   * **[!UICONTROL Description]**:: Edite la descripción de la empresa. Este campo es obligatorio.
   * **[!UICONTROL Subdomain]**:: (Requerido) Especifique el subdominio de la empresa. El texto que se introduce es lo que se muestra como subdominio de la llamada al evento. Esto no se puede cambiar. Debe ser una cadena de caracteres [!DNL URL]-válidos.

      Por ejemplo, si se nombrara a su empresa [!DNL AcmeCorp], el subdominio sería [!DNL acmecorp].

      Audience Manager utiliza el subdominio para [!UICONTROL Data Collection Server] ([!UICONTROL DCS]). En el ejemplo anterior, si la empresa está llena [!DNL URL] en [!UICONTROL DCS] sería [!DNL acmecorp.demdex.net].

   * **[!UICONTROL imsOrgld]**:: ([!UICONTROL Identity Management System Organization ID]) Este ID le permite conectar su empresa con Adobe Experience Cloud.
   * **[!UICONTROL Lifecyle]**:: Especifique la etapa deseada para la empresa:
      * **[!UICONTROL Active]**:: Especifique que la empresa será un cliente activo de Audience Manager. Una cuenta activa significa un cliente de pago, no solo para consultar, sino también para el SKU de Audience Manager.
      * **[!UICONTROL Demo]**:: Especifique que la empresa será solo para fines de demostración. Los datos de informes se falsificarán automáticamente.
      * **[!UICONTROL Prospect]**:: Especifique que la empresa es un cliente potencial de Audience Manager, como una empresa a la que se le ha dado una configuración gratuita [!DNL POC] o de cuenta para una demostración de ventas.
      * **[!UICONTROL Test]**:: Especifique que la empresa será solo para pruebas internas.
   * **[!UICONTROL Account Types]**:: Especifique el conjunto completo de tipos de cuenta para esta empresa. Ningún tipo de cuenta se excluye mutuamente con ningún otro tipo.
      * **[!UICONTROL Full AAM]**:: Especifique que la empresa tendrá una cuenta completa de Adobe Audience Manager y que los usuarios tendrán acceso de inicio de sesión.
      * **[!UICONTROL MMP]**:: Especifique que la empresa ha sido habilitada para usar las capacidades de Perfil de marketing maestro ([!UICONTROL MMP]).

         Si selecciona este tipo de cuenta, también **[!UICONTROL Visitor ID Service]** se selecciona automáticamente.
Para obtener más información, consulte [Servicios de audiencias - Perfil](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html)de marketing principal.
   * **[!UICONTROL Data Source]**:: Especifique que la empresa es un proveedor de datos de terceros dentro de Audience Manager.
   * **[!UICONTROL Targeting Partner]**:: Especifique que la empresa actúa como plataforma de segmentación para los clientes de Audience Manager.
   * **[!UICONTROL Visitor ID Service]**:: Especifique que la empresa se ha habilitado para usar el servicio de ID de visitante de Experience Cloud.

      El servicio de identificación de visitantes de Experience Cloud proporciona un ID de visitante universal en las soluciones de Experience Cloud. For more information, see the [Experience Cloud Visitor ID Service user guide](https://microsite.omniture.com/t2/help/en_US/mcvid/mcvid_service.html).

   * **[!UICONTROL Agency]**:: Especifique que la empresa tendrá una cuenta de agencia.
   * **[!UICONTROL Features]**: Seleccione las opciones que desee:
      * **[!UICONTROL Password Expiration]**:: Establece que todas las contraseñas de usuario de esta empresa caduquen pasados 90 días para aumentar la seguridad de Audience Manager.
      * **[!UICONTROL Reporting]**:: Habilita los informes de Audience Manager para esta empresa.
      * **[!UICONTROL Role Based Access Controls]**:: Habilite los controles de acceso basados en roles para esta empresa. Los controles de acceso basados en roles permiten crear grupos de usuarios con diferentes permisos de acceso. Los usuarios individuales dentro de estos grupos solo pueden acceder a funciones específicas en Audience Manager.


1. Haga clic en **[!UICONTROL Submit Updates]**.

## Eliminar un perfil de empresa {#delete-company-profile}

Utilice la página [!UICONTROL Companies] de la herramienta Audience Manager [!UICONTROL Admin] para eliminar una empresa existente.

<!-- t_delete_company.xml -->

>[!NOTE]
>
>Debe tener la [!UICONTROL DEXADMIN] función para eliminar las empresas existentes.

1. Para eliminar una empresa existente, haga clic en **[!UICONTROL Companies]**.

   ![Resultado del paso](assets/companies.png)

1. Haga clic ![](assets/icon_delete.png) en la **[!UICONTROL Actions]** columna de la empresa deseada.
1. Click **[!UICONTROL OK]** to confirm the deletion.
