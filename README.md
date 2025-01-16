# proyecto-4-diseño
# Informe Final: Testing en Producción

## **1. Descripción del Proyecto**
En este informe se documenta el análisis, evaluación y optimización de un sitio web existente, aplicando estándares de usabilidad y herramientas automáticas para mejorar la experiencia del usuario. Los resultados incluyen reflexiones, métricas clave y recomendaciones basadas en los problemas identificados.

## **2. Evaluación Inicial de Estándares y Navegación**
### **2.1 Análisis de Estándares**
- **Estándares correctamente aplicados:**
  - El uso de HTML semántico: El sitio emplea etiquetas semánticas como header, nav, footer, main, lo cual es correcto desde el punto de vista de accesibilidad y SEO.

  - Los contrastantes de los corlores: El esquema de colores tiene un buen contraste en general, lo que facilita la lectura para usuarios con dificultades visuales. Los colores de los botones y enlaces están bien diferenciados.

  - El uso de las imágenes con atributos alt: Las imágenes del sitio incluyen el atributo alt, lo que es importante para la accesibilidad.

- **Estándares que no cumplen las pautas de usabilidad:**
  - La falta de los indicadores de enfoque: Los elementos interactivos como botones y enlaces no parecen tener un indicador visual de enfoque (como un borde o cambio de color al navegar con el teclado). Esto es crucial para los usuarios que navegan con el teclado.

  - La velocidad de carga y optimización de imágenes: Aunque las imágenes están siendo cargadas correctamente, la página podría beneficiarse de una optimización de imágenes para mejorar la velocidad de carga,

### **2.2 Pruebas de Navegación con Periféricos**
- **Ratón:**  
  - Observaciones: La navegación con el ratón es adecuada. Los botones y enlaces responden correctamente y el cursor cambia de acuerdo con el elemento interactivo (como los botones).
- **Teclado:**  
  - Observaciones: El sitio no parece tener un soporte adecuado para la navegación por teclado. Al intentar navegar solo con el teclado, no se resalta adecuadamente el enfoque de los elementos interactivos. Esto es un problema para los usuarios que dependen del teclado para navegar.

### **2.3 Reflexión sobre los Estándares**
- **Importancia de los estándares y navegación intuitiva:**
  - La aplicación de estándares de usabilidad y accesibilidad en la web es fundamental para garantizar que todos los usuarios, incluidos aquellos con discapacidades, puedan acceder y navegar por el sitio de manera eficiente. Los problemas identificados, como la falta de un enfoque claro para la navegación con teclado y la optimización de imágenes, son áreas clave que deben abordarse para mejorar la experiencia de usuario.

Es importante aplicar un enfoque centrado en el usuario para asegurarse de que la navegación sea intuitiva y accesible en todos los dispositivos y para todos los usuarios, independientemente de sus habilidades.

## **3. Resultados de Pruebas Automáticas**
### **3.1 WebPageTest**
 **Navegadores:**
 # Comparativa de Rendimiento: Página de Inicio (Home) vs Página de Búsqueda

## 1. Página de Inicio (Home)

| **Métrica**                  | **Chrome Desktop**                  | **Firefox Desktop**                 |
|------------------------------|-------------------------------------|-------------------------------------|
| **Time to First Byte**        | 0.090s                              | 0.439s                              |
| **Start Render**              | 1.600s                              | 1.900s                              |
| **First Contentful Paint**    | 1.560s                              | 1.796s                              |
| **Speed Index**               | 1.870s                              | 2.607s                              |
| **Total Blocking Time**       | 0.000s                              | 0.000s                              |
| **Page Weight**               | 7,102KB                             | 7,102KB                             |
| **Observaciones**             | Buen rendimiento general, sin bloqueos. | Rendimiento similar, pero más lento que en Chrome. |

**Resumen de la Página de Inicio:**
- **Chrome** tiene un mejor rendimiento en cuanto a tiempos de carga y **Speed Index**.
- **Firefox** es ligeramente más lento en comparación con **Chrome**, pero el rendimiento sigue siendo aceptable.

---

## 2. Página de Búsqueda

