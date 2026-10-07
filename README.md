# Windows Web Emulator 2.0 — Windows 10 Edition

Interfaz tipo Windows 10 + acceso al runtime real Wine64/WebAssembly.

## EXE real

El escritorio no simula la ejecución del EXE. El icono **Wine64** abre
Boxedwine64, que ejecuta Wine64 x86-64 real en WASM y permite seleccionar
un `.exe` desde su botón "Run my own .exe".

## GitHub Pages

1. Crea un repositorio.
2. Sube este ZIP descomprimido.
3. Settings → Pages → Source: GitHub Actions.
4. Haz push a `main`.
5. Abre la URL publicada.

El workflow está incluido.

## Nota técnica

GitHub Pages no permite enviar los headers COOP/COEP directamente. Boxedwine64
usa `coi-serviceworker.js` para conseguir aislamiento de origen en Pages.
Su build 64-bit requiere SharedArrayBuffer/Memory64 y actualmente está orientado
a Chrome/Edge/Safari modernos, con compatibilidad todavía en desarrollo.

Fuente:
https://github.com/andrewnakas/Boxedwine64
