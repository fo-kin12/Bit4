# Especificación de Requisitos de Software (ERS)
## BIT4 - Tienda de Vinilos y Colección de Ediciones Especiales

* **Versión:** 2.0
* **Fecha:** 08/11/2026
* **Estado:** Aprobado / En Desarrollo
* **Plataforma:** Aplicación Web Interactiva (Responsive Design)

---

## 1. Introducción

### 1.1. Propósito
El presente documento tiene como objetivo establecer, analizar y detallar los requisitos funcionales y no funcionales del sistema de software **BIT4**. Esta plataforma digital está concebida para operar como una tienda especializada en la venta de discos de vinilo de colección, rescatando el valor cultural del sonido analógico y la experiencia de posesión física frente al consumo efímero del streaming moderno. El documento sirve como guía formal para el diseño, desarrollo, pruebas y despliegue del software.

### 1.2. Alcance del Sistema
**BIT4** es una plataforma web orientada a coleccionistas, entusiastas de la música y melómanos. En su versión actual, el sistema permite:
1. Explorar un catálogo curado de álbumes históricos y los grandes clásicos de la música mundial.
2. Visualizar preventas y ediciones limitadas/numeradas equipadas con un contador de tiempo real para fomentar la exclusividad.
3. Facilitar la comunicación directa entre el comprador y la tienda mediante una pasarela de redirección a **WhatsApp**, emulando la cercanía de una tienda de discos tradicional ("mano a mano").

---

## 2. Descripción General del Producto

### 2.1. Perspectiva del Producto
**BIT4** funciona como un sitio web estático optimizado con componentes interactivos ligeros. Su arquitectura visual emplea una estética de modo oscuro (*Dark Mode*) con acentos neón y gradientes, transmitiendo una atmósfera nocturna, sofisticada y vinculada a la alta fidelidad musical.

### 2.2. Funciones Principales del Producto
* **Módulo de Inicio:** Bienvenida inmersiva con la filosofía de marca (*"Vinilos que inspiran"*) y accesos directos a los destacados.
* **Módulo de Catálogo General:** Visualización en cuadrícula responsiva de álbumes icónicos con información detallada (artista, título, descripción breve, precio y botón de compra).
* **Sistema de Filtrado Dinámico:** Pestañas de filtrado rápido por géneros musicales (*Clásicos, Rock, Jazz, Electrónica*).
* **Módulo de Preventas y Ediciones Especiales:** Sección dedicada a lanzamientos limitados con un contador regresivo interactivo (días, horas, minutos, segundos) programado mediante JavaScript nativo.
* **Canal de Venta Asistida (WhatsApp):** Automatización de enlaces de contacto directo con textos predefinidos para concretar transacciones, dudas de stock y métodos de envío.

### 2.3. Clases y Características de los Usuarios
* **Coleccionista / Comprador:** Usuario final con afinidad por el formato físico, interesado en la calidad de sonido, carátulas originales y ediciones numeradas. No requiere autenticación previa para navegar o iniciar el proceso de compra.
* **Administrador de la Tienda:** Operador encargado de actualizar el catálogo en el código fuente, gestionar el inventario físico y atender las solicitudes de compra que llegan a través del canal de WhatsApp.

### 2.4. Entorno Operativo y Tecnológico
* **Frontend:** HTML5 semántico, Bootstrap 5.3.x para maquetación responsiva, y CSS3 Custom Properties para la gestión centralizada de estilos y paleta de colores.
* **Interactividad:** JavaScript nativo (*Vanilla JS*) enfocado exclusivamente en la lógica del temporizador de preventas y la manipulación de elementos visuales en tiempo real.
* **Dispositivos Compatibles:** Computadores de escritorio, portátiles, tabletas y teléfonos inteligentes modernos.

---

## 3. Requisitos Funcionales

* **RF-01: Visualización del Catálogo.** El sistema debe renderizar tarjetas de productos estructuradas que incluyan la carátula oficial del disco, el nombre del artista, el título del álbum, una breve reseña histórica, el precio en pesos colombianos ($ COP) y un botón de acción de compra.
* **RF-02: Filtrado por Géneros.** La interfaz de catálogo debe proporcionar botones interactivos de filtrado (Todos, Clásicos, Rock, Jazz, Electrónica, Ediciones Especiales) para segmentar la visualización de los discos de manera inmediata.
* **RF-03: Temporizador de Preventas.** La sección de preventas debe integrar un contador en tiempo real con actualización segundo a segundo de los días, horas, minutos y segundos restantes antes del lanzamiento de una edición limitada.
* **RF-04: Redirección a WhatsApp (Proceso de Compra).** Al hacer clic en los botones de "Comprar" o "Reservar", el sistema debe abrir una pestaña externa con la API oficial de WhatsApp, enviando un mensaje preformateado que identifique inequívocamente el producto seleccionado por el usuario.

---

## 4. Requisitos No Funcionales

* **RNF-01: Rendimiento y Velocidad.** Al no utilizar bases de datos pesadas ni frameworks de JavaScript complejos en esta versión, el tiempo de carga inicial de la página debe ser inferior a 1.5 segundos.
* **RNF-02: Usabilidad y Diseño Responsivo.** El diseño debe adaptarse fluidamente a diferentes tamaños de pantalla (desde dispositivos móviles de 320px hasta pantallas 4K) utilizando las clases de rejilla de Bootstrap 5.
* **RNF-03: Mantenibilidad.** El código CSS debe estructurarse mediante variables personalizadas (`:root`) para facilitar cambios globales de color, tipografía o espaciados de forma limpia.

---

## 5. Restricciones y Fuera del Alcance (Versión 1.0)

Para garantizar la viabilidad y entrega ágil de esta primera versión del proyecto, se establecen explícitamente las siguientes exclusiones:
* ❌ No se implementarán pasarelas de pago automatizadas (tarjetas de crédito, PSE, pasarelas de terceros).
* ❌ No existirá un sistema de registro de usuarios, bases de datos relacionales o paneles de inicio de sesión (*Login*).
* ❌ El control de inventario de los vinilos se manejará de forma externa y manual a través del tendero por WhatsApp, no de forma automatizada en la web.
* ❌ No se desarrollarán aplicaciones móviles nativas para sistemas operativos iOS o Android.

---

## 6. Guía de Estilos y Paleta de Colores

* **Fondo Principal (`--bg-primary`):** `#060b1e` (Azul medianoche profundo).
* **Tarjetas y Contenedores (`--bg-card`):** `#0e1738` (Azul marino oscuro).
* **Texto Principal (`--text-main`):** `#ffffff` (Blanco puro).
* **Texto Secundario (`--text-muted`):** `#8a99ad` (Gris azulado).
* **Acentos Neón (`--accent-cyan`):** `#00d2ff` (Cyan brillante para elementos interactivos).
* **Gradientes de Acción (`--active-gradient`):** Gradiente dinámico de Violeta (`#7b2cbf`) a Cyan (`#00d2ff`).