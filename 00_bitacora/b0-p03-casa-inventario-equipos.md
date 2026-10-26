# b0-0.1 · Metodología y estructura

- **Alumno:** Lucas Chico
    
- **Bloque:** B0 — Prerrequisitos
    
- **Fase / ejercicio:** Fase 0.8 (Práctica 03-Casa: Inventario de equipos)
    
- **Fecha de inicio:** 26/10/2026
    
- **Fecha de entrega:** 26/10/2026
    

### 🎯 Qué se pedía

Crear un inventario de equipos desde cero en una nueva bóveda local (`Boveda_Inventario_Casa`) y un repositorio remoto (`sor-inventario-equipos-casa`), gestionando el ciclo completo con tres versiones de producto y un cuarto commit documental posterior con la bitácora cerrada, asegurando el aislamiento frente a OneDrive y otros contextos del centro.

### ⌨️ Comandos y pasos importantes

- `git --version` — Para comprobar la versión instalada de Git.
    
- `git config --global user.name` — Para verificar el nombre global del autor configurado.
    
- `git config --global user.email` — Para verificar el correo configurado para Git.
    
- `ls -l ~/.ssh/id_ed25519 ~/.ssh/id_ed25519.pub` — Para comprobar la existencia de las claves SSH privada y pública sin mostrarlas.
    
- `ssh -T git@github.com` — Para probar la autenticación SSH con GitHub y verificar el saludo del usuario.
    
- `pwd` — Para comprobar en todo momento la ruta absoluta y asegurarse de estar trabajando dentro de `01_Proyecto`.
    
- `git init` — Para inicializar el repositorio Git local exclusivamente en `01_Proyecto`.
    
- `git branch -M main` — Para fijar y forzar `main` como el nombre de la rama principal.
    
- `git status` — Para consultar el estado actual del repositorio, los archivos nuevos sin seguimiento o los cambios pendientes.
    
- `git remote add origin ...` — Para registrar la URL remota SSH del repositorio en GitHub.
    
- `git remote -v` — Para mostrar y confirmar las URLs de consulta y envío del remoto.
    
- `git add <archivo>` — Para preparar selectivamente archivos específicos hacia el índice (staging area).
    
- `git diff` — Para comparar los cambios en el disco con el índice actual.
    
- `git diff --cached` — Para revisar los archivos y cambios que ya han sido preparados con `add` antes de guardarlos.
    
- `git commit -m "Mensaje"` — Para guardar una nueva versión local del producto con un mensaje descriptivo.
    
- `git push` / `git push -u origin main` — Para enviar los commits al repositorio remoto en GitHub.
    
- `git check-ignore -v <recurso>` — Para identificar la regla exacta de exclusión de `.gitignore` para un archivo local.
    
- `git log --oneline` — Para visualizar el historial resumido de commits del repositorio.
    
- `git switch --detach <codigo>` — Para viajar temporalmente en el historial y consultar un commit antiguo sin alterar la rama.
    
- `git switch main` — Para regresar de forma segura a la rama principal del proyecto.
    

### 🛠️ Qué he hecho

1. **Aislamiento y preparación inicial:** Elegí una ubicación local completamente independiente, fuera de OneDrive y ajena a cualquier árbol de carpetas del centro o de la fase anterior (`Boveda_SOR`).
    
2. **Comprobación de entorno:** Ejecuté las validaciones de Git, identidad y autenticación SSH para asegurar que todo funcionaba correctamente antes de empezar.
    
3. **Creación de la bóveda y estructura:** Creé la bóveda `Boveda_Inventario_Casa` en Obsidian y configuré exclusivamente las carpetas iniciales requeridas (`00_Grabaciones/` y `01_Proyecto/00_Bitacora/` junto con `inventario/`).
    
