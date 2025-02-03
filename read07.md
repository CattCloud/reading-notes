### ¿Qué es el control de versiones?
> El control de versiones es un sistema que registra los cambios realizados en un archivo o conjunto de archivos a lo largo del tiempo, permitiendo recuperar versiones anteriores y colaborar eficientemente en proyectos de software.  

### ¿Qué es “clone” en Git?
> En Git, `clone` es un comando que se usa para crear una copia exacta de un repositorio remoto en tu máquina local. Esto permite trabajar con el código sin afectar el repositorio original hasta que se realicen cambios y se suban nuevamente.  

### ¿Cuál es el comando para agregar los archivos modificados a la zona de preparación?
> El comando es `git add <archivo>` o `git add .`  
> - `git add <archivo>`: Agrega un archivo específico a la zona de preparación.  
> - `git add .`: Agrega todos los archivos modificados en el directorio actual a la zona de preparación.  

### ¿Cuál es el comando para enviar la captura de los archivos modificados a GitHub?
> Primero, se debe confirmar los cambios con `git commit -m "Mensaje del commit"` y luego enviarlos con `git push origin <rama>`.  
> - `git commit -m "Mensaje del commit"`: Guarda los cambios en la historia del repositorio con un mensaje descriptivo.  
> - `git push origin <rama>`: Envía los cambios confirmados al repositorio remoto en la rama especificada.  

