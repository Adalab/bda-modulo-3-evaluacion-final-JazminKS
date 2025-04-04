# Evaluación Final Módulo 3: Transformando de Datos

> Esta evaluación tiene como objetivo medir tu comprensión y dominio de las técnicas de Transformación de Datos, habilidades esenciales para el trabajo con bases de datos.
>
##  Criterios de evaluación

 - Análisis Exploratorio de los datos.
 
 - Gestión de nulos. 
 
 - Visualización de datos con matplotlib y seaborn.
 
 - Estadística descriptiva e inferencial.

## Contenido

Los datos que se proporciona consisten en dos conjuntos de archivos que, en conjunto, describen el comportamiento de los clientes dentro de un programa de lealtad de una aerolínea.

  -  ***Customer Flight Analysis.csv:*** Este archivo contiene información sobre la actividad de vuelo de los clientes, incluyendo el número de vuelos reservados, la distancia volada, puntos acumulados y redimidos, y costos asociados a los puntos redimidos.

  -  ***Customer Loyalty History.csv:*** Este archivo proporciona un perfil detallado de los clientes, incluyendo su ubicación, nivel educativo, ingresos, estado civil, y detalles sobre su membresía en el programa de lealtad (como el tipo de tarjeta, valor de vida del cliente, y fechas de inscripción y cancelación).


## Desarrollo de ejercicio
    Ejemplo:
    ¿Cuál es la proporción de clientes con diferentes tipos de tarjetas de fidelidad?

```js
## #PASO1. Calcula la frecuencia de cada tipo de tarjeta de fidelidad.
tarj_counts = df_customer['loyalty_card'].value_counts()

#PASO2. Paleta de colores de seaborn
colores = sns.color_palette("pastel")

#PASO3. Crear el gráfico
plt.pie(tarj_counts,
        labels=tarj_counts.index,
        autopct='%1.1f%%',
        colors=colores,
        textprops={'fontsize': 10},
        startangle=90,
        wedgeprops={'linewidth': 1, 'edgecolor': 'white'})

#PASO4. Ponemos título a la gráfica
plt.title("Porcentaje de clientes con diferentes tipos de tarjetas de fidelidad", fontsize=10) # Ajustar el tamaño del título
plt.show(); 
```
![Diagrama](https://github.com/Adalab/bda-modulo-3-evaluacion-final-JazminKS/blob/main/FILES/Diagrama.png)