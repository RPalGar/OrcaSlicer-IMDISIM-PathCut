> **¿Windows 11?** Si al abrir sale *«Imagen incorrecta… TKernel.dll… 0xc0e90002»*, es una protección de Windows 11 con los programas sin firma. Solución paso a paso en el [README](https://github.com/RPalGar/OrcaSlicer-IMDISIM-PathCut#si-no-abre-en-windows-11).

> **¿La has probado?** Cuéntanos si has encontrado algún error y qué te ha parecido en el [formulario de errores y opinión](https://forms.gle/iAx6crNoZSRnkDvk7) (abierto hasta el 15 de noviembre de 2026).

<p align="center">
  <a href="https://forms.gle/iAx6crNoZSRnkDvk7"><img src="https://raw.githubusercontent.com/RPalGar/OrcaSlicer-IMDISIM-PathCut/main/docs/formulario/boton_formulario_15nov.png" alt="Cuéntanos qué te parece: formulario de errores y opinión (abierto hasta el 15 de noviembre)" width="460"></a>
</p>

Cuarta versión de **OrcaSlicer · IMDISIM · Cortar por ruta**, y la primera **también para Mac y Linux**. Es la misma herramienta que hemos propuesto para el OrcaSlicer oficial ([PR #17056](https://github.com/OrcaSlicer/OrcaSlicer/pull/17056)), con la interfaz en español.

> **¿Quieres que llegue al OrcaSlicer oficial?** Dale 👍 a la [petición de la función (#17041)](https://github.com/OrcaSlicer/OrcaSlicer/issues/17041) y al [PR (#17056)](https://github.com/OrcaSlicer/OrcaSlicer/pull/17056) en GitHub.

## Novedades respecto a la Beta 3
- **Versión para Mac** (Apple Silicon e Intel) **y para Linux** (Flatpak, 64 bits).
- **Seguir los bordes del modelo:** el lazo se pega a las aristas de la figura entre los puntos que marcas y corta exactamente por ellas.
- **Conectores a tu gusto:** se ve el conector bajo el ratón, **en verde donde cabe y en rojo donde no**; puedes **inclinar su eje** arrastrando una esfera de dirección y **forzar** un conector donde la comprobación no lo deja.
- **Varios cortes seguidos:** los conectores se pueden poner en las caras de **todos** los cortes que hicieron falta para separar las piezas, no solo en la del último, también si sales de la herramienta y vuelves a entrar.
- **Ruta con límites:** si la ruta termina dentro de la figura, corta lo que atraviesa y deja entero el resto.
- **Lazos más fiables:** un lazo alrededor de una parte que sigue unida por otro sitio también corta, y si la parte tiene agujeros por dentro, quedan abiertos.
- **Más rápido en modelos grandes:** solo se refina la malla donde pasa el corte.
- Cambiar entre ruta y lazo ya no borra el corte hecho, y la herramienta sigue abierta si el corte deja la figura en una pieza.

## Qué trae
- **Ruta desde la vista:** marca con clics la línea por donde quieres separar la figura; el corte sigue esa línea en la dirección en que miras (o nivelado, vertical o con el giro que elijas).
- **Lazo sobre la superficie:** rodea un brazo o una pierna y se separa solo esa parte, cortando justo por la línea que marcas (o con cara de corte plana si lo prefieres).
- **Conectores:** espiga y agujero o pasador suelto, cilíndricos o cuadrados, con holgura ajustable; automáticos o colocados a mano.

## Descarga en Windows (64 bits)
1. Descarga **`OrcaSlicer_Windows_V2.5.0-dev_x64_portable.zip`** (abajo, en *Assets*).
2. Clic derecho → **Extraer todo…** y abre **`orca-slicer.exe`**. No hace falta instalar.
3. Windows avisará de que no está firmado: **Más información → Ejecutar de todas formas**. En Windows 11, si sale *«Imagen incorrecta»*, sigue los pasos del [README](https://github.com/RPalGar/OrcaSlicer-IMDISIM-PathCut#si-no-abre-en-windows-11).
4. Selecciona una figura y pulsa el icono **Cortar por ruta**.

## Descarga en Mac (Apple Silicon e Intel)
1. Descarga **`OrcaSlicer_Mac_universal_V2.5.0-dev.dmg`** (abajo, en *Assets*), ábrelo y arrastra **OrcaSlicer** a **Aplicaciones**.
2. La primera vez, macOS dirá que no puede comprobar el desarrollador (no está firmada). Ve a **Ajustes del Sistema → Privacidad y seguridad**, baja hasta el aviso de OrcaSlicer y pulsa **Abrir igualmente**.
3. Si dice que la app **«está dañada»**, abre **Terminal** y escribe `xattr -cr /Applications/OrcaSlicer.app`; después ábrela de nuevo.
4. Selecciona una figura y pulsa el icono **Cortar por ruta**.

## Descarga en Linux (64 bits, Flatpak)
1. Necesitas **Flatpak** (viene de serie en Fedora, Linux Mint y otras; en Ubuntu: `sudo apt install flatpak`) y el repositorio Flathub, del que se bajan sus dependencias: `flatpak remote-add --user --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo`
2. Descarga **`OrcaSlicer_Linux_V2.5.0-dev_x86_64.flatpak`** (abajo, en *Assets*).
3. En una terminal, en la carpeta de la descarga: `flatpak install --user OrcaSlicer_Linux_V2.5.0-dev_x86_64.flatpak`
4. Ábrelo desde el menú de aplicaciones o con `flatpak run com.orcaslicer.OrcaSlicer`.

Las versiones de Mac y Linux solo se han compilado y pasado las pruebas automáticas; no se han probado a mano. Si las usas, cuéntanos cómo van en el formulario.

## Aviso
Versión **beta**, sin garantía. Guarda tu proyecto antes de cortar. Si el objeto tiene varias partes, se unen en una sola antes de cortar (y se quedan con los ajustes de la primera). No corta objetos con varias copias. Los modelos pintados en varios colores todavía no están probados con el corte.

Desarrollada por Rubén Palenzuela (IMDISIM) con Claude (IA de Anthropic); revisada con auditorías y pruebas automáticas hechas también con IA, sin revisión de programadores humanos.

## Código fuente
`codigo-fuente-{{COMMIT_CORTO}}.zip` contiene el código exacto con el que se compilaron las versiones de Windows, Mac y Linux (commit [`{{COMMIT_CORTO}}`](https://github.com/RPalGar/OrcaSlicer/commit/{{COMMIT}})). Es el código del [PR #17056](https://github.com/OrcaSlicer/OrcaSlicer/pull/17056) más la traducción al español de la herramienta. Licencia AGPL-3.0, basada en [OrcaSlicer](https://github.com/OrcaSlicer/OrcaSlicer). No es una versión oficial de OrcaSlicer.

**Contacto:** [LinkedIn](https://www.linkedin.com/in/rub%C3%A9n-palenzuela-imdisim) · [info@imdisim.es](mailto:info@imdisim.es)
