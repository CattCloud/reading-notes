## Mitos y Verdades sobre Prototipos en JavaScript  
---  

1. **“El `prototype` de una función y el `__proto__` de un objeto son exactamente lo mismo.”**  
   ##### ❌ Mito  
   > Aunque están relacionados, no son lo mismo. `prototype` es una propiedad de las funciones constructoras, mientras que `__proto__` es la referencia al prototipo de un objeto.  

2. **“La cadena de prototipos permite la reutilización de métodos y propiedades, lo cual es esencial para la herencia en JavaScript.”**  
   ##### ✅ Verdad  
   > La cadena de prototipos permite que los objetos hereden propiedades y métodos, evitando la duplicación de código y mejorando la eficiencia.  

3. **“Las funciones constructoras son obsoletas y no se usan en el desarrollo moderno de JavaScript.”**  
   ##### ❌ Mito  
   > Aunque las clases de ES6 son más comunes hoy en día, las funciones constructoras siguen siendo funcionales y utilizadas en ciertos contextos.  

4. **“Manipular correctamente `__proto__` puede mejorar la reutilización de código, pero su uso inadecuado puede generar problemas de seguridad y mantenimiento.”**  
   ##### ✅ Verdad  
   > Modificar `__proto__` manualmente puede ser útil, pero hacerlo de manera incorrecta puede generar errores difíciles de depurar y problemas de rendimiento.  

5. **“Modificar el `prototype` de una función siempre afecta a todas las instancias existentes sin excepción.”**  
   ##### ❌ Mito  
   > Si se modifica el `prototype` antes de crear instancias, estas heredarán los cambios, pero las instancias previas conservarán el prototipo original a menos que se modifiquen explícitamente.
