# Mi_App - Distribución Profesional JavaFX

Este proyecto es una aplicación desarrollada en **JavaFX** y gestionada con **Maven**. El objetivo principal de este repositorio es demostrar el ciclo completo de distribución de software, desde el código fuente hasta la creación de un instalador ejecutable para Windows que no requiere una instalación previa de Java en el sistema.

## 🚀 Proceso de Distribución

El despliegue de la aplicación se ha realizado siguiendo estos hitos:

### 1. Generación del JAR Ejecutable
He utilizado el plugin `maven-shade-plugin` en el archivo `pom.xml` para empaquetar todas las dependencias de JavaFX en un único **"Fat JAR"**. Esto permite que la aplicación sea portable y se pueda ejecutar mediante el comando:
```bash
java -jar target/PruebaJAR-1.0-SNAPSHOT.jar
2. Creación del Ejecutable (.exe) con Launch4j
Para profesionalizar la entrega, he convertido el JAR en un ejecutable nativo de Windows usando Launch4j:

Modo GUI: Configurado para que la aplicación abra directamente la interfaz gráfica sin mostrar la consola de comandos.

Bundled JRE: He vinculado una carpeta JRE (Java Runtime Environment) interna para que el programa funcione en equipos que no tengan Java instalado.

3. Instalador con Inno Setup
Finalmente, he diseñado un instalador profesional con Inno Setup que ofrece las siguientes características:

Asistente de instalación guiado en varios idiomas.

Creación automática de accesos directos en el escritorio.

Proceso de instalación y desinstalación limpio en el sistema.

📁 Estructura del Repositorio
/src: Código fuente de la aplicación JavaFX.

pom.xml: Configuración de dependencias y plugins de Maven.

/target: Contiene el JAR generado.

/Instalador: Incluye el archivo setup.exe final para el usuario.

🛠️ Tecnologías Utilizadas
Java 21 & JavaFX 21

Maven (Gestión de dependencias)

Launch4j (Wrapper para el .exe)

Inno Setup (Generador del instalador)
