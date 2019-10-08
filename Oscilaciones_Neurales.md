# __Oscilaciones neurales__.
Este tutorial sirve de introducción al ejercicio de extracción de oscilaciones neurales desde datos electroencefalográficos (EEG). Esta introducción requiere un conocimiento básico de Python y MNE para el análisis de datos de EEG. 

# ¿Qué son las oscilaciones neurales?
Las oscilaciones neurales son patrones de frecuencia repetitivos, rítmicos y sincronizados en el sistema nervioso central. Ocurren durante la activación de grandes agrupaciones de neuronas, aunque pueden involucrar a una sola neurona también. Aunque los datos brutos (sin procesar) obtenidos con electroencefalogramas son capturados en función del tiempo, las oscilaciones neurales son visualizadas en términos de frecuencia y medidas en unidades de Hertz (Hz); un ciclo por segundo. En tanto tal, las agrupaciones neurales generan oscilaciones que pueden ser caracterizadas por el rango de frecuencia en el que ocurren:

*	Ondas Alfa (7.5 – 12.5 Hz): Son generalmente asociadas con funciones cognitivas como atención y alerta. Las ondas alfa están también relacionadas con procesos de aprendizaje y corresponden a las frecuencias más comúnmente analizadas en aplicaciones de ánimo y meditación. 
* Ondas Beta (13 – 30 Hz): Son ondas generalmente asociadas con atención y concentración.
 * SCSCSCSCSCS
*	Ondas Delta (1 – 4 Hz): Estas ondas de alta amplitud están relacionadas con el fenómeno de sueño-de-onda-lenta, o “slow-wave-sleep” (SWS). 
*	Ondas Gama (30 – 70 Hz): Las ondas gama son ondas rápidas asociadas con atención, conciencia y percepción. 
*	Ondas Mu (7.2 – 12.5, principalmente 9 – 11 Hz): Estas ondas están localizadas sobre la corteza motora y están principalmente asociadas con un estado de reposo físico. Están desincronizadas (suprimidas) durante la acción motora.
*	Ondas Teta (4 – 8 Hz): Dos tipos de oscilaciones teta han sido descritas dependiendo de la localización en la que ocurren. El ritmo teta hipocampal es una oscilación fuerte que puede ser observada en el hipocampo, mientras que el ritmo teta cortical consiste en componentes de frecuencia lenta de señales EEG en el cuero cabelludo. No se sabe claramente sobre la función de las ondas teta; sin embargo, una combinación de varias teorías sugiere que las ondas teta hipocampal están vinculadas a la actividad de navegación y memoria. Ondas teta corticales son observadas más frecuentemente en infantes y aparecen en estados de meditación, hipnóticos, sopor, y de sueño no-profundo.   

<img src ="https://github.com/jfrayshe/learn.neurotechedu.com/blob/gh-pages/images/Brain%20wave%20frequency%20chart.png">
 
# ¿Por qué producimos oscilaciones neurales?
No sabemos todavía por qué nuestro cerebro produce oscilaciones neurales. Algunos investigadores teorizan que las oscilaciones neurales no son nada más que derivados de actividad neuronal, indicadores de patrones cerebrales esperados en respuesta a eventos de estímulos. Por ejemplo, el movimiento produce ocurrencias predecibles de ondas alfa (en la frecuencia mu) en la corteza motora, y ciclos de sueño están caracterizados por el flujo alterno de ondas neurales diferentes. Otros investigadores han teorizado que ciertas oscilaciones, como las que ocurren en el rango delta, son críticas para develar los misterios de nuestra conciencia. 

# ¿Por qué son importantes las ondas neurales? 
Las oscilaciones neurales son útiles en varias formas. Desde un punto de vista de diagnóstico e imagen, pueden ser usadas como indicadores de fenómenos neurológicos específicos, tales como: 
* 	Sueño y el estado de conciencia
*	Control motor
*	Procesamiento de la percepción e información.
*	Generación de patrones. 
*	Memoria.
*	Función neural anormal, como epilepsia y Parkinson. 

Aplicaciones prácticas para extraer oscilaciones neurales usando tu propio BCI podría ser observar la presencia de ondas mu cuando realizamos movimientos, o confirmar si ondas alfa y beta están presentes en estados de meditación. Podrías incluso querer observar todas las ondas diferentes que ocurren cuando estás ejecutando una tarea específica.

# ¿Cómo extraemos oscilaciones neurales como una característica de nuestros datos de EEG?

<img scr="https://github.com/NeuroTechX/eeg-101/blob/dano-dev/EEG101/src/assets/wavedecomposition.gif" alt="This should display an animated GIF" />

