## Frameworks CSS Modernos: Bootstrap y Tailwind CSS  
---

1. **"¿Cómo difieren las Component Classes y Utility Classes en su uso diario?"**  
   ##### Diferencia clave  
   > Las **Component Classes** agrupan estilos en clases predefinidas reutilizables (ej., `.btn-primary` en Bootstrap), mientras que las **Utility Classes** aplican estilos individuales directamente en el HTML (ej., `bg-blue-500` en Tailwind).  

2. **"¿Cuándo es más eficiente utilizar Component Classes en lugar de Utility Classes?"**  
   ##### Caso óptimo  
   > Cuando se necesita coherencia visual en múltiples elementos sin repetir muchas clases en el HTML, facilitando el mantenimiento del código.  

3. **"¿Cómo afecta el uso de Utility Classes a la legibilidad del código?"**  
   ##### Impacto  
   > Puede hacer que el HTML se vea más desordenado debido a la cantidad de clases aplicadas, pero evita la creación de archivos CSS adicionales, facilitando cambios rápidos.  

4. **"¿En qué tipos de proyectos prefieres usar Bootstrap? ¿Por qué?"**  
   ##### Preferencia  
   > En proyectos que requieren rapidez en el desarrollo y un diseño preestablecido, como páginas corporativas o dashboards, gracias a su sistema de componentes listos para usar.  

5. **"¿Cuáles son las ventajas principales de Tailwind CSS frente a otros frameworks?"**  
   ##### Beneficios  
   > - Mayor flexibilidad sin depender de estilos predefinidos.  
   > - Genera CSS optimizado al eliminar clases no utilizadas (purging).  
   > - Facilita la personalización sin necesidad de sobrescribir estilos.  

6. **"¿Cómo impacta la elección del framework en el tiempo de desarrollo?"**  
   ##### Eficiencia  
   > Bootstrap acelera el desarrollo inicial con componentes listos, mientras que Tailwind permite ajustes rápidos sin escribir CSS personalizado, reduciendo el tiempo de iteración.  

7. **"¿Por qué es esencial usar ramas en Git al trabajar en equipos?"**  
   ##### Importancia  
   > Permite a los desarrolladores trabajar en funciones o correcciones sin afectar la rama principal, asegurando estabilidad y colaboración eficiente.  

8. **"¿Cómo ayuda el uso de ramas a mantener la estabilidad del código principal?"**  
   ##### Beneficio  
   > Evita que cambios experimentales o con errores afecten el código en producción, permitiendo revisar y probar antes de fusionar a `main`.  

9. **"¿Qué desafíos has enfrentado al fusionar ramas y cómo los resolviste?"**  
   ##### Problema y solución  
   > Conflictos en archivos modificados por varios desarrolladores. Se resolvió revisando los cambios en cada versión y eligiendo manualmente la mejor combinación antes de confirmar la fusión.  
