---
description: Enumera las macros que puede utilizar para crear archivos de datos basados en FTP. Algunas macros se pueden utilizar para todos los campos y filas de archivos de datos. Otras macros son específicas sólo para encabezados y filas de datos.
seo-description: Enumera las macros que puede utilizar para crear archivos de datos basados en FTP. Algunas macros se pueden utilizar para todos los campos y filas de archivos de datos. Otras macros son específicas sólo para encabezados y filas de datos.
seo-title: Macros de formato de archivo
title: Macros de formato de archivo
uuid: f 91 c 91 b 6-6581-4 ed 7-8 d 7 f-f 8532 bd 41 df 9
translation-type: tm+mt
source-git-commit: e1122a7f3d3e8c2d67616eb56cb186a4750ed29b

---


# Macros de formato de archivo {#file-format-macros}

Enumera las macros que puede utilizar para crear archivos de datos [!DNL FTP]basados en certificados. Algunas macros se pueden utilizar para todos los campos y filas de archivos de datos. Otras macros son específicas sólo para encabezados y filas de datos.

## Macros comunes {#common-macros}

Estas macros se pueden utilizar en cualquier campo de formato. Por ejemplo, consulte [Formato de archivo Ejemplos de macro](../formats/file-format-examples.md).

<table id="table_A3309E175ABF4651BD11CE3632B3C553"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Macro </th> 
   <th colname="col2" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>ASCII_ SOH</code> </p> </td> 
   <td colname="col2"> <p>Carácter ASCII no imprimible. Indica el inicio de una fila o una sección de contenido. También se puede utilizar para separar las columnas de datos en un archivo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPID</code> </p> </td> 
   <td colname="col2"> <p>ID del proveedor de datos de Target. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MASTER_ DPID</code> </p> </td> 
   <td colname="col2"> <p>ID del proveedor de datos clave de ID de usuario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ ID</code> </p> </td> 
   <td colname="col2"> <p>ID de pedido/destino. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PIDALIAS</code> </p> </td> 
   <td colname="col2"> <p>Alias para un ID de pedido/destino. </p> <p>El valor de este alias se establece en <span class="wintitle"> el campo ID </span> de cuenta externa de un destino (en la sección Ajustes <span class="wintitle"></span> básicos). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_ MODE</code> </p> </td> 
   <td colname="col2"> <p>Indica el tipo de sincronización. Acepta las siguientes variables opcionales: </p> 
    <ul id="ul_87E8E3CE6565447A9810B5119298CC7B"> 
     <li id="li_66F4889FB84E40AC92F69F3FF6B0042C"> <code>full</code>: Sincronización completa. </li> 
     <li id="li_BFE2C2D9A33A44FB9A840A7232ECCFFF"> <code>iter</code>: Incrementa la sincronización. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_ TYPE</code> </p> </td> 
   <td colname="col2"> <p>Indica el método de transferencia de datos. Acepta las siguientes variables opcionales: </p> 
    <ul id="ul_13BE35BBBF7C4C67AEFC514C5D192902"> 
     <li id="li_195FE9B4C5494600BD17D7172A8FB630"> <code>ftp</code> </li> 
     <li id="li_751AD59C4C934D66BC530D9806B500AF"> <code>http</code> </li> 
     <li id="li_4638AF7D1FB54E2C890045048B85309C"> <code>s3</code> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TIMESTAMP</code> </p> </td> 
   <td colname="col2"> <p>Marca de tiempo de 10 dígitos, UTC y Unix. </p> <p>También se puede formatear como <code>aaaammddhhmmss</code> siguiendo las reglas de formato de fecha y hora de Java. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Macros de campo de encabezado {#header-field-macros}

Macros utilizadas únicamente en los campos del encabezado. Por ejemplo, consulte [Formato de archivo Ejemplos de macro](../formats/file-format-examples.md).

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
   <td colname="col2"> <p>Esta macro, utilizada como separador, inserta una ficha entre campos. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Macros de fila de datos {#data-row-macros}

Macros utilizadas únicamente en filas de datos. Por ejemplo, consulte [Formato de archivo Ejemplos de macro](../formats/file-format-examples.md).

<table id="table_E378F94A3907407AA8110C8EE6C10909"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Macro </th> 
   <th colname="col2" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>CLOSE_ CURLY_ BRACKET</code> </p> </td> 
   <td colname="col2"> <p>Inserta un carácter de llave cerrada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>COMA</code> </p> </td> 
   <td colname="col2"> <p>Inserta una coma. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_ UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="term"> Identificador de usuario único de socio de datos </span>. Devuelve el ID que ha asignado a un visitante de usuario o sitio si dicho ID ya se ha sincronizado con un <span class="keyword"> ID </span> de dispositivo de Audience Manager. </p> <p>Si el DPID es 0, esta macro devolverá el ID <span class="keyword"> de Audience Manager </span> en lugar del ID para el usuario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_ UUID_ LIST</code> </p> </td> 
   <td colname="col2"> <p>Devuelve una lista que contiene varios ID para un socio de datos. Esto resulta útil si tiene una gran organización con varias subdivisiones u otros grupos organizativos con los que puede compartir datos. Esta macro devuelve una lista de los ID de esos grupos subordinados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPUUIDS</code> </p> </td> 
   <td colname="col2"> <p>El resultado de esta macro asigna el ID de proveedor de datos (DPID) a ID de usuarios únicos relacionados (DPUUID). Esta macro debe tener una cadena de formato para controlar su salida. El resultado de la muestra tendría un aspecto similar al siguiente: </p> <p> <code>" dpids = dpid 1, dpid 2,… dpid n | maxmappings = n | format = json "</code> </p> <p>La configuración <code>maxmappings</code> determina cuántas asignaciones desea que devuelvan la macro. Cuando <code>maxmappings = 0</code>, esta macro devuelve todas las asignaciones de cada DPID especificado. Los datos se ordenan por marca de tiempo (primero más reciente) y devuelven primero los resultados con la marca de fecha y hora más grande. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>endif</code> </p> </td> 
   <td colname="col2"> <p>Necesario al utilizar las macros condicional <code>if</code> y <code>SEGMENT_ LIST</code> y <code>REMOVED_ SEGMENT_ LIST</code> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>if (SEGMENT_ LIST &amp; &amp; REMOVED_ SEGMENT_ LIST) endif</code> </p> </td> 
   <td colname="col2"> <p>Esta combinación de macros crea una afirmación condicional que enumera los segmentos a los que pertenecen los usuarios <i>y</i> que se han eliminado de. Devuelve una cadena vacía si no se cumplen ambas condiciones o si no hay datos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MCID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Adobe Experience Cloud </span> ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPEN_ CURLY_ BRACKET</code> </p> </td> 
   <td colname="col2"> <p>Inserta un corchete abierto {carácter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPT_ OUT</code> </p> </td> 
   <td colname="col2"> <p>Obsoleta. No utilice. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ ATTRIBUTE_ TYPE</code> </p> </td> 
   <td colname="col2"> <p>Obsoleta. No utilice. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ ATTRIBUTE_ VALUE</code> </p> </td> 
   <td colname="col2"> <p>Devuelve <code>1</code> como valor estático y estático. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PID</code> </p> </td> 
   <td colname="col2"> <p>ID del socio (PID). El PID aparece en la ficha <span class="wintitle"> Perfil </span> de la interfaz de usuario de administración. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_ SEGMENT_ LIST</code> </p> </td> 
   <td colname="col2"> <p>Devuelve una lista de segmentos que se han eliminado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENT_ LIST</code> </p> </td> 
   <td colname="col2"> <p>Devuelve una lista de segmentos en una lista. Acepta las siguientes variables opcionales: </p> 
    <ul id="ul_B111AA0D6C18445598A1444B8B7E9325"> 
     <li id="li_8603B40229624856AF1FBC434DB8F16A"> <code>Segmentid</code>: ID heredado. Obsoleta. Utilice <code>sid</code> (solo en minúscula). </li> 
     <li id="li_1EF40DDCA3C5447586904CF021D8F912"> <code>csegid</code>: ID heredado. Obsoleta. Utilice <code>sid</code> (solo en minúscula). </li> 
     <li id="li_D85F0A5D16AE4DAFB55C17DBB35EA66E"> <code>sid</code>: ID de segmento. </li> 
     <li id="li_9BE103EFD8384464B46FAC00422431DB"> <code>type</code>: Devuelve <code>5</code>, un valor estático y estático que identifica los datos como datos de segmento. </li> 
     <li id="li_FE5049089F2944FA9DB9F9D546DBA167"> <code>alias</code>: Asignación del segmento. Obsoleta. Utilice <code>sid</code> (solo en minúscula). </li> 
     <li id="li_DD778AA2D1DB4D409CF5026B5D9DBD27"> <code>Lastupdatetime</code>: Marca de hora Unix que indica la última vez que se ha realizado un segmento. </li> 
    </ul> <p>Coloque estas variables entre llaves después de la macro. Por ejemplo, este código separa los resultados con una barra vertical "|" character: <code>&lt; SEGMENT_ LIST: {seg|&lt; seg. type &gt;, &lt; seg. sid &gt;}; separator = "|" &gt;</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SET_ ATTRIBUTES</code> </p> </td> 
   <td colname="col2"> <p>Devuelve <code>1</code> como valor estático y estático. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>Inserta un separador de tabuladores. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TRAIT_ LIST</code> </p> </td> 
   <td colname="col2"> <p>Devuelve una lista de características. Acepta los siguientes argumentos opcionales: </p> 
    <ul id="ul_757DEB56E4F849768468F3C166B0D171"> 
     <li id="li_859E1F4F21D645519F150DC512B3EB1A"> <code>type</code>: Tipos de características identificados por un ID numérico. Esta variable devuelve: 
      <ul id="ul_C9839266783D42CCADAAC3FEA33BE4D7"> 
       <li id="li_6996A218E3F04EC3BC70032559DD87FC"> <code>10</code> que identifica un rasgo DPM (sin conexión, onquecado por un trabajo entrante). </li> 
       <li id="li_831FF929BF50434C8804C13E5786DF79"> <code>3</code> , que identifica un rasgo basado en reglas (en tiempo real; onbogged a través del <span class="wintitle"> DCS </span>). </li> 
      </ul> </li> 
     <li id="li_E84D6BC80AEE4F10963C9882C4151ED4"> <code>Traitid</code>: ID de característica. </li> 
     <li id="li_D30A849BA35248E6B9110FA3ADEFC332"> <code>Lastended</code>: La última vez que se realizó la característica. Marca de tiempo Unix. </li> 
    </ul> <p>Coloque estas variables entre llaves después de la macro. Por ejemplo, este código separa los resultados con una barra vertical "|" character: <code>TRAIT_ LIST {type | traitid}; separator = "|"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> ID </span> de usuario de Audience Manager. </p> </td> 
  </tr> 
 </tbody> 
</table>