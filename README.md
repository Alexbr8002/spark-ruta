# Spark Mileage + Taxes — PWA v0.3

## Qué incluye
- Registro diario manual:
  - odo inicio
  - odo fin
  - MPG
  - precio gasolina
  - gasolina comprada opcional
  - fotos locales como evidencia
- Cálculos:
  - millas Spark
  - gasolina estimada por MPG
  - costo interno por milla
  - deducción IRS por millas
  - self-employment tax aproximado
- Ganancias semanales:
  - confirmed weekly earnings
  - trip earnings
  - confirmed tips app
- Cash tips: no tracked.
- Gaps entre días: personales.
- Importar JSON histórico desde ChatGPT.
- Exportar backup JSON y CSV.

## Cómo usar local
Abre `index.html` en el navegador.

## Cómo publicar en GitHub Pages
1. Sube estos archivos al repo:
   - index.html
   - manifest.json
   - service-worker.js
   - icon.svg
2. Activa GitHub Pages desde Settings → Pages.
3. Abre la URL del sitio desde el celular.
4. En Chrome Android: menú ⋮ → Add to Home screen.

## Nota fiscal
El modo del vehículo está fijo en `standard_mileage_only`.
La app no mezcla gasolina con deducción de vehículo para taxes.
Gasolina queda para análisis operativo interno.


## Icono de app
Esta versión incluye iconos PNG:
- icons/icon-192.png
- icons/icon-512.png
- icons/icon-maskable-192.png
- icons/icon-maskable-512.png

En Android/Chrome, al usar “Add to Home screen”, debe aparecer como icono de app.


## Cambio v0.2
- Se quitó `capture="environment"` de los campos de imagen.
- Ahora Android/Chrome debe ofrecer Cámara, Galería o Archivos al cargar fotos de odómetro/bomba.
- Service worker actualizado a cache v02 para evitar que el navegador mantenga la versión anterior.


## Cambio v0.3
- Los campos de imagen usan extensiones/MIME explícitos: `.jpg,.jpeg,.png,.webp,image/jpeg,image/png,image/webp`.
- Se evita `accept="image/*"` porque en algunos Android/Chrome prioriza cámara.
- Se eliminó `capture`.
- Flujo recomendado: tomar foto con la cámara normal del teléfono y luego subir desde Galería/Archivos.
- Service worker actualizado a cache v03.
