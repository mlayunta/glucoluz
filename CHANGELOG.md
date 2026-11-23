# 📝 Historial de cambios

Todos los cambios relevantes de este proyecto se documentan en este archivo.

El formato sigue las recomendaciones de [Keep a Changelog](https://keepachangelog.com/es-ES/1.1.0/)
y el proyecto se adhiere al [Versionado Semántico](https://semver.org/lang/es/).

---

## [1.5.0] — 2026-11-23

### ✨ Añadido
- **Escáner real de códigos de barras** con la cámara del dispositivo.
  - Soporte de `BarcodeDetector` nativo (Chrome, Edge, Android) con los formatos EAN-13, EAN-8, UPC-A, UPC-E, Code 128 e ITF.
  - Respaldo con **ZXing 0.21.3** cargado desde CDN para iOS Safari y Firefox.
  - Entrada manual del código como tercera vía.
- **Integración con la API de Open Food Facts** (`/api/v2/product/`): hidratos, azúcares, grasas totales y saturadas, sal, fibra, proteínas, kcal, Nutri-Score y grupo NOVA.
- **Ficha de producto** con semáforo nutricional por 100 g, imagen, marca, cantidad e ingredientes.
- **Categoría «Mis alimentos»** para los productos escaneados o creados a mano, con opción de eliminarlos.
- **Creación manual de alimentos** con nombre, marca, hidratos por 100 g, índice glucémico y ración habitual.
- Nota informativa cuando un alimento no tiene índice glucémico registrado (se estima con 55 para la carga glucémica).

### 🔧 Cambiado
- El índice glucémico ahora admite el valor «no disponible» (`IG s/d`) en lugar de mostrarse como 0.
- La búsqueda de alimentos incluye los productos personalizados.
- El botón del escáner en la pantalla de Comidas usa un icono de código de barras.

### 🛡️ Seguridad
- La cámara se detiene automáticamente al cerrar cualquier modal.
- El vídeo nunca sale del dispositivo: solo se envía el número de código de barras a la API pública.

---

## [1.2.0] — 2026-11-23

### ✨ Añadido
- **Semáforo del etiquetado nutricional** en la pestaña Consejos, con los umbrales del Reglamento (UE) 1924/2006 por 100 g para azúcares, grasas totales, grasas saturadas, sal, fibra y grasas trans, junto a los límites diarios recomendados por la OMS y AESAN.
- **Modal «Cómo leer una etiqueta en 6 pasos»** con:
  - Los 18 alias con los que el azúcar aparece en las listas de ingredientes.
  - Las cuatro afirmaciones engañosas más habituales («sin azúcares añadidos», «sin azúcar», «light», «0 % materia grasa»).
- **Semáforo de edulcorantes y sustitutos del azúcar** en tres grupos:
  - 🟢 Opción preferente: estevia (E960), eritritol (E968) y polialcoholes.
  - 🟡 Aceptables con moderación: sucralosa, acesulfamo K, aspartamo, sacarina, neotame y advantamo.
  - 🔴 No recomendados como estrategia: ciclamato, miel/agave/panela/azúcar de coco, fructosa añadida y jarabe de maíz de alta fructosa.
- **Modal «Edulcorantes: lo que dice la evidencia»** con la explicación de la ingesta diaria admisible (IDA), la directriz de la OMS de 2023 y las claves específicas para diabetes.

### 📚 Documentación
- Cada edulcorante incluye su número E, su IDA y una nota de matiz sobre el estado de la evidencia.

---

## [1.1.0] — 2026-11-23

### ✨ Añadido
- **Pestaña Salud** con panel metabólico completo:
  - Semáforo de control con 7 indicadores (glucemia media, GMI, TIR, peso, perímetro abdominal, tensión arterial y actividad física).
  - Cálculo automático del IMC con clasificación y barra de progreso.
  - Gráfica de evolución del peso a 90 días.
  - Gráfica de tensión arterial (sistólica y diastólica) a 90 días.
  - Gráfico de barras de glucemia media por momento del día.
  - Cribado de complicaciones (fondo de ojo, microalbuminuria, pie diabético y perfil lipídico) con recordatorio anual.
  - Adherencia a la medicación de los últimos 7 días.
  - Resumen de hipoglucemias y cetonas para diabetes tipo 1.
  - Infografía del plato saludable.
- **Pestaña Consejos** con:
  - Ocho píldoras educativas ampliadas.
  - Directorio de más de 20 enlaces a organismos oficiales y sociedades científicas.
  - Guía «Cómo elegir buena información» con cuatro criterios de verificación.
- **Objetivos personalizables** de control (HbA1c, peso, perímetro, tensión arterial y actividad).
- **Registro de tomas de medicación** con cálculo de adherencia semanal.
- **Comidas frecuentes**: guardar y recargar combinaciones de alimentos.
- **Importación de copia de seguridad** en JSON (antes solo se podía exportar).
- **Botón de instalación de la PWA** dentro de Ajustes.
- **Compartir resumen** mediante la API nativa `navigator.share`.
- **Racha de días registrando** en la pantalla de inicio.
- Avisos de conexión (en línea / sin conexión).

### 🔧 Cambiado
- Los **Ajustes** se han movido al engranaje de la barra superior para dejar sitio a las nuevas pestañas.
- La barra de navegación pasa de 5 a 6 pestañas: Inicio, Comidas, Registro, Informes, Salud y Consejos.

---

## [1.0.0] — 2026-11-22

### ✨ Añadido
- Primera versión funcional de GlucoLuz.
- **Onboarding** adaptativo para diabetes tipo 1 y tipo 2.
- **Base de datos local** de más de 160 alimentos con hidratos, índice glucémico y ración habitual.
- **Calculador de hidratos y carga glucémica** de comidas.
- **Calculador de bolo** con ratio por franja horaria, factor de sensibilidad, glucemia objetivo e insulina activa (IOB), bloqueado hasta su validación con el equipo sanitario.
- **Registro** de glucosa, comidas, eventos (ejercicio, estrés, enfermedad, ciclo, cetonas, alcohol) y medidas corporales.
- **Métricas**: tiempo en rango (TIR), GMI, coeficiente de variación y desglose por rangos.
- **Gráfica AGP** con percentiles y gráfica de las últimas 24 horas.
- **Informe PDF** imprimible para la consulta clínica.
- **Módulo de diabetes tipo 2** con raciones visuales, recordatorios de medicación y educación contextual.
- **Modo cuidador** con alertas simuladas.
- **Tema claro y oscuro**.
- **PWA instalable** con manifiesto, service worker y funcionamiento sin conexión.
- **Exportación de copia de seguridad** en JSON y borrado completo de datos.

---

## Tipos de cambios

- `✨ Añadido` — nuevas funcionalidades.
- `🔧 Cambiado` — cambios en funcionalidades existentes.
- `🗑️ Obsoleto` — funcionalidades que se retirarán próximamente.
- `❌ Eliminado` — funcionalidades retiradas.
- `🐛 Corregido` — corrección de errores.
- `🛡️ Seguridad` — cambios relacionados con la seguridad o la privacidad.
- `📚 Documentación` — cambios en la documentación.

---
[1.5.0]: https://github.com/TU-USUARIO/glucoluz/compare/v1.4.0...v1.5.0
[1.4.0]: https://github.com/TU-USUARIO/glucoluz/compare/v1.3.0...v1.4.0
[1.3.0]: https://github.com/mlayunta.github.io/glucoluz/compare/v1.2.0...v1.3.0
[1.2.0]: https://github.com/mlayunta.github.io/glucoluz/compare/v1.1.0...v1.2.0
[1.1.0]: https://github.com/mlayunta.github.io/glucoluz/compare/v1.0.0...v1.1.0
[1.0.0]: https://github.com/mlayunta.github.io/glucoluz/releases/tag/v1.0.0
