# ARCHIVOS Y DATOS EN COLAB.  
**Ricardo Vega M. - rivegam@uc.cl**. 

**Universidad Católica de Chile**.  

En la clase trabajaremos con Colab, un servicio online de Google para programar en Python. Como dice su sitio: “Colab es un servicio alojado de Jupyter Notebook que no requiere configuración y que ofrece acceso gratuito a recursos de computación, como GPUs y TPUs. Colab es una solución especialmente adecuada para el aprendizaje automático, la ciencia de datos y la educación.”  

Para trabajar en Colab, deben tener una cuenta Gmail habilitada. Al trabajar con archivos de datos, y una vez abierto un archivo de Colab, tenemos dos opciones para subir datos al colab:  


## OPCIÓN A– Subir archivos desde archivo computador local:   

1. Agregar esta línea de código en una celda de código. Ejecutar código.   
from google.colab import files
uploaded = files.upload()  

2. Recordar importar Pandas para trabajar con los datos.   
import pandas as pd
import io

3. Importar datos desde su computador (para el ejercicio, en la carpeta “datos” que descargó).    
df = pd.read_csv(‘nombredearchivo, sep=';')  # ruta y nombre del archivo.  



## OPCIÓN B– Leer archivo alojado en tu Drive:   

1. Crear carpeta donde se dejarán los datos.   

2. Importar biblioteca drive para montar la unidad, y montar la unidad:   
`from google.colab import drive`
`drive.mount('/content/drive')`   

3. Confirmar la cuenta a acceder, aceptar acuerdo de confiabilidad. Ver confirmación:   
`Mounted at /content/drive`   

4. Buscar ubicación del archivo en carpetas Drive: menú barra lateral izquierda.     
`ruta content -> drive -> MyDrive...` 

5. Guardar ruta en variable:     
`dato = midato.read_csv('/content/drive/MyDrive/Colab Notebooks/NN_python/datos/losdatos.csv')`    

6. Recordar importar Pandas para trabajar con los datos.
`import pandas as pd` 
`import io`   

(Ojo que cada vez que trabajemos en los colabs, debemos subir los archivos de datos pues son temporales para la sesión, por lo tanto y se borran cuando se termina de trabajar)



<br>
**Para saber más de los Colab, pueden visitar esta página:
https://research.google.com/colaboratory/intl/es/faq.html** 



