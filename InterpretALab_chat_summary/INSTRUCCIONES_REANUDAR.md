INSTRUCCIONES_REANUDAR.md

Pasos rápidos para reanudar el trabajo con Android Studio y el proyecto InterpretALab-Mobile-v2 (Windows 10)

1) Colocar el ZIP / proyecto en la máquina de trabajo
   - GitHub: crear repo y subir la carpeta descomprimida.
   - Google Drive: subir el ZIP y descargar en la máquina de trabajo.
   - Ruta recomendada local: C:\Users\<tu_usuario>\Projects\InterpretALab-Mobile-v2

2) Verificar JDK (obligatorio para Gradle 8.x)
   - Debes tener JDK 17 instalado y JAVA_HOME apuntando a la carpeta del JDK.
   - Verificar en cmd: `java -version` → debe mostrar OpenJDK 17.x.

3) Configurar Android Studio
   - File → Settings → Build, Execution, Deployment → Build Tools → Gradle
     - Use Gradle from: gradle-wrapper.properties
     - Gradle JDK: seleccionar JDK 17
   - File → Settings → Appearance & Behavior → System Settings → HTTP Proxy
     - Seleccionar No Proxy si usas hotspot doméstico.

4) Archivos críticos a revisar
   - gradle/wrapper/gradle-wrapper.properties -> distributionUrl=https\://services.gradle.org/distributions/gradle-8.7-all.zip
   - build.gradle (project level) -> classpath "org.jetbrains.kotlin:kotlin-gradle-plugin:1.9.0"
   - %USERPROFILE%\.gradle\gradle.properties -> agregar org.gradle.jvmargs=-Xmx2048m y limpiar proxy

5) Sincronizar y compilar
   - File → Sync Project with Gradle Files
   - Build → Build Bundle(s) / APK(s) → Build APK(s)
