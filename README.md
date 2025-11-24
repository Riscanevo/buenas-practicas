# Análisis Comparativo de Calidad — SonarCloud

Este informe presenta un análisis comparativo entre tres versiones del mismo proyecto evaluadas mediante SonarCloud, identificando problemas de calidad, mantenibilidad, seguridad y buenas prácticas.

Los proyectos comparados son:

Versión legado_refactoring

Versión legacy_V2

Versión buenas-practicas

📝 1. Repositorios Analizados
Proyecto	Enlace
legado_refactoring	https://github.com/Riscanevo/legado_refactoring.git

legacy_V2	https://github.com/Riscanevo/legacy_V2.git

buenas-practicas	https://github.com/Riscanevo/buenas-practicas.git

🔍 2. Observaciones de SonarCloud por Proyecto

A continuación se listan los hallazgos detectados por SonarCloud según tu reporte.

📌 2.1 Proyecto: legado_refactoring

Principales observaciones detectadas:

Problema en style.css:

"Text does not meet the minimal contrast requirement with its background"
➝ Esto indica que existe un problema de accesibilidad: contraste insuficiente entre texto y fondo.

(El documento no muestra más reportes para esta versión.)

📌 2.2 Proyecto: legacy_V2

Principales observaciones detectadas por SonarCloud:

Múltiples ítems reportados (del 1 al 16 según tu archivo), aunque sin descripción textual.

Observación destacada:

Problema en style.css:
"Text does not meet the minimal contrast requirement with its background"
➝ Igual que en la versión anterior, SonarCloud detecta fallas de accesibilidad visual.

(El documento solo presenta números de ítems pero sin descripción, por lo que se reporta lo que realmente está documentado.)

📌 2.3 Proyecto: buenas-practicas

Esta versión muestra reportes más concretos y detallados:

“Prefer Number.parseInt over parseInt”
➝ Sonar recomienda usar la versión moderna y más segura del método para evitar comportamientos inesperados.



📈 3. Comparación General entre Proyectos

<img width="828" height="428" alt="Captura de pantalla 2025-11-23 200244" src="https://github.com/user-attachments/assets/339183e0-db36-4c0d-a8d8-c6c7a9597d81" />


🧠 4. Análisis Profesional
✔ legado_refactoring

Esta versión muestra pocos hallazgos, aunque esto no significa necesariamente que tenga mejor calidad. Podría indicar falta de análisis profundo o poco código evaluado. El único problema documentado está relacionado con accesibilidad visual en CSS.

✔ legacy_V2

Es la versión con más elementos detectados por SonarCloud, aunque el reporte no detalla cada uno de los issues. Se repite el problema de contraste en style.css, lo cual evidencia que el error no se corrigió entre versiones. La cantidad de hallazgos sugiere problemas de mantenibilidad.

✔ buenas-practicas

Es la versión donde se observan mejoras claras en calidad del código, especialmente en JavaScript. El uso recomendado de Number.parseInt indica cumplimiento de estándares modernos de desarrollo. También es la versión con más orden, estructuración y enfoque en buenas prácticas.

🏆 5. Conclusiones

La mejor versión en términos de calidad es buenas-practicas.
Presenta reportes más detallados, buenas prácticas aplicadas y menos problemas repetitivos.

La versión con más problemas aparentes es legacy_V2.
Aunque no se muestran los detalles en tu documento, la cantidad de elementos listados indica que aún existen múltiples issues sin resolver.

legado_refactoring muestra pocos hallazgos, pero no evidencia mejoras profundas.
Puede que sea una versión transicional.

📌 6. Recomendaciones Generales
🔧 Correcciones prioritarias

Arreglar los problemas de contraste en style.css en todas las versiones donde aparezca.

Completar los reportes faltantes en legacy_V2 para entender qué tipo de problemas persisten.

Adoptar estándares modernos como uso correcto de Number.parseInt en todo el proyecto.
