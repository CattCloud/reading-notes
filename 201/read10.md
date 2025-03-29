
## Quizz Funciones y Callbacks en JavaScript 
---

### 1. **Funciones como valores**  
##### ✅ Ventaja  
> Tratar a las funciones como valores en JavaScript permite pasarlas como argumentos, retornarlas desde otras funciones y almacenarlas en variables u objetos. Esto facilita la reutilización y la programación funcional.  

##### ❌ Dificultad  
> Puede generar código difícil de depurar cuando se anidan muchas funciones o cuando se pasan funciones anónimas sin nombres claros, dificultando la identificación de errores en la pila de ejecución.  

---

### 2. **Uso de Callbacks**  
##### ✅ Cuándo usar callbacks  
> Son útiles cuando una operación es asíncrona (como solicitudes HTTP o temporizadores) y queremos ejecutar una función solo cuando la tarea finaliza.  

##### ❌ Impacto en la legibilidad  
> Un uso excesivo de callbacks puede hacer que el código sea difícil de seguir, especialmente si hay muchas funciones anidadas sin una estructura clara.  

---

### 3. **Callback Hell**  
##### ❌ Problema  
> El uso excesivo de callbacks puede generar código difícil de entender y mantener, con muchas funciones anidadas en distintos niveles, lo que se conoce como *Callback Hell*.  

##### ✅ Alternativas  
> - **Promises:** Permiten encadenar operaciones de forma más legible con `.then()`.  
> - **Async/Await:** Hace que el código asíncrono se vea más secuencial y fácil de entender.  

---

### 4. **Funciones de Orden Superior en la Práctica**  
##### ✅ Beneficio  
> Permiten escribir código más modular y reutilizable al aceptar funciones como argumentos o devolver nuevas funciones.  

##### 🎯 Ejemplo  
> En un array de productos, en lugar de escribir bucles manualmente, se puede usar `.map()` para transformar datos de manera más limpia:  

```js
const precios = [10, 20, 30];
const conIVA = precios.map(precio => precio * 1.18); // Agrega 18% de IVA
console.log(conIVA); // [11.8, 23.6, 35.4]
```

---

### 5. **Eficiencia y Performance**  
##### ❌ Impacto en rendimiento  
> El uso excesivo de funciones de orden superior y callbacks puede afectar el rendimiento si se ejecutan en grandes volúmenes de datos debido a la sobrecarga de llamadas de funciones.  

##### ✅ Cuándo evitarlas  
> En operaciones críticas de alto rendimiento, como algoritmos intensivos o manipulación de grandes volúmenes de datos, donde un bucle simple puede ser más eficiente.  

---

### 6. **Aplicación en el Editor de Markdown**  
##### ✅ Uso de funciones de orden superior  
> Se pueden usar para modularizar la lógica de formato, como la función `toggleFormat(texto)`, que recibe un texto y decide si aplicar negrita o cursiva.  

##### 🔍 Ejemplo en el código  
> La función `toggleFormat()` actúa como una función de orden superior al recibir y procesar un callback que decide el formato a aplicar.  

```js
function toggleFormat(text, formatFn) {
    return formatFn(text);
}

// Uso con una función para aplicar negrita
const applyBold = text => `**${text}**`;
console.log(toggleFormat("Hola", applyBold)); // **Hola**
```

---

Este formato te da claridad y estructura. ¿Te parece bien así? 😊
