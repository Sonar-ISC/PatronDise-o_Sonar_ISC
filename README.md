# Proyecto: Implementación de un Patrón de Diseño - Page Object Model (POM)

## Integrantes
- **Cesar David Villegas Naranjo**
- **Valentina Rosas Coral**

## Objetivo
El propósito de este proyecto es implementar el patrón de diseño **Page Object Model (POM)** para automatizar las pruebas de una página web utilizando **Python** y **Selenium**. Este proyecto forma parte de las actividades realizadas dentro del **semillero Sonar ISC**, donde aprendimos sobre **automatización de pruebas** y **patrones de diseño de software**.

## Actividades del Semillero

### 1. **Introducción a Python y Selenium**
A lo largo de varias sesiones en el semillero, tuvimos la oportunidad de familiarizarnos con herramientas esenciales para la automatización de pruebas, como **Python** y **Selenium**. Estas herramientas nos permitieron desarrollar un enfoque práctico de la automatización web, utilizando un navegador real para interactuar con los elementos de una página.

Durante las sesiones, **Selenium** fue presentado como un framework de automatización de pruebas que facilita la interacción con elementos de una página web, como formularios, botones y campos de texto. Aprendimos a controlar un navegador desde Python para realizar acciones como hacer clic, introducir texto y validar los resultados esperados en una página web.

**Python**, como lenguaje de programación, se utilizó por su sencillez y poderosas bibliotecas, que hacen que sea una opción excelente para tareas de automatización y pruebas.

### 2. **Estudio de Patrones de Diseño**
En paralelo, exploramos el concepto de **patrones de diseño**, que son soluciones reutilizables a problemas comunes en el desarrollo de software. En particular, nos centramos en el **Page Object Model (POM)**, un patrón de diseño utilizado para automatizar pruebas de manera efectiva y organizada.

El patrón **POM** sugiere que cada página de la aplicación que estamos probando sea representada por una clase, que se encarga de gestionar la interacción con los elementos de esa página. Este patrón facilita la reutilización de código y mejora la mantenibilidad, ya que cualquier cambio en la página (como un cambio en los elementos de la interfaz) solo requerirá modificaciones en la clase correspondiente, sin necesidad de cambiar cada uno de los scripts de prueba.

### 3. **Implementación del Proyecto**
#### Selección de la Página para la Automatización
Para este proyecto, elegimos automatizar las pruebas de la página web [http://the-internet.herokuapp.com/login](http://the-internet.herokuapp.com/login). Esta página web es un entorno de prueba comúnmente utilizado para aprender y practicar automatización de pruebas. Cuenta con un formulario de inicio de sesión que permite experimentar con diferentes tipos de pruebas, tanto con credenciales válidas como inválidas.

La página cuenta con:
- Un campo para ingresar el nombre de usuario.
- Un campo para ingresar la contraseña.
- Un botón de inicio de sesión.
- Un mensaje de "flash" que aparece después de intentar iniciar sesión, el cual puede ser un mensaje de éxito o error, dependiendo de las credenciales ingresadas.

#### Diseño del Código
El diseño del código fue implementado siguiendo el patrón **Page Object Model (POM)**. Creamos dos clases principales:
1. **LoginPage**: Representa la página de inicio de sesión y contiene los métodos que interactúan con los elementos de la página (como los campos de texto y el botón de inicio de sesión).
2. **LoginTest**: Contiene los métodos de prueba que validan el comportamiento de la página de inicio de sesión, como verificar los mensajes de éxito o error.

Cada clase fue estructurada para que la interacción con los elementos de la página esté claramente separada de la lógica de las pruebas, lo que permite una mejor organización y mantenimiento del código.

#### Pruebas de Funcionalidad
Las pruebas implementadas incluyen:
- **Prueba de inicio de sesión con credenciales válidas**: Se verifica que al ingresar un nombre de usuario y contraseña correctos, el mensaje de éxito "You logged into a secure area!" sea mostrado.
- **Prueba de inicio de sesión con credenciales inválidas**: Se verifica que al ingresar credenciales incorrectas, el mensaje de error "Your username is invalid!" sea mostrado.

Estas pruebas fueron automatizadas utilizando **Selenium**, lo que permite ejecutar las pruebas de manera repetitiva y consistente.

### 4. **Frameworks de Pruebas**
Además de **Selenium**, también aprendimos sobre **frameworks de pruebas** en el semillero. Un **framework de pruebas** es una estructura que organiza y facilita la ejecución de pruebas automatizadas. El framework más comúnmente utilizado para automatizar pruebas en Python es **unittest**, que nos permitió ejecutar y verificar nuestras pruebas de manera sencilla y estructurada.

#### ¿Qué es Selenium?
**Selenium** es una herramienta popular para la automatización de pruebas web que soporta varios lenguajes de programación, como Python, Java, C#, entre otros. En este proyecto, utilizamos **Selenium WebDriver** con Python para controlar el navegador, interactuar con los elementos de la página y verificar que la página se comporte como se espera.

### 5. **Estructura del Proyecto**
El proyecto está estructurado de la siguiente manera:

```plaintext
.
├── src/                   # Código fuente del proyecto
│   ├── LoginPage.py       # Página del formulario de inicio de sesión
│   └── LoginTest.py       # Pruebas para el inicio de sesión
├── .gitignore             # Archivos que deben ser ignorados por Git
├── README.md              # Descripción general del proyecto