Como mencionamos antes, los datos obtenidos por EEG son capturados como función del tiempo, pero las oscilaciones neurales están descritas en unidades de frecuencia. Para transformar datos, necesitamos emplear transformadas de Fourier. 
La transformada de Fourier es una fórmula pilar para el procesamiento de señales y descomposición de señales. Si quisieras aprender más acerca de las transformada de Fourier y FFT, recomendamos este video (https://www.youtube.com/watch?v=FjmwwDHT98c). Es un poco largo, ¡pero vale la pena verlo!

<img src="eeg-101/EEG101/src/assets/wavedecomposition.gif" alt="This should display an animated GIF" />

La mejor manera de extraer oscilaciones neurales es realizar una transformada de Fourier en tus datos preprocesada y luego graficar los patrones de frecuencias resultantes en la categoría de ondas cerebrales que te interesan. Puedes preprocesar aún más tus datos para excluir ciertos canales, o apuntar a rangos de frecuencia específicas para observar características de la oscilación neural. >Lee en NeuroTechX.edu la lección titualada “preprocesamiento” para tener una idea detallada sobre los pasos de pre-procesamiento que pueden ser aplicados a tus datos. 

Antes de extraer oscilaciones neurales, hay varios pasos que deben ser tomados para preparar tus datos:
*	Importar datos, leer datos, formatear datos.
*	Preprocesamiento.
*	“Epoching”.
*	Ensamble de clasificadores (graficar un mapa topográfico, “topomap”).
*	Graficar la figura relevante.

### Importando, leyendo y formateando datos.

En el siguiente ejemplo, hemos usado un conjunto de datos (data) creados por ejecuciones experimentales (referencia de investigación), de manera que cuando se obtienen los datos, ya habrá experimentado un preprocesamiento que no se cubrirá en ninguno de los ejemplos. Sin embargo, en ambos casos los datos se obtendrán utilizando los siguientes comandos:
```
subject = 1 <br/>
runs = [3] <br/>
tmin = -0.1 <br/>
tmax = 0.3 <br/>
raw_fnames = eegbci.load_data(subject,runs) <br/>
raw_files = [read_raw_edf(f, preload=True) for f in raw_fnames] <br/>
raw = concatenate_raws(raw_files) <br/>
raw.ch_names.index('STI 014') <br/>
```
Este código de arriba puede separarse en dos componentes. Los parámetros de las líneas 1 a la 4 definen qué partes del set de datos han de ser analizados, mientras que las líneas 5 a la 8 extraen los datos y conectan lo que cada línea hace (¿Qué hacen esas líneas?)
Línea 2 es relevante en este ejemplo, ya que hay 14 ejecuciones experimentales para elegir de aquellas que se realizaron en este estudio y cada una fue probada bajo diferentes condiciones. En este experimento, la ejecución 3 midió la señal EEG obtenida durante el movimiento de las manos izquierda y derecha, ambas de forma separada y simultáneamente. 

### Preprocesamiento.

El preprocesamiento es un paso crítico al analizar los datos de EEG. Los datos de EEG contienen mucho ruido y datos que no son relevantes para lo que estás intentando visualizar. El preprocesamiento es un tema profundo y hay muchas maneras de limpiar los datos de EEG. Consulta nuestra publicación sobre preprocesamiento aquí. Al graficar la densidad espectral de potencia (PSD, siglas en inglés), solo es necesario el “epoching” ya que queremos ver el PSD en todo el rango de frecuencia disponible. Sin embargo, para el gráfico de “topomap” deberás preprocesar tus datos con un filtro de paso de banda para aislar el rango de frecuencia específico que deseas visualizar. El siguiente ejemplo también elimina los nombres de los canales de sus claves predeterminadas "." para evitar errores al leer los nombres de tus canales.

### Epoching los datos.

Epoching consiste en dividir datos en segmentos de data basados en una ventana de tiempo de interés. El interés es generalmente determinado por un evento, sea un evento evocado o un evento inducido. (¿Tenemos un segmento de información que explore epoching más a fondo?). Para epoch tus datos, puedes seguir los siguientes pasos:
```
events = mne.find_events(raw, stim_channel='STI 014', verbose=True) <br/>
picks = pick_types)raw.info, meg=Fale, eeg=True, stim=False, eog=False, exclude='bas') <br/>
baseline = 0, None <br/>
```
Estas líneas (arriba) definen los eventos que vas a buscar, como también el tipo de señal tu programa debiera analizar (MEG vs. EEG vs. EOG). Seleccionamos eeg=True ya que los datos apuntarán hacia donde fueron obtenidos usando un equipo (“headset”) EEG. Abajo, continuamos las entradas (inputs) necesarias para el “epoching”. 
```
epochs = Epochs(raw, events, event_id, tmin, tmax, proj=True, picks=picks, baseline-baselin, preload=True) <br/>
epochs_train=epochs.copy().crop(tmin=-0.2,tmax=0.5) <br/>
labels=epochs.events[:,-1]- <br/>
```
Este código define las “épocas” (epochs) que serán manipuladas a fondo. Prueba la función __plot.epochs()__ para ver cómo tus datos se han transformado. (Pista: puede lucir algo similar a la imagen de abajo).

<img src="https://github.com/jfrayshe/learn.neurotechedu.com/blob/gh-pages/images/neurosc/Screen%20Shot%202017-06-02%20at%209.49.47%20PM.png">
  
Los pasos siguientes van a divergir dependiendo en los métodos de visualización que quieres aplicar. Abajo subrayamos cómo usar PSD para visualizar frecuencias dominantes como también los mapas topográficos para destacar frecuencias específicas en áreas localizadas. 

### Usando PSD para categorizar ocurrencia oscilatoria basada en contenido espectral de poder.
 
La densidad espectral de poder mide el poder de una señal en microvoltios. La función __epochs[events].plot_psd()__ puede ser usada para graficar eventos de “época” específicos como una función de densidad espectral de poder sobre un rango de frecuencia específica. Abajo, un ejemplo de un guión (script) que puedes ejecutar para lograr esto. Ten en cuenta que el conjunto de datos (dataset) importado desde eegbci está ya preprocesado y transformado usando la función Fourier. Los pasos que deberías ver son:
*	Importar, leer, y formatear tus datos.
*	Epoch de datos.
*	Grafica los datos con __epochs[events].plot_psd()__.

<img src="https://github.com/jfrayshe/learn.neurotechedu.com/blob/gh-pages/images/neurosc/CH3.png">
 
__Figura 1:__ Densidad espectral de poder graficada para el electrodo C3 localizado en el lado izquierdo de la corteza motora. Es evidente que el contenido PSD es más evidente en el rango alfa y beta. Evidencia de oscilaciones neurales ocurriendo durante el movimiento de la mano derecha. 

<img src="https://github.com/jfrayshe/learn.neurotechedu.com/blob/gh-pages/images/neurosc/CH4.png">
 
__Figura 2:__ Densidad espectral de poder graficada para el electrodo C4 localizado en el lado izquierdo de la corteza motora. El contenido PSD es más evidente en el rango alfa y el rango teta. Evidencia de oscilaciones neurales que ocurren durante el movimiento de la mano izquierda. 

### Usando un mapa topográfico (topomapa) para visualizar oscilaciones locales. 
Asuntos destacados de topomapa.
Se aplicará un clasificador para visualizar la presencia de oscilaciones neurales usando discriminación binaria para destacar si hay ondas a ciertas frecuencias o no. Mientras hay un poco de variabilidad en la visualización de la fuerza de tu señal, este es un método simple que consiste en observar neuronas disparando sobre electrodos específicos. Comprender qué electrodos corresponden a qué regiones del cerebro te ayudará a entender dónde la mayoría de la actividad está ocurriendo en el cerebro. 
Graficar PSD para visualizar frecuencia está restringido a canales específicos y puede requerir un exceso de trabajo para visualizar la presencia local de ondas. En contraste, el uso de topomapa ofrece retroalimentación específica en la presencia local de ondas. El clasificador ensamblado en el ejemplo siguiente usa un rango binario caracterizado por los valores positivos rojos y los valores azules negativos. El rango total va desde -0.1 a 1.0 y se refiere al potencial eléctrico con 1.0 indicando la presencia de una señal medible. 
Hay varios pasos más involucrados en visualización de topomapa. El primero consiste en el paso de preprocesamiento ya que puedes usar un filtro de paso de banda (raw.filter(fmin,fmax)) para aislar el rango de frecuencia que te interesa. Lee la sección de arriba donde identificamos cada onda dependiendo de su rango de frecuencia respectiva. El ejemplo siguiente usará un filtro de paso de banda para ondas alfa y beta considerando que las ejecuciones de conjunto de datos eegbci están basadas en la actividad de la corteza motora.
Cinco puntos de tiempo arbitrarios fueron elegidos en el ejemplo de abajo para resaltar el cambio de presencia de onda en el tiempo. En vista de que la ejecución involucra apretar las manos derecha e izquierda, deberíamos esperar ver un incremento en la presencia de ondas alfa (específicamente la frecuencia mu) y una disminución recíproca de frecuencia de ondas beta en el área que corresponde a la mano derecha o a la mano izquierda (lados opuestos del cerebro de la mano involucrados). Los puntos de tiempo 4 y 5 ilustran esta diferencia:

<img src="https://github.com/jfrayshe/learn.neurotechedu.com/blob/gh-pages/images/neurosc/alpha.png">
 
__Figura 3:__ Topomapa de ondas alfa (7.5 – 12.5 Hz) durante movimiento. 

<img src="https://github.com/jfrayshe/learn.neurotechedu.com/blob/gh-pages/images/neurosc/beta.png">
 
__Figura 4:__ Topomapa de ondas beta (13 - 30 Hz) durante movimiento. 
