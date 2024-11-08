# Enunciados para ejercicios de ejemplo (Android)

## App de lista de la compra o to-do list

Elaborar una app sencilla de una sola pantalla en la que tendremos una disposición de un TextField y un botón para añadir elementos a la lista con el nombre que el usuario introduzca en el TextField. 

La lista debe estar gestionada con un LazyColumn y debe incluirse un paquete data con un datasource con datos de ejemplo que la lista debe almacenar de primeras para poder probar la aplicación.

Hacer varias versiones de la app pasando por los siguientes pasos:

1. Gestionando el estado de forma sencilla, los elementos de la lista tan solo tendrán un nombre.
2. Añadir un botón en cada elemento para que al pulsarlo este se borre. 
3. Añadir un CheckBox a cada elemento para marcar el item como realizado o no realizado. Este estado debe manejarse correctamente.
4. Elevar el estado de la app para manejarlo mediante un ViewModel y su correspondiente StateFlow. 
5. Añadir una barra superior a la app a través de un Scafold, en la barra superior debe aparecer el título de la app y un botón para elminar todos los elementos de la lista marcados como realizados de golpe.

## App de contadores

Elaborar una app sencilla de una sola pantalla en la que manejaremos el estado de uno o varios contadores. 

Debemos elaborar varios ejemplos de la misma app pasando por los siguientes:

1. Una app con un único contador que se muestre en pantalla y al que se le añada 1 cada vez que se pulse un botón. Debe existir también un botón para reiniciar el contador a 0.
2. En esta versión tendremos dos contadores y un contador general, de forma que los dos primeros funcionarán de forma independiente y el general aumentará cada vez que cualquiera de los otros aumente.
3. Modificar la versión anterior añadiendo un TextField que solo admita números enteros positivos por cada contador, para que si el usuario lo desea, se pueda modificar la cantidad que se aumenta con cada pulsación. Esto debe afectar al contador y al contador general.
4. Crear una pantalla principal con botones que mediante navegación te llevan a cada uno de los 3 ejemplos anteriores y configurarlos con una barra superior que incluya una flecha para volver a la pantalla principal.
5. Incluir una nueva versión en la que se eleva el estado de los contadores para manejarlo mediante un ViewModel y su correspondiente StateFlow.

## App de pruebas de navegación

Elaborar una app con 4 pantallas diferentes y gestionar su navegación tal y como hemos visto en ejemplos anteriores de forma que sea posible navegar así:

- Desde la pantalla principal se debe poder ir mediante un botón a la pantalla 2 y la 3.
- Desde la pantalla 2 se debe poder volver a la 1 y moverse a la 3.
- Desde la pantalla 3 se debe poder volver a la 1 o a la 2 dependiendo de cuál se venga. Se debe poder también ir a la 4 de forma simple o pasándole uno o dos parámetros textuales que se visualizarán en ella.
- Desde la pantalla 4 se debe poder volver a la 3 o a la 1 directamente y borrando la pila de pantallas. Además, si se reciben parámetros deben mostrarse, en caso contrario debe mostrarse un mensaje de que no se han recibido. 

## App de calculadora

Elaborar la interfaz y el control del estado para una aplicación sencilla de pantalla única que cuente con una calculadora. 

Se pueden añadir tantas posibles operaciones matemáticas como se quieran. 

- Operaciones básicas: suma, resta, multiplicación, división, división entera, resto de la división entera.

- Otras operaciones: potencia, logaritmo neperiano, logaritmo para base elegida, raíz cuadrada, raíz para cualquier radical.

- Operaciones trigonométricas: seno, coseno, tangente, arcoseno, arcocoseno, arcotangente. 

Y todas las que se os ocurran y queráis implementar.

## App de TicTacToe

Elaborar una app de una sola pantalla en la que se pueda jugar por turnos al tres en raya. Debe controlarse el estado mediante ViewModel y StateFlow. 

Se pueden utilizar elementos clickables para poner las X o las O y se pueden usar iconos o imágenes para mostrarlas, es indiferente. 

