## Programación Funcional en JavaScript  
---  

1. **Diferencias entre programación imperativa y funcional**    
   > La programación imperativa se centra en el "cómo" resolver un problema, detallando los pasos a seguir, mientras que la programación funcional se enfoca en el "qué", utilizando funciones y evitando cambios de estado.

2. **Ventajas y desventajas de las funciones puras**  
   > Son ideales para cálculos y transformaciones de datos, ya que garantizan predictibilidad y reutilización. No son convenientes cuando se necesita manipular el DOM o realizar operaciones asíncronas con efectos secundarios.

3. **Rol de map(), filter() y find() en la calidad del código**  
   > Estas funciones de orden superior mejoran la legibilidad y reducen el uso de bucles, permitiendo escribir código más declarativo y fácil de mantener.

4. **Facilitación de pruebas unitarias y debugging en programación funcional**  
   > Las funciones puras hacen que las pruebas sean más sencillas, ya que siempre producen el mismo resultado para los mismos parámetros, eliminando la incertidumbre causada por estados mutables.

5. **Integración del paradigma funcional en proyectos imperativos**  
   > Se puede adoptar gradualmente refactorizando funciones para hacerlas más puras, utilizando inmutabilidad y reemplazando estructuras imperativas con funciones como map(), reduce() y filter().
