---
description: Lista las macros que puede utilizar para crear archivos de datos basados en FTP. Algunas macros se pueden utilizar para todos los campos y filas de archivos de datos. Otras macros son específicas de las filas de datos y encabezados.
seo-description: Lista las macros que puede utilizar para crear archivos de datos basados en FTP. Algunas macros se pueden utilizar para todos los campos y filas de archivos de datos. Otras macros son específicas de las filas de datos y encabezados.
seo-title: Macros de formato de archivo
title: Macros de formato de archivo
uuid: f91c91b6-6581-4ed7-8d7f-f8532bd41df9
translation-type: tm+mt
source-git-commit: 0ee7aa9c13f1b9b8fd64dddff4e52d101055e77c
workflow-type: tm+mt
source-wordcount: '717'
ht-degree: 2%

---


# Macros de formato de archivo {#file-format-macros}

Lista las macros que puede utilizar para crear archivos [!DNL FTP]de datos basados en. Algunas macros se pueden utilizar para todos los campos y filas de archivos de datos. Otras macros son específicas de las filas de datos y encabezados.

## Macros comunes {#common-macros}

Estas macros se pueden utilizar en cualquier campo de formato. Por ejemplo, consulte Ejemplos [de macros de formato](../formats/file-format-examples.md)de archivo.

