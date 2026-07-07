# Phantom OS - User Guide

Bienvenido a **Phantom OS**. Este manual explica paso a paso cómo inyectar y configurar tu herramienta para dominar MU Online.

---

## 1. Ejecución e Inyección

1. **Abre el Programa:** Haz doble clic en `Phantom OS.exe`.
2. **Concede Permisos:** Windows te mostrará una ventana de confirmación (UAC) pidiendo permisos de Administrador. Debes hacer clic en **"Sí"**. *Si no le das permisos, el programa no podrá leer la memoria del juego.*
3. **Selecciona tu Cliente:** En la pantalla principal, verás una lista de procesos. Ubica el que diga `main.exe` o el nombre de tu cliente de MU, selecciónalo haciendo clic en él, y presiona el botón **INYECTAR**.
   > En el recuadro negro de la derecha (consola de LOGS) verás el mensaje: *"Enganchando a PID..."*

---

## 2. Herramientas y Módulos

### 👁️ Zoom Engine (Cámara Extendida)
Te permite alejar la cámara del juego a distancias masivas para tener control total de tu entorno.

* **Aplicar Zoom:** Mueve el deslizador (Slider) entre los valores `1` (Normal) y `100` (Súper Lejos). Haz clic en **APLICAR**.
* **El botón mágico "MANTENER":** ¡Recomendado! Cuando cruzas puertas (Warps), cambias de mapa, o tu personaje muere, el servidor de MU fuerza tu cámara a volver a la normalidad. Si presionas **MANTENER**, Phantom OS re-aplicará automáticamente tu Zoom configurado cada segundo en segundo plano sin que tengas que hacer nada.

### 🧪 Motor Auto-Potas (Curación Automática)
Automatiza la presión de teclas (generalmente Q, W, E) para curarte a velocidades sobrehumanas durante los combates (PVP/PVE).

1. **Configurar Teclas:** Escribe las teclas que quieres usar separadas por coma. Ej: `Q, W, E`.
2. **Configurar Retraso (Delay):** Es la velocidad de curación. `0.20` equivale a presionar las teclas cada 200 milisegundos.
3. **Atajo de Encendido:** Por defecto es **F4**. Puedes cambiarlo por la tecla que te resulte más cómoda.
4. **Guardar:** ¡IMPORTANTE! Dale al botón **GUARDAR CONFIGURACIÓN**.
5. **Uso en el juego:** Presiona tu tecla de atajo (`F4`). En la ventana de Logs leerás *"Auto-Potas ACTIVADO"*. Presiónalo de nuevo para apagarlo.

### ⚔️ Combos Cíclicos Dinámicos
Diseñado para clases como el Blade Knight (BK) que requieren una secuencia perfecta de habilidades.

1. **Seleccionar Perfil:** Elige un combo de la lista desplegable (Ej: `BK (1-2-3)`).
2. **Velocidad (Delay Base):** Ajusta qué tan rápido saltará de una habilidad a otra.
3. **Guardar:** Haz clic en **GUARDAR COMBO**.
4. **Uso en el juego:** Este sistema es **Dinámico**. No hay botón de encendido. El combo se dispara **únicamente mientras mantengas presionada la tecla L-CTRL (Control Izquierdo)** de tu teclado. Esto te permite lanzar un combo y, al soltar la tecla, volver al control manual instantáneamente para reposicionarte.

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
