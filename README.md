# KARIO Media — Panel Digital (HTML + CSS)

Proyecto frontend **estático y modular** desarrollado únicamente con **HTML y CSS** para el panel digital de **KARIO Media**. Este sistema permite visualizar, añadir, eliminar y reportar indicadores (KPI) dentro de una interfaz limpia, responsive y reutilizable, manteniendo el diseño original sin depender de JavaScript.

---

## Objetivo del Proyecto

Construir una interfaz web profesional que sirva como base visual y estructural para un futuro sistema con backend, permitiendo:

* Autenticación visual (login)
* Bienvenida personalizada al usuario
* Visualización de indicadores (KPI)
* Creación de nuevos indicadores
* Eliminación de indicadores existentes
* Envío de reportes y solicitudes de ayuda

Todo el proyecto está diseñado bajo principios de:

* **Modularidad CSS**
* **Reutilización de componentes**
* **Responsive Design (Mobile First)**
* **Accesibilidad básica**
* **Código limpio y mantenible**

***Pagina para visualizar el proyecto:*** https://ayuda-de-proyecto.netlify.app/
---

## Tecnologías Utilizadas

* **HTML5** — Estructura semántica de las vistas
* **CSS3** — Diseño, animaciones, responsive y sistema de estilos
* **Figma** — Prototipado visual y sistema de componentes

> Nota: Este proyecto no utiliza JavaScript por diseño. Está preparado para integrarse posteriormente con cualquier backend (Node.js, PHP, Python, .NET, etc.).

---

## Estructura del Proyecto

```
kario-modular/
├── index.html              # Página de login
├── inicio.html             # Pantalla de bienvenida
├── portafolio.html         # Panel de indicadores (dashboard)
├── anadir.html             # Formulario añadir indicador
├── eliminar.html           # Página eliminar indicadores
├── reporte.html            # Formulario reportar problema
├── ayuda.html              # Formulario de contacto/ayuda
│
├── styles/
│   ├── base/
│   │   ├── reset.css       # Reset CSS + Variables globales
│   │   └── animations.css  # Animaciones reutilizables
│   │
│   ├── components/
│   │   ├── header.css      # Header y navegación
│   │   ├── layouts.css     # Layouts comunes (container, sections)
│   │   ├── forms.css       # Estilos de formularios
│   │   ├── buttons.css    # Estilos de botones
│   │   └── tables.css     # Tablas KPI
│   │
│   └── pages/
│       ├── responsive.css  # Media queries responsive
│       ├── login.css       # Específico página login
│       ├── inicio.css     # Específico pantalla inicio
│       ├── anadir.css     # Específico página añadir
│       ├── eliminar.css   # Específico página eliminar
│       ├── reporte.css    # Específico página reporte
│       └── contacto.css   # Específico página ayuda
│
└── assets/
    └── img/               # Imágenes del proyecto
```

---

## Arquitectura CSS

El proyecto utiliza una **arquitectura por capas**, separando estilos globales, componentes reutilizables y estilos específicos por página.

### 1. Base (`styles/base/`)

Contiene la configuración global del sistema visual.

### `reset.css`

Responsabilidades:

* Reset de márgenes y paddings
* Definición de variables CSS globales
* Tipografía base
* Colores del sistema
* Bordes, radios y sombras estándar

Ejemplo de variables:

```css
:root {
  --color-primary: #ff7a1a;
  --color-text: #1f1f1f;
  --color-muted: #8c8c8c;
  --color-border: #e6e6e6;

  --radius-sm: 8px;
  --radius-md: 16px;
  --radius-lg: 24px;

  --shadow-soft: 0 8px 24px rgba(0,0,0,0.1);
}
```

### `animations.css`

Incluye animaciones reutilizables como:

* Fade In
* Slide Up
* Hover transitions
* Micro-interacciones de botones

---

### 2. Componentes (`styles/components/`)

Aquí se definen los bloques reutilizables en todas las páginas.

### `header.css`

Controla:

* Barra superior
* Logo central
* Acciones (Añadir, Refrescar, Eliminar, Reportar, Ayuda)
* Avatar de usuario
* Menú desplegable (Cerrar sesión)

### `layouts.css`

Maneja:

* Contenedores centrados
* Sistema de grids
* Espaciados estándar
* Secciones
* Wrappers responsive

### `forms.css`

Incluye estilos para:

* Inputs
* Selects
* Labels
* Textareas
* Mensajes de ayuda
* Estados focus y disabled

### `buttons.css`

Define variantes:

* Botón primario (naranja)
* Botón secundario (gris)
* Botón peligro (rojo)

