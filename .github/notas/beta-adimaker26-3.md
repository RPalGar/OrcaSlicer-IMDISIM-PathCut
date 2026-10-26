> **¿Windows 11?** Si al abrir sale *«Imagen incorrecta… TKernel.dll… 0xc0e90002»*, es una protección de Windows 11 con los programas sin firma. Solución paso a paso en el [README](https://github.com/RPalGar/OrcaSlicer-IMDISIM-PathCut#si-no-abre-en-windows-11).

> **¿Has encontrado un fallo?** Cuéntamelo en el [cuestionario de fallos]({{CUESTIONARIO}}) (abierto hasta el {{CUESTIONARIO_FIN}}).

Tercera versión de **OrcaSlicer · IMDISIM · Cortar por ruta**: la que se usó en las demostraciones de **Adimaker 2026** (Tenerife), con las mejoras que salieron de probarla allí.

## Novedades respecto a la Beta 2
- **Vista previa del corte:** antes de cortar ves las piezas separadas. Si no te convence, **Editar** y ajustas los puntos; si está bien, **Realizar corte**. También con Enter y Esc.
- **Si la figura sigue unida por otro sitio** (por ejemplo, una mano apoyada en el cuerpo), la vista previa marca **en rojo** dónde sigue unida. Puedes editar el trazo o hacer el corte y **cortar esa unión en un segundo corte**.
- **Conectores rectos según la dirección en que se separan las piezas**: ya no salen inclinados en cortes curvos o en U.
- **Separación de la vista previa** proporcional al tamaño de la pieza (para verlas bien).
- **Puntos de la ruta más pequeños** y atenuados cuando quedan detrás de la figura, para no confundirte al trazar.
- **Menús desplegables legibles** (fondo claro).
- **Arreglos:** la vista previa ya no se desactiva al añadir un conector o mover un punto, y Orca ya no se cierra al colocar un conector en el lazo después de cambiar sus ajustes.

## Qué trae
- **Ruta desde la vista:** marca con clics la línea por donde quieres separar la figura; el corte sigue esa línea en la dirección en que miras (o nivelado, vertical o con el giro que elijas).
- **Lazo sobre la superficie:** rodea un brazo o una pierna y se separa solo esa parte, cortando justo por la línea que marcas (o con cara de corte plana si lo prefieres).
- **Conectores:** espiga y agujero o pasador suelto, cilíndricos o cuadrados, con holgura ajustable; automáticos o colocados a mano.

## Descarga (Windows 64 bits)
1. Descarga **`OrcaSlicer_Windows_V2.5.0-dev_x64_portable.zip`** (abajo, en *Assets*).
2. Clic derecho → **Extraer todo…** y abre **`orca-slicer.exe`**. No hace falta instalar.
3. Windows avisará de que no está firmado: **Más información → Ejecutar de todas formas**. En Windows 11, si sale *«Imagen incorrecta»*, sigue los pasos del [README](https://github.com/RPalGar/OrcaSlicer-IMDISIM-PathCut#si-no-abre-en-windows-11).
4. Selecciona una figura y pulsa el icono **Cortar por ruta**.

## Aviso
Versión **beta**, sin garantía. Guarda tu proyecto antes de cortar. Si el objeto tiene varias partes, se unen en una sola antes de cortar (y se quedan con los ajustes de la primera). No corta objetos con varias copias. Los modelos pintados en varios colores todavía no están probados con el corte.

Desarrollada por Rubén Palenzuela (IMDISIM) con Claude (IA de Anthropic); revisada con auditorías y pruebas automáticas hechas también con IA, sin revisión de programadores humanos.

## Código fuente
`codigo-fuente-{{COMMIT_CORTO}}.zip` contiene el código exacto con el que se compiló este ejecutable (commit [`{{COMMIT_CORTO}}`](https://github.com/RPalGar/OrcaSlicer/commit/{{COMMIT}})). Licencia AGPL-3.0, basada en [OrcaSlicer](https://github.com/OrcaSlicer/OrcaSlicer). No es una versión oficial de OrcaSlicer.

**Contacto:** [LinkedIn](https://www.linkedin.com/in/rub%C3%A9n-palenzuela-imdisim) · [info@imdisim.es](mailto:info@imdisim.es)
