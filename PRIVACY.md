# Política de privacidad de GlucoLuz

**Última actualización:** 23 de noviembre de 2026
**Versión de la aplicación:** 1.3.0
**Responsable:** Miguel Ángel Layunta López

---

## 1. Resumen

GlucoLuz es una aplicación web progresiva (PWA) que funciona **íntegramente en tu dispositivo**.

- **No hay servidores propios.** No existe backend, ni base de datos remota, ni cuentas de usuario.
- **No se recopilan datos personales.** Ni nombre, ni correo, ni teléfono, ni identificadores de dispositivo.
- **No hay analítica, ni telemetría, ni publicidad, ni cookies de seguimiento.**
- **Toda tu información de salud permanece en tu navegador** y nunca se transmite a terceros.

En la práctica, esto significa que **el desarrollador no tiene acceso, en ningún momento, a los datos que introduces en la aplicación**.

---

## 2. Responsable del tratamiento

**Titular:** Miguel Ángel Layunta López
**Contacto:** [mlayuntalopez@gmail.com]

Dado que la aplicación no transmite datos a ningún servidor controlado por el responsable, este **no actúa como encargado ni como responsable del tratamiento** de los datos de salud que el usuario introduce. El usuario es el único poseedor y controlador de su propia información.

Esta política se publica por transparencia y para informar de las características técnicas del tratamiento.

---

## 3. Qué datos NO se recopilan

GlucoLuz **no recopila ni solicita** en ningún momento:

- Nombre completo, documento de identidad, dirección postal o correo electrónico.
- Número de teléfono ni contactos del dispositivo.
- Geolocalización.
- Identificadores publicitarios o de dispositivo.
- Historial de navegación.
- Fotografías, audio o vídeo (ver apartado 7).
- Datos biométricos.

Tampoco utiliza servicios de terceros de analítica, publicidad, redes sociales ni rastreo.

---

## 4. Qué datos se tratan y dónde se almacenan

La aplicación permite al usuario registrar voluntariamente datos relacionados con su salud. Todos ellos se guardan **exclusivamente en el almacenamiento local del navegador** (`localStorage`) del propio dispositivo:

| Categoría | Ejemplos | Finalidad |
|---|---|---|
| Perfil | Nombre o alias, peso, altura, tipo de diabetes | Personalizar la interfaz y los cálculos |
| Parámetros de tratamiento | Ratio insulina/hidratos, factor de sensibilidad, objetivo de glucemia, duración de la insulina activa | Calcular la dosis orientativa de insulina |
| Glucosa | Lecturas con fecha, hora y momento del día | Métricas de control (TIR, GMI, CV) y gráficas |
| Comidas | Alimentos, cantidades, hidratos, carga glucémica | Conteo de hidratos e historial |
| Eventos | Ejercicio, estrés, enfermedad, ciclo menstrual, cetonas, alcohol | Contextualizar las variaciones de glucemia |
| Medidas corporales | Peso, perímetro abdominal, tensión arterial | Panel metabólico y seguimiento |
| Medicación | Nombre, dosis, horario y registro de tomas | Recordatorios y adherencia |
| Cribados | Fecha de fondo de ojo, microalbuminuria, pie y perfil lipídico | Recordatorio de revisiones |
| Alimentos personalizados | Productos escaneados o creados a mano | Ampliar la base de datos local |

**Ninguno de estos datos sale del dispositivo.** No se envían a ningún servidor, ni se sincronizan en la nube, ni se comparten con el desarrollador.

---

## 5. Base jurídica

En la medida en que el usuario decide voluntariamente introducir datos relativos a su salud, el tratamiento se basa en:

- **Consentimiento explícito** del interesado para el tratamiento de categorías especiales de datos (artículo 9.2.a del Reglamento (UE) 2016/679, RGPD).
- **Consentimiento** para el tratamiento de los datos generales (artículo 6.1.a del RGPD).

El consentimiento se otorga de forma inequívoca al utilizar la aplicación y se puede retirar en cualquier momento **borrando los datos** (ver apartado 10).

---

## 6. Comunicación de datos a terceros

GlucoLuz **no cede, vende ni comparte datos personales con terceros**.

Existe **una única conexión externa**, que se activa solo cuando el usuario decide utilizar el escáner de códigos de barras:

- Se envía el **número de código de barras** del producto a la API pública de **Open Food Facts** (`world.openfoodfacts.org`).
- Se trata de un **identificador de producto**, no de un dato personal ni de salud.
- Como en cualquier petición web, el servidor de Open Food Facts puede registrar la **dirección IP** desde la que se realiza la consulta. Este registro es ajeno al control del desarrollador y se rige por la política de privacidad de Open Food Facts: https://world.openfoodfacts.org/privacy
- Si no utilizas el escáner, **la aplicación no realiza ninguna conexión externa**.

Adicionalmente, si accedes a la aplicación alojada en GitHub Pages, **GitHub puede registrar datos de acceso** (dirección IP, agente de usuario) como proveedor de hosting. Este tratamiento es responsabilidad de GitHub y se rige por su propia política de privacidad.

