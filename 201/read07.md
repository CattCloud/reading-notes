## Mitos y Verdades: Programación Orientada a Objetos (POO) con Funciones Constructoras en JavaScript  
---  

1. **“Todos los lenguajes orientados a objetos soportan herencia múltiple por defecto.”**  
   ##### ❌ Mito  
   > No todos los lenguajes permiten herencia múltiple. JavaScript, por ejemplo, usa prototipos y delegación en lugar de herencia múltiple directa.  

2. **“La Programación Orientada a Objetos permite organizar el código en entidades con responsabilidad clara.”**  
   ##### ✅ Verdad  
   > POO ayuda a estructurar el código en clases u objetos, facilitando la separación de responsabilidades y el mantenimiento.  

3. **“En JavaScript, usar funciones constructoras es obsoleto porque existen las clases desde ES6.”**  
   ##### ❌ Mito  
   > Aunque las clases de ES6 son más intuitivas, las funciones constructoras siguen siendo válidas y funcionales en JavaScript.  

4. **“La abstracción implica eliminar cualquier detalle que no sea importante para la funcionalidad principal.”**  
   ##### ✅ Verdad  
   > La abstracción oculta detalles innecesarios y expone solo lo esencial, simplificando la complejidad del sistema.  

5. **“Para crear objetos usando funciones constructoras, es obligatorio usar el prototipo explícitamente.”**  
   ##### ❌ Mito  
   > No es obligatorio, pero usar el prototipo mejora la eficiencia al compartir métodos entre instancias en lugar de duplicarlos en cada objeto.  

6. **“La POO promueve la escalabilidad al agrupar datos y comportamiento en entidades lógicas.”**  
   ##### ✅ Verdad  
   > Al encapsular datos y lógica en objetos, POO facilita la escalabilidad y el mantenimiento del código.  

7. **“La palabra clave this en las funciones constructoras apunta a un objeto global, sin importar si se usa new.”**  
   ##### ❌ Mito  
   > Si se usa `new`, `this` apunta al nuevo objeto creado; sin `new`, puede referirse al objeto global (o `undefined` en modo estricto).
