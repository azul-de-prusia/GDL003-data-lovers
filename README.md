# Data Lovers

## Índice

- [Preámbulo](#preámbulo)
- [Descripción](#resumen-del-proyecto)
- [Consideraciones generales](#consideraciones-generales)
- [Objetivos de aprendizaje](#objetivos-de-aprendizaje)
- [Parte obligatoria](#parte-obligatoria)
- [Parte opcional](#parte-opcional-hacker-edition)
- [Consideraciones técnicas](#consideraciones-técnicas)
- [Contenido de referencia](#contenido-de-referencia)
- [Checklist](#checklist)

---

## Preámbulo

Según un [estudio de IBM](https://www-01.ibm.com/common/ssi/cgi-bin/ssialias?htmlfid=WRL12345USEN),
el 90% de la data que existe hoy ha sido creada durante los últimos dos años.
Cada día generamos 2.5 trillones de bytes de datos, una cifra sin precedentes.

No obstante, los datos por sí mismos son de poca utilidad. Para que esas
grandes cantidades de datos se conviertan en **información** fácil de leer para
los usuarios, necesitamos entender y procesar estos datos. Una manera simple de
hacerlo es creando _interfaces_ y _visualizaciones_.

En la siguiente imagen, podrás ver cómo con la data que que se ve en la parte
izquierda se puede construir una interfaz amigable y entendible por el usuario.

![json-interfaz](https://lh4.googleusercontent.com/Tn-RPXS26pVvOTdUzRT1KVaJ-_QbFs9SpcGLxSPE43fgbHaXtFgMUInuDt7kV41DkT1j8Tt29V0LxQW7SMtC6digOIhfTXSBKdwI08wUwhD3RAqlwy0hjfmhZ2BFe91mtmCSEqysfgk)

\* Puedes ver el detalle de la data [aquí](https://gist.github.com/lalogf/dd4aa3017a9f8aa8f90dfbca382c4dc9#file-student-json)
y la interfaz construida [aquí](https://app.talento.laboratoria.la/profile/HFOoMpOreBU2psCcjjLg5O2EWEv2).

## Resumen del proyecto

En este proyecto construimos una _página web_ para visualizar un
_conjunto (set) de datos que se adecúe a lo que nuestro usuario definido
necesita.

A continuación se ecuentra la fuente de nuestros datos, que provienen de la serie Rick and Morty:

- [Rick and Morty](src/data/rickandmorty/rickandmorty.json).
  Este set nos proporciona la lista de los personajes de la serie Rick and
  Morty. Puedes revisar la documentación de su API en este [link](https://rickandmortyapi.com).


Como entregable final tendrás una página web que permita **visualizar la data,
filtrarla, ordenarla y hacer algún cálculo agregado**. Como aclaración,
con cálculo agregado nos referimos a distintos cálculos que puedes hacer con
la data que tienes para mostrar información aún más relevante a los usuarios.
Una opción serían cálculos estadísticos como el promedio, el máximo o el mínimo,
por ejemplo, si tenemos una colección que representa a un grupo de personas,
y cada persona está representada como un _objeto_ con una _propiedad_ `altura`,
podríamos elegir calcular la altura promedio en el grupo entre otras cosas.

## Consideraciones generales

- El proyecto será entregado subiendo tu código a GitHub (commit/push) y la
  interfaz será desplegada usando [GitHub Pages](https://pages.github.com/).


- Este proyecto se desarrolló en una dupla formada por Gloria Ramírez Robles y Tegthyn Coral Quiñones Gutiérrez como el segundo proyecto del bootcamp de Laboratoria, el cual se titula _Data Lovers_.
- Tiempo para completarlo: 3 semana divididas en 3 sprints (una entrega del producto funcional al término de cada sprint).

## Objetivos de aprendizaje

El objetivo principal de este proyecto es que aprendas a diseñar y construir una
interfaz web donde se pueda visualizar y manipular data, entendiendo lo que el
usuario necesita.

Dicho en palabras sencillas, aprenderás a:

- Aplicar y profundizar todo lo que aprendiste en el proyecto anterior.
- Pensar en las **necesidades de los usuarios** para crear historias de usuario.
- Escribir y trabajar con **historias de usuario**, sus definiciones de
  terminado (_definition of done_) en la organización y planificación de tu
  trabajo.
- Definir qué data y de qué forma mostrarla en el producto, basándote en
  tu **entendimiento del usuario**.
- Crear productos que sigan los **principios básicos de diseño visual** y
  las **heurísticas de usabilidad**.
- Iterar el diseño del producto, basándote en los resultados de los
  **tests de usabilidad**.
- Manipular **_arreglos_ (_arrays_) y _objetos_ (_objects_)**.
- **Manipular el DOM** (agregar elementos dinámicamente basados en la data).
- **Manejar eventos del DOM** para permitir interacción con el usuario
  (filtrado, ordenado, ...).
- Entender los beneficios y complejidades de **trabajar en equipo** en un
  ambiente de incertidumbre.

## Alcances esperados

Los criterios para considerar que has completado este proyecto son:

### Definición del producto

Este ejercicio de Web app está diseñado para que el usuario Rick Sánchez tenga acceso a la información básica de todos los seres del multiverso en que se desarrolla la serie.

La presente Web app provee esta información ordenada en base a los filtros seleccionados a partir de la cual se muestran los datos ordenados en dos formas; en una estadística y en tarjetas de identificación, las cuales a su vez pueden ser seleccionadas individualmente y se ordenan alfabéticamente.

En conclusión, este proyecto cubre la función de monitoreo de los personajes, su localización, estatus, etc. para que Rick pueda continuar con sus investigaciones evadiendo la justicia y a quienes lo persiguen, considerando esta información.

Los criterios de diseño están basados en la estética visual propia de la serie, para favorecer el hecho de que pueda verse como si fuera una Web app que usa Rick dentro de la serie para agendar sus planes, a manera de metahistoria. De forma general tratamos de apegarnos a los colores saturados, elementos delineados en negro y un  poco de volumen a algunos objetos como botones.

### Historias de usuario

Yo, Rick Sánchez de la Tierra C-137 (https://es.wikipedia.org/wiki/Rick_S%C3%A1nchez_(personaje)) quiero una base de datos para monitorear a todo el universo, poder anticiparme a sus planes y conocer su ubicación exacta. Ello me ayudará a planear mis actividades minimizando los riesgos y con resultados óptimos.

![alt text](https://www.lavanguardia.com/r/GODO/LV/p5/WebSite/2018/05/10/Recortada/img_psola_20170929-140352_imagenes_lv_terceros_rick-and-morty-season-3-episode-1-review-the-rickshank-redemption-kQJG-U443479379590EYD-992x558@LaVanguardia-Web.jpg)

Definition of done:
1. Inicio de sesión, pensado para que sólo nuestro único usuario pueda acceder.
2. Seleccionar los filtros para la búsqueda, para estadísticas o por palabra.
 * Mostrar la información filtrada alfabéticamente, donde se puede elegir entre orden ascendente o descendente.
 * Mostrar las estadísticas para el filtro seleccionado.
 * En caso de no encontrarse resultados para la búsqueda mostrar una leyenda que así lo especifique.
3. Las 3 opciones anteriores tienen la opción de regresar para hacer otra búsqueda.
4. Todo el código estará enmarcado en un diseño responsivo pensando en que pueda ser usado en diferentes dispositivos manteniendo el orden y el diseño inicial.
5. Al finalizar el proyecto podrán ejecutarse satisfactoriamente los tests de usabilidad y funcionalidad.


### Diseño de la Interfaz de Usuario

Siguiendo la temática de la serie y los inventos de Rick Sanchez, el diseño de la web app se pensó para ser mostrado como si fuera un aparato utilizado por Rick. Se busca simular la interfaz con la que funcionaría dentro del universo de la serie un aparato con objetivos similares a nuestra historia de usuario, utilizando los colores saturados y delineados en negro ya caracteristicos.

#### Prototipo de baja fidelidad

En un inicio creamos un boceto del prototipo en un post it, con detalles que considerabamos vitales al estar trabajando con el Definition of done y que debiamos tomar en cuenta al hacer el prototipo en papel
![](https://i.ibb.co/phQqMkw/IMG-20190624-185118.jpg)

Al momento de realizar el prototipo en lapiz y papel con mayor conciencia de las páginas que necesitabamos, nos basamos en lo anteriormente creado en el post it y en el feedback recibido  por nuestras compañeras para incluirlo en el prototipo.
![](https://i.ibb.co/XXJwBKX/IMG-20190624-145442.jpg)
![](https://i.ibb.co/yyX0R0F/IMG-20190624-145500.jpg)

Estos son los dibujos en los que basamos el diseño que teniamos pensado para la interfaz de la web app, simulando desde un principio el aparato donde se manejarán los datos.

#### Prototipo de alta fidelidad

Teniendo ya claro el estilo y las páginas que queriamos utilizar en nuestra web app, buscamos una imagen que se adaptará al aparato que buscamos simular, y con ayuda de editores de gráficos(gimp y photoshop) la limpiamos de detalles externos(fondo, manos, borrar lo que ya aparecía en la pantalla del mismo), y agregamos el diseño que buscabamos tuviera en nuestro proyecto. A su vez utilizamos Marvel para agregar algunos botones con el mismo estilo ya utilizado y creamos un prototipo de alta fidelidad con botones funcionales para recorrer la interfaz de la web app.

## https://marvelapp.com/541bc74

El principal reto con lo esperado en base al diseño de nuestro prototipo de alta fidelidad será poder diseñar la web app dentro de la pantalla del aparato, con todos sus formularios y botones funcionales dentro de un diseño responsivo. En caso de estar limitadas con el tiempo nos enfocaremos en recrear solo la pantalla del aparato para mas adelante en el sprint 3 de iteración buscar lograr el resultado esperado con el diseño de la pantalla y que funcione de manera responsiva.

Lo siguiente es diseñar tu Interfaz de Usuario (UI por sus siglas en inglés -
_User Interface_). Para eso debes aprender a utilizar alguna herramienta de
diseño visual. Nosotros te recomendamos [Figma](https://www.figma.com/) que es
una herramienta que funciona en el navegador y, además, puedes crear una cuenta
gratis. Sin embargo, eres libre de utilizar otros editores gráficos como
Illustrator, Photoshop, PowerPoint, Keynote, etc.

El diseño debe representar el _ideal_ de tu solución. Digamos que es lo que
desearías implementar si tuvieras tiempo ilimitado para hackear. Además, tu
diseño debe seguir los fundamentos de _visual design_. También, te recomendamos exportar
tu diseño a [Zeplin](https://zeplin.io/) y podrías utilizar las especificaciones de
estilo que te proporcione Zeplin al momento de implementar tus diseños en código.

#### Testeos de usabilidad

Durante el reto deberás realizar tests de usabilidad con distintos usuarios, y
en base a los resultados de esos tests, deberás iterar tus diseños. Cuéntanos
qué problemas de usabilidad detectaste a través de los tests y cómo los
mejoraste en tu propuesta final.

### Implementación de la Interfaz de Usuario (HTML/CSS/JS)

Luego de diseñar tu interfaz de usuario deberás trabajar en su implementación.
Como mencionamos, **no** es necesario que construyas la interfaz tal como la
diseñaste. Tendrás un tiempo limitado para hackear, así es que deberás
priorizar.

Como mínimo, tu implementación debe:

1. Mostrar la data en una interfaz: puede ser un card, una tabla, una lista, etc.
2. Permitir al usuario filtrar y ordenar la data.
3. Calcular estadísticas de la colección (o subcolección) como media aritmética,
   máximo y/o mínimo de algún atributo numérico, o contar cuántas veces aparece
   un determinado valor, por ejemplo.
4. Visualizarse sin problemas desde distintos tamaños de pantallas: móviles,
   tablets y desktops.

Es importante que tu interfaz, a pesar de ser una versión mínima de tu ideal,
siga los fundamentos de _visual design_.

### Pruebas unitarias

El _boilerplate_ de este proyecto no incluye pruebas unitarias, pero esperamos
que escribas tus propias pruebas unitarias para las funciones encargadas de
_procesar_, _filtrar_ y _ordenar_ la data, así como _calcular_ estadísticas.
Para ello te recomendamos implementar las siguientes funciones en el archivo
`src/data.js`:

- `filterData(data, condition)`: esta función `filter` o filtrar recibiría la
  data, y nos retornaría aquellos datos que sí cumplan con la condición.

- `sortData(data, sortBy, sortOrder)`: esta función `sort` u ordenar
  recibe tres parámetros.
  El primer parámetro, `data`, nos entrega los datos.
  El segundo parámetro, `sortBy`, nos dice con respecto a cuál de los campos de
  la data se quiere ordenar.
  El tercer parámetro, `sortOrder`, indica si se quiere ordenar de manera
  ascendente o descendente.

- `computeStats(data)`: la función `compute` o calcular, nos permitirá hacer
  cálculos estadísticos básicos para ser mostrados de acuerdo a la data
  proporcionada.

Estas son propuestas de funciones que podrías implementar.

El archivo `src/data.js` debe tener una cobertura del 70% de _statements_
(_sentencias_), _functions_ (_funciones_), _lines_ (_líneas_), y _branches_
(_ramas_).

**Estas funciones deben ser [_puras_](https://medium.com/laboratoria-developers/introducci%C3%B3n-a-la-programaci%C3%B3n-funcional-en-javascript-parte-2-funciones-puras-b99e08c2895d)
e independientes del DOM**. Estas funciones serán después usadas desde el archivo
`src/main.js`, al cargar la página, y cada vez que el usuario interactúe (click,
filtrado, ordenado, ...).

## Hacker edition

Features/características extra sugeridas:

- En lugar de consumir la data estática brindada en este repositorio, puedes
  consumir la data de forma dinámica, cargando un archivo JSON por medio de
  `fetch`. La carpeta `src/data` contiene una versión `.js` y una `.json`
  de cada set datos.
- Agregarle a tu interfaz de usuario implementada visualizaciones gráficas. Para
  ello te recomendamos explorar librerías de gráficas como [Chart.js](https://www.chartjs.org/)
  o [Google Charts](https://developers.google.com/chart/).


## Consideraciones técnicas

La lógica del proyecto debe estar implementada completamente en JavaScript
(ES6), HTML y CSS. En este proyecto NO está permitido usar librerías o
frameworks, solo [vanilla JavaScript](https://medium.com/laboratoria-how-to/vanillajs-vs-jquery-31e623bbd46e),
con la excepción de librerías para hacer gráficas (charts); ver
[_Hacker Edition_](#parte-opcional-hacker-edition) más arriba.

No se debe utilizar la _pseudo-variable_ `this`.

El _boilerplate_ contiene una estructura de archivos como punto de partida así
como toda la configuración de dependencias:

```text
.
├── package.json
├── README.md
├── src
│   ├── data
│   │   ├── injuries
│   │   │   ├── injuries.js
│   │   │   └── injuries.json
│   │   ├── lol
│   │   │   ├── lol.js
│   │   │   └── lol.json
│   │   ├── pokemon
│   │   │   ├── pokemon.js
│   │   │   └── pokemon.json
│   │   ├── steam
│   │   │   ├── steam.js
│   │   │   └── steam.json
│   │   └── worldbank
│   │       ├── worldbank.js
│   │       └── worldbank.json
│   ├── data.js
│   ├── index.html
│   ├── main.js
│   └── style.css
└── test
    └── data.spec.js

8 directories, 17 files
```

### `src/index.html`

Al igual que en el proyecto anterior, existe un archivo `index.html`. Como ya
sabrás, acá va la página que se mostrará al usuario. También nos sirve para
indicar qué scripts se usarán y unir todo lo que hemos hecho.

En este archivo encontrarás una serie de _etiquetas_ (_tags_) `<script>`
_comentadas_. Para _cargar_ las diferentes fuentes de datos tendrás que
_descomentar_ estas _etiquetas_. Cada uno de estos scripts asignará una variable
global con la data correspondiente a esa fuente de datos.

Por ejemplo, si descomentamos la siguiente línea:

```html
<!-- <script src="./data/worldbank/worldbank.js"></script> -->
```

La línea quedaría así:

```html
<script src="./data/worldbank/worldbank.js"></script>
```

Y ahora tendríamos la variable global `WORLDBANK` disponible en nuestros otros
scripts (como `src/data.js` o `src/main.js`).

### `src/main.js`

Recomendamos usar `src/main.js` para todo tu código que tenga que ver con
mostrar los datos en la pantalla. Con esto nos referimos básicamente a la
interacción con el DOM. Operaciones como creación de nodos, registro de
manejadores de eventos (_event listeners_ o _event handlers_), ....

Esta no es la única forma de dividir tu código, puedes usar más archivos y
carpetas, siempre y cuando la estructura sea clara para tus compañeras.

### `src/data.js`

El corazón de este proyecto es la manipulación de datos a través de arreglos y
objetos. La idea de este archivo es contener toda la funcionalidad
que corresponda a obtener, procesar y manipular datos.

En este archivo esperamos que implementes las funciones detalladas en la sección
de [_Pruebas Unitarias_](#pruebas-unitarias).

### `src/data`

En esta carpeta están los datos de las diferentes fuentes. Encontrarás una
carpeta por cada fuente, y dentro de cada carpeta dos archivos: uno con la
extensión `.js` y otro `.json`. Ambos archivos contienen la misma data; la
diferencia es que el `.js` lo usaremos a través de una etiqueta `<script>`,
mientras que el `.json` está ahí para opcionalmente cargar la data de forma
asíncrona con [`fetch()`](https://developer.mozilla.org/es/docs/Web/API/Fetch_API)
(ver sección de [_Parte Opcional_](#parte-opcional-hacker-edition)).

### `test/data.spec.js`

Tendrás también que completar las pruebas unitarias de las funciones
implementadas en el archivo `data.js`.


---

## Pistas sobre cómo empezar a trabajar en el proyecto

Antes de empezar a escribir código, debes definir qué deberá hacer el producto
en base al conocimiento que puedas obtener de tu usuario. Estas preguntas te
pueden ayudar:

- ¿Quiénes son los principales usuarios de producto?
- ¿Cuáles son los objetivos de estos usuarios en relación con el producto?
- ¿Cuáles son los datos más relevantes que quieren ver en la interfaz y por qué?
- ¿Cuándo utilizan o utilizarían el producto?

Cuando ya estés lista para codear, te sugerimos empezar de esta manera:

1. Una de las integrantes del equipo debe realizar un :fork_and_knife:
   [fork](https://help.github.com/articles/fork-a-repo/) del repo de tu cohort,
   tus \_coaches\* te compartirán un \_link\* a un repo y te darán acceso de lectura
   en ese repo. La otra integrante del equipo deber hacer un fork **del
   repositorio de su compañera** y [configurar](https://gist.github.com/BCasal/026e4c7f5c71418485c1)
   un `remote` hacia el mismo.
2. :arrow_down: [Clona](https://help.github.com/articles/cloning-a-repository/)
   tu :fork_and_knife: [fork](https://help.github.com/articles/fork-a-repo/) a tu computadora (copia local).
3. 📦 Instala las dependencias del proyecto con el comando `npm install`. Esto
   asume que has instalado [Node.js](https://nodejs.org/) (que incluye [npm](https://docs.npmjs.com/)).
4. Si todo ha ido bien, deberías poder ejecutar las :traffic_light:
   pruebas unitarias (unit tests) con el comando `npm test`.
5. A codear se ha dicho! :rocket:

---

## Contenido de referencia

### Diseño de experiencia de usuario (User Experience Design)

- Investigación con usuarios / entrevistas
- Principios de diseño visual

### Desarrollo Front-end

- Unidad de testing en curso de JavaScript en LMS.
- Unidad de arreglos en curso de JavaScript en LMS.
- Unidad de objetos en curso de JavaScript en LMS.
- Unidad de funciones en curso de JavaScript en LMS.
- Unidad de DOM en curso de Browser JavaScript en LMS.
- [Array en MDN](https://developer.mozilla.org/es/docs/Web/JavaScript/Referencia/Objetos_globales/Array)
- [Array.sort en MDN](https://developer.mozilla.org/es/docs/Web/JavaScript/Referencia/Objetos_globales/Array/sort)
- [Array.map en MDN](https://developer.mozilla.org/es/docs/Web/JavaScript/Referencia/Objetos_globales/Array/map)
- [Array.filter en MDN](https://developer.mozilla.org/es/docs/Web/JavaScript/Referencia/Objetos_globales/Array/filter)
- [Array.reduce en MDN](https://developer.mozilla.org/es/docs/Web/JavaScript/Referencia/Objetos_globales/Array/reduce)
- [Array.forEach en MDN](https://developer.mozilla.org/es/docs/Web/JavaScript/Referencia/Objetos_globales/Array/forEach)
- [Object.keys en MDN](https://developer.mozilla.org/es/docs/Web/JavaScript/Referencia/Objetos_globales/Object/keys)
- [Object.entries en MDN](https://developer.mozilla.org/es/docs/Web/JavaScript/Referencia/Objetos_globales/Object/entries)
- [Fetch API en MDN](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)
- [json.org](https://json.org/json-es.html)

### Herramientas

- [Git](https://git-scm.com/)
- [GitHub](https://github.com/)
- [GitHub Pages](https://pages.github.com/)
- [Node.js](https://nodejs.org/)
- [Jest](https://jestjs.io/)

---

## Checklist

- [ ] Usa VanillaJS.
- [ ] No hace uso de `this`.
- [ ] Pasa linter (`npm pretest`)
- [ ] Pasa tests (`npm test`)
- [ ] Pruebas unitarias cubren un mínimo del 70% de statements, functions y
      lines y branches.
- [ ] Incluye _Definición del producto_ clara e informativa en `README.md`.
- [ ] Incluye historias de usuario en `README.md`.
- [ ] Incluye _sketch_ de la solución (prototipo de baja fidelidad) en
      `README.md`.
- [ ] Incluye _Diseño de la Interfaz de Usuario_ (prototipo de alta fidelidad)
      en `README.md`.
- [ ] Incluye el listado de problemas que detectaste a través de tests de
      usabilidad en el `README.md`.
- [ ] UI: Muestra lista y/o tabla con datos y/o indicadores.
- [ ] UI: Permite ordenar data por uno o más campos (asc y desc).
- [ ] UI: Permite filtrar data en base a una condición.

## Checklist (Hacker Edition)

- [ ] Consume data de forma dinámica (`fetch()`).
- [ ] Utiliza Librerías de graficas (`chart.js` ó `google chart`).
- [ ] Cobertura de coverage al 100%.
