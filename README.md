# **Capítulo V: Product Implementation, Validation & Deployment**

## **5.1. Software Configuration Management**
Durante el desarrollo del proyecto se emplearán diversas herramientas de trabajo. 

### **5.1.1. Software Development Environment Configuration**

En la siguiente sección se presentan las herramientas de software utilizadas durante el desarrollo del proyecto, junto con las rutas de acceso a cada producto, con el fin de asegurar una colaboración eficiente entre los miembros del equipo.

#### **Herramientas Utilizadas en el Proyecto**


#### **Gestión de Proyectos**

- **WhatsApp**: [https://web.whatsapp.com/](https://web.whatsapp.com/)  
  Empleamos WhatsApp como nuestro medio principal de comunicación, lo que permitió una coordinación fluida del equipo, el seguimiento de actividades y el intercambio constante de ideas a lo largo del desarrollo.



#### **Diseño UX/UI del Producto**

- **Figma**: [https://www.figma.com](https://www.figma.com)  
  Esta herramienta fue utilizada como base para el diseño visual del sistema, facilitando la elaboración de wireframes y mockups tanto de la landing page.

- **Uxpressia**: [https://uxpressia.com/](https://uxpressia.com/)  
  A través de Uxpressia, desarrollamos perfiles de usuario (User Personas) y Mapas de Empatía, impact mapping, elementos clave para comprender mejor las necesidades y expectativas de los usuarios finales.

- **Lucidchart**: [https://www.lucidchart.com/pages/](https://www.lucidchart.com/pages/)  
  Lucidchart nos permitió crear  diagrama de clases y base de datos.



#### **Modelado de Software**

- **Visual Paradigm**: [https://www.visual-paradigm.com/](https://www.visual-paradigm.com/)  
  Con Visual Paradigm elaboramos los diagramas C4 que describen los niveles arquitectónicos del sistema.



#### **Control de Versiones y Documentación**

- **GitHub**: [https://github.com/](https://github.com/)  
  Utilizamos GitHub como plataforma para gestionar la documentación del proyecto, facilitando la colaboración entre los integrantes del equipo y llevando un control detallado de los cambios realizados mediante los commits individuales.




### **5.1.2. Source Code Management**

La organización y administración de las modificaciones realizadas en el proyecto se llevaron a cabo mediante la creación de un repositorio en GitHub. La estructura de este repositorio se organizó de la siguiente forma:

#### **Estructura del Repositorio**

- **Repositorio en GitHub**: [https://github.com/1ASI0730-2510-4366-G1-EduTalent](https://github.com/1ASI0730-2510-4366-G1-EduTalent)  
- **Landing Page**: [https://github.com/1ASI0730-2510-4366-G1-EduTalent/Landing-Page](https://github.com/1ASI0730-2510-4366-G1-EduTalent/Landing-Page)

#### **Ramas Principales**

- **`main`**: Esta rama almacena las versiones finales del repositorio, que son las que se pasan a producción una vez validadas.

- **`develop`**: Es utilizada como punto de integración de las ramas de nuevas funcionalidades (`feature`). Una vez que el equipo determina que la integración está lista, se pasa a la rama `develop` para su revisión final.



#### **Ramas Auxiliares**

- **`refactor/structure`**: Estas ramas están destinadas al desarrollo de funcionalidades generales que serán integradas posteriormente en la rama `develop`. Estas funcionalidades corresponden a las peticiones de los usuarios, tanto para la página de inicio como para la aplicación web.  
  Un ejemplo de estas ramas es `feature/navbar`.



### **5.1.3. Source Code Style Guide & Conventions**


Para garantizar la coherencia y calidad en el desarrollo de nuestra Landing Page y la aplicación web, se implementarán una serie de convenciones específicas para los diferentes lenguajes y tecnologías que utilizamos:

#### **HTML**

- **Tipo de Documento**: Todos los archivos HTML comenzarán con `<!DOCTYPE html>` para asegurar una interpretación correcta del documento.
- **Uso de Minúsculas**: Las etiquetas y atributos HTML siempre estarán en minúsculas, como `<body>` y `<p>`.
- **Cierre de Etiquetas**: Las etiquetas se cerrarán adecuadamente para mantener una estructura ordenada.
- **Atributos con Comillas**: Los valores de los atributos siempre estarán entre comillas, por ejemplo, `<a href="https://example.com">`.
- **Especificaciones de Imágenes**: Se añadirán los atributos `alt`, `width` y `height` en las imágenes para mejorar la accesibilidad y asegurar un diseño responsivo.
- **Atributos sin Espacios**: No habrá espacios alrededor del signo igual en los atributos, por ejemplo, `<link rel="stylesheet" href="styles.css">`.
- **Elemento `<title>`**: No se omitirá el elemento `<title>`, ya que es fundamental para el SEO y la accesibilidad del sitio.
- **Idioma y Codificación**: Usaremos el atributo `lang` para definir el idioma del documento y `<meta charset="UTF-8">` para la codificación de caracteres.
- **Uso de HTTPS**: Todos los recursos externos, como fuentes y multimedia, se cargarán mediante HTTPS para garantizar la seguridad, por ejemplo:  
  `@import 'https://fonts.googleapis.com/css?family=Open+Sans';`.


#### **CSS**

- **Nombres en Minúsculas**: Todos los nombres de elementos, atributos y valores estarán en minúsculas para asegurar consistencia, por ejemplo: `color: #e5e5e5;`.
- **Clases Descriptivas**: Las clases CSS tendrán nombres claros que describan su propósito y estarán separadas por guiones, como `.barra-navegacion`, `.autor-articulo`.
- **Propiedades Abreviadas**: Se emplearán propiedades abreviadas siempre que sea posible, para reducir el tamaño del código y mejorar la legibilidad, por ejemplo: `border-top: 0;`.
- **Colores Hexadecimales Reducidos**: Se utilizarán colores en formato hexadecimal de tres caracteres cuando sea aplicable, como `color: #ebc;`.
- **Orden Alfabético**: Las propiedades CSS dentro de un bloque estarán organizadas en orden alfabético para facilitar su mantenimiento.
- **Uso de Punto y Coma**: Cada declaración CSS terminará con un punto y coma para evitar errores de interpretación, por ejemplo: `display: block;`.
- **Espaciado Consistente**: Se aplicará un espacio después de los dos puntos en las declaraciones y entre las llaves que abren un bloque, como en `font-weight: bold;`.
- **Comillas Simples en Atributos**: Los valores de los atributos en CSS se escribirán entre comillas simples, por ejemplo:  
  `font-family: 'Open Sans', Arial, sans-serif;`.
#### **JS**

 - **El fragmento de código JavaScript se utiliza para mejorar la experiencia del usuario en la interfaz web, agregando interactividad tanto al encabezado como al menú de navegación.  
 - **Sticky Header**: La primera parte del script aplica la clase `sticky` al elemento `<header>` cuando el usuario hace scroll más de 60 píxeles, logrando que el encabezado permanezca visible en la parte superior de la pantalla.  
 - **Menú Responsive**: La segunda parte controla la funcionalidad del menú responsive. Al hacer clic en el ícono con el ID `menu-icon`, se alterna la clase `bx-x` para cambiar el ícono (por ejemplo, de hamburguesa a una "X") y se activa o desactiva la clase `open` en la barra de navegación `.navbar`, permitiendo mostrar u ocultar el menú según la interacción del usuario.




### **5.1.4. Software Deployment Configuration**

## **5.2. Landing Page, Services & Applications Implementation**
### **5.2.1. Sprint 1**
#### **5.2.1.1. Sprint Planning 1**

#### **5.2.1.2. Sprint Backlog 1**


#### **5.2.1.3. Development Evidence for Sprint Review**

#### **5.2.1.4. Testing Suite Evidence for Sprint Review**


#### **5.2.1.5. Execution Evidence for Sprint Review**

#### **5.2.1.6. Services Documentation Evidence for Sprint Review**

#### **5.2.1.7. Software Deployment Evidence for Sprint Review**



#### **5.2.1.8. Team Collaboration Insights during Sprint**
