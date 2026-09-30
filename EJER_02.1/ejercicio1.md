1. ¿En qué archivo está el punto de entrada de la aplicación? ¿Qué hace la función createRoot?

El punto de entrada esta en "src/main.jsx". La función createRoot crea la raíz de la aplicación React y permite indicar en qué elemento HTML se va a mostrar la aplicación.


2. ¿Cuál es el ID del elemento HTML donde se monta la aplicación? ¿En qué archivo está definido?

El ID es "root". Está definido en "index.html".


3. Dibuja el árbol de componentes que se renderiza al arrancar el proyecto recién creado.

   StrictMode
   └── App
       └── (fragmento <>, no es componente)
           ├── section#center (hero, h1, p, button)
           ├── div.ticks
           ├── section#next-steps (docs y social)
           ├── div.ticks
           └── section#spacer


4. ¿Qué ocurre en la página si eliminas <StrictMode> de main.jsx? ¿Y en la consola en modo desarrollo?

Sin <StrictMode> se ve exactamente igual. En desarrollo, 


5. Abre App.jsx y localiza tres fragmentos de código JavaScript escritos entre llaves { } dentro del JSX. Explica qué hace cada uno.

"src={heroImg}" inserta el valor de la variable importada en el atributo.

onClick={() => setCount((count) => count + 1)} pasa una función que se ejecuta al hacer clic y suma 1 al estado.

Count is {count} muestra el valor actual del estado dentro del texto del botón.

6. ¿Qué es el elemento <> que envuelve el JSX devuelto por App? ¿Genera algún elemento en el DOM? Compruébalo con las herramientas de desarrollo del navegador (pestaña Elementos).

Es un Fragment, agrupa varios elementos hermanos, porque un componente solo puede devolver un elemento raíz. No genera ningún nodo en el DOM.