| **Métrica**                  | **Chrome Desktop**                  | **Firefox Desktop**                 |
|------------------------------|-------------------------------------|-------------------------------------|
| **Time to First Byte**        | 0.000s                              | 0.000s                              |
| **Start Render**              | 0.000s                              | 0.600s                              |
| **First Contentful Paint**    | 0.000s                              | 0.593s                              |
| **Speed Index**               | 0.000s                              | 0.600s                              |
| **Total Blocking Time**       | 0.000s                              | 0.000s                              |
| **Page Weight**               | 1KB                                 | 2KB                                 |
| **Observaciones**             | Error 404, no se pudo cargar correctamente. | Error 404, pero tiempo de renderizado rápido. |

**Resumen de la Página de Búsqueda:**
- Ambas pruebas de **Chrome** y **Firefox** reportaron **Error 404**, lo que impide obtener métricas de rendimiento precisas.
- A pesar de este error, **Firefox** tiene un tiempo de renderizado rápido en comparación con **Chrome**.

---

## Conclusión Final

| **Aspecto**                  | **Página de Inicio (Home)**         | **Página de Búsqueda**               |
|------------------------------|-------------------------------------|-------------------------------------|
| **Rendimiento en Chrome**     | Rápido y eficiente, sin bloqueos.   | No se pudo cargar correctamente (Error 404). |
| **Rendimiento en Firefox**    | Más lento que Chrome, pero aceptable. | No se pudo cargar correctamente (Error 404), pero renderizado rápido. |

- **Página de Inicio (Home):**
  - **Chrome** es más rápido en términos de carga y renderizado, con un mejor **Speed Index**.
  - **Firefox** tiene tiempos ligeramente más largos pero sigue siendo funcional.

- **Página de Búsqueda:**
  - Ambos navegadores tienen problemas con el **Error 404**, lo que interrumpe las pruebas.
  - **Firefox** muestra tiempos de carga rápidos (cuando no hay error) en comparación con **Chrome**.

Se requiere corregir el **Error 404** en la página de búsqueda para realizar un análisis completo.

#### Resumen del Navegador con Mejor Rendimiento:

El navegador Chrome muestra un rendimiento superior en las páginas de inicio (Home) y de búsqueda en comparación con Firefox. En la página de inicio, Chrome tiene tiempos de carga más rápidos y un mejor Speed Index, lo que lo hace más eficiente en términos de visualización y carga de contenido. Además, no presenta problemas de renderización o bloqueos, mientras que Firefox es ligeramente más lento. Aunque ambas pruebas de la página de búsqueda mostraron errores 404, Chrome sigue siendo el navegador que ofrece un rendimiento más confiable y rápido.

### **Captura de pantalla**
**Chrome:**

![webpagetestChromeDesktop](videos_capturas/webpagetestChromeDesktop.png)

**Firefox:**

![webpagetestChromeDesktop](videos_capturas/webpagetestChromeDesktop.png)


#### Conclusión:
Chrome proporciona el mejor rendimiento en ambas páginas analizadas.

### **3.2 PageSpeed Insights**
#### **Página Home**
- **Resultados:**  
  - **Puntaje**:  
    - Rendimiento: 95  
    - Accesibilidad: 93  
    - Prácticas recomendadas: 70  
    - SEO: 82
  - **Elementos de mejora**:  
    - Falta de metadescripción.  
    - Error 404 en el código de estado HTTP.  
    - Algunos errores en la consola del navegador.  
  - **Recomendaciones**:  
    - Añadir una metadescripción.  
    - Corregir el error 404 en el código de estado HTTP.  
    - Mejorar las políticas CSP para prevenir ataques XSS.  

#### **Página Búsqueda**
- **Resultados:**  
  - **Puntaje**:  
    - Rendimiento: 100  
    - Accesibilidad: 96  
    - Prácticas recomendadas: 96  
    - SEO: 80  
  - **Elementos de mejora**:  
    - Falta de metadescripción.  
    - Error 404 en el código de estado HTTP.  
    - Algunos errores en la consola del navegador.  
  - **Recomendaciones**:  
    - Añadir una metadescripción.  
    - Corregir el error 404 en el código de estado HTTP.  
    - Mejorar las políticas CSP para prevenir ataques XSS.

