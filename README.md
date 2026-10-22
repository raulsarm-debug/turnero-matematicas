# Turnero de Matemática 📐

Aplicación de turnos estilo **Fresha** para un profesor de matemáticas.

## Características

- **Turnos de 1 hora** de 09:00 a 13:00 y de 17:00 a 21:00 (pausa 13:00–17:00).
- **Hasta 8 alumnos por turno** (clase grupal).
- **Lunes a viernes**, con visualización de la semana completa en un calendario.
- **Vista de alumnos**: ven los cupos libres y reservan con su nombre (reciben un **código de reserva**).
- **Vista del profesor 🔒** (protegida con PIN): agrega/quita alumnos, bloquea turnos, edita configuración y exporta la semana a CSV.
- **Única fuente de datos**: todo se guarda en el navegador (no se envía nada a internet).

## Cómo usar

1. **Abrir la aplicación**: Arrastra `turnero-matematicas.html` al navegador, haz doble clic en él, o abre desde el menú *Archivo > Abrir* del navegador.
2. **Como alumno**: elige un casillero abierto, ingresá tu nombre y confirmá. Te dará un **código** (ej. `M-8K2QZ`). Guardalo: lo necesitás para ver o cancelar tu reserva.
3. **Como profesor**: pulsá el botón `👨‍🏫 Panel del profesor` e ingresá el PIN (por defecto `1234`). Allí podés:
    - **+B Agregar** un alumno manualmente.
    - **Quitar** una reserva.
    - **Bloquear** un turno (por ejemplo, por una clase particular) o **Desbloquearlo**.
    - **Configuración**: cambiar el nombre del profesor y el PIN.
    - **⬇ CSV**: exportar todas las reservas de la semana a un archivo Excel/CSV.

**Nota rápida:** Para abrir directamente, copiá esta ruta en la barra de direcciones del navegador (se usa el formato file:// según el sistema operativo):
```
file:///Users/raulsarmiento/Downloads/turnero-matematicas/turnero-matematicas.html
```

## Configuración del horario

Editá la constante `CONFIG` en el archivo HTML para cambiar:
- `slots` → los horarios de turnos.
- `capacity` → cupo máximo por turno.
- `days` → días de cursada.
- `pauseAfterSlot` y `pauseText` → el descanso del medio día.
- `fewLeftThreshold` → cuántos lugares libres muestran "últimos lugares".

## Notas técnicas

- Los datos se guardan en `localStorage` de tu navegador; si lo limpias o usás otro navegador, se pierden las reservas.
- No hay conexión a internet ni servidores: el archivo es 100% autónomo.
- Para usarlo en otros dispositivos (teléfono, tablet) necesitarías un tiny server o un storage compartido; pedí que lo agregue si lo necesitás.