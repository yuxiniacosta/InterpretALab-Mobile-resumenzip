RESUMEN_ERRORES_Y_SOLUCIONES.md

Errores principales y soluciones rápidas:

1) Permission denied: getsockopt
   - Causa: bloqueo por proxy/firewall o red hotspot restringida.
   - Solución: No Proxy en Android Studio, permitir Android Studio en firewall, usar otra red o compilar en otra máquina.

2) Kotlin version mismatch (1.9.0 vs 1.5.20)
   - Solución: Alinear versiones; preferible actualizar el IDE o usar kotlin-gradle-plugin 1.9.0 si Android Studio lo soporta.

3) JDK no encontrado en PATH
   - Solución: configurar JAVA_HOME y añadir %JAVA_HOME%\bin al PATH.

4) BuildDir deprecated & typos
   - Solución: eliminar asignaciones innecesarias a buildDir y corregir typos en archivos de configuración.
