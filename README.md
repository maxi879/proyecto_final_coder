# Proyecto Final CoderHouse

## Base de datos
- Los datos pertenecen a un DATABASE publico, https://www.kaggle.com/shivamb/machine-predictive-maintenance-classification .
- Dentro del directorio https://github.com/maxi879/proyecto_final_coder/blob/c6ad029288470c03c1b1730be33d6b686970f367/DATOS se encuentra los datos en formato .xlsx y un .txt con los detalles tecnicos necesarios para realizar un analisis.
## Bibliotecas externas 
- Las bibliotecas utilizadas son :
    - Pandas ==> Utilizado el objeto DataFrame para la manipulacion de  datos.
    - Seaborn ==> Utilizado para la creacion y visualizacion de datos.
    - Matplotlib ==> Llamando especificamente a pyplot para graficar.
    - Warnings ==> Para filtrar errores relativamente ignorables.
    - Nunpy ==> Para manipulacion de los datos.
    - Sklearn ==> Machine Learning y metricas.
    - Imblearn ==> Para solucionar problemas de balanceo de datos.
    - pandas_profiling ==> Profile
## Objetivo
Este repositorio tiene como objetivo realizar un analisis para luego implementar un modelo de MACHINE LEARNING. 
Dentro de este repositorio se utiliza exclusivamente el lenguaje de Python.
## Contenido
- Dentro del directorio principal se encuentra :

    - \\analisis
        - \clasificacion ==> contiene .ipynb con la implementacion y evaluacion.

        - \EDA ==> contiene dos .ipynb con el analisis exploratorio de los datos, y otro .ipynb con un panda profile.

        - \hypertuninga ==> contiene un .ipynb con el hipertuneo de parametros del Random Forest.

    - \\datos
        - descripcion_variables.txt ==> leer antes de explorar el EDA.

        - Base_predictive_maintenance.csv ==> dataset.

    - \\Resultados_importantes.pdf ==> presentacion de los datos.

    - \\README.md

## Aspectos importante de los datos
    El data set contiene 10 variables, dos son usadas como index (UDI,Product_ID). El data set contiene dos variables, Target y Failure_Type, ambas son las variables a predecir. Target es una variable binaria, mientras que Failure_Type es es multiclass.
    Dentro de las restantes 6 se encuentran Type, es una variable categorica, mientras que las otras 5 son variables numericas, que representan datos continuos proviniente de sensores instalados en las maquinas.
## Puntos de interes
- Este analisis parte de la necesidad de brindar la capacidad de prevenir y evitar roturas de maquinas de produccion masiva.
- Buscaremos identificar cuales son las variables mas significativas al momento de rotura segun su tipo. Esto permitira a la empresa disminuir los momentos de falla, logrando asi una mayor estabilidad de la linea de produccion y evitar costos mayores por fallas serias causadas por problemas constantes sin resolver. Se fijaran paramentros de funcionanmientos normales.
Estos datos pueden ser observados en los cuadros de medianas. Dentro del directorio //inicio.
     - Falla por desgaste de la herramienta (TWF): la herramienta se reemplazar?? por falla en un tiempo de desgaste de la herramienta seleccionado aleatoriamente entre 200 y 240 minutos (120 veces en nuestro conjunto de datos). En este momento, la herramienta se reemplaza 69 veces y falla 51 veces (asignadas aleatoriamente).
     - Falla por disipaci??n de calor (HDF): la disipaci??n de calor provoca una falla en el proceso, si la diferencia entre la temperatura del aire y la del proceso es inferior a 8,6 K y la velocidad de rotaci??n de la herramienta es inferior a 1380 rpm. Este es el caso de 115 puntos de datos.
     - Falla de energ??a (PWF): el producto del par y la velocidad de rotaci??n (en rad/s) es igual a la potencia requerida para el proceso. Si esta potencia est?? por debajo de 3500 W o por encima de 9000 W, el proceso falla, que es el caso 95 veces en nuestro conjunto de datos.
     - Fallo por sobreesfuerzo (OSF): si el producto del desgaste de la herramienta y el par supera los 11??000 minNm para la variante de producto L (12??000 M, 13??000 H), el proceso falla debido al sobreesfuerzo. Esto es cierto para 98 puntos de datos.
## Machine Learning 
El modelo optimo para la prediccion de ambas variables Target, es RandomForestClassifier, las metricas utilizadas para esta conclusion se encuentra dentro de analisis\clasificacion\clasificadores.ipynb este notebook esta basado en codigo ageno, pero fue personalizado.

