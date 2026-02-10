# Investigación Técnica: Funcionalidades Nativas en HTML y CSS

Este repositorio contiene la implementación práctica y el análisis técnico de tres novedades recientes en los estándares web: la propiedad CSS `field-sizing`, el elemento semántico `<search>` y el atributo de control de renderizado `blocking="render"`.

## Objetivos de la Práctica
El propósito de este proyecto es demostrar cómo las nuevas especificaciones de la W3C permiten sustituir soluciones históricamente dependientes de JavaScript por implementaciones nativas más eficientes, accesibles y fáciles de mantener.

## Novedades Implementadas

### 1. CSS field-sizing: content
Tradicionalmente, para conseguir que un elemento `textarea` o un `input` ajustara su tamaño automáticamente al contenido introducido por el usuario, era imprescindible recurrir a scripts que calcularan el `scrollHeight` en cada evento de entrada.

Mediante la implementación de `field-sizing: content`, el navegador asume la responsabilidad del cálculo del layout, permitiendo que el elemento crezca o decrezca de forma intrínseca. Esto reduce la carga en el hilo principal (main thread) y simplifica el código CSS.

### 2. Elemento HTML <search>
Este elemento representa una sección de un documento que contiene funcionalidades de búsqueda. A diferencia de un `div` genérico, `<search>` proporciona una capa semántica nativa que:
- Mejora la accesibilidad para tecnologías de asistencia (lectores de pantalla) sin necesidad de atributos ARIA adicionales (`role="search"`).
- Organiza de forma lógica el formulario de consulta y los resultados asociados.

### 3. Atributo blocking="render"
Se ha aplicado este atributo en la carga de recursos críticos. Su función es asegurar que el motor de renderizado del navegador no inicie el pintado de la interfaz hasta que el recurso especificado haya sido procesado por completo, mitigando el efecto FOUC (Flash of Unstyled Content).

## Implementación Técnica
El código se ha estructurado en un ejemplo de interfaz de usuario que incluye:
- Un motor de búsqueda semántico.
- Un área de entrada de datos dinámica.
- Una hoja de estilos optimizada para demostrar el comportamiento intrínseco de los nuevos valores de dimensionamiento.

## Requisitos de Visualización
Debido a la naturaleza reciente de estas especificaciones, para una correcta visualización de la propiedad `field-sizing`, se recomienda utilizar versiones de navegadores basadas en Chromium (Chrome, Edge o Brave) superiores a la versión 123. En navegadores que no soporten estas propiedades, el sistema aplicará una degradación elegante (progressive enhancement), manteniendo la funcionalidad básica con dimensiones estáticas.

## Autor
[Tu Nombre y Apellidos]
Fecha de entrega: Febrero 2026