4. **Archivos iniciales y exclusiones:** Redacté el fichero `.gitignore` para excluir vídeos y archivos auxiliares del sistema, creé el `README.md`, la bitácora inicial de notas y el fichero de datos inicial `inventario/equipos.csv` con dos equipos (`EQ01` y `EQ02`).
    
5. **Versión 1:** Inicialicé Git en `01_Proyecto`, creé el repositorio vacío en GitHub (`sor-inventario-equipos-casa`), enlacé el remoto por SSH, preparé de forma individual los archivos iniciales, revisé el `diff --cached`, realicé el primer commit ("_Crear inventario inicial de equipos_") y subí los cambios a `main` con éxito.
    
6. **Versión 2:** Modifiqué el archivo `inventario/equipos.csv` actualizando la ubicación de `EQ01` a `Aula-3` y el estado de `EQ02` a `mantenimiento`. Comprobé los cambios con `git diff`, preparé el archivo, creé el segundo commit ("_Actualizar ubicacion y estado de equipos_") y ejecuté el `push`.
    
7. **Ampliación (Versión 3):** Creé las carpetas de ampliación (`mantenimiento/`, `imagenes/` y `videos/`), añadí la ficha de mantenimiento `EQ02.md`, el archivo de criterios de estado, la imagen del equipo (`equipo.png`), añadí una tercera fila al CSV (`EQ03`) y actualicé el `README.md` con sus enlaces correspondientes. Asimismo, añadí dos clips de vídeo locales de prueba (`revision-01.mp4` y `revision-02.mp4`) para comprobar que el archivo `.gitignore` los ocultaba y mantenía ignorados correctamente. Preparé de forma individual cada archivo nuevo o modificado, validé el contenido con `git diff --cached`, realicé el tercer commit ("_Ampliar inventario y documentar mantenimiento_") y lo subí al remoto.
    
8. **Consulta histórica:** Tras dejar el árbol limpio, utilicé `git switch --detach` con el código del primer commit para viajar en el tiempo y comprobar que los datos del CSV y el estado del proyecto correspondían exactamente a la primera entrega, regresando posteriormente a `main` de forma limpia.
    
9. **Cierre y entrega:** Detuve la grabación de OBS, guardé el vídeo resultante en `00_Grabaciones/` (fuera de control de versiones), lo subí a YouTube como "No listado" en la playlist correspondiente e inserte las nueve marcas de tiempo reales en su descripción. Por último, completé los apartados de la bitácora con los enlaces definitivos, preparé el archivo mediante un cuarto commit documental ("_Completar bitacora y enlace del video de casa_") y realicé el último `push` antes de entregar en Teams.
    

### 🚩 Qué me ha fallado y cómo lo he resuelto

- **Error / Problema:** Durante la comprobación del estado con `git status` tras añadir los clips de vídeo de prueba en `inventario/videos/`, aparecieron momentáneamente como archivos sin seguimiento debido a un error tipográfico menor en las extensiones configuradas en el archivo `.gitignore`.
    
- **Resolución:** Revisé la sintaxis del `.gitignore`, corregí los patrones de exclusión para que coincidieran exactamente con los ficheros `.mp4` y comprobé mediante `git check-ignore -v` que la regla de exclusión volvía a aplicarse correctamente sobre los vídeos locales antes de continuar con la preparación de los ficheros de la ampliación.
    

### 🤔 Respuestas a las preguntas

1. **¿Por qué el repositorio está en `01_Proyecto` y no en la raíz de la bóveda?**
    
    Porque la bóveda de Obsidian contiene tanto los elementos de trabajo y proyectos como las grabaciones en vídeo y apuntes personales. Al aislar Git únicamente en `01_Proyecto`, evitamos que archivos grandes, grabaciones o metadatos internos del editor afecten al control de versiones del proyecto técnico.
    