Se debe mostrar en cada momento si es el turno del jugador X o de las O. Se debe mostrar al finalizar el juego quién ha ganado o si se ha empatado y dar una opción para volver a jugar. Esto debe hacerse en un cuadro de diálogo.

Este ejemplo puede basarse en [siguiente Codelab](https://developer.android.com/codelabs/basic-android-kotlin-compose-viewmodel-and-state?hl=es-419&continue=https%3A%2F%2Fdeveloper.android.com%2Fcourses%2Fpathways%2Fandroid-basics-compose-unit-4-pathway-1%3Fhl%3Des-419%23codelab-https%3A%2F%2Fdeveloper.android.com%2Fcodelabs%2Fbasic-android-kotlin-compose-viewmodel-and-state#0) cuyo código final está disponible en [este repositorio](https://github.com/resuadam2/basic-android-kotlin-compose-training-unscramble).

## App de Trivial

Basándonos en el mismo ejemplo que el ejercicio anterior:

Este ejemplo puede basarse en [siguiente Codelab](https://developer.android.com/codelabs/basic-android-kotlin-compose-viewmodel-and-state?hl=es-419&continue=https%3A%2F%2Fdeveloper.android.com%2Fcourses%2Fpathways%2Fandroid-basics-compose-unit-4-pathway-1%3Fhl%3Des-419%23codelab-https%3A%2F%2Fdeveloper.android.com%2Fcodelabs%2Fbasic-android-kotlin-compose-viewmodel-and-state#0) cuyo código final está disponible en [este repositorio](https://github.com/resuadam2/basic-android-kotlin-compose-training-unscramble).

Elaborar un pequeño juego de Trivial, las preguntas deben estar contenidas en un datasource en el paquete data, se debe crear un modelo de datos acorde para almacenar cada pregunta. 

La aplicación debe tener una pantalla principal dónde se muestre la puntuación máxima en porcentaje de aciertos (0% por defecto al iniciar) y se deje al usuario elegir la cantidad de pregunas que quiere responder (mínimo de 5 y máximo de 20). 

Una vez elegida la cantidad de preguntas debe comenzar el juego en una pantalla secundaria, a partir de esta pantalla se irán respondiendo preguntas hasta llegar a las establecidas y se calculará el porcentaje de acierto que, si es superior al record se debe actualizar. 

Se pueden elaborar variantes de esta aplicación añadiendo cosas como tiempos límite de respuesta, cambiando a un número de preguntas fijo pero con un máximo de errores permitido o cualquier variante que e os ocurra.

## App genérica de un modelo de datos a elegir

Elaborar una app con navegación y control del estado mediante ViewModels y StateFlow. Se debe elaborar en base a un modelo de datos sencillo elegido por cada uno/a. 

La app debe de contar con una pantalla principal que contenga una barra superior con el título de la app y en su MainContent debe haber una lista de elementos visuales basados en el modelo de datos elegido. 

Cada elemento de la lista debe poder eliminarse. 

Debe crearse una segunda pantalla con un formulario desde el cuál poder añadir nuevos elementos a la lista. 

Debe ser posible también editar los elementos existentes, dependiendo del modelo de datos tendrá más o menos sentido poder editar uno o varios campos del mismo. Se puede reutilizar la pantalla de añadir para editar usando navegación y dependiendo de si esta pantalla recibe o no un /id. 

Deben precargarse datos en la lista desde un datasource contenido en el paquete data del proyecto. 

A este proyecto se le pueden añadir tantas features como se quieran, desde búsqueda de elementos, hasta ordenación en base a diferentes propiedades del modelo de datos elegido u otras como selección de varios elementos para su eliminación o cambios de estado en grupo. 

También se pueden añadir otras pantallas para gestionar datos secundarios o preferencias.

## App generadora de alarmas

Generar una app en la que podamos añadir una alarma o aviso para una fecha y hora determinada, la app debe mostrar en la pantalla cuánto falta para que llegue la alarma. 

Esta app puede ampliarse con niveles de importancia o tematizándola. 

Puede ampliarse también para configurar notificaciones push cuándo suene una alarma o aviso.