# Banco de cuestiones 4º semestre - V4

Esta versión separa el sitio en archivos de código y archivos de preguntas.

## Estructura principal

```text
bancodecuestiones/
├── index.html
├── README.md
├── css/
│   ├── style-v4.css
│   └── style.css / style-v3.css  # antiguos, no obligatorios
├── js/
│   ├── data-loader.js
│   ├── app.js
│   ├── storage.js
│   ├── simulado.js
│   └── questions.js # solo aviso de compatibilidad
└── data/
    ├── manifest.json
    ├── plantilla-bloque.json
    ├── neuro/
    │   ├── clase1.json
    │   ├── clase2.json
    │   └── ...
    └── fisio/
        ├── fisio_cap75_aleatorio.json
        ├── fisio_cap76_aleatorio.json
        └── ...
```

## Cómo agregar preguntas a un bloque existente

Ejemplo: para agregar una pregunta en Neurociencias, Clase 12, abre:

```text
data/neuro/clase12.json
```

Dentro de `questions`, agrega una nueva pregunta siguiendo este formato:

```json
{
  "id": "clase12_026",
  "q": "Escribe aquí la pregunta.",
  "topic": "Diagnóstico",
  "options": [
    "Alternativa A",
    "Alternativa B",
    "Alternativa C",
    "Alternativa D"
  ],
  "answer": 1,
  "exp": "Explicación clara de la respuesta correcta."
}
```

### Regla de la respuesta correcta

```text
0 = A
1 = B
2 = C
3 = D
4 = E
```

No necesitas cambiar manualmente el número de preguntas. La V4 cuenta las preguntas automáticamente.

## Cómo agregar un bloque nuevo

1. Copia `data/plantilla-bloque.json`.
2. Pega el archivo en `data/neuro/` o `data/fisio/`.
3. Cambia el nombre del archivo, por ejemplo:

```text
data/neuro/clase13.json
```

4. Edita `data/manifest.json` y agrega el nuevo bloque en la lista de `sections` del área correspondiente:

```json
{
  "key": "clase13",
  "file": "data/neuro/clase13.json"
}
```

## Importante

- No abras el `index.html` directamente desde tu computadora para probar la V4, porque algunos navegadores bloquean la carga de JSON local.
- Para probar localmente, usa un servidor local:

```bash
python -m http.server 8000
```

Luego abre:

```text
http://localhost:8000
```

En GitHub Pages funcionará normalmente.


## V4.1 - Modo simulado

En modo simulado no se muestran aciertos, errores ni lista de preguntas durante el intento. La corrección aparece solamente al finalizar.


## Actualización V4.2

Se agregó en Neurociencias el bloque **Especial para examen final ordinário** con 200 preguntas tomadas del archivo `Cuestionario_Neurociencia_Final.pdf`.

Para editar ese bloque, modifica:

```text
data/neuro/clase13_final_ordinario.json
```


## V4.3
- En modo simulado no se muestra progreso durante el intento.
- En modo simulado no aparece la lista de preguntas.
- La corrección y los resultados aparecen solamente al finalizar.


## V4.4
- Corrección del bloque de Fisiología: Cuestionario difícil. Se retiraron textos residuales del PDF que aparecían dentro de algunas alternativas y explicaciones.


## V4.6

- Agrega 39 preguntas verificadas al bloque Fisiología → Capítulo 78.
- Mantiene las 28 preguntas agregadas al Capítulo 75 en V4.5.
- Archivo modificado: `data/fisio/fisio_cap78_aleatorio.json`.


## Versión 4.7
- Agrega el PDF completo de Fisiología con 567 preguntas.
- Incluye índice interactivo por bloque y gabarito explicado al final.
- El botón de descarga de Fisiología apunta a `pdf_fisiologia_banco_completo_567_preguntas_emmanuel.pdf`.


## V4.8
- PDF completo de Fisiología en formato simple de 2 columnas.
- Índice interactivo para todos los bloques, incluyendo los cuestionarios finales.
- Gabarito simplificado al final.

## V4.10 - Capítulo 80 y PDF actualizado

- Agrega 35 preguntas revisadas del capítulo 80 al bloque de Fisiología.
- El bloque `Capítulo 80` pasa de 25 a 60 preguntas.
- El banco completo de Fisiología pasa a 640 preguntas.
- El botón de descarga de Fisiología apunta a `pdf_fisiologia_banco_completo_640_preguntas_2_columnas_emmanuel.pdf`.