---

## 7. Cámara del dispositivo

El escáner de códigos de barras requiere acceso a la cámara. Es importante que sepas que:

- **El vídeo nunca se graba, ni se almacena, ni se transmite.** Se procesa en tiempo real en el propio dispositivo.
- **Solo se extrae el número del código de barras**, que es lo único que se envía a la API pública.
- El permiso de cámara es **opcional**: la aplicación funciona con normalidad sin él.
- Puedes revocar el permiso en cualquier momento desde los ajustes de tu navegador.

---

## 8. Conservación de los datos

Los datos se conservan en el dispositivo **hasta que el usuario decide eliminarlos**. No existe ningún plazo de caducidad automático impuesto por la aplicación.

Ten en cuenta que:

- **Borrar los datos de navegación** del navegador eliminará la información almacenada.
- **Desinstalar la aplicación** (o eliminar el icono de la pantalla de inicio) puede eliminar los datos asociados.
- Se recomienda realizar **copias de seguridad periódicas** mediante la función de exportación en formato JSON.

---

## 9. Seguridad

Medidas aplicadas:

- Los datos **nunca se transmiten por la red**, salvo el código de barras descrito en el apartado 6.
- La aplicación **no incluye bibliotecas de terceros** en su núcleo, lo que reduce la superficie de riesgo.
- El código es **abierto y auditable**.

Limitaciones que debes conocer:

- El almacenamiento local del navegador (`localStorage`) **no está cifrado**. Cualquier persona con acceso físico a tu dispositivo desbloqueado podría consultar los datos.
- El **archivo de copia de seguridad exportado tampoco está cifrado**. Guárdalo en un lugar seguro.

Recomendaciones:

- Protege tu dispositivo con **bloqueo de pantalla** (PIN, patrón, huella o reconocimiento facial).
- No compartas el archivo de copia de seguridad por canales inseguros.
- Realiza copias de seguridad con regularidad.

---

## 10. Derechos del usuario

Como titular de tus datos, tienes derecho a:

| Derecho | Cómo ejercerlo en GlucoLuz |
|---|---|
| **Acceso** | Consulta todos tus datos en las pestañas Registro, Salud e Informes |
| **Rectificación** | Edita cualquier dato desde Ajustes o desde el propio registro |
| **Supresión** | Botón «Borrar todos mis datos» en Ajustes |
| **Portabilidad** | Botón «Exportar copia de seguridad» (archivo JSON) |
| **Limitación y oposición** | Deja de utilizar la aplicación y borra los datos |
| **Retirada del consentimiento** | Borra los datos en cualquier momento |

Dado que el desarrollador **no tiene acceso a tus datos**, no es posible atender solicitudes de acceso, rectificación o supresión por su parte: **el ejercicio de estos derechos se realiza directamente en la aplicación**.

Si consideras que el tratamiento no se ajusta a la normativa, puedes presentar una reclamación ante la **Agencia Española de Protección de Datos** (www.aepd.es).

---

## 11. Menores de edad

La diabetes tipo 1 afecta con frecuencia a niños y adolescentes. En esos casos:

- La aplicación debe ser **configurada y supervisada por el padre, madre o tutor legal**.
- El consentimiento para el tratamiento de los datos de salud del menor corresponde a su representante legal.
- Se recomienda que el uso del calculador de bolo esté siempre supervisado por un adulto y validado por el equipo sanitario.

---

## 12. Cookies y tecnologías de seguimiento

GlucoLuz **no utiliza cookies** de ningún tipo: ni técnicas, ni analíticas, ni publicitarias, ni de terceros.

El único almacenamiento que emplea es `localStorage`, con la finalidad exclusiva de guardar los datos que tú introduces para que estén disponibles la próxima vez que abras la aplicación.

---

## 13. Notificaciones

La aplicación puede mostrar avisos internos (recordatorios de medicación, alertas de hipoglucemia simuladas). Estos avisos:

- Se generan **localmente** en el dispositivo.
- **No utilizan servidores de notificaciones push.**
- Requieren que la aplicación esté abierta para mostrarse.

---

## 14. Cambios en esta política

Esta política puede actualizarse para reflejar cambios en la aplicación o en la normativa aplicable. La fecha de la última actualización figura al inicio del documento.

Los cambios relevantes se documentarán en el archivo `CHANGELOG.md` del repositorio.

---

## 15. Contacto

Para cualquier duda sobre esta política de privacidad:

**Miguel Ángel Layunta López**
Correo: [tu-correo@ejemplo.com]
Repositorio: https://github.com/mlayunta.github.io/glucoluz

---

## 16. Legislación aplicable

Esta política se rige por el Reglamento (UE) 2016/679 (Reglamento General de Protección de Datos) y por la Ley Orgánica 3/2018, de Protección de Datos Personales y garantía de los derechos digitales (LOPDGDD).