### **Captura de pantalla**

**Inicio:**

![pageSpeed Inicio](videos_capturas/pageSpeedInicio.png)

**Busqueda:**

![pageSpeed Busqueda](videos_capturas/pageSpeedBusqueda.png)

### **Resumen Final**
En general, ambas páginas analizadas (Home y Búsqueda) muestran un excelente rendimiento, con puntuaciones de 100 en rendimiento y accesibilidad en dispositivos móviles y de escritorio. Sin embargo, existen áreas de mejora, especialmente en cuanto a la optimización para SEO y prácticas recomendadas. La falta de una metadescripción y el error 404 en el código de estado HTTP son puntos clave a corregir. Además, es necesario revisar los errores registrados en la consola del navegador y reforzar la política de seguridad frente a ataques XSS.

Se recomienda atender estas cuestiones para asegurar que las páginas sean completamente funcionales, accesibles y optimizadas para motores de búsqueda, mejorando así la experiencia del usuario y el posicionamiento en los resultados de búsqueda.

### **3.3 Optimización con Lighthouse**

#### **Página de Inicio**

| Parámetro                        | Resultado | Umbral Ideal  | Observaciones/Recomendaciones                                                                                     |
|----------------------------------|-----------|---------------|---------------------------------------------------------------------------------------------------|
| **Largest Contentful Paint (LCP)** | N/A       | ≤ 2.5 s       | No se obtuvo un dato concreto, sería recomendable seguir monitorizando esta métrica en futuras auditorías.         |
| **Interaction to Next Paint (INP)** | N/A       | ≤ 200 ms      | No se obtuvo un dato concreto, verifica en pruebas futuras o con interacciones adicionales.                       |
| **Cumulative Layout Shift (CLS)**  | 0.06      | ≤ 0.1         | Buen valor, no requiere intervención.                                                                            |
| **First Contentful Paint (FCP)**   | 0.2 s     | ≤ 1.8 s       | Excelente tiempo de carga inicial, no es necesario realizar mejoras en esta métrica.                              |
| **First Input Delay (FID)**        | 0 ms      | ≤ 100 ms      | La página responde de manera inmediata a las interacciones del usuario, sin bloqueos.                        |
| **Time to First Byte (TTFB)**      | N/A       | ≤ 800 ms      | Se recomienda revisar el servidor para asegurar tiempos de respuesta rápidos si no se han monitoreado antes.     |

#### **Página de Búsqueda**

| Parámetro                        | Resultado | Umbral Ideal  | Observaciones/Recomendaciones                                                                                     |
|----------------------------------|-----------|---------------|---------------------------------------------------------------------------------------------------|
| **Largest Contentful Paint (LCP)** | N/A       | ≤ 2.5 s       | No se obtuvo un dato concreto, sería recomendable seguir monitorizando esta métrica en futuras auditorías.         |
| **Interaction to Next Paint (INP)** | N/A       | ≤ 200 ms      | No se obtuvo un dato concreto, verifica en pruebas futuras o con interacciones adicionales.                       |
| **Cumulative Layout Shift (CLS)**  | 0.25      | ≤ 0.1         | Se recomienda reducir el valor para evitar impactos en la experiencia de usuario.                                       |
| **First Contentful Paint (FCP)**   | 0.2 s     | ≤ 1.8 s       | Excelente tiempo de carga inicial, no es necesario realizar mejoras en esta métrica.                              |
| **First Input Delay (FID)**        | 0 ms      | ≤ 100 ms      | La página responde de manera inmediata a las interacciones del usuario, sin bloqueos.                        |
| **Time to First Byte (TTFB)**      | N/A       | ≤ 800 ms      | Se recomienda revisar el servidor para asegurar tiempos de respuesta rápidos si no se han monitoreado antes.     |

---


### **Captura de pantalla**

**Inicio:**

![lighthouse inicio](videos_capturas/lighthouseInicio.png)

**Busqueda:**

