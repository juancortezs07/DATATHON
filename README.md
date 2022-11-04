![HenryLogo](https://d31uz8lwfmyn8g.cloudfront.net/Assets/logo-henry-white-lg.png)
​
# Proyecto individual 2
​
¡Bienvenidos al segundo proyecto! Durante estos días estarán poniendo en práctica sus habilidades en el campo de la predicción. Deberán usar cierta métrica para medir la performance del modelo la cual, a su vez, será usada para elegir los mejores modelos.
​
## Información relevante
​
Para este proyecto tomando en cuenta que nos piden elaborar un modelo que se aplique para el  mercado de bienes raíces de Colombia, por tal motivo se usarán las columnas que contengan información de cantidad salas, dormitorios, baños y superficie total. Ya que hemos consideramos a esos valores como los más importantes para determinar el  precio de un inmueble.
​
## Mercado inmobiliario
​
El mercado inmobiliario a estudiar es de Colombia
​
## Descripción del problema
​
Predecir si el precio de un inmueble es barato o caro, se tomará a los valores 0 como barato y 1 como caro, se usará  un modelo de aprendizaje supervisado random forest classifier , sus principales ventajas son :

    *Funciona bien -aún- sin ajuste de hiperparámetros

    *Funciona bien para problemas de clasificación y también de regresión.

    *Al utilizar múltiples árboles se reduce considerablemente el riesgo de overfiting

    *Se mantiene estable con nuevas muestras puesto que al utilizar cientos de árboles sigue prevaleciendo el promedio de sus votaciones.
​
## Entrega:

​
*Un archivo ipynb llamado PROYECTO-02

*Un archivo csv llamado juancortezs07   

​
## Métrica a utilizar
​
Como método de evaluación del desempeño del modelo, se utilizará la métrica de Exhaustividad (Recall) para las propiedades caras, a partir de la matriz de confusión (Confusion Matrix). 
​
$$ Recall=\frac{TP}{TP+FN}$$
​
Donde $TP$ son los verdaderos positivos y $FN$ los falsos negativos.

Adicionalmente, se incluye la Accuracy como métrica de control.
​
## Archivos provistos
​
Se proveen los archivos dentro del archivo comprimido 'properties_colombia.zip':
 - 'properties_colombia_train.csv': Contiene 197549 registros y 26 dimensiones, el cual incluye la información **numérica** del precio.
 - 'propiedades_colombia_test.csv': Contiene 65850 registros y 25 dimensiones, el cual no incluye la información del precio. 
​
## Descripción de las dimensiones
- id - Identificador del aviso. No es único: si el aviso es actualizado por la inmobiliaria (nueva versión del aviso) se crea un nuevo registro con la misma id pero distintas fechas: de alta y de baja.
- ad_type - Tipo de aviso (Propiedad, Desarrollo/Proyecto).
- start_date - Fecha de alta del aviso.
- end_date - Fecha de baja del aviso.
- created_on - Fecha de alta de la primera versión del aviso.
- lat - Latitud.
- lon - Longitud.
- l1 - Nivel administrativo 1: país.
- l2 - Nivel administrativo 2: usualmente provincia.
- l3 - Nivel administrativo 3: usualmente ciudad.
- l4 - Nivel administrativo 4: usualmente barrio.
- l5 - Nivel administrativo 5.
- l6 - Nivel administrativo 6.
- rooms - Cantidad de ambientes.
- bedrooms - Cantidad de dormitorios (útil en el resto de los países).
- bathrooms - Cantidad de baños.
- surface_total - Superficie total en m².
- surface_covered - Superficie cubierta en m².
- price - Precio publicado en el anuncio.
- currency - Moneda del precio publicado.
- price_period - Periodo del precio (Diario, Semanal, Mensual)
- title - Título del anuncio.
- description - Descripción del anuncio.
- property_type - Tipo de propiedad (Casa, Departamento, PH).
- operation_type - Tipo de operación (Venta).
- geometry - Puntos geométricos formados por las coordenadas latitud y longitud. 
​
## Sugerencias
​
- Exploren el dataset. Saquen medidas resumen, vean distribuciones de los datos, analicen bien el tipo de problema, etc.
- Piensen que tipo de modelo podría ser aplicable según la descripción del problema y el tipo de variable de salida.
- Busquen información sobre la métrica aplicada, cada métrica tiene pros y contras.
- Siempre que vean en un dataset coordenadas geoespaciales, es buena estrategia revisar que las mismas correspondan en el mapa al lugar que deberían.
- Si se presentan comentarios, es una buena oportunidad de aplicar procesamiento del lenguaje natural (NLP) para mejorar nuestro modelo.
- En cuanto a la utilización de git, recuerden que si quieren hacer un cambio experimental pero no quieren romper el modelo, pueden utilizar [branching](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging).
- Aprovechen esta instancia de aprendizaje, experimenten y, sobre todo, ¡diviértanse!

