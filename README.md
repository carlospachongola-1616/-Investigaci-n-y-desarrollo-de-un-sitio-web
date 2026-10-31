Raíz Verde - Cocina vegana en Neiva

Landing page de un restaurante vegano ficticio inspirado en la comida típica del Huila.
Proyecto individual de la práctica IA + Tailwind CSS del Seminario en Gestión de Software Ágil Asistido por IA (SOF) 2, Fundación Escuela Tecnológica de Neiva (FET).

Sitio publicado:
Video:

Tecnologías
HTML5
Tailwind CSS 4 mediante Play CDN
JavaScript puro, sin librerías

Público objetivo
Jóvenes y adultos de Neiva entre 18 y 40 años interesados en comida vegana, saludable o local, incluyendo estudiantes universitarios y personas que quieren probar platos típicos del Huila en versión vegetal.

Paleta de colores (regla 60-30-10)
Color dominante (60 %): verde muy claro #F4F7F1, usado en el fondo.
Color secundario (30 %): verde bosque #1F3D2B, usado en textos, navbar y pie de página.
Color de acento (10 %): terracota #C2410C, usado en botones y precios.
Éxito: verde #15803D
Error: rojo #B91C1C
Advertencia: ámbar #B45309

Fuentes
DM Serif Display para títulos.
DM Sans para textos.

Funcionalidades
Navbar fija con menú hamburguesa en celular.
Modo oscuro con botón que recuerda la preferencia.
Menú en tarjetas con filtro por categoría.
Preguntas frecuentes en acordeón.
Formulario con validación en JavaScript, mensajes de error junto a cada campo y toast de confirmación.
Diseño responsive con los prefijos sm, md y lg.


Prompt maestro

Rol: Actúa como desarrollador frontend senior especializado en Tailwind CSS 4, diseño responsive y accesibilidad web.

Contexto: Voy a crear la landing page de "Raíz Verde", un restaurante de comida vegana ubicado en Neiva (Huila). El restaurante reinventa platos típicos del Huila, como el tamal, el asado y las achiras, usando solo ingredientes de origen vegetal. El público son jóvenes y adultos de 18 a 40 años interesados en comida vegana, saludable o local. El objetivo del sitio es mostrar el menú, contar la historia del restaurante y recibir pedidos o reservas por medio de un formulario.

Tareas: Construye una página con estas secciones, en este orden:
1. Navbar fija con el nombre del restaurante en texto, enlaces a Menú, Nosotros, Preguntas y Contacto, un botón "Pedir ahora" y un botón para cambiar entre modo claro y oscuro. En celular los enlaces deben convertirse en un menú hamburguesa que se abre y se cierra con JavaScript y que se cierra al tocar un enlace.
2. Hero con una imagen de fondo de comida vegetal con capa oscura, un texto pequeño "Cocina 100 % vegetal · Neiva, Huila", un título principal, un subtítulo y dos botones: "Ver menú" y "Hacer un pedido".
3. Menú en tarjetas con grid de 1 columna en celular, 2 en tablet y 3 en computador. Seis platos inspirados en la comida huilense, cada uno con imagen, nombre, descripción corta, precio en pesos colombianos y efecto hover. Arriba de las tarjetas agrega un filtro con botones "Todos", "Platos fuertes", "Para picar" y "Bebidas" que muestre solo las tarjetas de la categoría elegida.
4. Sección "Nosotros" con imagen y texto en dos columnas (una columna en celular), con la historia del restaurante y tres valores: ingredientes vegetales, compra a productores locales y empaques compostables.
5. Preguntas frecuentes en acordeón con 4 preguntas que se abren y se cierran con JavaScript.
6. Formulario de pedido o reserva con nombre, correo, tipo de solicitud (domicilio, reserva o evento), número de personas (1 a 20) y comentarios. Valida con JavaScript que los campos obligatorios estén llenos y que el correo sea válido; muestra el error en rojo debajo de cada campo y, al enviar correctamente, un toast verde de confirmación que desaparece a los 4 segundos.
7. Pie de página con dirección, horario, redes sociales y derechos reservados con el año actual.

