# Actividad de GitHub Classroom: Propuesta de Práctica Temática (Enfoque en Documentación)

## 1) Título

**Diseño de Mini Práctica Temática en Sistemas (Documentación Primero)**

> Ejemplos de títulos que podrías usar para tu proyecto:
> - “Mini Toolkit en ARM64”
> - “Asistente de Estudio en Terminal”
> - “Reporteador de Información del Sistema”
> - “Organizador de Archivos”
> - “Juego de Aprendizaje en Línea de Comandos”

---

## 2) Descripción General

En esta actividad **no vas a construir un proyecto grande**. Vas a diseñar y documentar una propuesta de práctica temática **pequeña, clara y realizable** en un tiempo corto.

Tu objetivo es definir una idea con enfoque en:
- documentación técnica,
- planeación,
- estructura del repositorio,
- explicación del caso de uso,
- y plan básico de pruebas.

Debes elegir **un solo lenguaje principal** para tu propuesta:
- ARM64 Assembly
- C
- Python
- Bash

> **Nota importante sobre ARM64 Assembly:** úsalo únicamente para programas **muy pequeños** (por ejemplo, operaciones simples, manejo básico de cadenas o lectura/escritura mínima), debido al nivel de detalle del lenguaje.

### Restricciones de alcance
Para asegurar que el proyecto sea viable con herramientas gratuitas (Codex/IA con límites):
- Mantén el alcance pequeño (MVP funcional y acotado).
- Evita frameworks complejos.
- No uses APIs pagadas.
- No uses bases de datos.
- No uses servicios de nube.
- No uses contenedores.
- Evita dependencias pesadas o difíciles de instalar.

**Prioridad de la actividad:** justificar y documentar bien la idea **antes** de escribir mucho código.

---

## 3) Entregables del Estudiante

Tu repositorio debe incluir, como mínimo:

- `README.md`
- `docs/propuesta.md`
- `docs/caso_de_uso.md`
- `docs/estructura_repositorio.md`
- `docs/plan_de_pruebas.md`

Opcionales (si decides incluir prototipo mínimo):
- `src/`
- `scripts/`
- `tests/`

### Contenido esperado por archivo

#### `README.md`
Debe incluir:
- Nombre del proyecto.
- Problema que resuelve (2–4 líneas).
- Lenguaje principal elegido y por qué.
- Alcance del MVP (qué sí incluye y qué no incluye).
- Instrucciones mínimas para ejecutar (si hay código).

#### `docs/propuesta.md`
Debe incluir:
- Tema del proyecto.
- Objetivo general.
- Objetivos específicos (3 a 5).
- Justificación técnica breve.
- Requisitos funcionales mínimos.
- Requisitos no funcionales básicos (simplicidad, portabilidad, claridad).
- Riesgos y limitaciones.

#### `docs/caso_de_uso.md`
Debe incluir:
- Usuario objetivo.
- Escenario principal de uso.
- Entradas esperadas.
- Proceso general.
- Salidas esperadas.
- Ejemplo de ejecución (puede ser simulado en texto).

#### `docs/estructura_repositorio.md`
Debe incluir:
- Árbol de carpetas/archivos propuesto.
- Propósito de cada carpeta/archivo.
- Convenciones de nombres.
- Estrategia de crecimiento (cómo escalar sin complicarlo).

#### `docs/plan_de_pruebas.md`
Debe incluir:
- Casos de prueba mínimos (al menos 5).
- Entradas por caso.
- Resultado esperado por caso.
- Criterios de aceptación.
- Errores comunes previstos y cómo verificarlos.

---

## 4) Estructura Recomendada del Repositorio

Usa esta estructura base como mínimo:

```text
nombre-del-proyecto/
├── README.md
├── docs/
│   ├── propuesta.md
│   ├── caso_de_uso.md
│   ├── estructura_repositorio.md
│   └── plan_de_pruebas.md
├── src/
│   └── main.<ext>
├── scripts/
│   └── run.sh
└── tests/
    └── test_plan.md
```

> `<ext>` depende del lenguaje elegido (`s`, `c`, `py`, `sh`, etc.).

---

## 5) Reglas de Diseño de la Propuesta

1. **Proyecto pequeño y concreto.**
2. **Una sola responsabilidad principal.**
3. **MVP en máximo 1–2 comandos de ejecución.**
4. **Sin dependencias complejas.**
5. **Documentación entendible para otra persona del grupo.**

---

## 6) Rúbrica Sugerida (100 puntos)

- **Claridad del problema y objetivo (20 pts)**
  - El problema está bien definido y el objetivo es alcanzable.
- **Calidad de la propuesta técnica (20 pts)**
  - La solución es coherente con el lenguaje elegido.
- **Caso de uso y flujo operativo (20 pts)**
  - El escenario está completo, con entradas/proceso/salidas claros.
- **Estructura del repositorio (20 pts)**
  - Organización limpia, consistente y fácil de mantener.
- **Plan de pruebas (20 pts)**
  - Casos suficientes, medibles y alineados al MVP.

---

## 7) Criterios de Aceptación

Se considera **entregada** la actividad cuando:

- Existen todos los archivos obligatorios solicitados.
- La propuesta describe un proyecto pequeño y viable.
- Se identifica claramente el lenguaje principal.
- El caso de uso está completo.
- El plan de pruebas contiene casos verificables.
- La estructura del repositorio es consistente con la documentación.

---

## 8) Recomendaciones finales para estudiantes

- Empieza por el caso de uso, no por el código.
- Si eliges ARM64 Assembly, reduce al máximo el alcance.
- Usa ejemplos simples y medibles.
- Prefiere scripts locales y ejecución por terminal.
- Si agregas código, que sea mínimo y demostrable.

---

## 9) Formato de Entrega en GitHub Classroom

1. Crea/usa tu repositorio asignado.
2. Sube los archivos requeridos en la estructura indicada.
3. Haz al menos 3 commits significativos (ejemplo: propuesta inicial, caso de uso, plan de pruebas).
4. Verifica que tu `README.md` explique cómo revisar tu propuesta.
5. Entrega dentro de la fecha indicada por el docente.
