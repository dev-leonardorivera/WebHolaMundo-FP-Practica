# Descripción del Proyecto: Hola Mundo en Entorno Cliente

**Módulo:** Desarrollo Web en Entorno Cliente

**Unidad Didáctica:** UD 1. Arquitecturas y lenguajes de programación en clientes web

**Autor/a:** Leonardo

## 1. Introducción y Objetivos

Este documento describe una aplicación web mínima desarrollada para ilustrar los conceptos fundamentales de la **UD 1: Arquitecturas y lenguajes de programación en clientes web**.

El objetivo principal es comprobar el funcionamiento básico de la ejecución de código en el lado del cliente (navegador web), estructurando el contenido estático mediante **HTML** y ejecutando lógica de programación mediante **JavaScript**.

## 2. Arquitectura del Proyecto

La aplicación sigue una arquitectura puramente del lado del cliente. Todo el procesamiento se realiza en el navegador web del usuario, el cual descarga, interpreta y ejecuta los archivos estáticos de forma local.

El proyecto está compuesto por dos ficheros organizados en una estructura básica:
1. **`index.html`**: Página principal que define la estructura del documento y enlaza el script externo.
2. **`js/main.js`**: Archivo de script que contiene la lógica en JavaScript y se encarga de registrar eventos del ciclo de vida de la ventana y mostrar mensajes por consola.

## 3. Descripción de los Ficheros del Código Fuente

### 3.1. Estructura HTML (`index.html`)

El código HTML define la estructura básica de la página e incorpora la etiqueta `<script>` en la cabecera con la ruta correspondiente al directorio `js/`.

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <script src="js/main.js"></script>
  </head>
  <body>
    <h1>
      ESTO es un ejemplo para la tarea de Desarrollo web en entorno cliente UD1
    </h1>
  </body>
</html>
```

### 3.2. Lógica en JavaScript (`js/main.js`)

El archivo JavaScript utiliza el evento `window.onload` para asegurar que todos los recursos de la página se han cargado por completo antes de invocar la función `saludar()`, la cual emite un mensaje personalizado por la consola de desarrollo del navegador.

```javascript
// ejemplo de codigo js
window.onload = function () {
  saludar();
};

function saludar() {
  console.log("Hola, mundo! Soy leonardo");
}
```

## 4. Conclusiones y Relación con la UD 1

Este ejercicio sencillo pero ilustrativo permite comprobar los siguientes aspectos teóricos de la unidad:
* **El navegador como máquina virtual de cliente:** Capaz de interpretar lenguajes de marcado y lenguajes de programación interpretados como JavaScript.
* **El ciclo de vida de la página (`window.onload`):** Control del momento adecuado para ejecutar scripts tras la carga completa del DOM y los recursos asociados.
* **La consola del navegador:** Utilizada como herramienta básica de depuración y salida de datos (`console.log`) en el entorno de desarrollo cliente.