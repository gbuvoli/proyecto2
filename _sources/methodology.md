# Metodología

La metodología propuesta para este estudio es la **CRISP DM (Cross-Industry Standard Process for Data Mining)**, la cual se adaptará para abordar los objetivos específicos previamente mencionados y constará de las siguientes etapas:

![Metodología CRISP-DM](crisp.png)



1. **Comprensión del negocio (Understanding the Business)**: 

    En esta etapa, se busca comprender los objetivos del negocio y los requisitos del proyecto. Se identifican los objetivos de la minería de datos y se establece un plan preliminar para alcanzarlos.

    Para nuestro caso, se llevarán a cabo reuniones con la oficina de Calidad y Proyectos académicos y el Observatorio de Educación Uninorte, para entender el contexto, antecedentes y las necesidades actuales de la estrategia institucional de preparación para las pruebas SABER PRO.

2. **Comprensión de los datos (Data Understanding)**: 

    En esta fase, se recopilan los datos relevantes para el proyecto y se exploran para comprender su naturaleza, calidad, distribución y posibles problemas. También se identifican las variables importantes y se seleccionan aquellas que serán útiles para el análisis.

    En esta etapa esperamos recopilar y revisar los datos históricos de los resultados de las pruebas SABER PRO, desde 2016 hasta 2023, los cuales incluyen información sociodemográfica delos  estudiantes que han tomado las pruebas SABER PRO a nivel nacional, la mayor parte de esta data es de tipo categórica y pueden llegar a tener muchos niveles.

    Por otro lado, la informacion institucional como el promedio acumulado del estudiante semestre a semestre, así como las notas finales obtenidas en algunas asignaturas o grupos de asignaturas que alimentan las competencias evaluadas en las pruebas y la información registrada en el formulario de admisión puede tener muchos datos faltantes, y estar almacenada de diferentes bases de datos. 
    La recopilación de los datos de interés puede requerir un trabajo manual importante.

3. **Preparación de los datos (Data Preparation)**: 

    Aquí se lleva a cabo la limpieza, integración y transformación de los datos para prepararlos para el modelado. Esto puede implicar la eliminación de valores atípicos, la imputación de datos faltantes, la codificación de variables categóricas y la creación de nuevas variables derivadas.

    Uno de los principales retos de este proyecto es el cruce de la información obtenida del ICFES y la información institucional, este paso es crucial para lograr el alcance propuesto  en este proyecto.

    Debido a la cantidad importante de variables categóricas, para entender las relaciones entre ellas usaremos un *Analisis Factorial de Correspondencia*


4. **Modelado (Modeling)**: 

    En esta etapa, se seleccionan y aplican técnicas de modelado de datos para construir modelos predictivos o descriptivos. Se prueban múltiples algoritmos y se ajustan sus parámetros para encontrar el mejor modelo posible.

    La etapa de modelado, será la más compleja, puesto que para utilizaremos diferentes sets de datos de entrada en los modelos, con el propósito de encontrar el "momento" optimo para hacer las predicciones.
    
    Usaremos modelos tanto de regresión como de clasificación para comparar rendimientos. En los modelos de regresión, pretendemos predecir los puntajes de las pruebas, mientras que en los modelos de clasificación buscaremos predecir los niveles de desempeño.

   1. **El momento más temprano posible**

        - El momento "mas temprano" para intentar hacer la predicción es durante el tramite de admisión a la universidad, al diligenciar el formulario se registra información sociodemográfica y los resultados de las pruebas SABER 11. Con esta información realizaremos nuestras primeras predicciones, tanto de puntaje Global como de pruebas específicas.

        
   2. **Primer cuarto y mitad de carrera**
       - Momentos intermedios de la carrera universitaria, en los cuales ya podemos contar con información de promedios acumulados y notas de diferentes asignaturas que podrían ser importante para estimar los resultados de las pruebas genericas, por ejemplo (asignaturas de calculo para la prueba de razonamiento cuantitativo). Se propone hacer modelos con los promedio acumulados y notas del 25% y 50% del programa.
       


5. **Evaluación (Evaluation)**: 

    Aquí se evalúan los modelos construidos utilizando criterios de rendimiento específicos, como precisión, sensibilidad o especificidad. Se selecciona el modelo final que mejor se ajuste a los objetivos del proyecto.
    
    - Para la evaluación de modelos, se usará validación cruzada, se particionarán los datasets para entrenamiento y validación, ya que tenemos suficientes datos para comparar las predicciones con los datos reales que los estudiantes obtuvieron en la prueba.
    
    
6. **Despliegue (Deployment)**: En la última fase, se implementa el modelo seleccionado en el entorno operativo del negocio. Se monitorea su rendimiento continuamente y se realizan ajustes según sea necesario.

    - Para esta etapa, buscaremos explorar y proponer una implementación que sea viable dentro de las limitaciones de los sistemas institucionales, para que los modelos puedan ser fácilmente utilizados por los funcionarios de las dependencias que lo requieran.



