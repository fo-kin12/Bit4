# Product Backlog e Historias de Usuario (Versión Extendida)
## BIT4 - Tienda de Vinilos y Colección de Ediciones Especiales

Este documento detalla el Product Backlog completo, compuesto por Épicas, Historias de Usuario (User Stories), Criterios de Aceptación y Reglas de Negocio del sistema **BIT4**. Su propósito es estructurar el desarrollo ágil priorizando la experiencia del coleccionista analógico, la exploración musical y la atención personalizada.

---

## 📋 Resumen de Épicas del Proyecto

1. **Épica 1: Experiencia de Inicio e Identidad Visual (Branding)**
2. **Épica 2: Catálogo de Clásicos y Sistema de Filtrado Dinámico**
3. **Épica 3: Preventas, Ediciones Limitadas y Temporizador en Tiempo Real**
4. **Épica 4: Pasarela de Atención y Cierre de Venta "Mano a Mano" (WhatsApp)**
5. **Épica 5: Optimización de Interfaz y Diseño Responsivo**

---

## 🚀 Detalle de Historias de Usuario y Criterios de Aceptación

---

### Épica 1: Experiencia de Inicio e Identidad Visual (Branding)

#### HU-01: Inmersión en la Propuesta de Valor y Estética Nocturna
* **Como** coleccionista de música nostálgico y amante del formato físico,
* **Quiero** ingresar a una página web con una interfaz oscura y acentos neón que evoque la mística de un club o tienda de discos clásica,
* **Para** sentirme inmediatamente conectado con la cultura del vinilo y la preservación de la tradición musical frente al streaming masivo.

* **Criterios de Aceptación:**
  1. La aplicación web debe implementar la paleta de colores corporativa basada en variables CSS (`:root`), destacando fondos en azul medianoche (`#060b1e`) y tarjetas en azul marino (`#0e1738`).
  2. El encabezado principal debe mostrar de forma prominente el eslogan de la marca: *"Vinilos que inspiran"*.
  3. La tipografía principal debe garantizar una legibilidad óptima utilizando fuentes institucionales combinadas con acentos modernos.

---

### Épica 2: Catálogo de Clásicos y Sistema de Filtrado Dinámico

#### HU-02: Visualización de Álbumes Históricos en Tarjetas de Catálogo
* **Como** usuario apasionado por la historia de la música,
* **Quiero** visualizar un catálogo estructurado en tarjetas uniformes que muestren la carátula oficial del disco, el artista, el título del álbum, una breve reseña, el precio y un botón de acción rápida,
* **Para** identificar de un vistazo los discos icónicos que deseo añadir a mi colección personal.

* **Criterios de Aceptación:**
  1. Cada tarjeta de vinilo (`card-vinyl`) debe contener una imagen de portada de alta resolución (ej. *Thriller*, *Back in Black*, *Dark Side of the Moon*, *Their Greatest Hits*).
  2. El precio del producto debe reflejarse claramente en pesos colombianos ($ COP) con formato estándar.
  3. Las tarjetas deben mantener una distribución simétrica adaptable mediante el sistema de grillas de Bootstrap 5 (`col-md-6`).

#### HU-03: Filtrado Rápido por Géneros Musicales
* **Como** coleccionista enfocado en un estilo o género particular,
* **Quiero** hacer clic en botones de filtro rápido ubicados en la barra superior (Todos, Clásicos, Rock, Jazz, Electrónica, Ediciones Especiales),
* **Para** segmentar la visualización del inventario y encontrar los álbumes de mi interés sin fricciones.

* **Criterios de Aceptación:**
  1. Los botones de filtro deben adoptar un diseño de píldora redondeada (`rounded-pill`).
  2. Al seleccionar un filtro, este debe aplicar de forma dinámica un gradiente visual activo (`--active-gradient`) para indicar el estado seleccionado al usuario.

---

### Épica 3: Preventas, Ediciones Especiales y Temporizador

#### HU-04: Temporizador Regresivo para Lanzamientos Exclusivos
* **Como** coleccionista ávido de piezas raras y ediciones numeradas,
* **Quiero** visualizar un contador regresivo en tiempo real (días, horas, minutos, segundos) en la sección de preventas,
* **Para** conocer con exactitud el tiempo disponible antes de que se agoten las copias limitadas de un nuevo lanzamiento en vinilo translúcido.

* **Criterios de Aceptación:**
  1. La sección de preventas debe integrar un script de JavaScript nativo que calcule la diferencia horaria entre el momento actual y la fecha límite de lanzamiento.
  2. El contador debe actualizarse de forma fluida segundo a segundo de manera automática en pantalla.
  3. Si la fecha de la preventa expira, el script debe contemplar una condición de seguridad para mantener los valores en cero (`00`) e impedir errores en el renderizado.

---

### Épica 4: Pasarela de Atención y Cierre de Venta (WhatsApp)

#### HU-05: Redirección Asistida a WhatsApp para Compra Personalizada
* **Como** comprador interesado en adquirir un vinilo o asegurar una preventa,
* **Quiero** hacer clic en el botón "Comprar" o "Reservar" de un disco específico,
* **Para** ser redirigido instantáneamente a un chat directo de WhatsApp con el tendero y coordinar el pago y el envío "mano a mano", rescatando la cercanía de las antiguas tiendas de barrio.

* **Criterios de Aceptación:**
  1. Los botones de compra y reserva deben estar enlazados mediante la API oficial de mensajes de WhatsApp (`https://wa.me/...`).
  2. El enlace debe generar un mensaje automatizado y preformateado que indique el nombre exacto del disco consultado por el usuario.
  3. El flujo de compra no debe exigir registros de usuario ni pasarelas de pago automatizadas complejas, cumpliendo con la arquitectura ligera de la Versión 1.0.

---

### Épica 5: Optimización de Interfaz y Diseño Responsivo

#### HU-06: Adaptabilidad multidispositivo (Responsive Design)
* **Como** usuario que navega desde su teléfono móvil o computadora portátil,
* **Quiero** que todos los elementos de la interfaz (menú de navegación, barra de búsqueda, tarjetas de vinilos y contadores) se adapten automáticamente al tamaño de mi pantalla,
* **Para** poder consultar el catálogo y hacer reservas desde cualquier lugar sin perder calidad visual.

* **Criterios de Aceptación:**
  1. La barra de navegación debe incluir un menú colapsable tipo hamburguesa (`navbar-toggler`) para dispositivos móviles.
  2. Las imágenes y contenedores deben utilizar clases responsivas de Bootstrap (`img-fluid`, `object-fit-cover`) para evitar desbordamientos visuales.