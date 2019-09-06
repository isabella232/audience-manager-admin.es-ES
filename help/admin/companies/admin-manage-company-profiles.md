---
description: Utilice la página Empresas de la herramienta Administración de Audience Manager para crear una nueva empresa.
seo-description: Utilice la página Empresas de la herramienta Administración de Audience Manager para crear una nueva empresa.
seo-title: Crear un perfil de empresa
title: Crear un perfil de empresa
uuid: 55 de 18 f 8-883 d -43 fe-b 37 f-e 8805 bb 92 f 7 a
translation-type: tm+mt
source-git-commit: 71bf4cec222428686c1eab0998f66887db06da68

---


# Crear un perfil de empresa {#create-a-company-profile}

Utilice [!UICONTROL Companies] la página de la herramienta de administración de Audience Manager para crear una nueva empresa.

<!-- t_create_company.xml -->

>[!NOTE]
>
>Debe tener **[!UICONTROL DEXADMIN]** la función para crear nuevas empresas.

1. Click **[!UICONTROL Companies]** &gt; **[!UICONTROL Add Company]**.
1. Rellene los campos:

   * **[!UICONTROL Name]**: (Obligatorio) Especifique el nombre de la empresa.
   * **[!UICONTROL Description]**: (Requerido) Proporcione información descriptiva sobre la empresa, como la industria o su nombre completo.
   * **[!UICONTROL Subdomain]**: (Requerido) Especifique el subdominio de la empresa. El texto introducido es lo que se muestra como subdominio de la llamada de evento. Esto no se puede cambiar. Debe ser una cadena de [!DNL URL]caracteres válidos.

      Por ejemplo, si se nombra [!DNL AcmeCorp]a su empresa, el subdominio [!DNL acmecorp]será.

      Audience Manager utiliza el subdominio para el [!UICONTROL Data Collection Server]([!UICONTROL DCS]). En el ejemplo anterior, si la empresa [!DNL URL][!UICONTROL DCS] está llena [!DNL acmecorp.demdex.net].

   * **[!UICONTROL Lifecyle]**: Especifique el paso que desee para la empresa:
      * **[!UICONTROL Active]**: Especifique que la empresa será cliente activo de Audience Manager. Una [!UICONTROL Active] cuenta significa un cliente pago, no sólo para consultoría, sino para el SKU de Audience Manager.
      * **[!UICONTROL Demo]**: Especifique que la empresa será solo para propósitos de demostración. Se apilarán automáticamente los datos de informes.
      * **[!UICONTROL Prospect]**: Especifique que la empresa es un cliente potencial de Audience Manager, como por ejemplo una empresa gratuita [!DNL POC] o una configuración de cuenta para una demostración de ventas.
      * **[!UICONTROL Test]**: Especifique que la empresa será únicamente para fines de prueba interna.
   * **[!UICONTROL Account Types]**: Especifique el conjunto completo de tipos de cuenta para esta empresa. Ningún tipo de cuenta es mutuamente excluyente con ningún otro tipo.
      * **[!UICONTROL Full AAM]**: Especifique que la empresa tendrá una cuenta completa de Adobe Audience Manager y que los usuarios tengan acceso de inicio de sesión.
      * **[!UICONTROL MMP]**: Especifique que la empresa ha sido habilitada para utilizar las capacidades [!UICONTROL Master Marketing Profile] ([!UICONTROL MMP]). [!UICONTROL MMP] Permite compartir audiencias en Experience Cloud usando un [!UICONTROL Experience Cloud ID] ([!DNL MCID]) asignado a cada visitante y luego utilizado por Audience Manager. Si selecciona este tipo de cuenta, también [!UICONTROL Experience Cloud ID Service] se selecciona automáticamente.

         Para obtener más información, consulte [Audience Services - Master Marketing Profile](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html).
   * **[!UICONTROL Data Source]**: Especifique que la empresa es un proveedor de datos de terceros dentro de Audience Manager.
   * **[!UICONTROL Targeting Partner]**: Especifique que la empresa actúe como plataforma de segmentación para los clientes de Audience Manager.
   * **[!UICONTROL Visitor ID Service]**: Especifique que la empresa ha sido habilitada para utilizar [!UICONTROL Experience Cloud Visitor ID Service]la.

      [!UICONTROL Experience Cloud Visitor ID Service] La proporciona un ID de visitante universal en las soluciones de Experience Cloud. For more information, see the [Experience Cloud Visitor ID Service user guide](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-overview.html).

   * **[!UICONTROL Agency]**: Especifique que la empresa tendrá [!UICONTROL Agency] una cuenta.



