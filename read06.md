### ¿Qué hacen los siguientes comandos?
- `pwd`
  > pwd imprime el directorio actual donde nos encontramos   
- `ls`
  > Esto mostrará una lista en horizontal con todos los ficheros y carpetas encontradas en la ruta indicada.
- `cd`
  > cd se utiliza para cambiar de directorio
- `mkdir`
  > Comando usado para crear una carpeta nueva
- `touch`
  > Comando usado para crear un archivo nuevo

### ¿Puedes explicar qué sucede en el siguiente escenario si ingresas estos comandos y argumentos en la línea de comandos? (Los argumentos son instrucciones adicionales dadas a un comando).
`cd projects`   Te mueves a la carpeta projects

`mkdir new-project`  Creas una carpeta en el directorio donde estas ubicado

`touch new-project/newfile.md` Creas un archivo en la carpeta indicada en la ruta , osea en new_project

`cd ..` Te mueves al directorio anterior

`ls projects/new-project` Enlistas el contenido de la carpeta indicada en la ruta , osea new-project

### ¿Qué comando usarías en la terminal para listar todos los archivos, incluidos los archivos ocultos, en un directorio de Linux o macOS? Explica qué significan los parámetros utilizados en el comando.
> La respuesta es `ls -la`  
>  ls : Lista los archivos y directorios en el directorio actual.  
>  -l : Muestra los detalles en formato de lista (permisos, propietario, tamaño, fecha de modificación, etc.).  
>  -a : Muestra todos los archivos, incluidos los ocultos (los que empiezan con . en Linux y macOS).  
 
 

**Prototipo no tendrá por ahora** 
 -  Recuperación de contraseña(Se quito)
Sobre la recuperación de contraseñas ,se mandara un mensaje del código al numero telefónico o a un Whattsap con el código correspondiente.



Diagrama de Flujo
Repositorio para el sistema




---
¡Excelente que lo menciones, Erick!
Veamos esto **con lupa** para encajarlo con tu nuevo backend **Node.js + Express**.

---

## ✅ **Tu contexto actual**

* Estás usando **Navigo** como **router del lado del cliente (Frontend SPA)**.
* Cada ruta:

  * Carga una vista HTML **(plantilla)**.
  * Ejecuta su **controlador JS** para traer datos o manejar eventos.
* Autenticación muy básica: `localStorage`.

Esto **es perfectamente válido para tu prototipo**, y **NO tienes que desecharlo**.
Navigo cubre **las rutas del cliente** (qué muestra cada página sin recargar todo).

---

## ✅ **Dónde entra Express entonces**

| **Navigo (Frontend)**                                    | **Express (Backend)**                                                                |
| -------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| Gestiona rutas de la SPA (qué HTML y qué JS renderizar). | Gestiona rutas API (`/api/usuarios`, `/api/mensajes`) para CRUD y lógica de negocio. |
| Nunca toca la base de datos directamente.                | Sí toca la base de datos MySQL.                                                      |
| Usa `fetch` o `AJAX` para pedir datos.                   | Devuelve JSON y responde a peticiones.                                               |

**Ejemplo:**

* Navigo abre `/comunicados` → llama a `view_comunicados` → `initComunicados()` → `fetch('/api/comunicados')` → Express responde con los comunicados desde la BD.

---

## ✅ **¿Debes cambiar Navigo?**

No.
Navigo funciona perfecto para tu SPA.
Solo asegúrate de que cada **controlador JS** use `fetch` para hablar con tu backend **Express**.

**Por ejemplo:**

```js
// Dentro de initComunicados()
async function initComunicados() {
  try {
    const res = await fetch('/api/comunicados');
    const data = await res.json();
    console.log(data);
    // Renderiza los comunicados en tu vista
  } catch (err) {
    console.error(err);
  }
}
```

---

## ✅ **Cómo se complementan**

| Parte              | Responsable         | Cómo funciona                                    |
| ------------------ | ------------------- | ------------------------------------------------ |
| **Navigo**         | SPA en el navegador | Cambia vistas dinámicamente sin recargar         |
| **Controlador JS** | SPA en el navegador | Llama a tu backend usando `fetch`                |
| **Express API**    | Node.js Backend     | Maneja `/api/*`, habla con MySQL y responde JSON |
| **Base de datos**  | MySQL               | Guarda todo                                      |

---

## ✅ **Entonces tu flujo final:**

1️⃣ Usuario navega: `/#/comunicados`
2️⃣ Navigo carga `view_comunicados`
3️⃣ `initComunicados()` hace `fetch('/api/comunicados')`
4️⃣ Express escucha en `/api/comunicados` → busca en MySQL → devuelve JSON
5️⃣ JS pinta los datos.

---

## ✅ **Conclusión**

* ✔️ **Navigo se queda** → NO cambies nada.
* ✔️ Tu backend **NO maneja rutas de vista**. Solo `/api/...` para datos.
* ✔️ `login.html` sigue manejado por el Front. El formulario de login ahora hace `fetch('/api/auth/login')` para verificar en la BD.
* ✔️ Todo calza: limpio, escalable y funcional para tu prototipo.

---

## ⚡ **¿Próximo paso?**

Puedo ayudarte a armar:
✅ Ejemplo de **ruta Express `/api/auth/login`**
✅ Ejemplo de **ruta `/api/comunicados`** con GET y POST.

¿Quieres que preparemos **`/api/auth/login`** ahora mismo para que conecte con tu tabla `usuarios`? 🚀✨



| **Sprint** | **Módulo**                    | **HU** | **Descripción** |
|-----------|--------------------------------|--------|----------------|
| **Sprint 1** | Autenticación y Perfiles     | HU1    | Inicio de sesión básico con usuario y contraseña |
|           |                                | HU2    | Acceso segmentado según el rol (Padre, Docente, Administrador) |
|           |                                | HU3    | Asignación de permisos a docentes por parte del director |
| **Sprint 2** | Asistencia y Calificaciones  | HU4    | Consulta de calificaciones por curso y bimestre |
|           |                                | HU5    | Consulta de asistencias con filtro por fecha o bimestre |
|           |                                | HU6    | Notificación por inasistencias consecutivas |
|           |                                | HU7    | Notificación de bajo rendimiento académico |
| **Sprint 3** | Comunicados y Avisos         | HU8    | Publicación de comunicados por directores/docentes autorizados |
|           |                                | HU9    | Visualización de comunicados segmentados |
|           |                                | HU10   | Gestión de comunicados (editar, eliminar, desactivar) |
| **Sprint 4** | Encuestas                    | HU11   | Creación de encuestas dinámicas |
|           |                                | HU12   | Responder encuestas asignadas |
|           |                                | HU13   | Reporte de resultados y análisis |
| **Sprint 5** | Mensajes y Consultas         | HU14   | Enviar y recibir mensajes entre docentes y padres |
|           |                                | HU15   | Responder consultas de manera estructurada |
|           |                                | HU16   | Supervisión de historial de mensajes por el director |
| **Sprint 6** | Soporte Técnico y Ayuda      | HU17   | Consultar preguntas frecuentes del sistema |
|           |                                | HU18   | Crear solicitud de soporte técnico |
|           |                                | HU19   | Ver estado y detalle de solicitudes enviadas |