<table id="table_A3309E175ABF4651BD11CE3632B3C553"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Macro </th> 
   <th colname="col2" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>ASCII_SOH</code> </p> </td> 
   <td colname="col2"> <p>Carácter ASCII no imprimible. Indica el inicio de una fila o una sección de contenido. También se puede utilizar para separar columnas de datos en un archivo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPID</code> </p> </td> 
   <td colname="col2"> <p>ID del proveedor de datos de destinatario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MASTER_DPID</code> </p> </td> 
   <td colname="col2"> <p>ID de usuario ID del proveedor de datos clave. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ID</code> </p> </td> 
   <td colname="col2"> <p>ID de pedido/destino. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PIDALIAS</code> </p> </td> 
   <td colname="col2"> <p>Un alias para un ID de pedido/destino. </p> <p>El valor de este alias se establece en el campo ID de la cuenta <span class="wintitle"> externa </span> para un destino (en la sección Configuración <span class="wintitle"> básica </span> ). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_MODE</code> </p> </td> 
   <td colname="col2"> <p>Indica el tipo de sincronización. Acepta las siguientes variables opcionales: </p> 
    <ul id="ul_87E8E3CE6565447A9810B5119298CC7B"> 
     <li id="li_66F4889FB84E40AC92F69F3FF6B0042C"> <code>full</code>:: Sincronización completa. </li> 
     <li id="li_BFE2C2D9A33A44FB9A840A7232ECCFFF"> <code>iter</code>:: Sincronización incremental. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_TYPE</code> </p> </td> 
   <td colname="col2"> <p>Indica el método de transferencia de datos. Acepta las siguientes variables opcionales: </p> 
    <ul id="ul_13BE35BBBF7C4C67AEFC514C5D192902"> 
     <li id="li_195FE9B4C5494600BD17D7172A8FB630"> <code>ftp</code> </li> 
     <li id="li_751AD59C4C934D66BC530D9806B500AF"> <code>http</code> </li> 
     <li id="li_4638AF7D1FB54E2C890045048B85309C"> <code>s3</code> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TIMESTAMP</code> </p> </td> 
   <td colname="col2"> <p>Marca de tiempo UTC, Unix de 10 dígitos. </p> <p>También se le puede dar formato <code>YYYYMMDDhhmmss</code> siguiendo las reglas de formato de fecha y marca de hora de Java. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Macros de campo de encabezado {#header-field-macros}

Macros utilizadas solo en campos de encabezado. Por ejemplo, consulte Ejemplos [de macros de formato](../formats/file-format-examples.md)de archivo.

<table id="table_1A8BD1750F4940B3A34E3F80371A447A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Macro </th> 
   <th colname="col2" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>Utilizada como separador, esta macro inserta una ficha entre campos. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Macros de fila de datos {#data-row-macros}

Macros utilizados sólo en filas de datos. Por ejemplo, consulte Ejemplos [de macros de formato](../formats/file-format-examples.md)de archivo.

<table id="table_E378F94A3907407AA8110C8EE6C10909"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Macro </th> 
   <th colname="col2" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>CLOSE_CURLY_BRACKET</code> </p> </td> 
   <td colname="col2"> <p>Inserta un carácter de corchete <code>}</code> redondeado cerrado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>COMMA</code> </p> </td> 
   <td colname="col2"> <p>Inserta una coma. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="term"> Identificador de usuario único de socio de datos </span>. Devuelve el ID que ha asignado a un visitante de usuario/sitio si dicho ID ya se ha sincronizado con un ID de dispositivo <span class="keyword"> Audience Manager </span> . </p> <p>Si el DPID es 0, esta macro devolverá el ID de <span class="keyword"> Audience Manager </span> en lugar del ID del usuario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID_LIST</code> </p> </td> 
   <td colname="col2"> <p>Devuelve una lista que contiene varios ID para un socio de datos. Esto resulta útil si tiene una organización grande con varias subdivisiones u otros grupos organizativos con los que puede compartir datos. Esta macro devuelve una lista de los ID para esos grupos subordinados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPUUIDS</code> </p> </td> 
   <td colname="col2"> <p>El resultado de esta macro asigna el ID del proveedor de datos (DPID) a los ID de usuario único relacionados (DPUUID). Esta macro debe tener una cadena de formato para controlar su salida. El resultado de muestra sería similar al siguiente: </p> <p> <code>"dpids=dpid1,dpid2,...dpid n|maxMappings= n|format=json"</code> </p> <p>La <code>maxMappings</code> configuración determina cuántas asignaciones desea que devuelva la macro. Cuando <code>maxMappings=0</code>, esta macro devuelve todas las asignaciones para cada DPID especificado. Los datos se ordenan por marca de tiempo (la más reciente primero) y devuelven los resultados con la marca de tiempo más grande primero. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>endif</code> </p> </td> 
   <td colname="col2"> <p>Necesario cuando se utilizan las variables condicional <code>if</code> y <code>SEGMENT_LIST</code> y <code>REMOVED_SEGMENT_LIST</code> macros. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>if(SEGMENT_LIST &amp;&amp; REMOVED_SEGMENT_LIST)endif</code> </p> </td> 
   <td colname="col2"> <p>Esta combinación de macros crea una afirmación condicional que lista a los segmentos a los que pertenecen los usuarios <i>y de los</i> que se han eliminado. Devuelve una cadena vacía si no se cumplen ambas condiciones o no hay datos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MCID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Adobe Experience Cloud ID.</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPEN_CURLY_BRACKET</code> </p> </td> 
   <td colname="col2"> <p>Inserta un carácter de corchete <code>{</code> redondeado abierto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPT_OUT</code> </p> </td> 
   <td colname="col2"> <p>Obsoleta. No usar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ATTRIBUTE_TYPE</code> </p> </td> 
   <td colname="col2"> <p>Obsoleta. No usar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ATTRIBUTE_VALUE</code> </p> </td> 
   <td colname="col2"> <p>Devuelve <code>1</code> como un valor estático codificado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PID</code> </p> </td> 
   <td colname="col2"> <p>ID del socio (PID). El PID aparece en la ficha <span class="wintitle"> Perfil </span> de la interfaz de usuario de administración. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p>Devuelve una lista de segmentos, si los hay, que se han eliminado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p>Devuelve una lista de segmentos en una lista. Acepta las siguientes variables opcionales: </p> 
    <ul id="ul_B111AA0D6C18445598A1444B8B7E9325"> 
     <li id="li_8603B40229624856AF1FBC434DB8F16A"> <code>segmentId</code>:: ID heredado. Obsoleta. Utilice <code>sid</code> (solo en minúsculas). </li> 
     <li id="li_1EF40DDCA3C5447586904CF021D8F912"> <code>csegid</code>:: ID heredado. Obsoleta. Utilice <code>sid</code> (solo en minúsculas). </li> 
     <li id="li_D85F0A5D16AE4DAFB55C17DBB35EA66E"> <code>sid</code>:: ID del segmento. </li> 
     <li id="li_9BE103EFD8384464B46FAC00422431DB"> <code>type</code>:: Devuelve <code>5</code>, un valor estático y codificado que identifica los datos como datos de segmentos. </li> 
     <li id="li_FE5049089F2944FA9DB9F9D546DBA167"> <code>alias</code>:: Asignación del segmento. Obsoleta. Utilice <code>sid</code> (solo en minúsculas). </li> 
     <li id="li_DD778AA2D1DB4D409CF5026B5D9DBD27"> <code>lastUpdateTime</code>:: Marca de hora Unix que indica la última vez que se realizó un segmento. </li> 
    </ul> <p>Coloque estas variables entre llaves después de la macro. Por ejemplo, este código separa los resultados con un carácter de barra vertical "|": <code>&lt;SEGMENT_LIST:{seg|&lt;seg.type&gt;,&lt;seg.sid&gt;}; separator="|"&gt;</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SET_ATTRIBUTES</code> </p> </td> 
   <td colname="col2"> <p>Devuelve <code>1</code> como un valor estático codificado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>Inserta un separador de tabulación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TRAIT_LIST</code> </p> </td> 
   <td colname="col2"> <p>Devuelve una lista de características. Acepta los siguientes argumentos opcionales: </p> 
    <ul id="ul_757DEB56E4F849768468F3C166B0D171"> 
     <li id="li_859E1F4F21D645519F150DC512B3EB1A"> <code>type</code>:: Tipos de características identificados por un ID numérico. Esta variable devuelve: 
      <ul id="ul_C9839266783D42CCADAAC3FEA33BE4D7"> 
       <li id="li_6996A218E3F04EC3BC70032559DD87FC"> <code>10</code> que identifica un rasgo DPM (sin conexión, incorporado por un trabajo entrante). </li> 
       <li id="li_831FF929BF50434C8804C13E5786DF79"> <code>3</code> que identifica una característica basada en reglas (en tiempo real, incorporado a través del <span class="wintitle"> DCS </span>). </li> 
      </ul> </li> 
     <li id="li_E84D6BC80AEE4F10963C9882C4151ED4"> <code>traitId</code>:: ID de característica. </li> 
     <li id="li_D30A849BA35248E6B9110FA3ADEFC332"> <code>lastRealized</code>:: Última vez que se realizó la característica. Marca de hora Unix. </li> 
    </ul> <p>Coloque estas variables entre llaves después de la macro. Por ejemplo, este código separa los resultados con un carácter de barra vertical "|": <code>TRAIT_LIST{type|traitId};separator="|"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> ID </span> de usuario de Audience Manager. </p> </td> 
  </tr> 
 </tbody> 
</table>