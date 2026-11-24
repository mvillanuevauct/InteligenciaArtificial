## Plantilla de Prompt Reutilizable: Generador de Sopa de Letras Educativa
Actúa como un Desarrollador Web Frontend Senior y Diseñador Instruccional especializado en gamificación educativa.

Tu objetivo es crear una actividad interactiva de Sopa de Letras completa, autocontenida en un único archivo HTML5 (con CSS3 y JavaScript vanilla integrado, sin dependencias externas), basada en el documento adjunto o la siguiente temática:

- **Tema / Módulo:** [ESCRIBE AQUÍ EL TEMA, EJ: Conceptos de Redes WAN - Módulo 7]
- **Nivel educativo:** [ESCRIBE EL NIVEL, EJ: Educación Superior Técnico-Profesional / Universitario]
- **Cantidad de conceptos a incluir:** [NÚMERO, EJ: 16] conceptos clave extraídos directamente del material proporcionado.

Asegúrate de cumplir estrictamente con los siguientes requisitos pedagógicos, técnicos y de UI/UX:

1. **LÓGICA Y CONFIGURACIÓN DEL TABLERO (JS):**
   - Matriz de letras de dimensiones: `[FILAS]x[COLUMNAS]` (ej. `25x25` o `20x20`).
   - Algoritmo de generación aleatoria que garantice la colocación sin colisiones erróneas de todos los conceptos en direcciones **horizontales, verticales y diagonales** (tanto en sentido normal como inverso).
   - Validación en tiempo real tanto en sentido directo como inverso (por si el estudiante arrastra desde la última letra hacia la primera).
   - Relleno de celdas vacías con letras aleatorias del alfabeto español (incluyendo la Ñ si aplica).

2. **INTERFAZ DE USUARIO Y DISEÑO VISUAL (CSS):**
   - Estética moderna, limpia e institucional, utilizando una paleta de colores coherente (`[INDICA PALETA, EJ: tonos azules corporativos y grises pizarra]`).
   - Tipografía legible de palo seco (*sans-serif*) con contraste mínimo de nivel **WCAG AA**.
   - Diseño responsivo (*Responsive Design*) basado en CSS Grid/Flexbox que aproveche el alto de pantalla (`vh`) en laptops y escritorio para evitar el scroll vertical incómodo al interactuar con el tablero.
   - Panel lateral fijo en escritorio (y colapsable/desplegable en dispositivos móviles o pantallas estrechas) que muestre:
     - La lista de conceptos a encontrar en mayúsculas.
     - Una breve pista conceptual o definición corta (máximo 5-7 palabras) debajo de cada término para reforzar el aprendizaje.

3. **EXPERIENCIA DE USUARIO E INTERACTIVIDAD (UX/JS):**
   - Selección fluida mediante **Pointer Events** (`pointerdown`, `pointermove`, `pointerup`) para garantizar compatibilidad tanto con ratón (clic y arrastre) como con pantallas táctiles.
   - Restricción geométrica inteligente durante el arrastre para que la selección solo trace líneas rectas válidas (0°, 45°, 90°).
   - Vista previa en tiempo real de las letras que se están seleccionando y resaltado visual inmediato en el tablero.
   - Verificación automática al soltar el cursor si la palabra es correcta, complementada con botones explícitos de control: **"Verificar Selección"**, **"Limpiar Selección"** y **"Nuevo Tablero"** (regenera la matriz).
   - Retroalimentación al acertar una palabra:
     - Resaltado permanente en las celdas del tablero (ej. fondo verde suave con borde definido).
     - Tachado automático del término en el panel lateral junto con un ícono de verificación (`✓`).
     - Notificación breve no intrusiva (*toast*).
   - Barra y contador de progreso en tiempo real en la cabecera (ej. `Encontradas: X / Total`).
   - Ventana modal de felicitación al alcanzar el 100% de la actividad, con opciones para revisar el tablero resuelto o reiniciar con una distribución nueva.

**Formato de entrega:**
Entrega únicamente el código fuente completo dentro de un único bloque de código HTML, listo para guardar como `.html` y ejecutar en cualquier navegador moderno.