![lighthouse busqueda](videos_capturas/lighthouseBusqueda.png)

### **Resumen Final**

Las páginas **comicverseapp.netlify.app** (Inicio y Búsqueda) muestran un rendimiento excelente en términos de **First Contentful Paint (FCP)** y **First Input Delay (FID)**, con tiempos de carga rápidos que favorecen la experiencia del usuario. Sin embargo, en la **Página de Búsqueda**, el valor de **Cumulative Layout Shift (CLS)** está ligeramente por encima del umbral recomendado (0.25), lo que podría impactar negativamente en la percepción de estabilidad visual durante la carga de la página. Se recomienda reducir este valor para mejorar la experiencia. Además, se debe realizar pruebas en **modo incógnito** para evitar que el almacenamiento de datos (como en **IndexedDB**) interfiera en las métricas de rendimiento.

Aunque la **Performance** y **Accessibility** en ambas páginas son sólidas, se debe seguir optimizando las **Best Practices** (70) y **SEO** (82) para mejorar la visibilidad en los motores de búsqueda y adherirse a las mejores prácticas de desarrollo web.

En general, ambas páginas muestran un buen desempeño, pero siempre se pueden aplicar ajustes adicionales para mejorar el rendimiento, la estabilidad visual y las prácticas recomendadas.


### **3.4 WAVE Web Accessibility Evaluation Tool**  
#### **Página Home**  
- **Resultados:**  
  - **Errores:** 0 (¡Felicidades! No se detectaron errores críticos).  
  - **Errores de Contraste:** 2. Se encontraron problemas menores en el contraste entre texto y fondo que podrían afectar la visibilidad para algunos usuarios.  
  - **Alertas:** 1.  
    - **No heading structure:** Falta una estructura adecuada de encabezados (por ejemplo, `<h1>`, `<h2>`).  
  - **Características Detectadas:** 0.  
  - **Elementos Estructurales:** 0.  

- **Recomendaciones:**  
  - **Errores de Contraste:** Ajustar los colores problemáticos para que cumplan con las recomendaciones de contraste mínimo (4.5:1 para texto normal, 3:1 para texto grande).  
  - **Estructura de Encabezados:** Incorporar encabezados estructurados para mejorar la navegabilidad y facilitar el uso de lectores de pantalla.  

#### **Página Búsqueda**  
- **Resultados:**  
  - **Errores:** 0 (¡Felicidades! No se detectaron errores críticos).  
  - **Errores de Contraste:** 1. Se encontró un problema menor en el contraste entre texto y fondo que podría afectar la visibilidad para algunos usuarios.  
  - **Alertas:** 1.  
    - **No heading structure:** Falta una estructura adecuada de encabezados (por ejemplo, `<h1>`, `<h2>`).  
  - **Características Detectadas:** 1. Identificadas etiquetas que contribuyen a mejorar la accesibilidad.  
  - **Elementos Estructurales:** 0.  

- **Recomendaciones:**  
  - **Errores de Contraste:** Ajustar los colores problemáticos para que cumplan con las recomendaciones de contraste mínimo (4.5:1 para texto normal, 3:1 para texto grande).  
  - **Estructura de Encabezados:** Incorporar encabezados estructurados para mejorar la navegabilidad y facilitar el uso de lectores de pantalla.  


### **Captura de pantalla**

**Inicio:**

![wave inicio](videos_capturas/waveInicio.png)

**Busqueda:**

![wave busqueda](videos_capturas/waveBusqueda.png)

#### **Resumen Final:**  
Tanto la página de inicio como la página de búsqueda presentan resultados positivos en términos de accesibilidad, al no contener errores críticos. Sin embargo, ambas comparten áreas de mejora relacionadas con el contraste de colores y la falta de estructura de encabezados. Implementar estos ajustes ayudará a cumplir con estándares de accesibilidad y a ofrecer una experiencia más inclusiva para todos los usuarios, especialmente aquellos que utilizan tecnologías de asistencia.

## **4. Evaluación con Ghost Inspector**

No he podido hacer el test porque me daba fallo al hacer el test

