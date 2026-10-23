# Formatos digitales Cañaveral (prueba real con QR)

App de una sola página para registrar la temperatura de neveras y cuartos fríos escaneando el QR de cada equipo.

- App: https://felipeanali.github.io/formatos-digitales/
- QR de ejemplo: https://felipeanali.github.io/formatos-digitales/?equipo=SC14-CBP-NEV-CON-01

## Dónde se guardan los datos

Este mismo repositorio funciona como base de datos: todo queda en `datos/db.json` de la rama
`datos-formatos`, que la app crea sola la primera vez. Las fotos y firmas quedan en `datos/archivos/`.
Lo que se registra en un celular aparece en los demás celulares y en el computador (revisa cada 10 segundos y le avisa al administrador).
Un navegador que no esté conectado sigue funcionando en modo local (sus datos quedan solo ahí).

## Puesta en marcha (una sola vez)

1. **Publicar:** Settings → Pages → Source: *Deploy from a branch* → `main` / `(root)` → Save.
2. **Token:** abrir la app en el computador → entrar como **Felipe** → **Sistema** →
   **Base de datos en GitHub** → *Crear el token en GitHub*. Repository access: **Only select
   repositories → formatos-digitales**. Permisos: **Contents: Read and write**. Generar y copiar.
3. Pegar el token → **Probar conexión** → **Conectar**. Se suben los datos de demostración.
4. **Celulares:** Sistema → **Conectar otro celular** → escanear ese QR una vez con cada celular.
5. **Imprimir QR de equipos:** Equipos y QR → Hoja de QR. Escanear con la cámara normal.

## Guion de demostración (10 minutos)

Todo es con datos de ejemplo: nombres, equipos y registros inventados.

**Antes:** computador conectado (paso 3) y un celular conectado (paso 4). Imprimir 3 o 4 QR de
SC PUNTO 14 desde Equipos y QR, o mostrarlos en una segunda pantalla con "Ver QR".

1. **El problema:** el formato de temperatura en papel (4 veces al día, por equipo).
2. **El administrador** (computador, entrar como **Laura Gómez** o **Felipe**): Tablero de hoy con
   el cumplimiento por horario, las alertas y el ranking de equipos; Resultados y Excel; el formulario
   y cómo se edita sin programar.
3. **La persona que registra** (celular): escanear el QR con la cámara normal → elegir
   **Carlos Rentería** → llenar las dos temperaturas → Enviar. Toma unos 20 segundos.
4. **En vivo:** a los pocos segundos el computador muestra "Nuevo registro: Carlos Rentería…" y el
   tablero se actualiza solo.
5. **Una alerta:** escanear de nuevo y poner una temperatura fuera de rango (ej. -5 en congelación):
   el formulario pide la acción tomada y en el computador el aviso sale en rojo.
6. **El operario solo ve lo suyo:** en el celular, pestaña Resultados (solo su área).

## Cuidado

- El QR de "Conectar otro celular" lleva el token: mostrarlo solo en pantalla, nunca imprimirlo.
  Si se pierde un celular, borrar el token en GitHub y crear uno nuevo.
- El repositorio es público: el archivo de datos se puede leer. Usar solo datos de prueba.
- Los permisos se revisan en el celular, no en GitHub. Para producción hace falta un servidor
  (la app ya trae el espacio en Sistema → Conexión a servidor).
