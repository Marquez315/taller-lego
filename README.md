<p align="center"><img src="icons/icon-192.png" alt="Ícono de Taller Lego: un ladrillo Lego rojo 2×4" width="120"></p>

# 🧱 Taller Lego

**Taller Lego** es una aplicación web educativa para **diseñar piezas tipo Lego en 3D** y **exportarlas en formato STL** para imprimirlas en una impresora 3D. Sirve para armar chasis de robots, soportes para motores y pilas, torres eólicas, semáforos, postes de luz, techos y otras piezas de maquetas, todo con las medidas reales de los ladrillos Lego.

Funciona **en línea y sin conexión**, en **celulares, tablets y computadoras**, y se puede **instalar** como una app. No necesita servidor, cuentas ni instalar programas: es solo HTML, CSS y JavaScript.

> Creado para educación, por la profesora **Marquez Camila Araceli** · Instagram: [@didactica_aumentada3.0](https://www.instagram.com/didactica_aumentada3.0/)

---

## ✨ ¿Qué hace?

- **Modelado 3D en el navegador** (WebGL): se agregan piezas desde una paleta, se mueven, se giran y se apoyan solas sobre las que están debajo.
- **Medidas reales de Lego**: stud de 8 mm, placa de 3,2 mm y ladrillo de 9,6 mm.
- **Ajuste a rejilla** de 8 mm (studs), 4 mm o 1 mm.
- **Panel de propiedades** para cambiar posición (X, Y, Z), tamaño, color y otros parámetros de cada pieza.
- **Revisión automática**: calcula las dimensiones del conjunto, avisa si **entra en la cama de impresión de 165 × 165 mm**, cuenta las piezas y da recomendaciones eléctricas básicas (por ejemplo, para pilas 18650 y motores TT).
- **Exportar a STL**: todo el diseño o una pieza suelta, listo para el laminador (Cura, PrusaSlicer, Bambu Studio, etc.).
- **Guardar y abrir diseños** en archivos `.json`, y **autoguardado** en el propio dispositivo.
- **Deshacer** (hasta 80 pasos), duplicar, girar 90°, apoyar y eliminar piezas.
- **Tema claro y oscuro** automático según el dispositivo.

## 🧩 Piezas disponibles

| Grupo | Piezas |
|---|---|
| Ladrillos y placas | Ladrillo 2×4, Ladrillo 2×2, Placa 2×6, Placa chasis 6×10 (todas con medidas editables) |
| Electrónica y movimiento | Motorreductor TT amarillo*, Soporte motor TT, Rueda, Rueda TT con eje D, Pila 18650*, Soporte pila 18650 |
| Maqueta y ciudad | Torre eólica, Aspas de turbina, Semáforo (huecos para LED), Poste de luz (LED), Techo a 2 aguas, Techo a 4 aguas |

\* El **motor** y la **pila** son **solo de referencia**: sirven para comprobar que todo encaja, pero **no se exportan** al STL.

## 🖱️ Cómo se usa

### En computadora
| Acción | Cómo |
|---|---|
| Agregar una pieza | Clic en la paleta de la izquierda |
| Girar la vista | Arrastrar sobre el fondo |
| Mover la vista | `Shift` + arrastrar, o clic derecho + arrastrar |
| Zoom | Rueda del mouse |
| Mover una pieza | Arrastrarla (se apoya sola sobre las de abajo) |
| Editar una pieza | Clic sobre ella y usar el panel derecho |
| Eliminar | Tecla `Supr` / `Backspace` o botón *Eliminar* |
| Deshacer | `Ctrl + Z` (o `⌘ + Z`) o botón *Deshacer* |

### En celular o tablet
| Acción | Cómo |
|---|---|
| Girar la vista | Un dedo sobre el fondo |
| Zoom | Pellizco con dos dedos |
| Mover la vista | Arrastrar con dos dedos |
| Mover una pieza | Arrastrarla con un dedo |
| Editar una pieza | Tocarla y usar el panel inferior |

### Para imprimir
1. Armá el diseño y mirá la **Revisión** (indica si entra en la cama de 165 × 165 mm).
2. Tocá **Exportar STL** (o *STL de esta pieza* para una sola).
3. Abrí el archivo en tu laminador y mandalo a la impresora.

## 📶 Funciona sin conexión

La app es una **PWA** (aplicación web progresiva):

1. Abrila **una vez con internet**. Se guarda todo lo necesario en el dispositivo.
2. Desde ese momento funciona **sin conexión**, incluso si cerrás y volvés a abrir el navegador.
3. Cuando hay internet, se **actualiza sola** en segundo plano (la nueva versión se ve la próxima vez que la abras).
4. En la barra superior se ve si estás **En línea** o **Sin conexión**.

Tus diseños se **autoguardan en el dispositivo** (almacenamiento local del navegador). Para pasarlos a otro dispositivo o hacer copias de seguridad, usá **Guardar** (descarga un `.json`) y **Abrir**.

### 📲 Instalarla como app
Tocá el botón **⬇ Descargar aplicación** de la barra superior. Se abre una ventana que indica si la app ya quedó guardada para usarla sin conexión y ofrece dos opciones:

- **📲 Instalar en este dispositivo** (Chrome / Edge en PC y Android): queda como una app más, con su ícono.
- **📄 Descargar archivo (.html)**: baja una copia de la aplicación en un solo archivo (`Taller_Lego.html`). Se abre con doble clic, en cualquier computadora o celular, **sin internet**, y se puede pasar por pendrive o WhatsApp.
- **iPhone / iPad (Safari):** *Compartir* → *Agregar a pantalla de inicio*.

## 🚀 Publicar en GitHub Pages

1. Creá un repositorio nuevo en GitHub (por ejemplo, `taller-lego`), público.
2. Subí **todos los archivos de esta carpeta**, respetando la carpeta `icons/`:
   *Add file → Upload files* y arrastrá el contenido (no la carpeta contenedora).
3. Entrá en **Settings → Pages**.
4. En *Build and deployment* elegí **Deploy from a branch**, rama **main** y carpeta **/ (root)**, y guardá.
5. Después de uno o dos minutos la app queda en:
   `https://TU-USUARIO.github.io/taller-lego/`

> GitHub Pages usa HTTPS, que es lo que necesitan el modo sin conexión y la instalación.
> Si abrís `index.html` haciendo doble clic (`file://`), la app funciona igual, pero sin instalación ni caché offline.

### Publicar una versión nueva
Después de modificar `index.html`, cambiá el número de `VERSION` al principio de `sw.js` (por ejemplo, `'v2'`). Así los dispositivos descargan la versión nueva y descartan la anterior.

## 📁 Estructura del proyecto

```
taller-lego/
├── index.html            ← la aplicación completa (HTML + CSS + JS)
├── sw.js                 ← service worker (modo sin conexión)
├── manifest.webmanifest  ← datos para instalarla como app
├── .nojekyll             ← para que GitHub Pages sirva los archivos tal cual
├── README.md
└── icons/                ← ícono de la app (ladrillo Lego en SVG y PNG)
```

## 🌐 Compatibilidad

Navegadores actuales con **WebGL**: Chrome, Edge, Firefox y Safari, en Windows, macOS, Linux, Android, iOS e iPadOS. El diseño se adapta a pantallas chicas (celular en vertical y horizontal), tablets y computadoras, y está pensado para uso táctil y con mouse.

## 🛠️ Tecnología

HTML, CSS y JavaScript puro, sin librerías ni dependencias externas. El 3D se dibuja con WebGL y la exportación genera archivos **STL binarios** directamente en el navegador.

## 👩‍🏫 Créditos

Creado para educación, por la profesora **Marquez Camila Araceli**.
Instagram: [@didactica_aumentada3.0](https://www.instagram.com/didactica_aumentada3.0/)


## 🦗🕷️ Grillo y araña caminantes (nuevo)

En la paleta, sección **Grillo caminante**: el botón **Armar grillo completo** coloca en la escena el chasis, el motorreductor TT amarillo, el soporte con la pila **18650**, la cabeza con antenas, dos manivelas, cuatro patas y cuatro bielas cruzadas (inspirado en los grillos de madera/3D con motor amarillo).

- Las barras (patas y bielas) y las manivelas tienen agujeros para **tornillos M3 con tuerca** (≈10 en total). Cada pieza se edita en el panel (largo, agujeros extra, ángulo).
- Imprimí cada barra con **STL de esta pieza** (sale acostada). Las piezas de referencia (motor y pila) no se exportan.
- El movimiento sale de una manivela en cada lado, desfasadas 180°, que mueve la pata delantera y la trasera en sentido contrario. Es un diseño para probar e iterar: ajustá largos de bielas y radio de manivela según tu impresión.
- Pila 18650: 3,7 V (4,2 V cargada); usá módulo con protección y un interruptor.

**🕷️ Araña robótica (8 patas):** botón **Armar araña robótica**. Usa el mismo chasis, motor TT y pila 18650, pero con un segundo par de caderas por lado (campo «2.º par de caderas» = 44) y una biela paralela que une cada pata con su vecina, así las ocho patas se mueven juntas (inspirada en las arañas de palitos de helado con zigzag).

## ▶ Simulador 3D (nuevo)

`simulador.html` (botón **Simulador 3D** del encabezado): muestra el grillo y la araña caminando en 3D con la misma geometría de las piezas. Se puede variar la velocidad del motor (rpm), el radio de la manivela y el brazo de pata, invertir el sentido y girar/acercar la cámara con el dedo o el mouse. Muestra avance, velocidad y altura del cuerpo, y avisa si el mecanismo se traba. Es un modelo cinemático ideal (sin deslizamiento ni masa): sirve para comparar diseños antes de imprimir.