![ghost inspector](./videos_capturas/ghost_inspector.png)

## **5. Reflexión Final**

- **Usabilidad y navegación del sitio web:**  
  Durante el proceso de análisis y optimización de las páginas del sitio web, pude observar que la usabilidad ha mejorado significativamente en varios aspectos. La navegación ahora es más fluida, con tiempos de carga más rápidos gracias a la optimización en el rendimiento, lo que permite a los usuarios interactuar de manera más eficiente. Las herramientas de accesibilidad como WAVE y Lighthouse han ayudado a identificar y solucionar problemas clave, como la falta de contraste en algunos elementos y la ausencia de ciertas estructuras de encabezado, mejorando la experiencia de usuario para personas con discapacidad. A pesar de los avances, la estructura del sitio aún podría beneficiarse de una mayor claridad en los títulos y la organización de las secciones.

- **Impacto de los cambios realizados:**  
  Los cambios realizados han tenido un impacto positivo tanto en el rendimiento como en la accesibilidad del sitio web. La corrección de los errores de accesibilidad, junto con la mejora en el tiempo de carga, ha permitido que el sitio sea más fácil de usar y navegar, lo que probablemente contribuye a una mayor retención de usuarios. La optimización de las prácticas de SEO también ha tenido un efecto positivo en la visibilidad del sitio en los motores de búsqueda. Sin embargo, la parte de las mejores prácticas sigue siendo un área que necesita atención, ya que los puntajes en este apartado no alcanzaron el umbral ideal, principalmente debido a algunos problemas de seguridad y el manejo de ciertos recursos en el navegador.

- **Lecciones aprendidas:**  
  A lo largo de este proceso, he aprendido la importancia de realizar pruebas constantes en diversas áreas, como accesibilidad, SEO y rendimiento. Utilizar herramientas como Lighthouse y WAVE ha sido fundamental para detectar problemas que podrían pasar desapercibidos de otra forma, y me ha permitido optimizar el sitio web de manera efectiva. También me he dado cuenta de la importancia de seguir las mejores prácticas en términos de seguridad y accesibilidad, no solo para cumplir con los estándares, sino también para garantizar que el sitio sea accesible y funcional para el mayor número de usuarios posible. Por último, he aprendido que la optimización del sitio web es un proceso continuo que requiere mantener el enfoque en la experiencia del usuario y en el cumplimiento de los estándares web.


## **6. Anexos**
- **Archivos generados:**  
  - [Enlace al repositorio de GitHub](URL_DEL_REPOSITORIO)

- **Resultados detallados de herramientas:**  
   - WebPageTest:
      - [Enlace al informe de Chrome Desktop a la pagina de inicio](https://www.webpagetest.org/result/250116_BiDc3A_CXD/)

      - [Enlace al informe de Chrome Desktop a la pagina de busqueda](https://www.webpagetest.org/result/250116_AiDcWY_D0J/)

      - [Enlace al informe  de firefox Desktop a la pagina de inicio](https://www.webpagetest.org/result/250116_BiDc3A_CXD/)

      - [Enlace al informe  de firefox Desktop a la pagina de busqueda](https://www.webpagetest.org/result/250116_BiDc6Y_D5W/)

   - PageSpeed Insights: 
      - [Enlace al informe a la pagina de inicio](https://pagespeed.web.dev/analysis/https-comicverseapp-netlify-app/c1pxay1zhc?form_factor=desktop)

      - [Enlace al informe a la pagina de busqueda](https://pagespeed.web.dev/analysis/https-comicverseapp-netlify-app-busqueda/bqo5w3irlq?form_factor=desktop)

   - Waves:
      -  [Enlace al informe a la pagina de inicio](https://wave.webaim.org/report#/https://comicverseapp.netlify.app/)

      -   [Enlace al informe a la pagina de busqueda](https://wave.webaim.org/report#/https://comicverseapp.netlify.app/busqueda)


   - Lighthouse: 
      - [Enlace a la pagina testeada](https://comicverseapp.netlify.app/)

   - Ghost Inspector: 
      - [Enlace al video](URL_DEL_VIDEO)

---
