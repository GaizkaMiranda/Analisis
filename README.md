# Proyecto de Análisis IoT

## Miembros del equipo
- **Miembro 1**: Ekaitz Garcia
- **Miembro 2**: Eneko Fuente
- **Miembro 3**: Gaizka Miranda

## Explicación de los pasos seguidos

1. **Importación de librerías**: Se importaron librerías necesarias como `numpy`, `pandas`, `faker`, y `matplotlib` para generar y visualizar los datos.
2. **Generación de datos aleatorios**: Utilizamos la librería `Faker` para crear nombres y otros datos realistas en español, y `numpy` para generar las notas y horas de estudio de manera aleatoria.
3. **Creación de un DataFrame**: Los datos generados se organizaron en un diccionario y se convirtió en un DataFrame de `pandas` con las columnas requeridas.
4. **Generación de archivos CSV**: Se dividió la información en dos archivos CSV: uno con los datos de los alumnos y otro con las notas de las asignaturas.
5. **Limpieza de los datos**: Se eliminaron duplicados y valores nulos en los datos utilizando las funciones de `pandas`.
6. **Análisis estadístico**: Se generaron estadísticas descriptivas de las columnas numéricas (Nota, Horas de estudio y Edad).
7. **Visualización**: Se crearon histogramas para visualizar la distribución de las notas y las horas de estudio.

## Instrucciones de uso

1. **Instalar dependencias**: Asegúrate de tener las librerías necesarias instaladas en tu entorno de Python. Puedes hacerlo ejecutando:
   ```bash
   pip install numpy pandas faker matplotlib

2. **Ejecutar el código**: Para generar los archivos CSV y las visualizaciones, simplemente ejecuta el archivo de Python. Asegúrate de que los archivos .csv se generen correctamente en el directorio de trabajo.

3. **Explorar los archivos CSV**: Los archivos generados se guardarán con los siguientes nombres:

alumnos_deusto.csv: Contiene la información completa de los alumnos.

alumnos.csv: Contiene solo los nombres de los alumnos.

notas.csv: Contiene las asignaturas y sus correspondientes notas.

4. **Ver los gráficos**: Al ejecutar el código, se mostrarán histogramas sobre la distribución de las notas y las horas de estudio.


## Posibles vías de mejora
1. **Ampliar la generación de datos**: Se podrían añadir más campos, como dirección, fecha de nacimiento o información sobre las clases.

2. **Mejora de la visualización**: Se pueden agregar más tipos de gráficos o hacer una visualización interactiva para analizar más a fondo los datos.

3. **Análisis predictivo**: Se podría aplicar un modelo de Machine Learning para predecir las notas de los estudiantes en función de sus horas de estudio.


## Problemas / Retos encontrados
1. **Generación de datos faltantes**: Se encontró un pequeño reto al generar datos faltantes de forma aleatoria, ya que es difícil controlar que la distribución de datos faltantes siga un patrón lógico o realista.

2. **Manipulación de datos duplicados**: Durante el proceso de limpieza de datos, se encontraron algunos duplicados en la columna DNI, los cuales fueron eliminados.

3. **Inconsistencias en los nombres generados por Faker**: A veces, el generador de nombres de Faker crea nombres con caracteres especiales que pueden no ser manejados correctamente en algunos entornos.

4. **Interprete de python**: Al principio costó ejecutar todo por primera vez por las requerimientos de versiones.

## Alternativas posibles
1. **Uso de otro generador de datos**: En lugar de Faker, podríamos haber utilizado otro generador de datos más específico para el contexto de la simulación.

2. **Aplicación de análisis más profundos**: En lugar de solo generar estadísticas descriptivas, podríamos aplicar técnicas más avanzadas de análisis de datos, como el análisis de correlación entre las horas de estudio y las notas.
