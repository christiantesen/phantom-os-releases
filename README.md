# Phantom OS 

Bienvenido a **Phantom OS**, una herramienta de utilidad avanzada para MU Online enfocada en rendimiento, estabilidad y capacidad de evasión (stealth). Este manual explica paso a paso cómo descargar, inyectar y configurar tu herramienta.

## 📥 Descarga e Instalación

1. Ve a la pestaña de **[Releases](../../releases)** a la derecha de esta página.
2. Descarga el archivo **`Phantom OS.exe`** de la versión más reciente.
3. No requiere instalación, simplemente guárdalo en una carpeta de tu preferencia.

---

## 1. Ejecución e Inyección

1. **Abre el Programa:** Haz doble clic en `Phantom OS.exe`.
2. **Concede Permisos:** Windows te mostrará una ventana de confirmación (UAC) pidiendo permisos de Administrador. Debes hacer clic en **"Sí"**. *Si no le das permisos, el programa no podrá leer la memoria del juego.*
3. **Selecciona tu Cliente:** En la pantalla principal, verás una lista de procesos activos. Ubica el que diga `main.exe` o el nombre de tu cliente de MU, selecciónalo haciendo clic en él, y presiona el botón **INYECTAR**.
   > En el recuadro negro de la derecha (consola de LOGS) verás el mensaje: *"Enganchando a PID..."*

---

## 2. Herramientas y Módulos

### 👁️ Zoom Engine (Cámara Extendida)
Te permite alejar la cámara del juego a distancias masivas para tener control total de tu entorno.

* **Aplicar Zoom:** Mueve el deslizador (Slider) entre los valores `1` (Normal) y `100` (Súper Lejos). Haz clic en **APLICAR**.
* **El botón mágico "MANTENER":** ¡Muy Recomendado! Cuando cruzas puertas (Warps), cambias de mapa, o tu personaje muere, el servidor de MU fuerza tu cámara a volver a la normalidad. Si presionas **MANTENER**, Phantom OS re-aplicará automáticamente tu Zoom configurado cada segundo en segundo plano sin que tengas que hacer nada.

### 🧪 Motor Auto-Potas (Curación Automática)
Automatiza la presión de teclas (generalmente Q, W, E) para curarte a velocidades sobrehumanas durante los combates (PVP/PVE).

1. **Configurar Teclas:** Escribe las teclas que quieres usar separadas por coma. Ej: `Q, W, E`.
2. **Configurar Retraso (Delay):** Es la velocidad de curación. `0.20` equivale a presionar las teclas cada 200 milisegundos.
3. **Tecla ON/OFF:** Por defecto es **F4**. Puedes cambiarlo por la tecla que te resulte más cómoda para prender o apagar el spammer.
4. **Guardar:** ¡IMPORTANTE! Dale al botón **GUARDAR CONFIGURACIÓN**.
5. **Uso en el juego:** Presiona tu tecla de atajo (`F4`). En la ventana de Logs leerás *"Auto-Potas ACTIVADO"*. Presiónalo de nuevo para apagarlo.

### ⚔️ Combos Cíclicos Dinámicos
Diseñado para clases como el Blade Knight (BK) que requieren una secuencia perfecta de habilidades.

1. **Seleccionar Perfil:** Elige un combo de la lista desplegable (Ej: `BK (1-2-3)`).
2. **Editar Teclas (Opcional):** Puedes hacer clic en cualquiera de las teclas del combo (ej: borrar el `4` y poner un `3`) para alterar la secuencia de habilidades.
3. **Velocidad (Delay Base):** Ajusta qué tan rápido saltará de una habilidad a otra.
4. **Guardar:** Haz clic en **GUARDAR COMBO**.
5. **Uso en el juego:** Enciende el Switch **ON/OFF** de la interfaz. Ahora, el combo se disparará **únicamente mientras mantengas presionada la tecla L-CTRL (Control Izquierdo)** de tu teclado. Esto te permite lanzar un combo y, al soltar la tecla, volver al control manual instantáneamente para reposicionarte. Si no vas a usar el combo un rato, puedes simplemente apagar el switch.

---

## 3. Seguridad Adicional (Stealth)

### 👻 Modo Camuflaje (Ghost Mode)
Arriba a la derecha encontrarás un ícono de Fantasma. Esto sirve para ocultar a Phantom OS de las capturas de pantalla o sistemas de stream.
* **Activar:** Haz clic en el botón. Selecciona cualquier otro programa que tengas abierto (por ejemplo, *Calculadora* o *Google Chrome*). Phantom OS copiará su ícono y su nombre en la barra de tareas de Windows.
* **¿Por qué usarlo?:** Evita que espectadores en un stream (como OBS) o administradores del juego vean que tienes la herramienta abierta.

---

### Solución de Problemas Comunes

* **"Las potas no se toman" / "El combo no dispara"**: Asegúrate de que iniciaste el ejecutable dando "Sí" a los permisos de Administrador, y de que la ventana del juego de MU Online está **seleccionada y activa** (en primer plano) en Windows.
* **"El Zoom no funciona"**: Asegúrate de haber inyectado el programa *después* de que tu personaje ya haya aparecido dentro del mapa del juego, no durante la pantalla de carga.
