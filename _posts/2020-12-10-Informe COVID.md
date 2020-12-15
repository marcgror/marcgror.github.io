# Indice

- [Indice](#indice)
- [Análisis de los datos del COVID-19 en España[WIP]](#análisis-de-los-datos-del-covid-19-en-españawip)
  - [Importante](#importante)
- [España](#españa)
  - [Métodos de diagnóstico del COVID-19](#métodos-de-diagnóstico-del-covid-19)
  - [Evolución de los contagios](#evolución-de-los-contagios)
  - [Hospitalizados e ingresados en UCI](#hospitalizados-e-ingresados-en-uci)
    - [Incidéncia acumulada](#incidéncia-acumulada)
  - [Fallecidos](#fallecidos)
  - [Mapa de incidencia](#mapa-de-incidencia)
- [CCAA](#ccaa)
  - [Métodos de diagnóstico del COVID-19](#métodos-de-diagnóstico-del-covid-19-1)
  - [Evolución de los contagios y fallecidos](#evolución-de-los-contagios-y-fallecidos)
    - [Evolución de la incidéncia acumulada](#evolución-de-la-incidéncia-acumulada)
  - [Evolución de los hospitalizados e ingresados en UCI](#evolución-de-los-hospitalizados-e-ingresados-en-uci)

# Análisis de los datos del COVID-19 en España[WIP]
2020 será siempre recordado como el año de la pandemia de COVID-19. España ha sido y es uno de los países más afectados, tanto en la primera ola en marzo como en la siguiente en septiembre.

Para analizar la situación, a nivel nacional, autonómico y provincial, se usarán los datos proporcionados por el Ministerio de Sanidad. En el siguiente repositorio de Github se detalla la obtención, manipulación y utilización de estos datos para su posterior análisis:
https://github.com/marcgror/COVID-19-Data-Analysis

**Todas las figuras son interactivas.**

## Importante
Como bien se explica en el repo anterior, los datos que proporciona el Ministerio de Sanidad por medio de archivos CSV o Excel no están completos hasta el último día. Esto quiere decir que se van completando con el paso del tiempo. Por lo tanto, es muy probable que en las tablas y representaciones gráficas que se mostrarán a continuación aparezcan valores muy bajos o incluso 0 en el número de casos o fallecidos de los días más recientes. Este error en la muestra, por tanto, también se transmitirá a otras estadísticas calculadas, como medias o Incidéncias Acumuladas.

Con esto se quiere indicar que los datos que aquí se muestran no son fiables al 100%, y que lo importante serán las tendéncias.

# España

Antes de analizar en detalle la situación de las Comunidades Autónomas, es importante conocer el panorama a nivel nacional.
## Métodos de diagnóstico del COVID-19
En España, el COVID se está detectando principalmente usando las pruebas de PCR y test de anticuerpos, a parte de otras pruebas como el test de antígenos.

La prueba PCR (Polimerasa Chain Reaction) es una prueba de diagnóstico utilizada para detectar fragmentos del material genético de un patógeno. En este caso en concreto, el patógeno se corresponde con el virus SARS-CoV-2. La idea es sencilla: se toma una muestra respiratoria de la persona sospechosa de infección, y se analiza en un laboratorio de microbiología con un PCR en busca de una molécula de ARN del virus. El positivo vendría cuando la prueba detecta ese ARN del virus, mientras será negativo en caso contrario.

Por su parte, los test de anticuerpos detectan la presencia de estos en el organismo, generados como respuesta a la presencia del virus.

Actualmente se dispone tanto de datos de contagiados diagnosticados con PCR como de diagnosticados con otros tipos de prueba, como puede ser el test de anticuerpos o de antígenos.

El siguiente gráfico muestra la contribución en porcentaje de cada tipo de prueba: 
<iframe id="igraph" scrolling="yes" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/718.embed" height="525" width="100%"></iframe>

Casi un 90 % de las detecciones de contagiados son gracias a pruebas PCR, mientras que otras pruebas como podrían ser los test de antígenos alcanzan casi un 10 % de cuota. Los test de anticuerpo y las pruebas desconocidas obtienen muy poca representación.

## Evolución de los contagios
En la siguiente tabla se muestran los casos diarios, acumulados, el incremento diario, en los últimos 7 y 14 días, la media de casos en los últimos 7 y 14 días, la incidéncia acumulada en los últimos 7 y 14 días y la acumulada para los últimos 10 días a nivel nacional:
<iframe id="igraph" scrolling="yes" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/720.embed" height="525" width="100%"></iframe>

La curva de contagiados en España desde el inicio de la pandémia se muestra a continuación:
<iframe id="igraph" scrolling="yes" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/722.embed" height="525" width="100%"></iframe>
Las dos olas se pueden diferenciar claramente. Los efectos del confinamiento, desescalada y fin del Estado de Alarma son también evidentes, ya que el número de contagios diarios decae a mínimos practicamente hasta principios de julio, fruto del parón social y laboral del país. Es entonces cuando empiezan a aumentar los nuevos positivos, seguramente porque la "Nueva Normalidad" lleva vigente 1-2 semanas en toda España, y por lo tanto la población empieza poco a poco a interactuar de nuevo. El hecho de que esta vuelta a la socialización y al trabajo se diera en verano seguramente no ayuda tampoco. A partir de septiembre, los casos positivos empiezan a subir descaradamente, siendo octubre y noviembre los meses donde se vuelve a alcanzar máximos. La declaración del Segundo Estado de Alarma en la pandémia, con las medidas de restricción que conlleva, consigue que los nuevos contagios empiecen a decaer.

Si nos fijamos en los positivos acumulados, las tendencias son prácticamente las mismas, como es lógico:
<iframe id="igraph" scrolling="yes" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/724.embed" height="525" width="100%"></iframe>

## Hospitalizados e ingresados en UCI
Otros indicadores útiles para valorar el estado actual de la pandemia a nivel de presión hospitalária son el número de positivos hospitalizados e ingresados en la UCI. Como se puede observar, en el peor momento de la primera ola (finales de marzo-mayo) es cuando se produjo el mayor número de personas hospitalizadas o en la UCI. Durante el inicio del verano los ingresados disminuyen, fruto del descenso de los contagios debido al confinamiento y la desescalada. Una vez llega Agosto, se empiezan a notar los efectos de la "nueva normalidad", y los hospitalizados e ingresados en UCI por COVID empiezan a aumentar de nuevo.
<iframe id="igraph" scrolling="yes" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/736.embed" height="525" width="100%"></iframe>
<iframe id="igraph" scrolling="yes" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/738.embed" height="525" width="100%"></iframe>

### Incidéncia acumulada
La incidéncia acumulada (IA) es una forma de medir el impacto de la pandémia en cada territorio teniendo en cuenta su población. Por lo tanto, permite comparar valores entre distintas regiones/paises y establecer valores máximos que, una vez superados, exijan aplicar medidas de restricción de movilidad.

La evolución de la IA en 7 y 14 días durante toda la pandémia se muestra a continuación:
<iframe id="igraph" scrolling="yes" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/726.embed" height="525" width="100%"></iframe>
Se observa una tendéncia similar a la curva de contágios. Durante los meses de septiembre, octubre y sobretodo noviembre, se alcanzaron valores exageradamente altos.

## Fallecidos
Una vez analizada la evolución de los contagios a nivel nacional, es el turno del número de fallecidos. En la siguiente tabla se muestran los fallecidos diarios, el acumulado desde el inicio de la pandémia, el incremento respecto al día anterior, el total en la última semana, los últimos 14 días, la media de fallecidos en los últimos 3 y 7 días, por 100000 habitantes y por 1M de habitantes en la última semana:
<iframe id="igraph" scrolling="yes" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/728.embed" height="525" width="100%"></iframe>
A continuación se muestra la evolución del número de fallecidos diario diagnosticados con COVID desde el inicio de la pandémia:
<iframe id="igraph" scrolling="yes" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/730.embed" height="525" width="100%"></iframe>
En cuanto al recuento semanal, se distribuye de la siguiente manera:
<iframe id="igraph" scrolling="yes" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/732.embed" height="525" width="100%"></iframe>

Durante la primera ola, se alcanzaron cifras diarias de más de 1000 muertos diarios positivos por COVID. Gracias al confinamiento, estas cifras fueron dismuyendo lentamente durante mayo y junio, llegando a su mínimo durante el verano. Una vez los contagios e infectados vuelven a incrementarse a finales de agosto, los fallecidos empiezan a aumentar también.
<iframe id="igraph" scrolling="yes" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/734.embed" height="525" width="100%"></iframe>
En el acumulado, se puede observar un estancamiento en el número de fallecidos durante el verano, pero a partir de los últimos días de agosto se observa de nuevo una tendencia al aumento.

## Mapa de incidencia
El siguiente mapa muestra la IA de dos semanas en cada Comunidad Autónoma. Esta información se acompaña del recuento de casos y fallecidos en los últimos 7 días y desde el inicio de la pandémia.
<iframe title="IA en dos semanas" aria-label="Mapa" id="datawrapper-chart-CPbTd" src="https://datawrapper.dwcdn.net/CPbTd/4/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="468"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"])for(var e in a.data["datawrapper-height"]){var t=document.getElementById("datawrapper-chart-"+e)||document.querySelector("iframe[src*='"+e+"']");t&&(t.style.height=a.data["datawrapper-height"][e]+"px")}}))}();
</script>

# CCAA
El impacto del COVID ha sido diferente según la zona en la que nos fijemos: grandes ciudades, zonas rurales, Comunidades Autónomas muy diferentes en cuanto a movilidad... Los datos de cada una de ellas pueden arrojar información importante sobre la transmisión del virus durante estos meses.
## Métodos de diagnóstico del COVID-19
Una de las críticas más habituales al modelo de gestión de la pandémia autonómico ha sido la diferencia de criterios. En el siguiente gráfico se muestra la distribución de pruebas de detección para cada Comunidad Autónoma:
<iframe id="igraph" scrolling="yes" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/740.embed" height="525" width="100%"></iframe>
El dominio de las pruebas PCR es muy evidente, y las principales diferencias las encontramos en regiones que han apostado por hacer más test de AC, por ejemplo.

## Evolución de los contagios y fallecidos
Empecemos con una tabla resumen: en ella se muestran los casos acumulados diagnosticados, el número de nuevos casos (diarios, en 7 y en 14 días) y la IA por 100000 habitantes para cada comunidad autónoma, ordenado por IA:

<iframe id="igraph" scrolling="yes" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/742.embed" height="800" width="100%"></iframe>

En la siguiente tabla se muestran los fallecimientos acumulados, diarios, incrementos respecto al día anterior, en la última semana y por cada 100000 habitantes, ordenados por este último:
<iframe id="igraph" scrolling="yes" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/744.embed" height="700" width="100%"></iframe>
La siguiente imagen presenta las curvas de contagios y fallecidos diarios para cada CA:
<iframe id="igraph" scrolling="yes" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/746.embed" height="1200" width="135%"></iframe>
Y la siguiente respecto a los valores acumulados desde el inicio de la pandémia:
<iframe id="igraph" scrolling="yes" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/752.embed" height="1200" width="135%"></iframe>

### Evolución de la incidéncia acumulada
La IA ha sido uno de los indicativos de la necesidad de medidas de restricción de movilidad más severas. Los valores para una semana se muestran a continuación:
<iframe id="igraph" scrolling="yes" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/748.embed" height="1200" width="135%"></iframe>
Mientras que los valores correspondientes a dos semanas son los siguientes, acompañados del valor máximo decretado por el Ministerio de Sanidad a partir del cual es necesario tomar medidas, en este caso 150:
<iframe id="igraph" scrolling="yes" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/750.embed" height="1200" width="135%"></iframe>

## Evolución de los hospitalizados e ingresados en UCI
Las presión hospitalária también es un indicativo de la situación de la región. La siguiente figura muestra la evolución de las hospitalizaciones e ingresos en UCI en cada CA:
<iframe id="igraph" scrolling="yes" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/754.embed" height="1200" width="135%"></iframe>
