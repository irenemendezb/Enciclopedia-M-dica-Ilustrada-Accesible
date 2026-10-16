# Enciclopedia Médica Ilustrada

Plataforma web de divulgación clínica, patologías y bienestar desarrollada bajo estándares internacionales de usabilidad y accesibilidad web (**WCAG 2.1 / 2.2** en sus niveles de conformidad **A, AA y AAA**).

**Autoras:** Lara Bañuls Martínez e Irene Méndez Botías  
Grado en Ingeniería Biomédica — Universidad de Alicante

---

## Descripción del Proyecto

Este proyecto consiste en el diseño, maquetación y desarrollo integral de un portal enciclopédico de divulgación médica accesible para todo tipo de usuarios, independientemente de sus capacidades físicas, visuales, auditivas o cognitivas, y optimizado para cualquier dispositivo.

La arquitectura de la web prioriza la claridad expositiva, la separación rigurosa entre contenido estructurado y diseño visual, y la ausencia de barreras de acceso a la información.

---

## Evolución y Registro de Trabajo por Sesiones

### Sesión 1: Estructura, Arquitectura de Información y Marcado Semántico
* **Estructuración Semántica Nativa:** Organización del sitio empleando puntos de referencia HTML5 (`<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<aside>`, `<footer>`).
* **Jerarquía de Contenidos:** Organización de títulos y subtítulos en una secuencia lógica estricta (`<h1>` a `<h3>`) sin saltos de nivel.
* **Tablas de Datos Clínicos:** Maquetación semántica de tablas informativas mediante `<caption>`, `<thead>`, `<tbody>`, `<th scope="col">` y `<th scope="row">` para asegurar la interpretación asistida por voz.
* **Formularios Accesibles:** Asociación unívoca entre controles y etiquetas mediante `<label for="...">`, con indicación textual explícita de campos obligatorios.
* **Accesibilidad Textual y Lingüística:** 
  * Declaración del idioma base (`lang="es"`) y marcado de términos técnicos y expresiones extranjeras (`lang="en"`).
  * Definición de acrónimos médicos especializados (OMS, BUN, TFG, LLA...) mediante etiquetas `<abbr title="...">`.
* **Recursos Gráficos y Multimedia:** Textos alternativos descriptivos en figuras anatómicas y descripciones contextuales para esquemas interactivos.

### Sesión 2: Arquitectura Modular CSS, Identidad Visual y Diseño Adaptativo
* **Modularización de Estilos:** Desacoplamiento de la presentación en hojas especializadas (`variables.css`, `base.css`, `layout.css` y `componentes.css`) unificadas mediante `@import` en `estilos.css`, facilitando la escalabilidad del sistema de diseño.
* **Variables y Tokens de Diseño:** Implementación de Custom Properties en `:root` para centralizar la escala cromática, espaciados y tipografías.
* **Cuidado Tipográfico y Legibilidad:**
  * Títulos: *Georgia*, aportando una impronta editorial, sobria y académica.
  * Cuerpo de texto: *Verdana*, tipografía de referencia en accesibilidad por su amplia altura de la 'x', apertura de glifos y distinción inequívoca de caracteres homólogos.
* **Paleta Cromática de Alto Contraste:** Selección de una escala en tonos ciruela y morado berenjena (`#441752`) sobre fondo claro (`#ffffff` / `#f8f6f9`), logrando ratios de contraste superiores a **14:1**, superando los requisitos del nivel AAA.
* **Navegación por Teclado y Foco Visible:** Contorno naranja ámbar (`#e65100`) de 3px con desplazamiento perimetral en la pseudoclase `:focus`, asegurando la visibilidad inmediata para usuarios que navegan sin ratón.
* **Enlace de Salto al Contenido (*Skip Link*):** Mecanismo accesible posicionado fuera de pantalla que emerge al tabular para obviar bloques de navegación repetitivos.
* **Optimización de Migas de Pan:** Inyección del separador decorativo exclusivamente vía CSS (`::before` con `content: ">"`), evitando la verbalización redundante en lectores de pantalla.
* **Diseño Adaptativo (*Responsive Design*):** Adaptación fluida del contenido a diferentes anchos de pantalla (desde teléfonos móviles de 480px hasta monitores de 1920px o superiores), incluyendo una maquetación a dos columnas en resoluciones de escritorio mediante *Flexbox* y *Media Queries*.
* **Interacción en Tablas y Formularios:** Estilo cebra para filas de datos, resaltado interactivo mediante `:hover` como guía visual de lectura horizontal, y alineación ordenada de controles en dos columnas.
* **Iconografía Híbrida y Accesible:** Empleo de iconos vectoriales con `aria-hidden="true"` para elementos decorativos y caracteres Unicode nativos integrados en formularios.