Estados:

* Hover
* Active
* Disabled
* Focus-visible

### `tables.css`

Controla el diseño del panel de indicadores:

* Filas tipo card
* Columnas
* Indicadores circulares de porcentaje
* Acciones por fila

---

### 3. Páginas (`styles/pages/`)

Cada archivo solo contiene estilos exclusivos de su pantalla.

| Archivo          | Función                                         |
| ---------------- | ----------------------------------------------- |
| `login.css`      | Fondo, centrado del card y formulario de acceso |
| `inicio.css`     | Layout de bienvenida y perfil                   |
| `anadir.css`     | Formulario de creación de indicadores           |
| `eliminar.css`   | Tabla con selección múltiple                    |
| `reporte.css`    | Formulario de reporte de problemas              |
| `contacto.css`   | Página de ayuda y contacto                      |
| `responsive.css` | Media queries globales                          |

---

## Pantallas del Sistema

### 1. Login (`index.html`)

![Panel KARIO Media](https://i.ibb.co/9k0q9gg6/image.png)

Función:

* Entrada visual del sistema
* Validación visual de usuario y contraseña

Elementos:

* Card central
* Inputs de usuario y contraseña
* Botón de acceso
* Mensaje de ayuda

---

### 2. Bienvenida (`inicio.html`)
![Panel KARIO Media](https://i.ibb.co/B2c2cW8p/image.png)
Función:

* Mostrar usuario autenticado
* Rol dentro del sistema

Elementos:

* Avatar circular
* Nombre completo
* Rol del usuario

---

### 3. Panel de Indicadores (`portafolio.html`)
![Panel KARIO Media](https://i.ibb.co/KcYnRQZF/image.png)
Función:

* Visualizar indicadores KPI

Incluye:

* Nombre del indicador
* Descripción
* Categoría
* Fechas
* Fórmula
* Frecuencia
* Porcentaje de cumplimiento
* Área responsable

---

### 4. Añadir Indicador (`anadir.html`)
![Panel KARIO Media](https://i.ibb.co/n8b5W0tg/image.png)
Formulario dividido en secciones:

* Información básica
* Fechas y plazos
* Métricas y seguimiento

Campos:

* Nombre
* Descripción
* Categoría
* Área
* Fechas
* Fórmula
* Frecuencia
* Objetivo

---

### 5. Eliminar Indicadores (`eliminar.html`)
![Panel KARIO Media](https://i.ibb.co/SwLgK9rC/image.png)
Función:

* Selección múltiple
* Eliminación visual de indicadores

Incluye:

* Checkbox por fila
* Botón de confirmación

---

### 6. Reportar (`reporte.html`)
![Panel KARIO Media](https://i.ibb.co/B2c2cW8p/image.png)
Formulario de soporte técnico:

* Información personal
* Tipo de problema
* Prioridad
* Descripción
* Pasos para reproducir

---

## Responsive Design

El sistema está diseñado para funcionar en:

* Desktop (≥ 1024px)
* Tablet (768px – 1023px)
* Mobile (≤ 480px)

### Estrategias usadas

* Cards con `max-width` y `width: 100%`
* Inputs con `flex-grow`
* Tablas KPI con scroll horizontal controlado en móvil
* Header adaptable (wrap o compactación de acciones)

Breakpoints recomendados:

```css
@media (max-width: 1024px) {}
@media (max-width: 768px) {}
@media (max-width: 480px) {}
```

---

## Accesibilidad

Implementado:

* Estados `:focus-visible`
* Labels asociados a inputs
* Tamaño mínimo de interacción (44px)
* Contraste alto en textos y botones

---

## Convención de Clases

Formato:

```
componente__elemento--modificador
```

Ejemplos:

* `btn--primary`
* `header__menu`
* `form__input`
* `table__row--active`

---

## Flujo de Desarrollo Recomendado

1. Ajustar diseño en Figma
2. Crear estructura HTML semántica
3. Aplicar estilos base
4. Conectar componentes
5. Ajustar responsive
6. Validar accesibilidad

---

## Preparado para Backend

Este proyecto puede integrarse con:

* Node.js (Express, Nest)
* PHP (Laravel)
* Python (FastAPI, Django)
* .NET

Los formularios están listos para:

* POST de datos
* Autenticación real
* Gestión de sesiones

---

## Autor

Desarrollado para **KARIO Media**
Frontend modular — HTML + CSS

---

## Licencia

Proyecto de uso educativo y/o interno. Redistribución y uso comercial bajo autorización del autor.
