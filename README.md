# Phantom OS 🚀

Herramienta de utilidad avanzada para MU Online enfocada en **rendimiento, estabilidad y capacidad Stealth**. Diseñada para darte una ventaja táctica absoluta sin comprometer la seguridad de tu cuenta.

---

## 📥 1. Descarga e Instalación

1. Ve a la sección de **[Releases](../../releases)** a la derecha de esta página (o en la pestaña superior).
2. Descarga el archivo **`Phantom-OS.exe`** de la versión más reciente.
3. No requiere instalación, simplemente guárdalo en una carpeta de tu preferencia.

> [!WARNING]
> Dado que Phantom OS inyecta instrucciones directamente en la memoria del juego para ser indetectable (evadiendo simuladores de teclado básicos), algunos Antivirus muy estrictos pueden marcarlo como falso positivo. Se recomienda añadir la carpeta donde lo guardaste a las exclusiones de tu Antivirus.

---

## 🔑 2. Activación (Sistema de Licencias)

Al abrir Phantom OS por primera vez, el sistema estará bloqueado. Phantom OS utiliza un sistema de seguridad avanzado atado al hardware de tu computadora (HWID) para evitar copias ilegales.

1. **Abre el programa**. Verás una pantalla roja solicitando una llave.
2. Copia el **Hardware ID** que se muestra en tu pantalla (ej. `A1B2-C3D4-E5F6-G7H8`).
3. Envía este código a tu administrador/vendedor.
4. Recibirás una **Llave de Activación** única.
5. Pégala en el programa y haz clic en **ACTIVAR Y ENTRAR**. Esta llave se guardará localmente y no volverá a pedírtela a menos que cambies de computadora.

---

## 💉 3. Ejecución e Inyección

1. Abre tu cliente de **MU Online** y entra al mundo con tu personaje.
2. Abre **`Phantom-OS.exe`**. Windows te mostrará una ventana de confirmación (UAC) pidiendo permisos de Administrador. Debes hacer clic en **"Sí"**. *(Vital para poder leer la memoria del juego)*.
3. En la pantalla principal, verás una lista de procesos activos. Selecciona tu cliente de MU (normalmente llamado `main.exe`) y haz clic en el botón **INYECTAR**.
   > En el recuadro negro de la derecha (consola de LOGS) verás el mensaje: *"Enganchando a PID..."* indicando éxito.

---

## 🛠️ 4. Guía de Funciones

### 👁️ Zoom Engine (Cámara Extendida)
Te permite alejar la cámara del juego a distancias masivas para tener control total de tu entorno, ver a los enemigos antes de que te vean, y cazar jefes fácilmente.

* **Aplicar Zoom:** Mueve el deslizador (Slider) entre los valores `1` (Normal) y `100` (Súper Lejos). Haz clic en **APLICAR**.
* **El botón mágico "MANTENER":** ¡Muy Recomendado! Cuando cruzas puertas (Warps), cambias de mapa, o tu personaje muere, el servidor de MU fuerza tu cámara a volver a la normalidad. Si activas **MANTENER**, Phantom OS re-aplicará automáticamente tu Zoom en segundo plano sin que tengas que hacer nada.

### 🧪 Motor Auto-Potas (Curación Automática)
Automatiza la curación a velocidades sobrehumanas durante los combates (PVP/PVE). A diferencia de otras herramientas, nuestro motor opera a nivel hardware (SendInput), engañando a LiveGuard y otros Anti-Cheats.

1. **Configurar Teclas:** Escribe las teclas que quieres usar separadas por coma. Ej: `Q, W, E`.
2. **Retraso (Delay):** Es la velocidad de curación. `0.20` equivale a presionar las teclas cada 200 milisegundos.
3. **Tecla ON/OFF:** Por defecto es **F4**. Puedes cambiarlo por la tecla que te resulte más cómoda para prender o apagar el spammer en medio de una pelea.
4. **Guardar:** ¡IMPORTANTE! Dale al botón **GUARDAR CONFIGURACIÓN**.
5. **Uso:** Presiona tu tecla de atajo en el juego. En los Logs leerás *"Auto-Potas ACTIVADO"*. Presiónalo de nuevo para apagarlo.

### ⚔️ Combos Cíclicos Dinámicos
Diseñado para clases como el Blade Knight (BK) que requieren una secuencia perfecta de habilidades. Es un sistema inteligente de ultra-baja latencia.

1. **Seleccionar Perfil:** Elige un combo de la lista desplegable (Ej: `BK (1-2-3)`).
2. **Editar Teclas (Opcional):** Puedes hacer clic en cualquiera de las teclas del combo (ej: borrar el `4` y poner un `3`) para alterar la secuencia de habilidades.
3. **Velocidad:** Ajusta qué tan rápido saltará de una habilidad a otra.
4. **Guardar:** Haz clic en **GUARDAR COMBO**.
5. **Uso Estratégico:** Enciende el Switch **ON/OFF** de la interfaz. Ahora, el combo se disparará **únicamente mientras mantengas presionada la tecla L-CTRL (Control Izquierdo)** de tu teclado. Esto te permite lanzar un combo y, al soltar la tecla, volver al control manual instantáneamente para reposicionarte. 

### 🎯 Rango Infinito (Range Hack)
Permite lanzar habilidades contra cualquier enemigo sin importar la distancia. Tu personaje podrá golpear desde el otro lado del mapa.

1. **Activar:** Enciende el Switch **ON/OFF** de la sección "Rango Infinito".
2. **Desactivar:** Apaga el Switch. Los bytes originales del juego se restaurarán al instante.
> [!CAUTION]
> Este módulo es agresivo e inyecta código de máquina directamente. Aunque es indetectable en memoria, los administradores podrían notar que atacas de muy lejos. **Úsalo bajo tu propio riesgo.**

---

## 👻 5. Modo Camuflaje (Ghost Mode)
Oculta el proceso para evadir escaneos y no ser capturado por tu software de grabación (OBS), Discord Streams o inspecciones manuales.

* **¿Cómo Funciona?** Arriba a la derecha encontrarás un ícono de Fantasma. Al presionarlo, podrás elegir un programa "Tapabedera" (ej: `Chrome.exe`, `Calculator.exe`).
* Phantom OS se auto-destruirá temporalmente, clonará el ícono y el nombre de ese programa, y se esconderá en tu bandeja de sistema haciéndose pasar por él.
* Ideal para jugadores que hacen directos o que son sometidos a "TeamViewer checks" por administradores de servidores competitivos.

---

## ❓ Solución de Problemas Comunes

* **"Las potas no se toman" / "El combo no dispara"**: Asegúrate de que le diste "Sí" a los permisos de Administrador al abrir Phantom OS, y de que la ventana del juego de MU Online está **seleccionada y activa** (en primer plano).
* **"El Zoom no funciona o crashea el juego"**: Asegúrate de haber inyectado el programa *después* de que tu personaje ya haya aparecido dentro del mapa del juego (viendo a tu personaje), **NUNCA** durante la pantalla de carga inicial o de selección de servidor.
* **"El programa se cierra al abrirlo"**: Asegúrate de que tu Antivirus no esté borrando los archivos temporales de ejecución. Agrega el `.exe` a exclusiones.