---

## Estructura del Repositorio

```text
├── P4LaraIrene/                      # Versión de estructura y marcado semántico inicial
│   ├── P4/                           # Archivos HTML y recursos
│   └── informeaccesibilidad (2).pdf  # Informe técnico de accesibilidad inicial
│
├── P5LaraIrene/                      # Versión con capa de diseño visual y responsive
│   ├── P5/                           # Sitio completo
│   │   ├── css/                      # Hojas de estilo modulares
│   │   │   ├── variables.css         # Tokens de diseño y variables globales
│   │   │   ├── base.css              # Reseteo, tipografía base y skip-link
│   │   │   ├── layout.css            # Estructura general, menú A-Z y media queries
│   │   │   ├── componentes.css       # Tablas cebra, formularios y migas de pan
│   │   │   └── estilos.css           # Archivo maestro agregador
│   │   ├── A/                        # Sección y artículos de la letra A
│   │   ├── I/                        # Sección y artículos de la letra I
│   │   ├── L/                        # Sección y artículos de la letra L
│   │   ├── error/                    # Página de error 404 accesible
│   │   ├── imagenes/                 # Esquemas anatómicos e ilustraciones
│   │   ├── index.html                # Portada con maquetación en dos columnas
│   │   ├── buscador.html             # Buscador clínico con campos alineados
│   │   ├── contacto.html             # Formulario de contacto
│   │   ├── sugerencias.html          # Formulario de aportaciones y valoración
│   │   ├── Mapa.html                 # Mapa del sitio estructurado
│   │   └── accesibilidad.html        # Declaración formal de accesibilidad
│   └── Informe_Accesibilidad_P5.tex  # Documento técnico de validación WCAG
│
├── Guia_Defensa_P5_CSS.tex           # Documento de estudio y fundamentación técnica
└── README.md                         # Documentación general del repositorio
```

---

## Resumen de Criterios de Accesibilidad (WCAG 2.1 / 2.2)

| Criterio | Nombre | Nivel | Implementación Técnica |
| :--- | :--- | :---: | :--- |
| **1.1.1** | Non-text Content | A | Iconos decorativos con `aria-hidden="true"` y símbolos Unicode con etiquetas descriptivas. |
| **1.3.1** | Info and Relationships | A | Separadores de migas de pan generados por CSS mediante `::before` para evitar ruido en lectores de pantalla. |
| **1.3.4** | Orientation | AA | Diseño adaptativo operativo sin restricciones tanto en orientación vertical como horizontal. |
| **1.4.1** | Use of Color | A | Enlaces subrayados por defecto (`text-decoration: underline`); los avisos combinan color, bordes diferenciados e iconos. |
| **1.4.3** | Contrast (Minimum) | AA / AAA | Ratios de contraste superiores a 14:1 en títulos y 16:1 en texto general, superando holgadamente el mínimo de 4.5:1. |
| **1.4.10** | Reflow | AA | Contenido adaptable a pantallas estrechas (hasta 320px/480px) sin forzar desplazamiento horizontal bidimensional. |
| **2.4.1** | Bypass Blocks | A | Enlace *Skip Link* al inicio de cada página visible con el foco de teclado. |
| **2.4.7** | Focus Visible | AA | Indicador de foco de alto contraste (`outline: 3px solid #e65100; outline-offset: 2px;`) activo en todos los controles interactivos. |
| **2.5.8** | Target Size (Minimum) | AA | Dimensiones táctiles de al menos 32px en botones de navegación y 44px de altura en botones de formularios. |

---

## Licencia

Proyecto desarrollado con fines académicos y de investigación en accesibilidad web — Universidad de Alicante.
