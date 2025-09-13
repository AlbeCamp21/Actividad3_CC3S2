## **Parte teórica**

1. **Introducción a DevOps: ¿Qué es y qué no es?**
   Explica DevOps desde el código hasta la producción, diferenciándolo de waterfall. Discute "you build it, you run it" en el laboratorio, y separa mitos (ej. solo herramientas) vs realidades (CALMS, feedback, métricas, gates).

   DevOps es una forma de trabajo donde es importante la colaboración. Con esta forma, las áreas de desarrollo y operaciones trabajan juntos para desarrollar el software de manera rápida y confiable. El método de cascada es totalmente diferente, acá cada área trabaja por separado, aumentando las probabilidades de que aparezcan errores, retardando el desarrollo del software.

   La frase "you build it, you run it" significa que es el mismo equipo el que crea el software y el que se encarga que funcione en la parte de producción.

2. **Marco CALMS en acción:**
   Describe cada pilar y su integración en el laboratorio (ej. Automation con Makefile, Measurement con endpoints de salud). Propón extender Sharing con runbooks/postmortems en equipo.

   .
   

3. **Visión cultural de DevOps y paso a DevSecOps:**
   Analiza colaboración para evitar silos, y evolución a DevSecOps (integrar seguridad como cabeceras TLS, escaneo dependencias en CI/CD).
   Propón escenario retador: fallo certificado y mitigación cultural. Señala 3 controles de seguridad sin contenedores y su lugar en CI/CD.

   En DevOps la colaboración entre áreas es importante. Todos los equipos comparten información, ayudando así a detectar y resolver problemas más rápido.

   Hablando de DevSecOps, esta es la integración de la seguridad desde el inicio del proyecto. Por ejemplo, aplicando DevSecOps, se puede aplicar escaneo de dependencias en CI/CD

   Controles de seguridad:
   1. Escaneo de dependencias en el momento de integración.
   2. 

4. **Metodología 12-Factor App:**
   Elige 4 factores (incluye config por entorno, port binding, logs como flujos) y explica implementación en laboratorio.
   Reto: manejar la ausencia de estado (statelessness) con servicios de apoyo (backing services).

   1. Logs: Los logs deben enviarse al stdout y no guardarse en archivos. Esto ayudará a que la información sea analizada por herramientas externas.
   2. Config: Usar variables de entorno, permitiendonos cambiar dichas variables de manera rápida sin afectar el código. Por ejemplo, usando el archivo `.env`.
   3. Por binding: La aplicación debe usar/escuchar un puerto definido en un variable, con esto se consigue que se pueda ejecutar en cualquier entorno.
   4. Codebase: Cada aplicación debe tener un único código fuente (repositorio), y este debe ser gestionado con un control de versiones.