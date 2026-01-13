# Memoria de Proyecto: Distribución y Despliegue de Mi_App

Este documento detalla el proceso técnico seguido para convertir una aplicación JavaFX en un producto listo para el usuario final en entornos Windows.

---

## 📄 Memoria del Proceso (Explicación paso a paso)

A continuación, explico los pasos realizados basándome en las capturas del proceso:

### Paso 1: Generación del JAR con Maven
En esta captura muestro mi archivo `pom.xml` configurado con el plugin *Shade* para empaquetar las dependencias de JavaFX. Se observa en el panel lateral de Maven que el proceso de empaquetado finalizó con éxito. El resultado es el archivo `.jar` que aparece en mi carpeta `target`, listo para ser convertido en ejecutable.

### Paso 2: Configuración básica en Launch4j
Aquí comienzo la conversión del JAR a un archivo `.exe` mediante la herramienta Launch4j. Defino la ruta de salida para el ejecutable y vinculo el archivo JAR generado previamente en el paso anterior. Es el primer paso técnico para transformar mi aplicación Java en un programa nativo de Windows.

### Paso 3: Configuración del modo GUI
En esta pestaña selecciono el tipo de encabezado **"GUI"** para mi aplicación. Con esto cumplo el requisito de la tarea de que el programa abra directamente la interfaz gráfica sin mostrar la consola de comandos. Esto mejora significativamente la experiencia de usuario y la estética profesional del software.

### Paso 4: Vinculación del JRE (Portabilidad)
En esta captura configuro el **"Bundled JRE path"** escribiendo la palabra `jre`. Esto indica al ejecutable que debe usar la carpeta de Java que he incluido manualmente en mi proyecto. Así, garantizo que la aplicación funcione en cualquier ordenador, aunque el usuario no tenga Java instalado.

### Paso 5: Información en Inno Setup
Una vez listo el `.exe`, inicio el asistente de **Inno Setup** para crear el instalador final. Aquí relleno los datos básicos como el nombre de la aplicación ("PruebaJAR") y la versión del software. Este paso es el comienzo para generar un asistente de instalación guiado y profesional.

### Paso 6: Selección de archivos del instalador
En esta sección del asistente añado el ejecutable principal y, muy importante, la carpeta `jre` y el archivo `.jar`. Al incluir estos archivos, me aseguro de que el instalador copie todo lo necesario en el PC del usuario. Es la base para que el programa se instale de forma completa y funcional.

### Paso 7: Creación de accesos directos
Aquí configuro la creación de iconos para facilitar el acceso al programa tras la instalación. Marqué la casilla para que el instalador cree automáticamente un **acceso directo en el escritorio** del usuario. Este detalle mejora la usabilidad y cumple con los estándares de calidad que pide la rúbrica.

### Paso 8: Resultado e instalación final
Muestro la selección de idioma y la prueba definitiva de funcionamiento con la ventana **"Hello!"** abierta. Esta imagen confirma que el instalador ha ubicado los archivos correctamente y que el ejecutable encuentra su JRE interno. El programa se instala, se ejecuta y se visualiza perfectamente sin errores.

---

## 🛠️ README del Repositorio (GitHub)

# Mi_App - Distribución Profesional JavaFX

Este proyecto es una aplicación desarrollada en **JavaFX** y gestionada con **Maven**. El objetivo es demostrar el ciclo completo de distribución de software para Windows.

## 🚀 Características del Despliegue
* **Fat JAR:** Empaquetado de todas las dependencias mediante `maven-shade-plugin`.
* **Ejecutable Nativo:** Archivo `.exe` generado con Launch4j que oculta la consola de comandos.
* **JRE Integrado:** Incluye su propio entorno de ejecución para funcionar sin Java preinstalado.
* **Instalador Profesional:** Generado con Inno Setup, incluyendo desinstalador y accesos directos.

## 📁 Estructura
* `/src`: Código fuente.
* `pom.xml`: Gestión de dependencias.
* `/target`: Artefactos generados (JAR).
* `setup.exe`: Instalador listo para su distribución.

## 💻 Requisitos para Compilar
1. Java JDK 21.
2. Maven.
3. Launch4j e Inno Setup (para generar el instalador).

---
**Autor:** [Tu Nombre]  
*Proyecto para el módulo de Desarrollo de Interfaces.*
