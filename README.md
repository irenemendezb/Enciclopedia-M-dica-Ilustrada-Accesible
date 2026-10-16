<div align="center">

# Enciclopedia Médica Ilustrada
### Portal Web Clínico Accesible y Adaptativo

[![Estándar - W3C HTML5](https://img.shields.io/badge/W3C-HTML5_Semántico-E34F26?style=for-the-badge&logo=html5&logoColor=white)](#)
[![Estándar - CSS3 Modular](https://img.shields.io/badge/CSS3-Modular_Custom_Properties-1572B6?style=for-the-badge&logo=css3&logoColor=white)](#)
[![Accesibilidad - WCAG 2.2](https://img.shields.io/badge/WCAG_2.2-Nivel_AA_/_AAA-441752?style=for-the-badge&logo=w3c&logoColor=white)](#)
[![Diseño - Responsive](https://img.shields.io/badge/Layout-Responsive_Design-028090?style=for-the-badge)](#)
[![Área - Ingeniería Biomédica](https://img.shields.io/badge/Área-Ingeniería_Biomédica-e65100?style=for-the-badge)](#)

<p align="center">
  <b>Universidad de Alicante</b> • Grado en Ingeniería Biomédica<br>
  <b>Autoras:</b> Lara Bañuls Martínez & Irene Méndez Botías
</p>

</div>

---

## Resumen Ejecutivo

La **Enciclopedia Médica Ilustrada** es una plataforma web desarrollada con el propósito de divulgar información clínica rigurosa, accesible y comprensible para toda la ciudadanía. El proyecto implementa una arquitectura basada en los estándares del Consorcio W3C y garantiza el cumplimiento estricto de las pautas de accesibilidad **WCAG 2.1 / 2.2** en sus niveles de conformidad **A, AA y AAA**.

Su diseño prescinde de dependencias externas pesadas o plantillas prefabricadas, apostando por una estructura semántica pura, un sistema de estilos modular desacoplado y una identidad visual sobria de alta legibilidad.

---

## Identidad Visual y Ergonomía de Lectura

### Paleta Cromática Institucional (Verificación WCAG)

| Muestra | Rol del Color | Código Hex | Fondo Evaluado | Ratio de Contraste | Nivel WCAG |
| :---: | :--- | :---: | :---: | :---: | :---: |
| <img src="https://via.placeholder.com/24/441752/441752.png" width="18" height="18" alt="#441752"> | **Cabeceras y Títulos** | `#441752` | `#ffffff` | **14.4 : 1** | **Supera AAA** (mín. 7.0:1) |
| <img src="https://via.placeholder.com/24/221d24/221d24.png" width="18" height="18" alt="#221d24"> | **Texto de Lectura** | `#221d24` | `#ffffff` | **16.6 : 1** | **Supera AAA** (mín. 7.0:1) |
| <img src="https://via.placeholder.com/24/5c1d73/5c1d73.png" width="18" height="18" alt="#5c1d73"> | **Hipervínculos** | `#5c1d73` | `#ffffff` | **11.9 : 1** | **Supera AAA** (con subrayado) |
| <img src="https://via.placeholder.com/24/e65100/e65100.png" width="18" height="18" alt="#e65100"> | **Foco de Teclado Activo** | `#e65100` | `#ffffff` / `#441752` | **4.7 : 1 / 3.5 : 1** | **Cumple AA** (visibilidad alta) |
| <img src="https://via.placeholder.com/24/f8f6f9/f8f6f9.png" width="18" height="18" alt="#f8f6f9"> | **Fondo General Suave** | `#f8f6f9` | - | - | Atenúa fatiga visual |

### Maridaje Tipográfico Editorial

* **Títulos (`h1` a `h6`, leyendas y cabeceras de tabla):** `"Georgia", "Times New Roman", Cambria, serif`  
  Aporta una estética académica y editorial formal, característica de publicaciones clínicas y enciclopédicas serias.
* **Cuerpo de texto (`p`, listas, tablas y formularios):** `"Verdana", "Geneva", "Tahoma", sans-serif`  
  Tipografía referente en accesibilidad digital por su amplia altura de la «x», gran apertura entre glifos y nítida distinción entre caracteres homólogos (`I`, `l`, `1`).

---

## Estructura del Repositorio

```text
.
├── css/
│   ├── variables.css          # Tokens de diseño y variables globales (:root)
│   ├── base.css               # Reseteo de caja universal, tipografía y skip-link
│   ├── layout.css             # Maquetación estructural, menú A-Z y Media Queries
│   ├── componentes.css        # Tablas cebra, formularios alineados y migas de pan
│   └── estilos.css            # Hoja maestra agregadora con directivas @import
│
├── A/
│   ├── indice_a.html          # Directorio de patologías con inicial A
│   └── anafilaxia.html        # Monografía clínica sobre Anafilaxia
│
├── I/
│   ├── indice_i.html          # Directorio de patologías con inicial I
│   └── insuficiencia_renal.html # Monografía clínica sobre Insuficiencia Renal
│
├── L/
│   ├── indice_l.html          # Directorio de patologías con inicial L
│   ├── leucemia.html          # Monografía clínica sobre Leucemia
│   └── linfoma_hodgkin.html   # Monografía clínica sobre Linfoma de Hodgkin
│
├── error/
│   └── error.html             # Página de estado y navegación alternativa (404)
│
├── imagenes/                  # Esquemas anatómicos e ilustraciones clínicas
├── index.html                 # Portada principal con maquetación en dos columnas
├── buscador.html              # Buscador de patologías con controles alineados
├── contacto.html              # Formulario de consulta clínica accesible
├── sugerencias.html           # Buzón de valoración y propuestas de artículos
├── Mapa.html                  # Índice jerárquico del sitio web
└── accesibilidad.html         # Declaración institucional de accesibilidad
```

---

## Registro Técnico de Trabajo por Sesiones

<details open>
<summary><b>🔹 Sesión 1: Arquitectura de la Información y Marcado Semántico</b> (Desplegar / Plegar)</summary>
<br>

* **Estructura HTML5 Estándar:** Empleo sistemático de etiquetas semánticas (`<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<aside>`, `<footer>`) que habilitan puntos de referencia (*landmarks*) para navegación asistida.
* **Jerarquía de Encabezados:** Estructuración de la información mediante títulos ordenados lógicamente sin saltos de nivel (`<h1>` a `<h3>`).
* **Tablas de Datos Clínicos:** Codificación accesible de tablas de patologías incorporando etiquetas `<caption>`, `<thead>`, `<tbody>`, y cabeceras asociadas mediante atributos `scope="col"` y `scope="row"`.
* **Formularios Semánticos:** Agrupación temática mediante `<fieldset>` y `<legend>`, vinculación explícita de controles a través de `<label for="...">` e indicación textual obligatoria.
* **Atributos de Idioma y Glosario:** Identificación del idioma global (`lang="es"`), etiquetado de terminología foránea (`lang="en"`) y desambiguación de abreviaturas médicas mediante `<abbr title="...">`.

</details>

<details open>
<summary><b>🔹 Sesión 2: Sistema de Diseño Modular CSS, Responsive y Accesibilidad Visual</b> (Desplegar / Plegar)</summary>
<br>

* **Arquitectura CSS Modular:** Distribución del código en 4 ficheros especializados (`variables.css`, `base.css`, `layout.css` y `componentes.css`) enlazados a través de `@import` en `estilos.css`.
* **Diseño Adaptativo (*Responsive*):** Incorporación de la metaetiqueta viewport e implementación de *Media Queries* fluidas para dispositivos móviles (desde 480px) hasta pantallas panorámicas (1920px o superiores), con distribución a dos columnas en escritorio.
* **Foco Visual de Alto Contraste (WCAG 2.4.7):** Indicador de foco perimetral de 3px (`outline: 3px solid #e65100; outline-offset: 2px;`) que garantiza la visibilidad al navegar por teclado mediante `Tab`.
* **Enlace de Salto (*Skip Link* - WCAG 2.4.1):** Enlace oculto fuera de pantalla que se visibiliza al enfocar, permitiendo omitir la barra de navegación recurrente alfabética A--Z.
* **Migas de Pan sin Ruido Auditivo (WCAG 1.3.1):** Sustitución de caracteres literales en HTML por inyección visual vía CSS (`::before` con `content: ">"`), evitando que los lectores de pantalla vocalicen «mayor que».
* **Interacción en Tablas:** Regla `border-collapse: collapse`, alternancia de filas cebra para facilitar el seguimiento visual horizontal y respuesta interactiva al cursor mediante la pseudoclase `:hover`.
* **Alineación de Formularios:** Disposición en dos columnas para etiquetas y controles sin el empleo de tablas decorativas, garantizando áreas táctiles mínimas de 44px de altura en botones (WCAG 2.5.8).
* **Iconografía Accesible:** Combinación de iconos vectoriales acompañados de `aria-hidden="true"` para elementos decorativos y caracteres Unicode nativos integrados en controles clínicos.

</details>

---

## Tabla de Conformidad con Estándares WCAG 2.1 / 2.2

<details open>
<summary><b>🔹 Matriz de Criterios de Éxito Aplicados</b> (Desplegar / Plegar)</summary>
<br>

| Criterio | Denominación Oficial | Nivel | Justificación e Implementación Técnica |
| :---: | :--- | :---: | :--- |
| **1.1.1** | Non-text Content | **A** | Iconografía decorativa con `aria-hidden="true"` y símbolos Unicode con etiquetas descriptivas asociadas. |
| **1.3.1** | Info and Relationships | **A** | Separadores de migas de pan generados mediante pseudoelementos `::before` para evitar ruido auditivo. |
| **1.3.4** | Orientation | **AA** | Maquetación adaptativa que permite visualización en orientación horizontal y vertical sin bloqueo de pantalla. |
| **1.4.1** | Use of Color | **A** | Enlaces con subrayado visible permanente (`text-decoration: underline`); los avisos combinan color, borde e iconos. |
| **1.4.3** | Contrast (Minimum) | **AA / AAA** | Contraste de 14.4:1 en encabezados y 16.6:1 en texto general, superando holgadamente el requisito de 4.5:1. |
| **1.4.10** | Reflow | **AA** | Contenido adaptable a pantallas estrechas (hasta 320px) sin forzar desplazamiento horizontal bidimensional. |
| **2.4.1** | Bypass Blocks | **A** | Mecanismo *Skip Link* al inicio de cada página visible exclusivamente bajo foco de teclado. |
| **2.4.7** | Focus Visible | **AA** | Indicador de foco evidente de alto contraste (`outline: 3px solid #e65100; outline-offset: 2px;`) en todos los controles interactivos. |
| **2.5.8** | Target Size (Minimum) | **AA** | Zonas interactivas con áreas mínimas de 32px en botones del abecedario y 44px de altura en botones de formulario. |

</details>

---

<div align="center">
  <sub>Desarrollado con fines académicos y de divulgación clínica • Grado en Ingeniería Biomédica (Universidad de Alicante)</sub>
</div>