Restricciones: Usa solo HTML, Tailwind CSS 4 mediante el Play CDN (https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4) y JavaScript puro, sin otras librerías. Define la paleta con @theme dentro de una etiqueta style type="text/tailwindcss": fondo verde muy claro #F4F7F1 (60 %), verde bosque #1F3D2B (30 %) y acento terracota #C2410C (10 %), más verde #15803D para éxito, rojo #B91C1C para error y ámbar #B45309 para advertencia. El modo oscuro debe funcionar con una clase en la etiqueta html y guardar la preferencia. Usa máximo dos fuentes de Google Fonts: DM Serif Display para títulos y DM Sans para textos. Diseña mobile-first y usa al menos los prefijos sm, md y lg. Cumple con accesibilidad: textos alternativos en las imágenes, etiquetas en todos los campos, contraste mínimo de 4.5:1, foco visible en botones y enlaces, y atributos aria en el menú y el acordeón.

Formato de salida: Entrega un único archivo index.html con el JavaScript al final del body, el código indentado y comentarios en español que separen cada sección. Usa imágenes de ejemplo de Unsplash. Al final explica en una lista corta cómo abrir el archivo y qué partes debería personalizar.


Bitácora de prompts

Versión 1: se envió el prompt maestro a Claude y se obtuvo el archivo index.html con todas las secciones. Al abrirlo en el navegador y probarlo con las herramientas de desarrollador (F12) en tamaño celular, tablet y computador, se encontraron los problemas que se corrigieron en las siguientes iteraciones.

Iteración 1
Prompt de ajuste enviado: "Si abro el menú hamburguesa en celular y luego agrando la ventana a tamaño computador, el menú desplegable sigue abierto por debajo de la navbar. Haz que se cierre automáticamente cuando la pantalla llegue al tamaño lg."
Problema que buscaba resolver: el menú móvil quedaba abierto al cambiar el tamaño de la pantalla.
Resultado obtenido: se agregó un evento resize que cierra el menú cuando el ancho de la ventana es de 1024 px o más.
¿Funcionó?: Sí.

Iteración 2
Prompt de ajuste enviado: "Cuando navego con el teclado y abro el menú hamburguesa, no hay forma de cerrarlo sin volver al botón. Haz que se cierre con la tecla Escape y que el foco regrese al botón del menú."
Problema que buscaba resolver: accesibilidad del menú para personas que usan solo el teclado.
Resultado obtenido: se agregó un evento keydown que detecta la tecla Escape, cierra el menú y devuelve el foco al botón hamburguesa.
¿Funcionó?: Sí.

Iteración 3
Prompt de ajuste enviado: "Cuando envío el formulario vacío salen los errores en rojo, pero si corrijo un campo el mensaje de error sigue ahí hasta que vuelvo a darle enviar. Haz que el error de cada campo desaparezca apenas el usuario empiece a corregirlo."
Problema que buscaba resolver: los mensajes de error no se actualizaban mientras el usuario escribía, lo que confundía.
Resultado obtenido: se agregó un evento input a los campos de texto y un evento change a la lista desplegable, que borran el error del campo cuando el usuario lo modifica.
¿Funcionó?: Sí.

Iteración 4
Prompt de ajuste enviado: "En las preguntas frecuentes se pueden abrir las cuatro al mismo tiempo y la sección queda muy larga en celular. Haz que al abrir una pregunta se cierren las demás."
Problema que buscaba resolver: el acordeón ocupaba demasiado espacio en pantallas pequeñas.
Resultado obtenido: al hacer clic en una pregunta, el código recorre las demás, las cierra, actualiza su aria-expanded y quita la rotación del ícono.
¿Funcionó?: Sí.

Iteración 5
Prompt de ajuste enviado: "En el campo de número de personas el formulario acepta valores decimales como 2.5 y muestra el toast de enviado. Corrige la validación para que solo acepte números enteros entre 1 y 20."
Problema que buscaba resolver: la validación permitía un dato que no tiene sentido para una reserva.
Resultado obtenido: se cambió la validación para usar Number.isInteger y se actualizó el mensaje de error a "Indica un número entero entre 1 y 20."
¿Funcionó?: Sí.


Cambios manuales
1.
2.
3.


Pruebas
Pruebas responsive: se revisó el sitio en tamaño celular, tablet y computador con el modo responsive de las herramientas de desarrollador del navegador.
Validador W3C:
Lighthouse accesibilidad:


Cómo verlo localmente
Descargar el repositorio y abrir el archivo index.html en el navegador.
