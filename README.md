# VHRCec-github.io
# ⚡ CONCURSO DE DELETREO
### Sistema Interactivo de Competencia por Equipos

> **Unidad Educativa PCEI Chimborazo — Extensión CAÍ Riobamba**
> Órgano Rector: Ministerio de Educación, Deporte y Cultura del Ecuador

---

## 📋 Descripción General

Sistema digital interactivo diseñado para la realización de concursos de deletreo en aula o proyector. Permite sortear equipos y palabras mediante ruletas animadas, cronometrar automáticamente cada turno, registrar puntajes en tiempo real y garantizar la participación equitativa de todos los equipos mediante un sistema de ciclos sin repetición.

El programa funciona como un único archivo `.html` autocontenido: no requiere instalación, servidor web ni conexión a internet.

---

## 🏫 Institución y Autoría

| Campo | Detalle |
|---|---|
| **Institución** | Unidad Educativa PCEI Chimborazo |
| **Extensión** | CAÍ Riobamba |
| **Órgano Rector** | Ministerio de Educación, Deporte y Cultura del Ecuador (MINEDUC) |
| **Diseñado y desarrollado por** | Ing. Víctor Remache, MBA |
| **Año** | 2025 |

---

## 🗂️ Archivos del Proyecto

```
📁 proyecto-deletreo/
├── deletreo-v3-final.html      ← Programa principal (único archivo necesario)
├── LISTADO.pdf                 ← Banco de palabras fuente (referencia)
├── IMG_4565.png                ← Logo MINEDUC (embebido en el HTML)
├── IMG_4566.png                ← Logo PCEI Chimborazo (embebido en el HTML)
└── README.md                   ← Este documento
```

> **Nota:** Los logos institucionales están embebidos en el HTML como imágenes Base64. El archivo `deletreo-v3-final.html` es completamente autónomo.

---

## 📚 Banco de Palabras

Las palabras provienen del documento oficial **LISTADO.pdf** y están organizadas en tres niveles de dificultad:

### Nivel 1 — Fácil
- **Criterios:** 3 a 5 letras, uso cotidiano, ortografía simple.
- **Cantidad:** 25 palabras.
- **Ejemplos:** sol, pan, mar, luz, pez, sal, pie, oso, ave, uva, oro, gas, mes, red, bar, sur, fin, paz, rey, ley, voz, sed, fe, ron, cal.

### Nivel 2 — Medio
- **Criterios:** 6 a 8 letras, uso académico, incluyen tildes.
- **Cantidad:** 25 palabras.
- **Ejemplos:** ácido, célula, átomo, método, teoría, física, química, cálculo, lógica, síntesis, análisis, gráfico, energía, sistema, materia, función, variable, fórmula, proceso, modelo, estudio, técnica, práctica, lectura, escrito.

### Nivel 3 — Avanzado
- **Criterios:** Más de 8 letras, uso científico, ortografía compleja.
- **Cantidad:** 25 palabras.
- **Ejemplos:** biodiversidad, ecosistema, organismo, evolución, adaptación, reproducción, metabolismo, respiración, circulación, digestión, polinización, germinación, fotosíntesis, cloroplasto, cromosoma, genética, herencia, mutación, biología, zoología, botánica, microbiología, bacteriología, citología, histología.

---

## ⚙️ Requisitos del Sistema

| Componente | Requisito |
|---|---|
| **Navegador** | Google Chrome, Microsoft Edge o Mozilla Firefox (versión moderna) |
| **Conexión a internet** | Solo necesaria para cargar las fuentes tipográficas (Google Fonts). El programa funciona sin internet, aunque con fuentes del sistema. |
| **Instalación** | Ninguna. Solo abrir el archivo `.html`. |
| **Resolución mínima recomendada** | 1024 × 768 px (ideal: proyector Full HD 1920 × 1080) |
| **Sistema Operativo** | Windows, macOS o Linux |

---

## 🚀 Instrucciones de Uso

### Paso 1 — Abrir el programa
1. Copie el archivo `deletreo-v3-final.html` a su computadora o USB.
2. Haga doble clic en el archivo, o ábralo con Google Chrome.
3. Aparecerá la **pantalla de configuración** con el encabezado institucional.

### Paso 2 — Configurar el concurso
1. Seleccione el **número de equipos** (de 2 a 8).
2. Escriba los **nombres de cada equipo** en los campos correspondientes.
3. Seleccione el **nivel de palabras**: Fácil, Medio, Avanzado o Todos los niveles.
4. Presione **🚀 INICIAR CONCURSO**.

### Paso 3 — Desarrollo del concurso

Cada turno sigue este flujo:

```
[1] Presionar "🎰 GIRAR EQUIPO"
        ↓
    La ruleta gira y selecciona un equipo pendiente
        ↓
[2] Presionar "🎰 GIRAR PALABRA"
        ↓
    La ruleta gira y selecciona una palabra del banco
        ↓
[3] El cronómetro de 20 segundos inicia automáticamente
        ↓
[4] El participante deletrea la palabra en voz alta
        ↓
[5] El docente presiona ✅ CORRECTO o ❌ INCORRECTO
        ↓
    Se suma 1 punto si es correcto → pasa al siguiente turno
```

