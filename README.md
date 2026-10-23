# Formatos digitales Cañaveral (prueba real con QR)

App de una sola página para registrar la temperatura de neveras y cuartos fríos escaneando el QR de cada equipo.

- App: https://felipeanali.github.io/formatos-digitales/
- QR de ejemplo: https://felipeanali.github.io/formatos-digitales/?equipo=SC14-CBP-NEV-CON-01

## Dónde se guardan los datos

Este mismo repositorio funciona como base de datos: todo queda en `datos/db.json` de la rama
`datos-formatos`, que la app crea sola la primera vez. Las fotos y firmas quedan en `datos/archivos/`.
Lo que se registra en un celular aparece en los demás celulares y en el computador.
Un navegador que no esté conectado sigue funcionando en modo local (sus datos quedan solo ahí).

## Puesta en marcha (una sola vez)

1. **Publicar:** Settings → Pages → Source: *Deploy from a branch* → `main` / `(root)` → Save.
2. **Token:** abrir la app en el computador → entrar como **Felipe** → **Sistema** →
   **Base de datos en GitHub** → *Crear el token en GitHub*. Repository access: **Only select
   repositories → formatos-digitales**. Permisos: **Contents: Read and write**. Generar y copiar.
3. Pegar el token → **Probar conexión** → **Conectar**. Se suben los datos de demostración.
4. **Celulares:** Sistema → **Conectar otro celular** → escanear ese QR una vez con cada celular.
5. **Imprimir QR de equipos:** Equipos y QR → Hoja de QR. Escanear con la cámara normal.

## Cuidado

- El QR de "Conectar otro celular" lleva el token: mostrarlo solo en pantalla, nunca imprimirlo.
  Si se pierde un celular, borrar el token en GitHub y crear uno nuevo.
- El repositorio es público: el archivo de datos se puede leer. Usar solo datos de prueba.
- Los permisos se revisan en el celular, no en GitHub. Para producción hace falta un servidor
  (la app ya trae el espacio en Sistema → Conexión a servidor).
