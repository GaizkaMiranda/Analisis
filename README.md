# Proyecto de Análisis IoT

## Miembros del equipo
- **Miembro 1**: Ekaitz Garcia
- **Miembro 2**: Eneko Fuente
- **Miembro 3**: Gaizka Miranda

## Explicación de los pasos seguidos

1. **Importación de librerías**: Se importaron librerías necesarias como `numpy`, `pandas`, `faker`, y `matplotlib` para generar y visualizar los datos. Ademas, se usan librerias como `elasticsearch`, `python-dotenv` y `requests` para almacenar datos en elastic y visualizarlos con kibana
2. **Generación de datos aleatorios**: Utilizamos la librería `Faker` para crear nombres y otros datos realistas en español, y `numpy` para generar las notas y horas de estudio de manera aleatoria.
3. **Creación de un DataFrame**: Los datos generados se organizaron en un diccionario y se convirtió en un DataFrame de `pandas` con las columnas requeridas.
4. **Generación de archivos CSV**: Se dividió la información en dos archivos CSV: uno con los datos de los alumnos y otro con las notas de las asignaturas.
5. **Limpieza de los datos**: Se eliminaron duplicados y valores nulos en los datos utilizando las funciones de `pandas`.
6. **Análisis estadístico**: Se generaron estadísticas descriptivas de las columnas numéricas (Nota, Horas de estudio y Edad).
7. **Visualización**: Se crearon histogramas para visualizar la distribución de las notas y las horas de estudio.

## Instrucciones de uso

1. **Levantar contenedores**: Levantaremos kibana y elastic haciendo uso del docker-compose.yml. Puedes hacerlo ejecutando:
   ```bash
   docker-compose up

2. **Instalar dependencias**: Asegúrate de tener las librerías necesarias instaladas en tu entorno de Python. Puedes hacerlo ejecutando:
   ```bash
   pip install -r requirements.txt

   Otra opción sería crear un nuevo kernel a partir del archivo requirements.txt

3. **Ejecutar el código**: Para generar los archivos CSV y las visualizaciones, simplemente ejecuta el archivo de Python. Asegúrate de que los archivos .csv se generen correctamente en el directorio de trabajo. Antes de hacerlo, asegúrate de que los contenedores estan corriendo. En caso de que no lo esten, no pasa nada, puedes ejecutar todo aunque el ultimo bloque dara error. Una vez todo esta levantado, puedes ejecutar el bloque que ha dado error y listo.

4. **Explorar los archivos CSV**: Los archivos generados se guardarán con los siguientes nombres:

alumnos_deusto.csv: Contiene la información completa de los alumnos.

alumnos.csv: Contiene solo los nombres de los alumnos.

notas.csv: Contiene las asignaturas y sus correspondientes notas.

5. **Ver los gráficos**: Al ejecutar el código, se mostrarán histogramas sobre la distribución de las notas y las horas de estudio.

6. **Acceder a elastic**: Para comprobar que los datos se han almacenado correctamente, puedes acceder a elastic abriendo http://localhost:5601/ y usanso el usuario `elastic` y la contraseña `admín1` (Se puede cambiar en el .env antes de ejecutar los contenedores.)

7. **Importar el dashboard**: Para comprobar de una manera mas visual que realmente hay datos, navegar a Stack Management > Saved Objects e importar el archivo vista.ndjson

8. **Visualizar el dashboard**: Una vez importado, para ver los datos, ve a Analytics > Dashboard y seleccionar el dashboard importado.

## Posibles vías de mejora
1. **Ampliar la generación de datos**: Se podrían añadir más campos, como dirección, fecha de nacimiento o información sobre las clases.

2. **Automatización completa del despliegue**: Crear un script que automatice la ejecución, ejecutando el jupyter notebook y añadiendo el dashboard.

3. **Análisis predictivo**: Se podría aplicar un modelo de Machine Learning para predecir las notas de los estudiantes en función de sus horas de estudio.


## Problemas / Retos encontrados
1. **Generación de datos faltantes**: Se encontró un pequeño reto al generar datos faltantes de forma aleatoria, ya que es difícil controlar que la distribución de datos faltantes siga un patrón lógico o realista.

2. **Manipulación de datos duplicados**: Durante el proceso de limpieza de datos, se encontraron algunos duplicados en la columna DNI, los cuales fueron eliminados.

3. **Inconsistencias en los nombres generados por Faker**: A veces, el generador de nombres de Faker crea nombres con caracteres especiales que pueden no ser manejados correctamente en algunos entornos.

4. **Interprete de python**: Al principio costó ejecutar todo por primera vez por las requerimientos de versiones.

## Alternativas posibles
1. **Uso de otro generador de datos**: En lugar de Faker, podríamos haber utilizado otro generador de datos más específico para el contexto de la simulación.

2. **Aplicación de análisis más profundos**: En lugar de solo generar estadísticas descriptivas, podríamos aplicar técnicas más avanzadas de análisis de datos, como el análisis de correlación entre las horas de estudio y las notas.
3. **PostgreSQL para gestión de datos**: PostgreSQL maneja grandes volúmenes de datos mejor que archivos CSV o SQLite y soporta consultas complejas y optimización de rendimiento.

