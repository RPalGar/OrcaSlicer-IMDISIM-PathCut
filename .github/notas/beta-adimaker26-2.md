> **¿Windows 11?** Si al abrir sale *«Imagen incorrecta… TKernel.dll… 0xc0e90002»*, es una protección de Windows 11 con los programas sin firma. Solución paso a paso en el [README](https://github.com/RPalGar/OrcaSlicer-IMDISIM-PathCut#si-no-abre-en-windows-11).

Segunda versión de **OrcaSlicer · IMDISIM · Cortar por ruta**, para **Adimaker 2026** (Tenerife).

## Novedades respecto a la primera versión
- **Corte exacto por el lazo:** ahora corta solo por la línea que marcas; fuera del lazo no se toca nada. Sirve para cortar por un pliegue y que la unión no se note. Ajuste «Desviación máx.» (1,5 mm por defecto). La opción «Cara de corte plana» mantiene el corte anterior.
- **Piezas con agujeros y volúmenes negativos:** ya se pueden cortar, y cada agujero se queda con su pieza.
- **Conectores cuadrados** que se ajustan a la cara de corte, y primera versión de la **colocación manual** con clics (todavía en mejora).
- **Cancelar** un corte o cerrar la herramienta la libera al momento; un corte fallido ya no deja la barra de progreso colgada.

## Qué trae
- **Ruta desde la vista:** marca con clics la línea por donde quieres separar la figura; el corte sigue esa línea en la dirección en que miras (o nivelado, vertical o con el giro que elijas).
- **Lazo sobre la superficie:** rodea un brazo o una pierna y se separa solo esa parte, con cara de corte plana o curva.
- **Conectores:** espiga y agujero o pasador suelto, cilíndricos o cuadrados, con holgura ajustable.

## Descarga (Windows 64 bits)
1. Descarga **`OrcaSlicer_Windows_V2.5.0-dev_x64_portable.zip`** (abajo, en *Assets*).
2. Clic derecho → **Extraer todo…** y abre **`orca-slicer.exe`**. No hace falta instalar.
3. Windows avisará de que no está firmado: **Más información → Ejecutar de todas formas**. En Windows 11, si sale *«Imagen incorrecta»*, sigue los pasos del [README](https://github.com/RPalGar/OrcaSlicer-IMDISIM-PathCut#si-no-abre-en-windows-11).
4. Selecciona una figura y pulsa el icono **Cortar por ruta**.

## Aviso
Versión **beta**, sin garantía. Guarda tu proyecto antes de cortar. Si el objeto tiene varias partes, se unen en una sola antes de cortar. No corta objetos con varias copias. La colocación manual de conectores aún se está mejorando.

Desarrollada por Rubén Palenzuela (IMDISIM) con Claude (IA de Anthropic); revisada con auditorías y pruebas automáticas hechas también con IA, sin revisión de programadores humanos.

## Código fuente
`codigo-fuente-{{COMMIT_CORTO}}.zip` contiene el código exacto con el que se compiló este ejecutable (commit [`{{COMMIT_CORTO}}`](https://github.com/RPalGar/OrcaSlicer/commit/{{COMMIT}})). Licencia AGPL-3.0, basada en [OrcaSlicer](https://github.com/OrcaSlicer/OrcaSlicer). No es una versión oficial de OrcaSlicer.

**Contacto:** [LinkedIn](https://www.linkedin.com/in/rub%C3%A9n-palenzuela-imdisim) · [info@imdisim.es](mailto:info@imdisim.es)
