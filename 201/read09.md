## Mitos y Verdades sobre el DOM como API de Objetos  
---

1. **“Usar querySelector() siempre devuelve una colección de nodos, incluso si selecciona uno solo.”**  
   ##### ❌ Mito  
   > `querySelector()` siempre devuelve el primer nodo que coincide con el selector. No devuelve una colección, incluso si la selección incluye un único nodo.

2. **“El DOM permite manipular estilos CSS directamente desde JavaScript usando propiedades específicas como .style y .classList.”**  
   ##### ✅ Verdad  
   > Es posible cambiar estilos de elementos en el DOM directamente a través de `.style` para estilos inline, o administrar clases CSS dinámicamente con `.classList`.

3. **“Una expresión regular (Regex) siempre devolverá el mismo resultado sin importar el contexto o idioma del texto que analice.”**  
   ##### ❌ Mito  
   > El comportamiento de las expresiones regulares puede variar dependiendo del motor que las interprete y si considera características específicas del idioma, como conjuntos de caracteres Unicode.

4. **“Utilizar querySelectorAll() es menos eficiente que getElementById cuando se busca un único elemento por su ID.”**  
   ##### ✅ Verdad  
   > `getElementById` es más rápido y eficiente para buscar elementos por ID porque está optimizado específicamente para este propósito. `querySelectorAll` tiene que procesar el selector, lo que lo hace más lento.

5. **“Todos los métodos del DOM devuelven elementos del mismo tipo, no existen diferencias entre ellos.”**  
   ##### ❌ Mito  
   > Los métodos del DOM como `getElementById` devuelven un único nodo, mientras que otros como `querySelectorAll` devuelven listas estáticas. Los tipos devueltos dependen del método utilizado.

6. **“querySelectorAll() permite seleccionar múltiples elementos y devuelve una lista estática (no viva) de nodos.”**  
   ##### ✅ Verdad  
   > `querySelectorAll` devuelve una lista estática que no se actualiza automáticamente si el DOM cambia después de la selección.

7. **“Las expresiones regulares (Regex) se pueden utilizar para transformar contenido de texto (Markdown a HTML, por ejemplo) sin necesidad de librerías externas.”**  
   ##### ✅ Verdad  
   > Aunque no es trivial, las expresiones regulares pueden usarse para realizar transformaciones de texto complejas como pasar de Markdown a HTML, pero el uso de librerías externas puede simplificar este proceso.

8. **“Los cambios realizados en los nodos del DOM usando JavaScript son permanentes incluso después de refrescar la página.”**  
   ##### ❌ Mito  
   > Los cambios realizados en el DOM son temporales y desaparecen tras un refresco de la página, ya que el DOM se reconstruye a partir del HTML original cargado.
