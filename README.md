# Banco de cuestiones 4º semestre - V4.13

Versión verificada del sitio de Emmanuel Farias.

## Estructura

```text
index.html
README.md
GUIA_AGREGAR_PREGUNTAS.md
css/style-v4.css
js/data-loader.js
js/storage.js
js/simulado.js
js/app.js
data/manifest.json
data/neuro/*.json
data/fisio/*.json
Cuestionario_Neurociencia_Final.pdf
pdf_fisiologia_banco_completo_747_preguntas_2_columnas_emmanuel.pdf
```

## Conteo actual

- Neurociencias: 15 bloques, 600 preguntas.
- Fisiología: 11 bloques, 747 preguntas.

## PDFs usados por el sitio

- Neurociencias: `Cuestionario_Neurociencia_Final.pdf`
- Fisiología: `pdf_fisiologia_banco_completo_747_preguntas_2_columnas_emmanuel.pdf`

## Cómo agregar preguntas

Edita los archivos JSON dentro de `data/fisio/` o `data/neuro/`. No necesitas tocar `app.js` para agregar nuevas preguntas.

## Verificación V4.12

- JSON validado.
- IDs únicos.
- Respuestas dentro del rango correcto.
- Archivos referenciados por el sitio presentes.
- Modo simulado mantiene progreso, lista y feedback ocultos durante el intento.
