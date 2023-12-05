# Proyecto: Produccion no convencional de petróleo y gas en Argentina

## Objetivo del trabajo: 
Nuestro objetivo es poder comprender el comportamiento de la producción hidrocarburífera no convencional en la cuenca neuquina y particularmente en Vaca Muerta, para contrastarlo con lo informado en los medios. 
Asimismo, buscamos poder predecir el tipo de formación (tight o shale) sobre la que se genera la explotación de hidrocarburos a en función de las características del pozo. . 

## Participantes Grupo 4:
Escalante Virginia
Ordinola Rocío

## Origen de los datos:
Trabajamos con dos datasets. 

* Producción de Pozos de Gas y Petróleo No Convencional:
Detalle mensual de producción por pozo, yacimiento, concesión y provincia. Petróleo [m3], gas en [Miles de m3] y agua en [m3]

*Datos de fractura de pozos de hidrocarburos:
Detalle por pozo, formación, tipo de reservorio, yacimiento, provincia, cantidad de fracturas,  longitud de rama horizontal (m), toneladas de arena bombeada nacional e importada. 

Ambos proporcionados por la Secretaría de Energía de la Nación Argentina

## Preguntas que nos hicimos:
#### AMBIENTAL
La fracturación hidráulica como técnica que permite la extracción de hidrocarburos que se encuentran en formaciones poco porosas e impermeables.
El declive de los recursos convencionales hace que esta técnica cada vez tenga más importancia, al igual que el impacto ambiental asociado.
#### COYUNTURAL
Privatización YPF, producción en Vaca Muerta. Producción de gas, aumento de la demanda, Gasoducto Presidente Néstor Kirchner.

## Conclusiones EDA: 
Esta etapa nos permitió: Conocer la estructura de los datos y familiarizarnos con las variables involucrada, verificar que la cantidad de registros es suficiente para construir los modelos de aprendizaje automático,constatar que el dataset tiene muy pocas variables con valores nulos, entender que probablemente las variables del dataset original no son suficientes para construir un modelo de aprendizaje no supervisado y que será necesario agregar otro dataset que nos permita incorporar variables y acotar las variable necesarias para el análisis, para lo que habrá que eliminar algunas, imputar o filtrar otras. Tomamos la decisión de quedarnos con los datos que permitan caracterizar la producción mayoritaria de hidrocarburos.

## Modelos: 
Con el modelo supervisado buscamos predecir el tipo de formación (tight o shale) correspondiente a cada pozo. Como nuestra variable objetivo es una variable cualitativa, nos encontramos ante un caso de clasificación. 

Con el modelo no supervisado buscamos analizar el comportamiento de la producción hidrocarburífera no convencional en la cuenca neuquina y particularmente en Vaca Muerta. 

## Diccionario de conceptos: 

* mes: que vemos están indicados con el número del mes con un entero.
* prod_pet: nos da la producción de petróleo como flotante, medidos como m3.
* prod_gas: nos da la producción de gas como flotante, medido en miles de m3.
* empresa: es la empresa que realiza la producción. Es objeto porque es un string.
* formacion: es la formación geológica desde donde se realiza la extracción. Es objeto porque es un string.
* areapermisoconcesion: es el área de concesión donde se encuentra el pozo que extrae la producción. Es objeto porque es un string.