1. Haga clic en **[!UICONTROL Create]**. Continúe con las instrucciones en [Editar un perfil de empresa](../companies/admin-manage-company-profiles.md#edit-company-profile).

   ![Resultado de paso](assets/add_company.png)

## Editar un perfil de empresa {#edit-company-profile}

Edite el perfil de una empresa, incluido su nombre, descripción, subdominio, ciclo de vida y más.

<!-- t_edit_company_profile.xml -->

1. Haga clic en **[!UICONTROL Companies]** y luego busque y haga clic en la empresa que desee para mostrar su [!UICONTROL Profile] página.

   Utilice [!UICONTROL Search] el cuadro o los controles de paginación en la parte inferior de la lista para encontrar la empresa que desee. Puede ordenar cada columna en orden ascendente o descendente haciendo clic en el encabezado de la columna que desee.

   ![Resultado de paso](assets/profile_company.png)

1. Edite los campos como sea necesario:

   * **[!UICONTROL Name]**: Edite el nombre de la empresa. Es un campo requerido.
   * **[!UICONTROL Description]**: Editar la descripción de la empresa. Es un campo requerido.
   * **[!UICONTROL Subdomain]**: (Requerido) Especifique el subdominio de la empresa. El texto introducido es lo que se muestra como subdominio de la llamada de evento. Esto no se puede cambiar. Debe ser una cadena de [!DNL URL]caracteres válidos.

      Por ejemplo, si se nombra [!DNL AcmeCorp]a su empresa, el subdominio [!DNL acmecorp]será.

      Audience Manager utiliza el subdominio para el [!UICONTROL Data Collection Server] ([!UICONTROL DCS]). En el ejemplo anterior, si la empresa [!DNL URL][!UICONTROL DCS] está llena [!DNL acmecorp.demdex.net].

   * **[!UICONTROL imsOrgld]**: ([!UICONTROL Identity Management System Organization ID]) Este ID permite conectar su empresa con Adobe Experience Cloud.
   * **[!UICONTROL Lifecyle]**: Especifique el paso que desee para la empresa:
      * **[!UICONTROL Active]**: Especifique que la empresa será cliente activo de Audience Manager. Una cuenta activa significa un cliente pago, no sólo para asesoría, sino para SKU de Audience Manager.
      * **[!UICONTROL Demo]**: Especifique que la empresa será solo para propósitos de demostración. Se apilarán automáticamente los datos de informes.
      * **[!UICONTROL Prospect]**: Especifique que la empresa es un cliente potencial de Audience Manager, como por ejemplo una empresa gratuita [!DNL POC] o una configuración de cuenta para una demostración de ventas.
      * **[!UICONTROL Test]**: Especifique que la empresa será únicamente para fines de prueba interna.
   * **[!UICONTROL Account Types]**: Especifique el conjunto completo de tipos de cuenta para esta empresa. Ningún tipo de cuenta es mutuamente excluyente con ningún otro tipo.
      * **[!UICONTROL Full AAM]**: Especifique que la empresa tendrá una cuenta completa de Adobe Audience Manager y que los usuarios tengan acceso de inicio de sesión.
      * **[!UICONTROL MMP]**: Especifique que la empresa ha sido habilitada para utilizar las capacidades Master Marketing Profile ([!UICONTROL MMP]).

         Si selecciona este tipo de cuenta, **[!UICONTROL Visitor ID Service]** también se selecciona automáticamente.
Para obtener más información, consulte [Audience Services - Master Marketing Profile](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html).
   * **[!UICONTROL Data Source]**: Especifique que la empresa es un proveedor de datos de terceros dentro de Audience Manager.
   * **[!UICONTROL Targeting Partner]**: Especifique que la empresa actúe como plataforma de segmentación para los clientes de Audience Manager.
   * **[!UICONTROL Visitor ID Service]**: Especifique que la empresa ha sido habilitada para utilizar el servicio de ID de visitante de Experience Cloud.

      El servicio de identificación de visitantes de Experience Cloud proporciona un ID de visitante universal en las soluciones de Experience Cloud. For more information, see the [Experience Cloud Visitor ID Service user guide](https://microsite.omniture.com/t2/help/en_US/mcvid/mcvid_service.html).

   * **[!UICONTROL Agency]**: Especifique que la empresa tendrá una cuenta de agencia.
   * **[!UICONTROL Features]**: Seleccione las opciones que desee:
      * **[!UICONTROL Password Expiration]**: Configura todas las contraseñas de usuario dentro de esta empresa para que caduquen después de 90 días para aumentar la seguridad de Audience Manager.
      * **[!UICONTROL Reporting]**: Habilita los informes de Audience Manager para esta empresa.
      * **[!UICONTROL Role Based Access Controls]**: Habilite los controles de acceso basados en roles para esta empresa. Los controles de acceso basados en roles permiten crear grupos de usuarios con diferentes permisos de acceso. Los usuarios individuales dentro de estos grupos pueden acceder a solo funciones específicas de Audience Manager.


1. Haga clic en **[!UICONTROL Submit Updates]**.

## Eliminar un perfil de empresa {#delete-company-profile}

Utilice [!UICONTROL Companies] la página de la herramienta Audience Manager [!UICONTROL Admin] para eliminar una empresa existente.

<!-- t_delete_company.xml -->

>[!NOTE]
>
>Debe tener [!UICONTROL DEXADMIN] la función para eliminar las empresas existentes.

1. Para eliminar una empresa existente, haga clic **[!UICONTROL Companies]** en.

   ![Resultado de paso](assets/companies.png)

1. Haga clic en ![](assets/icon_delete.png) la **[!UICONTROL Actions]** columna de la empresa que desee.
1. Click **[!UICONTROL OK]** to confirm the deletion.
