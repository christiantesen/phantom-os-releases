# Phantom OS

**Phantom OS** is an advanced memory injection and macro simulation tool designed specifically for MU Online. Built on Python with a modern CustomTkinter interface, it bypasses standard user-mode API hooking and implements low-level kernel inputs to achieve complete stealth (Anti-Cheat evasion).

[**👉 Read the User Guide (How to Use)**](GUIDE.md)

## Technical Architecture

The core of Phantom OS operates outside the traditional scope of standard macro recorders by reading and manipulating the target process's memory space directly, and interacting with the Windows subsystem via raw `ctypes` bindings.

### Core Modules

* **`zoom_engine.py` (Memory Scanner)**:
  * Emplea `pymem` para acceder a la memoria virtual del proceso (`main.exe`).
  * Utiliza un escaneo de floats secuencial (Pattern matching numérico) sobre los offsets de cámara conocidos (`39.0`, `35.0`).
  * Contiene un hilo cíclico (`_keep_loop`) protegido con *backoff-sleeps* (5.0s en desconexión) para evitar memory leaks o *CPU throttling* al perder las direcciones de los punteros durante las transiciones de pantalla (Warps).
* **`input_simulator.py` (Hardware Level Input)**:
  * Descarta el uso de `PostMessage` o `SendMessage` ya que son fácilmente interceptados por Anti-Cheats como LiveGuard.
  * Implementa `SendInput` (vía `user32.dll`), enviando estructuras nativas de Windows a la cola de hardware del sistema operativo, simulando el presionado físico del switch del teclado.
* **`macro_engine.py` (Threading & Polling)**:
  * Divide su carga de procesamiento en múltiples Daemon Threads.
  * **Auto-Potions:** Registra global hooks pasivos (`keyboard.add_hotkey`) que ceden el hilo principal al procesador (`0%` CPU footprint).
  * **Dynamic Combos:** Implementa un bucle *State-Machine* de latencia ultra-baja (30ms rest cycles) que evalúa interrupciones en tiempo real de la tecla `L-CTRL`.
* **`nt_api.py` (Kernel Manipulation & Process Enumeration)**:
  * Se apoya en enumeración nativa (`EnumWindows`, `GetWindowThreadProcessId`) garantizando la obtención de *Window Handles* (`HWND`) limpios sin detonar alarmas de inyección en librerías de terceros.
* **`ui/app.py` (GUI)**:
  * Arquitectura MVC que delega el estado y el bucle de UI principal a `CustomTkinter`. Corre en aislamiento total respecto a los motores lógicos.

## Project Structure

```
phantom-os/
├── src/
│   ├── config.py           # Global settings & process definitions
│   ├── main.py             # UAC Escalation and entry point
│   ├── ui/                 # CustomTkinter Views & Controllers
│   │   └── app.py
│   └── core/               # Engine Logic (Memory & Hooking)
│       ├── input_simulator.py 
│       ├── macro_engine.py    
│       ├── nt_api.py          
│       ├── speed_engine.py    
│       ├── range_engine.py
│       └── zoom_engine.py     
├── README.md               # Technical Documentation
├── GUIDE.md                # End-User Manual
├── LICENSE                 # MIT License
└── build.bat               # PyInstaller automated build script
```

## Development Environment Setup

1. **Prerequisites:** Python 3.10+
2. **Install Dependencies:**
   ```bash
   pip install customtkinter keyboard psutil pymem pywin32 pyinstaller
   ```
3. **Execution:**
   ```bash
   python src/main.py
   ```
   > *Note: Windows User Account Control (UAC) elevation is heavily strictly enforced for `pymem` OpenProcess handles. `main.py` auto-requests elevation.*

## Compiling for Distribution

To generate a standalone `.exe` without requiring end-users to have Python installed, simply run the included batch script:

```bash
./build.bat
```
This generates a single `Phantom OS.exe` payload inside the `dist/` directory using `--onefile` and integrates standard assets.

## License

This project is licensed under the [MIT License](LICENSE).
