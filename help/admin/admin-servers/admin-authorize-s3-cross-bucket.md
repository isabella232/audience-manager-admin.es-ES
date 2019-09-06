---
description: Es posible que algunos clientes no deseen proporcionar a Adobe su acceso de Amazon Simple Storage Service (Amazon S 3) o claves secretas para autorizar la carga de datos de destino en sus bloques.
seo-description: Es posible que algunos clientes no deseen proporcionar a Adobe su acceso de Amazon Simple Storage Service (Amazon S 3) o claves secretas para autorizar la carga de datos de destino en sus bloques.
seo-title: Cómo autorizar acceso de contenedor de Amazon S 3 para destinos por lotes
title: Cómo autorizar acceso de contenedor de Amazon S 3 para destinos por lotes
uuid: da 2 bcbda-a 765-437 a-bfe 9-4355383 a 4730
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# Cómo autorizar acceso de contenedor de Amazon S 3 para destinos por lotes{#authorize-cross-account-bucket-batch}

Es posible que algunos clientes no deseen proporcionar a Adobe su [!DNL Amazon S3] acceso o claves secretas para autorizar la carga de datos de destino a sus bloques.

Una alternativa que podemos ofrecer [!UICONTROL Cross-Account Bucket Permissions] a los clientes [!DNL Amazon S3]. Este proceso se describe en la documentación [de AWS](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html). Para habilitar esta alternativa en Audience Manager, siga los pasos a continuación:

1. Vaya a **[!UICONTROL Servers]** y seleccione **[!UICONTROL Create Server]**.
1. Seleccione **[!UICONTROL S3]** en la **[!UICONTROL Protocol/Credentials]** máscara desplegable.
1. Marque **[!UICONTROL Use Internal Adobe Key]** la opción.
1. Utilice la cuenta del cliente y el nombre del bucket en [!DNL Amazon S3].
1. Asegúrese de que el cliente en blanco enumere [!DNL Amazon S3] la cuenta `975822914085` en su [!DNL S3] bloque.

>[!NOTE]
>
>Nuestro editor saliente garantiza que el nivel de permiso `bucket-owner-full-control` se establezca en los datos cargados para que el cliente pueda ser propietario de esos datos.
