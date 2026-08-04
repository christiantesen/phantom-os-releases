# 📖 Guía de Usuario Completa - Phantom OS

Bienvenido al manual oficial de **Phantom OS**. Esta guía está diseñada para que entiendas visualmente y paso a paso cómo operar cada módulo de la herramienta, garantizando que le saques el máximo provecho de forma segura.

---

## 1. Flujo de Activación (Primer Ingreso)

Phantom OS utiliza un sistema de **Hardware ID (HWID)**. Esto significa que el programa se fusiona con los componentes físicos de tu PC y no puede ser usado por nadie más.

```mermaid
graph TD
    A(["Abrir Phantom-OS.exe"]) --> B{"¿Es la primera vez?"}
    B -- Sí --> C["Pantalla de Bloqueo HWID"]
    B -- No --> H(["Pantalla Principal del Cheat"])
    
    C --> D["Copiar código HWID de tu pantalla"]
    D --> E("Enviar HWID al Administrador")
    E --> F["Recibir tu Llave de Activación Única"]
    F --> G["Pegar Llave y Activar"]
    G --> H
```

**⚠️ Importante:** Si formateas tu PC o cambias tu Placa Base/Disco Duro, tu HWID cambiará y deberás solicitar una llave nueva.

---

## 2. Flujo de Inyección (Conexión al Juego)

Para que Phantom OS pueda operar, necesita "engancharse" a la memoria de MU Online. **Debe hacerse en un orden estricto para evitar bloqueos del Anti-Cheat.**

```mermaid
flowchart LR
    1["1. Entrar a MU Online"] --> 2["2. Logear personaje en el mapa"]
    2 --> 3["3. Abrir Phantom OS como Administrador"]
    3 --> 4["4. Seleccionar main.exe en la lista"]
    4 --> 5(["5. Clic en INYECTAR"])
```

* **No inyectes durante la pantalla de carga.** Siempre espera a estar dentro del mapa y ver a tu personaje.
* Si no corres Phantom OS como Administrador (clic derecho > Ejecutar como Administrador), el recuadro de LOGS te arrojará un error de "Acceso Denegado".

---

## 3. Módulo: Zoom Engine 👁️

El Zoom de Phantom OS no modifica archivos del cliente; altera la renderización 3D en la memoria RAM en tiempo real.

```mermaid
sequenceDiagram
    participant U as Usuario
    participant P as Phantom OS
    participant M as MU Online
    
    U->>P: Ajusta el Slider a 70
    U->>P: Clic en 'APLICAR'
    P->>M: Sobrescribe la matriz de cámara 3D
    M-->>U: La cámara se aleja inmediatamente
    
    note over U,M: Al cruzar un Warp (Puerta), el servidor reinicia la cámara.
    
    U->>P: Clic en botón 'MANTENER'
    loop Cada 1 Segundo
        P->>M: Inyecta el valor '70' silenciosamente
    end
```

---

## 4. Módulo: Auto-Potas y Combos (Mecánica Hardware) ⚔️

Phantom OS no usa funciones simuladas que los Anti-Cheats detectan fácilmente. En su lugar, envía pulsaciones directamente al controlador de tu teclado (SendInput).

### ¿Cómo usar el Combo Inteligente?
El combo no dispara a lo loco. Está diseñado para PvP táctico (como jugar con un Blade Knight).

```mermaid
stateDiagram-v2
    [*] --> Reposo
    Reposo --> Disparando : Mantener presionada L-CTRL
    Disparando --> Reposo : Soltar L-CTRL
    
    state Disparando {
        [*] --> Habilidad_1
        Habilidad_1 --> Habilidad_2 : Delay 30ms
        Habilidad_2 --> Habilidad_3 : Delay 30ms
        Habilidad_3 --> [*]
    }
```
* **Ventaja Táctica:** Mantienes presionado `Control Izquierdo` y el personaje hace el combo perfecto a velocidad luz. Sueltas `Control` e inmediatamente puedes correr, curarte o lanzar otro hechizo manualmente.

---

## 5. Módulo: Camuflaje / Ghost Mode 👻

¿Haces transmisiones en Twitch, usas Discord Streams, o un GM (Game Master) te pidió revisar tu PC por AnyDesk/TeamViewer? El Ghost Mode te salvará.

```mermaid
graph TD
    A["Clic en icono Fantasma (Arriba Der.)"] --> B["Selecciona un proceso tapadera"]
    B -->|"Ej: Calculadora.exe"| C("Phantom OS extrae el ícono de la calculadora")
    C --> D("Phantom OS adopta el nombre 'Calculadora'")
    D --> E("La ventana de Phantom desaparece de la vista")
    E --> F["Phantom OS se minimiza a la Bandeja de Sistema"]
    
    F --> G{"¿Alguien abre el Administrador de Tareas?"}
    G -- Sí --> H["¡Indetectable! Solo verán una calculadora corriendo."]
```

### ¿Cómo recuperar la ventana de Phantom OS?
Simplemente ve a la esquina inferior derecha de tu pantalla (junto al reloj de Windows), haz clic en la flechita para ver los "Iconos Ocultos", busca el icono de tu programa tapadera (la Calculadora) y hazle **Doble Clic**. La ventana de Phantom OS volverá a aparecer.

