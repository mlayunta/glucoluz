# 💧 GlucoLuz

**Aplicación web progresiva (PWA) de apoyo a la diabetes tipo 1 y tipo 2**

Conteo de hidratos, calculador de bolo, panel metabólico, informes AGP y educación terapéutica, todo en una sola app que funciona sin conexión y guarda tus datos únicamente en tu dispositivo.

[![Versión](https://img.shields.io/badge/versión-1.4.0-0d9488)](CHANGELOG.md)
[![Licencia](https://img.shields.io/badge/licencia-MIT-blue)](LICENSE)
[![PWA](https://img.shields.io/badge/PWA-instalable-5A0FC8)](manifest.json)
[![Sin dependencias](https://img.shields.io/badge/dependencias-0-success)](#-tecnología)

> ⚠️ **Aviso importante.** GlucoLuz es una herramienta de apoyo educativo. **No diagnostica, no prescribe y no sustituye el criterio de tu equipo sanitario.** Las funciones de cálculo de dosis deben validarse con tu médico o educador en diabetes antes de usarlas.

---

## 📑 Índice

- [Qué es GlucoLuz](#-qué-es-glucoluz)
- [Características](#-características)
- [Capturas](#-capturas)
- [Instalación y uso](#-instalación-y-uso)
- [Despliegue en GitHub Pages](#-despliegue-en-github-pages)
- [Estructura del proyecto](#-estructura-del-proyecto)
- [Tecnología](#-tecnología)
- [Fuentes de datos y referencias científicas](#-fuentes-de-datos-y-referencias-científicas)
- [Privacidad y RGPD](#-privacidad-y-rgpd)
- [Marco regulatorio](#�?marco-regulatorio)
- [Hoja de ruta](#�?hoja-de-ruta)
- [Historial de cambios](#-historial-de-cambios)
- [Autor](#-autor)
- [Licencia](#-licencia)

---

## 💡 Qué es GlucoLuz

GlucoLuz nace de una idea sencilla: que una persona con diabetes tenga en el bolsillo una herramienta **clara, rigurosa y sin ruido** para el día a día.

La app se adapta al tipo de diabetes desde el primer arranque:

| | **Diabetes tipo 1** | **Diabetes tipo 2** |
|---|---|---|
| **Enfoque** | Insulina intensiva, conteo preciso | Hábitos, medicación y seguimiento |
| **Módulos** | Calculador de bolo, IOB, MCG, modo cuidador | Raciones visuales, recordatorios, panel metabólico |
| **Interfaz** | Completa, con todos los parámetros | Simplificada, sin cálculo de dosis |

No hay servidores, no hay cuentas, no hay publicidad. **Tus datos no salen de tu dispositivo.**

---

## �?Características

### 🍽�?Alimentación y conteo de hidratos
- Base local de **más de 160 alimentos** con hidratos, índice glucémico (IG) y ración habitual, adaptada a productos de consumo habitual en España.
- Buscador con filtros por categoría y **cálculo automático de hidratos, carga glucémica e IG medio** de la comida.
- **Escáner real de códigos de barras** con la cámara: lee el EAN del producto y consulta **Open Food Facts** para obtener hidratos, azúcares, grasas, sal, fibra, Nutri-Score y grupo NOVA.
- Los productos escaneados se guardan en la categoría **«Mis alimentos»**.
- **Comidas frecuentes**: guarda una combinación de alimentos y recárgala con un toque.

### 💉 Cálculo de insulina (DT1)
- Calculador de bolo con **ratio insulina/hidratos por franja horaria**, factor de sensibilidad, glucemia objetivo e **insulina activa (IOB)**.
- **Bloqueado por defecto** hasta que el usuario confirma que ha validado los parámetros con su equipo sanitario.
- Advertencias automáticas ante hipoglucemia y ante dosis elevadas.

### 📊 Monitorización y análisis
- **Tiempo en rango (TIR)**, GMI, coeficiente de variación y desglose por rangos.
- **Gráfica AGP** (Perfil Ambulatorio de Glucosa) con percentiles 5�?5, 25�?5 y mediana.
- Gráfica de las **últimas 24 horas** con marcadores de eventos.
- **Informe PDF** listo para llevar a consulta, con datos del paciente, métricas y AGP.

### 🩺 Panel metabólico (pestaña Salud)
- **Semáforo de control**: glucemia media, GMI, TIR, peso, perímetro abdominal, tensión arterial y actividad física, con objetivos personalizables.
- **IMC** con clasificación y barra de progreso.
- Gráficas de **evolución del peso** y de **tensión arterial** a 90 días.
- **Glucemia media por momento del día** (ayunas, preprandial, postprandial, aleatoria).
- **Cribado de complicaciones**: fondo de ojo, microalbuminuria, exploración del pie y perfil lipídico, con recordatorio anual.
- **Adherencia a la medicación** de los últimos 7 días.
- Infografía del **plato saludable**.

### 📚 Educación y fuentes oficiales (pestaña Consejos)
- **8 píldoras educativas**: método del plato, índice y carga glucémica, hipoglucemias, hiperglucemias y cetonas, ejercicio, días de enfermedad, cuidado de los pies e interpretación de analíticas.
- **Semáforo del etiquetado nutricional** con los umbrales del Reglamento (UE) 1924/2006 y los límites diarios de la OMS.
- Guía **«Cómo leer una etiqueta en 6 pasos»**, con los 18 alias del azúcar y las afirmaciones engañosas más habituales.
- **Semáforo de edulcorantes** en tres grupos (preferente, moderación, no recomendados) con IDA, número E y matices de evidencia.
- **Directorio de más de 20 enlaces** a organismos oficiales y sociedades científicas: FEDE, Fundación para la Diabetes, SED, SEEN, Ministerio de Sanidad, AESAN, IDF, ADA, EASD, OMS, NICE, ISPAD, BEDCA, Open Food Facts�?

### 🔔 Otros módulos
- Registro de **glucosa, comidas, eventos** (ejercicio, estrés, enfermedad, ciclo, cetonas, alcohol) y **medidas corporales**.
- **Recordatorios de medicación** con registro de tomas y cálculo de adherencia.
- **Modo cuidador** con alertas simuladas de hipoglucemia.
- **Racha de días registrando** para mantener la constancia.
- Tema **claro y oscuro**, diseño responsive y accesibilidad cuidada.

### 🔒 Privacidad por diseño
- **100 % local**: los datos se guardan en `localStorage`, nunca en un servidor.
- **Sin cuentas, sin cookies, sin analítica, sin publicidad.**
- **Exportación e importación** de copia de seguridad en JSON.
- Borrado completo de datos con un solo botón.

---

## 📸 Capturas

> Añade aquí tus capturas. Crea una carpeta `screenshots/` y enlaza las imágenes:

```markdown
| Inicio | Comidas | Salud | Consejos |
|---|---|---|---|
| ![Inicio](screenshots/01-inicio.png) | ![Comidas](screenshots/02-comidas.png) | ![Salud](screenshots/03-salud.png) | ![Consejos](screenshots/04-consejos.png) |
```

---

## 🚀 Instalación y uso

### Opción 1: usarla directamente

1. Abre la app en tu móvil.
2. En Chrome/Edge (Android): menú **�?�?Instalar aplicación**.
3. En Safari (iOS): **Compartir �?Añadir a pantalla de inicio**.

La app se instalará como una aplicación nativa y funcionará sin conexión.

### Opción 2: ejecutarla en local

Necesitas un servidor local porque el service worker y la cámara requieren `localhost` o HTTPS.

```bash
# Clona el repositorio
git clone https://github.com/mlayunta.github.io/glucoluz.git
cd glucoluz

# Opción A: con Python (ya instalado en macOS y Linux)
python3 -m http.server 5173

# Opción B: con Node.js
npx serve -l 5173

# Opción C: con PHP
php -S localhost:5173
```

Abre **http://localhost:5173** en el navegador.

> ⚠️ **No abras `index.html` con doble clic** (`file://`): el service worker no se registrará y la cámara no funcionará.

---

## 🌐 Despliegue en GitHub Pages

### Paso 1: crear el repositorio

```bash
git init
git add .
git commit -m "feat: GlucoLuz v1.3.0"
git branch -M main
git remote add origin https://github.com/mlayunta.github.io/glucoluz.git
git push -u origin main
```

### Paso 2: activar GitHub Pages

1. Ve a tu repositorio �?**Settings** �?**Pages**.
2. En *Source*, selecciona **Deploy from a branch**.
3. Branch: **`main`** · Folder: **`/ (root)`**.
4. Pulsa **Save**.

En 1-2 minutos tendrás la app en:

```
https://mlayunta.github.io/glucoluz/
```

### Paso 3: verificar

- El **icono de instalar** debe aparecer en la barra de direcciones.
- Abre **F12 �?Application**:
  - *Manifest*: debe mostrar «GlucoLuz · Diabetes» sin errores.
  - *Service Workers*: debe aparecer `sw.js` como *activated and is running*.
- Prueba el escáner: requiere HTTPS, que GitHub Pages ya proporciona.

> 💡 El archivo `.nojekyll` ya está incluido para que GitHub Pages no procese los archivos con Jekyll.

---

## 📁 Estructura del proyecto

```
glucoluz/
├── index.html              # Aplicación completa (HTML + CSS + JS en un solo archivo)
├── manifest.json           # Manifiesto de la PWA (nombre, iconos, atajos)
├── sw.js                   # Service worker (caché offline y actualizaciones)
├── icons/
�?  ├── icon.svg            # Icono vectorial maestro
�?  ├── icon-192.png        # Icono PWA 192×192
�?  ├── icon-512.png        # Icono PWA 512×512
�?  ├── icon-maskable-512.png
�?  ├── apple-touch-icon.png
�?  └── favicon-32.png
├── tools/
�?  └── generate-icons.sh   # Script para regenerar los PNG desde el SVG
├── .github/
�?  └── workflows/
�?      └── deploy.yml      # Despliegue automático en GitHub Pages
├── screenshots/            # Capturas para el README
├── README.md
├── CHANGELOG.md
├── LICENSE
├── PRIVACY.md
├── DISCLAIMER.md
├── package.json
├── .gitignore
└── .nojekyll
```

---

## 🛠�?Tecnología

| Aspecto | Detalle |
|---|---|
| **Arquitectura** | Un único archivo `index.html` con CSS y JavaScript embebidos |
| **Dependencias** | **Cero** en el núcleo. ZXing se carga desde CDN solo si el navegador no soporta `BarcodeDetector` |
| **Almacenamiento** | `localStorage` (todo local, sin backend) |
| **Gráficas** | SVG generado a mano (sin librerías) |
| **Escáner** | `BarcodeDetector` nativo + ZXing 0.21.3 como respaldo |
| **PWA** | Service worker con caché *stale-while-revalidate* y manifiesto con atajos |
| **Compatibilidad** | Chrome, Edge, Safari, Firefox (móvil y escritorio) |

**¿Por qué un solo archivo?** Para que sea trivial de desplegar, auditar y modificar. No hay proceso de compilación, ni `node_modules`, ni dependencias que puedan romperse.

---

## 📚 Fuentes de datos y referencias científicas

### Composición de alimentos e índice glucémico
- **BEDCA** �?Base de Datos Española de Composición de Alimentos. [bedca.net](https://www.bedca.net)
- **Open Food Facts** �?base colaborativa de productos envasados. [world.openfoodfacts.org](https://world.openfoodfacts.org)
- Valores de índice glucémico basados en las tablas internacionales de referencia (Atkinson et al., *Diabetes Care*).

### Umbrales de etiquetado
- **Reglamento (UE) 1924/2006** sobre declaraciones nutricionales y de propiedades saludables.
- **Reglamento (UE) 1169/2011** sobre información alimentaria al consumidor.
- **Nutri-Score** �?sistema de etiquetado frontal adoptado voluntariamente en España por AESAN.

### Recomendaciones clínicas
- **OMS** �?directrices sobre azúcares libres, sal y edulcorantes no azucarados (2023).
- **ADA** �?*Standards of Care in Diabetes*.
- **EASD** �?guías de manejo de la diabetes.
- **NICE** �?guías NG17 (diabetes tipo 1) y NG28 (diabetes tipo 2).
- **ISPAD** �?guías pediátricas de diabetes tipo 1.
- **EFSA y JECFA** �?evaluaciones de seguridad de aditivos y edulcorantes.
- **IARC** �?clasificación de carcinogenicidad (monografías, 2023).

### Métricas
- **TIR, GMI y CV** según el *International Consensus on Time in Range* (Battelino et al., *Diabetes Care*, 2019).

> Los valores incluidos en la app son **orientativos y educativos**. No sustituyen el etiquetado oficial del producto ni las indicaciones de tu equipo sanitario.

---

## 🔐 Privacidad y RGPD

GlucoLuz está diseñada bajo el principio de **minimización de datos**:

- �?Todos los datos se almacenan **exclusivamente en el dispositivo** del usuario (`localStorage`).
- �?**No hay servidor, ni base de datos remota, ni cuentas de usuario.**
- �?**No se recopilan datos personales, ni identificadores, ni telemetría.**
- �?**No hay cookies de seguimiento ni publicidad.**
- �?El usuario puede **exportar** y **borrar** todos sus datos en cualquier momento.

**Única conexión externa:** al usar el escáner, se envía el **número de código de barras** a la API pública de Open Food Facts. No se envía ningún dato personal ni de salud. Consulta su política en [world.openfoodfacts.org/privacy](https://world.openfoodfacts.org/privacy).

📄 Ver [PRIVACY.md](PRIVACY.md) para el detalle completo.

---

## ⚖️ Marco regulatorio

Este proyecto se publica como **herramienta de apoyo educativo y de código abierto**.

- Las funciones de **cálculo de dosis de insulina** se ofrecen como ayuda y **requieren validación por el equipo sanitario**.
- Para su **comercialización como producto sanitario**, la aplicación debería someterse al **Reglamento (UE) 2017/745 (MDR)** y obtener el marcado CE correspondiente.
- El **informe AGP** es un documento de apoyo a la consulta clínica, no un informe médico oficial.
- Los **enlaces externos** se ofrecen como recurso informativo y no implican relación con sus titulares.

📄 Ver [DISCLAIMER.md](DISCLAIMER.md) para el detalle completo.

---

## 🗺�?Hoja de ruta

- [x] Base de datos local de alimentos con IG y carga glucémica
- [x] Calculador de bolo con IOB y bloqueo de seguridad
- [x] TIR, GMI, gráficas AGP e informe PDF
- [x] Panel metabólico para diabetes tipo 2
- [x] Directorio de fuentes oficiales y educación terapéutica
- [x] Semáforo de etiquetado nutricional y de edulcorantes
- [x] Escáner real de códigos de barras con Open Food Facts
- [ ] Integración real con FreeStyle Libre (API LibreLinkUp)
- [ ] Integración con Dexcom Share
- [ ] Sincronización con bombas de insulina
- [ ] Notificaciones push de recordatorios de medicación
- [ ] Modo multiusuario y perfiles familiares
- [ ] Internacionalización (inglés, catalán, gallego, euskera)
- [ ] Evaluación MDR y marcado CE

---

## 📝 Historial de cambios

Consulta [CHANGELOG.md](CHANGELOG.md) para el detalle de cada versión.

---

## 👤 Autor

**Miguel Ángel Layunta López**

Proyecto diseñado y desarrollado íntegramente por el autor.

---

## 📄 Licencia

Este proyecto se distribuye bajo la **Licencia MIT**. Consulta [LICENSE](LICENSE) para más detalles.

Los datos de **Open Food Facts** se distribuyen bajo la **Open Database License (ODbL)** y se atribuyen en la propia aplicación.

---

## 🤝 Contribuciones

Las contribuciones son bienvenidas, especialmente en estos ámbitos:

- 🩺 **Revisión clínica** por profesionales de endocrinología, enfermería o nutrición.
- 🍎 **Ampliación de la base de alimentos** con datos contrastados.
- 🌍 **Traducciones** a otras lenguas.
- �?**Accesibilidad** y usabilidad.
- 🐛 **Reporte de errores** mediante *issues*.

Antes de enviar una *pull request*, abre un *issue* para comentar el cambio.

---

<p align="center">
  <b>💧 GlucoLuz</b><br>
  <i>Tu diabetes, con luz propia.</i><br><br>
  Hecho con 💧 por <b>Miguel Ángel Layunta López</b>
</p>
