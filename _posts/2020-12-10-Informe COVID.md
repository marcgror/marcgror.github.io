# Análisis de los datos del COVID-19 en España
2020 será siempre recordado como el año de la pandemia de COVID-19. España ha sido y es uno de los países más afectados, tanto en la primera ola en marzo como en la siguiente en setiembre.

Para analizar la situación, a nivel nacional, autonómico y provincial, se usarán los datos proporcionados por el Ministerio de Sanidad.

# España

Antes de analizar en detalle la situación de las Comunidades Autónomas, es importante conocer el panorama a nivel nacional.
## Métodos de diagnóstico del COVID-19
En España, el COVID se está detectando principalmente usando las pruebas de PCR y test de anticuerpos, a parte de otras pruebas como el test de antígenos.

La prueba PCR (Polimerasa Chain Reaction) es una prueba de diagnóstico utilizada para detectar fragmentos del material genético de un patógeno. En este caso en concreto, el patógeno se corresponde con el virus SARS-CoV-2. La idea es sencilla: se toma una muestra respiratoria de la persona sospechosa de infección, y se analiza en un laboratorio de microbiología con un PCR en busca de una molécula de ARN del virus. El positivo vendría cuando la prueba detecta ese ARN del virus, mientras será negativo en caso contrario.

Por su parte, los test de anticuerpos detectan la presencia de estos en el organismo, generados como respuesta a la presencia del virus.

Actualmente se dispone tanto de datos de contagiados diagnosticados con PCR como de diagnosticados con otros tipos de prueba, como puede ser el test de anticuerpos o de antígenos.

El siguiente gráfico muestra la contribución en porcentaje de cada tipo de prueba: 
<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/44.embed" height="525" width="100%"></iframe>

Casi un 90 % de las detecciones de contagiados son gracias a pruebas PCR, mientras que otras pruebas como podrían ser los test de antígenos alcanzan casi un 10 % de cuota. Los test de anticuerpo y las pruebas desconocidas obtienen muy poca representación.

## Evolución de los contagios
En la siguiente tabla se muestran los casos diarios, acumulados, el incremento diario, en los últimos 7 y 14 días, la media de casos en los últimos 7 y 14 días, la incidéncia acumulada en los últimos 7 y 14 días y la acumulada para los últimos 10 días a nivel nacional:
<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/50.embed" height="525" width="100%"></iframe>

La curva de contagiados en España desde el inicio de la pandémia se muestra a continuación:
<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/52.embed" height="525" width="100%"></iframe>
Las dos olas se pueden diferenciar claramente. Los efectos del confinamiento, desescalada y fin del Estado de Alarma son también evidentes, ya que el número de contagios diarios decae a mínimos practicamente hasta principios de julio, fruto del parón social y laboral del país. Es entonces cuando empiezan a aumentar los nuevos positivos, seguramente porque la "Nueva Normalidad" lleva vigente 1-2 semanas en toda España, y por lo tanto la población empieza poco a poco a interactuar de nuevo. El hecho de que esta vuelta a la socialización y al trabajo se diera en verano seguramente no ayuda tampoco.
Si nos fijamos en los positivos acumulados, las tendencias son prácticamente las mismas, como es lógico:
<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/62.embed" height="525" width="100%"></iframe>
Otros indicadores útiles para valorar el estado actual de la pandemia son el número de positivos hospitalizados, en la UCI y recuperados. Como se puede observar, en el peor momento de la primera ola (finales de marzo-mayo) es cuando se produjo el mayor número de personas hospitalizadas o en la UCI, mientras que los recuperados iban aumentando a medida que pasaba las semanas. Durante el inicio del verano los ingresados disminuyen, fruto del descenso de los contagios debido al confinamiento y la desescalada. Una vez llega Agosto, se empiezan a notar los efectos de la "nueva normalidad", y los hospitalizados e ingresados en UCI por COVID empiezan a aumentar de nuevo.

Durante todo este tiempo, las cifras de recuperados no hacen más que aumentar, debido seguramente al gran número de personas infectadas con anterioridad.

### Incidéncia acumulada
La incidéncia acumulada (IA) es una forma de medir el impacto de la pandémia en cada territorio teniendo en cuenta su población. Por lo tanto, permite comparar valores entre distintas regiones/paises y establecer valores máximos que, una vez superados, exijan aplicar medidas de restricción de movilidad.

La evolución de la IA en 7 y 14 días durante toda la pandémia se muestra a continuación:
<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/54.embed" height="525" width="100%"></iframe>
Se observa una tendéncia similar a la curva de contágios.

## Fallecidos
<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/337.embed" height="525" width="100%"></iframe>
El siguiente paso es el número de fallecidos. A continuación se muestra la evolución del número de fallecidos diario diagnosticados con COVID desde el inicio de la pandémia:
<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/65.embed" height="525" width="100%"></iframe>

Durante la primera ola, se alcanzaron cifras diarias de más de 1000 muertos diarios positivos por COVID. Gracias al confinamiento, estas cifras fueron dismuyendo lentamente durante mayo y junio, llegando a su mínimo durante el verano. Una vez los contagios e infectados vuelven a incrementarse a finales de agosto, los fallecidos empiezan a aumentar también.
<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/67.embed" height="525" width="100%"></iframe>
En el acumulado, se puede observar un estancamiento en el número de fallecidos durante el verano, pero a partir de los últimos días de agosto se observa de nuevo una tendencia al aumento.

## Mapa de incidencia
<iframe title="IA en dos semanas" aria-label="Mapa" id="datawrapper-chart-CPbTd" src="https://datawrapper.dwcdn.net/CPbTd/4/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="468"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"])for(var e in a.data["datawrapper-height"]){var t=document.getElementById("datawrapper-chart-"+e)||document.querySelector("iframe[src*='"+e+"']");t&&(t.style.height=a.data["datawrapper-height"][e]+"px")}}))}();
</script>

# CCAA
## Métodos de diagnóstico del COVID-19
<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/318.embed" height="525" width="100%"></iframe>

A partir de los datos separados por Comunidades Autónomas es posible seguir la evolución de la pandemia en estas.
## Evolución de los contagios y fallecidos
Empecemos con una tabla resumen: en ella se muestran los casos acumulados diagnosticados, el número de nuevos casos (diarios, en 7 y en 14 días) y la IA por 100000 habitantes para cada comunidad autónoma, ordenado por IA:

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/322.embed" height="800" width="100%"></iframe>

En la siguiente tabla se muestran los fallecimientos acumulados, diarios, incrementos respecto al día anterior, en la última semana y por cada 100000 habitantes, ordenados por este último:
<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/330.embed" height="700" width="100%"></iframe>
<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/500.embed" height="1200" width="135%"></iframe>
<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/496.embed" height="1200" width="135%"></iframe>

### Evolución de la incidéncia acumulada
<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/326.embed" height="1200" width="135%"></iframe>
<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/328.embed" height="1200" width="135%"></iframe>

## Evolución de los hospitalizados e ingresados en UCI
<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plotly.com/~marcgror/563.embed" height="1200" width="135%"></iframe>
