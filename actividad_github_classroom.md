# Actividad: Propuesta de Práctica Temática Pequeña (Enfoque en Documentación)

## 1) Título de la práctica

**Diseña un título claro y específico para tu práctica temática.**

Ejemplos (puedes usar uno o crear el tuyo):
- **Mini Toolkit en ARM64**
- **Asistente de Estudio en Terminal**
- **Reporteador de Información del Sistema**
- **Organizador de Archivos**
- **Juego de Aprendizaje en Línea de Comandos**

> Tu título debe reflejar **qué problema resuelve** y **en qué contexto se usará**.

---

## 2) Descripción general

En esta actividad vas a **diseñar una propuesta de proyecto pequeño**, priorizando la **documentación**, la **planeación**, la **estructura del repositorio** y la **justificación del caso de uso**.

### Lenguaje principal (elige uno)
Debes seleccionar **un solo lenguaje principal** para tu propuesta:
- ARM64 Assembly
- C
- Python
- Bash

### Importante sobre ARM64 Assembly
Si eliges **ARM64 Assembly**, tu práctica debe ser **muy pequeña** (por ejemplo: cálculos simples, manejo básico de cadena, menú mínimo en terminal o lectura de entrada muy controlada).

### Enfoque de la actividad
Antes de programar en grande, debes demostrar que tu idea está bien definida:
1. Qué problema resuelve.
2. A quién le sirve.
3. Qué funcionalidad mínima tendrá.
4. Cómo se va a probar.
5. Cómo organizarás el repositorio.

> **Regla de alcance:** proyecto chico y viable para completarse con herramientas gratuitas (incluyendo Codex u otra IA con límite de uso).

---

## 3) Entregables del estudiante

Tu repositorio debe incluir, **como mínimo**, los siguientes archivos:

- `README.md`
- `docs/propuesta.md`
- `docs/caso_de_uso.md`
- `docs/estructura_repositorio.md`
- `docs/plan_de_pruebas.md`

Opcionales (si decides incluir código o automatización mínima):
- `src/`
- `scripts/`
- `tests/`

---

## 4) Estructura recomendada del repositorio

Usa esta estructura mínima como referencia:

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

> `<ext>` depende del lenguaje elegido: `s` (Assembly), `c`, `py` o `sh`.

---

## 5) Contenido requerido por archivo

### `README.md`
Debe incluir:
- Título del proyecto.
- Resumen breve (5–8 líneas).
- Lenguaje principal elegido y por qué.
- Alcance de la práctica (qué sí y qué no hará).
- Instrucciones mínimas de ejecución (aunque sea en borrador).
- Índice de documentos en `docs/`.

### `docs/propuesta.md`
Debe incluir:
- Problema a resolver.
- Objetivo general.
- 3 objetivos específicos.
- Funcionalidad mínima viable (MVP).
- Requisitos funcionales (mínimo 4).
- Requisitos no funcionales (mínimo 3; ejemplo: claridad, portabilidad básica, uso en terminal).
- Supuestos y limitaciones.

### `docs/caso_de_uso.md`
Debe incluir:
- Usuario objetivo.
- Escenario real de uso (narrativa corta).
- Flujo principal paso a paso.
- Al menos 2 flujos alternos o errores esperados.
- Criterios de aceptación (mínimo 4).

### `docs/estructura_repositorio.md`
Debe incluir:
- Árbol del repositorio actualizado.
- Propósito de cada carpeta/archivo principal.
- Convenciones de nombres (archivos, funciones, scripts).
- Estrategia para separar documentación y código.

### `docs/plan_de_pruebas.md`
Debe incluir:
- Estrategia de pruebas (manual, por scripts simples o ambas).
- Tabla de casos de prueba con:
  - ID
  - Entrada
  - Acción
  - Resultado esperado
  - Resultado obtenido (inicialmente “Pendiente”)
- Mínimo 6 casos de prueba.

---

## 6) Restricciones técnicas de la actividad

Para mantener el proyecto pequeño y realista:
- ❌ No usar frameworks grandes.
- ❌ No usar APIs pagadas.
- ❌ No usar bases de datos.
- ❌ No usar servicios en la nube.
- ❌ No usar contenedores (Docker/Podman).
- ❌ No agregar dependencias complejas o difíciles de instalar.
- ✅ Priorizar herramientas de línea de comandos y librerías estándar.

---

## 7) Criterios de evaluación sugeridos (100%)

1. **Claridad de la propuesta (25%)**  
   La idea está bien delimitada, es entendible y tiene objetivo concreto.

2. **Calidad de documentación (30%)**  
   Los documentos están completos, bien estructurados y son consistentes entre sí.

3. **Viabilidad técnica (20%)**  
   El alcance corresponde a una práctica pequeña y ejecutable con recursos limitados.

4. **Diseño del repositorio (15%)**  
   La estructura de carpetas/archivos es limpia y facilita el desarrollo.

5. **Plan de pruebas (10%)**  
   Casos de prueba relevantes, medibles y alineados al MVP.

---

## 8) Guía breve para definir el alcance (recomendación docente)

Antes de escribir código, responde estas preguntas en tu propuesta:
1. ¿Qué hará tu proyecto en su versión 1?
2. ¿Qué dejarás fuera explícitamente?
3. ¿Cuál es la entrada mínima y la salida esperada?
4. ¿Cómo demostrarás que funciona en menos de 5 minutos?

Si no puedes responder esto con claridad, reduce el alcance.

---

## 9) Entrega

- La entrega se realiza en este repositorio de GitHub Classroom.
- Tu entrega final debe tener **todos los archivos requeridos** y contenido suficiente para revisión.
- El código es opcional en esta fase; la prioridad es la **propuesta documentada**.

---

## 10) Plantilla rápida de inicio (opcional)

Puedes copiar esta lista de verificación en tu `README.md`:

```markdown
## Checklist de entrega
- [ ] Definí el título del proyecto
- [ ] Elegí lenguaje principal (ARM64 Assembly, C, Python o Bash)
- [ ] Completé docs/propuesta.md
- [ ] Completé docs/caso_de_uso.md
- [ ] Completé docs/estructura_repositorio.md
- [ ] Completé docs/plan_de_pruebas.md
- [ ] Validé que el alcance sea pequeño y realista
```

---

### Nota final
La meta de esta actividad es que aprendas a **pensar como arquitecto/a de software desde el inicio**: delimitar alcance, justificar decisiones y documentar con precisión antes de programar.