---

## 🎡 Sistema de Ruletas

### Ruleta de Equipos — Sin Repetición por Ciclo

El sistema garantiza que **ningún equipo se repite** dentro de un mismo ciclo de participación:

- La ruleta únicamente muestra los equipos que **aún no han jugado** en el ciclo actual.
- Una vez que un equipo participa, recibe la insignia **✓ YA JUGÓ** y desaparece de la ruleta.
- Cuando **todos los equipos han participado**, el sistema muestra un aviso y reinicia el ciclo automáticamente.
- El docente también puede reiniciar el ciclo manualmente con el botón **↺ REINICIAR CICLO**.

### Ruleta de Palabras

- Muestra una muestra aleatoria de hasta 20 palabras disponibles del banco.
- Las palabras **no se repiten** durante la sesión.
- Si se agotan todas las palabras del nivel seleccionado, el banco se reinicia.

---

## ⏱️ Cronómetro

- **Duración:** 20 segundos por turno.
- **Inicio:** Automático, 0.8 segundos después de que la ruleta de palabras se detiene.
- **Indicador visual:**
  - 🟢 Verde (> 10 seg) — tiempo suficiente.
  - 🟡 Amarillo (6–10 seg) — tiempo medio.
  - 🔴 Rojo (≤ 5 seg) — tiempo crítico.
- **Barra de progreso** que se reduce en tiempo real.
- Si el tiempo se agota sin respuesta, el turno se registra como incorrecto automáticamente.

---

## 🏆 Puntuación

| Evento | Puntos |
|---|---|
| Deletreo correcto dentro del tiempo | **+1 punto** |
| Deletreo incorrecto | 0 puntos |
| Tiempo agotado | 0 puntos |

- Los puntajes se acumulan durante toda la sesión.
- El marcador superior se actualiza en tiempo real.
- El botón **🏆 Ganador** muestra en cualquier momento el equipo con mayor puntaje.

---

## 📊 Barra de Información de Turno

Durante el juego, una barra informativa muestra:

| Indicador | Descripción |
|---|---|
| **TURNO** | Número de turno acumulado desde el inicio |
| **PENDIENTES** | Equipos que aún no han jugado en el ciclo actual |
| **YA JUGARON** | Equipos que ya participaron en el ciclo actual |

---

## 🎉 Efectos y Retroalimentación

- **Confeti animado** al registrar una respuesta correcta.
- **Flash verde** en pantalla al acertar.
- **Flash rojo** en pantalla al fallar.
- **Sonido de éxito** (tres notas ascendentes) al acertar.
- **Sonido de error** (dos notas descendentes) al fallar.
- **Historial de ronda** con las últimas 15 palabras, equipo y resultado.

---

## 🔧 Controles del Docente

| Botón | Función |
|---|---|
| 🎰 GIRAR EQUIPO | Inicia el sorteo del equipo participante |
| 🎰 GIRAR PALABRA | Inicia el sorteo de la palabra (disponible tras girar equipo) |
| ✅ CORRECTO | Registra respuesta correcta y suma 1 punto |
| ❌ INCORRECTO | Registra respuesta incorrecta, sin puntos |
| ↺ REINICIAR CICLO | Reinicia el ciclo de participación (todos los equipos vuelven a la ruleta) |
| 🔄 Nueva Ronda | Reinicia el turno actual (sin borrar puntajes) |
| 🏆 Ganador | Muestra el equipo con mayor puntaje |
| 🏠 Menú Principal | Vuelve a la pantalla de configuración inicial |

---

## 🌐 Opciones de Distribución

### Uso Local (recomendado para proyector en aula)
1. Copie `deletreo-v3-final.html` a una USB o carpeta del equipo.
2. Abra con Google Chrome.
3. Presione **F11** para pantalla completa en el proyector.

### Publicación en línea (acceso desde cualquier dispositivo)
1. Descargue el archivo `.html`.
2. Visite [netlify.com/drop](https://app.netlify.com/drop).
3. Arrastre el archivo a la página.
4. Recibirá una URL pública en segundos (ej. `https://nombre.netlify.app`).

---

## 🛠️ Tecnologías Utilizadas

| Tecnología | Uso |
|---|---|
| HTML5 | Estructura del documento |
| CSS3 | Estilos, animaciones, diseño responsivo |
| JavaScript (Vanilla) | Lógica del juego, ruletas, cronómetro |
| Canvas API | Renderizado de las ruletas giratorias |
| Web Audio API | Efectos de sonido |
| Google Fonts | Tipografías: Bebas Neue, Orbitron, Exo 2 |
| Base64 | Logos institucionales embebidos |

---

## 📄 Licencia y Uso

Este programa es de uso educativo interno para la **Unidad Educativa PCEI Chimborazo — Extensión CAÍ Riobamba**. Su reproducción o distribución fuera de la institución debe contar con autorización del autor.

---

*Desarrollado con fines pedagógicos para el fortalecimiento de competencias lingüísticas y ortográficas en el marco del Programa de Reinserción Educativa CAÍ Riobamba.*