2. **¿Qué dos celdas de datos cambiaste en la segunda versión y cómo se ven en diff?**
    
    Cambié la ubicación de `EQ01` de `Aula-1` a `Aula-3` y el estado de `EQ02` de `disponible` a `mantenimiento`. En el resultado de `git diff` se visualizan con un prefijo `-` las líneas originales retiradas y con un prefijo `+` las nuevas líneas incorporadas con los valores modificados.
    
3. **¿Qué diferencia hay entre editar una fila y preparar ese cambio con add?**
    
    Editar una fila modifica únicamente el archivo físico en el disco duro (trabajo local en el editor), mientras que ejecutar `git add` toma una "fotografía" de ese estado actual y lo traslada al índice (staging area) preparándolo para ser incluido en el próximo commit.
    
4. **¿Por qué la ficha nueva aparece en status y no en el diff de equipos.csv?**
    
    Porque `git status` informa de todos los archivos nuevos o modificados en el directorio de trabajo (incluyendo los ficheros nuevos sin seguimiento), mientras que `git diff` compara únicamente las modificaciones internas de archivos ya conocidos y seguidos, como `equipos.csv`, sin auditar ficheros independientes o recientes.
    
5. **¿Qué archivos preparaste individualmente en la ampliación y qué mostró diff --cached?**
    
    Preparé individualmente `inventario/mantenimiento/EQ02.md`, `inventario/criterios-estados.md`, `inventario/imagenes/equipo.png`, `inventario/equipos.csv` y `README.md`. El comando `git diff --cached` mostró un resumen estadístico y el contenido textual preparado de dichos cambios listos para ser consolidados en el commit.
    
6. **¿Cómo demostraste que los clips existen y están ignorados sin subirlos?**
    
    Mediante la ejecución de `git status` (donde se comprueba que no aparecen listados para subirse) y el comando `git check-ignore -v inventario/videos/revision-01.mp4 inventario/videos/revision-02.mp4`, el cual identificó explícitamente la regla del fichero `.gitignore` que los excluye, confirmando simultáneamente su existencia física en el explorador de archivos local.
    
7. **¿Qué ubicación y estado recuperaste al visitar el primer commit y qué ocurrió con EQ03?**
    
    Al situarme en modo detached sobre el primer commit, el inventario recuperó los valores originales donde `EQ01` figuraba en `Aula-1`, `EQ02` estaba `disponible` y el equipo `EQ03` no existía todavía al ser posterior a dicha versión histórica.
    
8. **¿Por qué este CSV necesita historial y qué limitaciones tiene frente a un inventario multiusuario real?**
    
    Necesita historial para auditar qué cambios se produjeron, quién los hizo y por qué motivos entre entrega y entrega. Sus limitaciones frente a un sistema real radican en que carece de bloqueos concurrentes, validación estricta de tipos de datos, control de permisos por roles y soporte para edición multiusuario simultánea en tiempo real.
    
9. **¿Cómo comprobaste la subida de la bitácora y por qué su cierre ocurre después del vídeo?**
    
    Comprobé la subida abriendo directamente la bitácora en la interfaz web de GitHub para verificar que los enlaces y respuestas eran correctos. Su cierre ocurre después de la grabación porque la bitácora documenta el proceso completo y contiene los enlaces definitivos del propio vídeo ya subido, constituyendo un registro documental posterior y no un elemento que deba aparecer grabado en la fase interactiva.
    

### 🔗 Enlaces

- **Vídeo de esta fase:** [https://youtu.be/IFqzCpi1IUU](https://youtu.be/IFqzCpi1IUU)
    
- **Playlist:** [https://www.youtube.com/playlist?list=PLeat0BY5EEl4](https://www.youtube.com/playlist?list=PLeat0BY5EEl4)
    
- **Repositorio en GitHub:** [Enlace a sor-inventario-equipos-casa]
    

### 💭 Dudas / a repasar

- Ninguna duda significativa; el flujo completo de aislamiento, gestión de ramas, commits selectivos e historiales detached ha quedado comprendido con claridad en este entorno de casa.