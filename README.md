# 🎵 BIT4 - Tienda de Vinilos y Colección

> *"Vinilos que inspiran"* — Rescatando la tradición, el ritual de escuchar música y el valor de poseer la obra en tus manos.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![Bootstrap 5](https://img.shields.io/badge/Bootstrap_5-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

---

## 🎧 ¿Qué es BIT4?

En una época donde la música se consume de forma efímera y fría a través de plataformas de streaming digital, **BIT4** nace como un refugio analógico para los verdaderos coleccionistas. Aquí no solo buscas una canción y ya; revivimos la experiencia de buscar en las tiendas de barrio, hojear carátulas icónicas y darle un verdadero sentido y valor cultural a la música.

Este proyecto web está diseñado para exhibir grandes clásicos de la historia musical, preventas con ediciones limitadas y un canal de comunicación directo y humano (*"mano a mano"*) tal como se hacía antes.

---

## 🛠️ Tecnologías Utilizadas

El proyecto está desarrollado con un enfoque ligero, rápido y sin dependencias pesadas de backend para esta primera versión:
* **HTML5** (Estructura semántica).
* **Bootstrap 5.3** (Diseño responsivo, grillas y componentes).
* **CSS3 Custom Properties (`:root`)** (Gestión de paleta de colores oscura y efectos neón).
* **JavaScript (Vanilla)** (Lógica del temporizador interactivo en tiempo real para preventas).

---

## 🎨 Paleta de Colores y Estética

El diseño implementa un modo oscuro (*Dark Mode*) con iluminación y gradientes inspirados en la atmósfera nocturna de los clubes de jazz y rock:
* **Fondo Principal (`--bg-primary`):** `#060b1e` (Azul medianoche profundo)
* **Tarjetas y Contenedores (`--bg-card`):** `#0e1738` (Azul marino)
* **Acentos Neón (`--accent-cyan`):** `#00d2ff` (Brillo tecnológico y branding)
* **Gradiente Activo (`--active-gradient`):** Gradiente dinámico de Violeta (`#7b2cbf`) a Cyan (`#00d2ff`)

---

## 📂 Estructura del Repositorio

```text
BIT4/
├── index.html              # Página principal original
├── catalogo.html           # Vista principal del catálogo de vinilos
├── style.css               # Estilos principales corporativos
├── README.md               # Documentación oficial del proyecto
├── Rthriller.jpg           # Recurso de preventa o destacado
├── pg/                     # [NUEVO] Carpeta desorganizada creada por el equipo
│   ├── pagDiscos.html      # Página de discos añadida recientemente
│   └── css/                # Subcarpeta de estilos innecesaria
│       └── style.css       # Estilos específicos de esa vista
├── imagenes/               # Carpeta de recursos visuales de las carátulas
│   ├── Michael_Jackson.png # Portada de Thriller
│   ├── Back_in_Black.jpg   # Portada de Back In Black
│   ├── dark.jpg            # Portada de The Dark Side of the Moon
│   ├── eagles.jpg          # Portada de Their Greatest Hits (Eagles)
│   ├── nirvana.jpg         # Portada de Nirvana (Nevermind)
│   └── led_zeppelin.jpg    # Portada de Led Zeppelin
└── docs/                   # Documentación formal de ingeniería (Docs-as-Code)
    ├── ERS.md              # Especificación de Requisitos de Software (v2.0)
    └── USER_STORIES.md     # Product Backlog e Historias de Usuario
