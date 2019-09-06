---
source-git-commit: b76aa4a35a5216aabd60d07352a7c4bd2b3e6e32
translation-type: tm+mt

---
# Instrucciones

**Nota: Esta página (o cualquier página léame. md) no se publicará en la documentación de cliente**

## TDC

+ `TOC.md` en la raíz de la guía del usuario proporciona la organización de los temas contenidos en la guía para esta solución.
+ Cada guía del usuario tendrá su propio valor, `TOC.md`en el cual puede ordenar todas las páginas o temas según sea necesario.
+ La primera página de todas las guías del usuario es `overview.md`.

## Guía de usuario

+ Se llama a la introducción a la guía del usuario `overview.md`
+ Cada tema de la guía del usuario tiene su propio directorio diferente.
   + Si hay un tema en la guía denominada *Implementación*, el directorio correspondiente es `/implementation`
+ Todos los recursos de imagen se almacenan en `/assets` la raíz de la guía del usuario.
   + Todas las imágenes del `/assets` directorio se localizarán.
   + Las imágenes del `/no-localize` directorio no se localizarán (hay una sorpresa). Esto se puede utilizar para asegurar en versiones loc que los recursos específicos no se reproducen de forma innecesaria.

## Metadatos del nivel de guía del usuario

+ Metadatos que describen la guía del usuario se almacena en `TOC.md`la. Esto incluye:
   + product - nombre de producto/capacidad.
   + cloud - cloud a la que pertenece este producto.
   + audiencia: audiencia o arquetipo a la que se dirige la guía.
   + user-guide - nombre de la guía del usuario.

## Metadatos de nivel de página

+ Los metadatos requeridos para describir un documento se almacenan como parte de cada página individual. Esto incluye:
   + title: título de la página.
   + description: descripción de la página.
   + seo-title: título alternativo.
   + seo-description: título alternativo para SEO.
   + short-title - (campo opcional).
   + index (sí/no); la página de búsqueda de Adobe indexará la página.
   + translate - yes/no - will this page be localized.
   + versión que se utiliza principalmente para AEM y Campaign, para denotar la versión del producto.
   + private-feature-pack: se usa principalmente para AEM.
   + beta -¿este producto está en beta?
   + redirigir: se puede utilizar para crear una ref a una página nueva que sea necesaria.
   + doc-type: reference (predeterminado)/troubleshooting/developer/tutorial/kb/whitepaper.

## Más información

Para obtener más instrucciones de publicación, guías de estilo, muestras y otros recursos, visite la documentación [de colaboración](https://git.corp.adobe.com/AdobeDocs/collaborative-doc-instructions)
