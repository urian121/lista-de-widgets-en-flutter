# <img width="48" height="48" src="https://miro.medium.com/v2/resize:fit:720/format:webp/0*Y37daFMFwerE_zUr.jpg" alt="logo flutter"/> Lista de Widgets en Flutter 😲

#### Los Widgets
Son los bloques de construcción fundamentales para crear interfaces de usuario interactivas y visualmente atractivas en las aplicaciones. En Flutter, todo es un widget.

#### Tipos de Widgets en Flutter
Flutter ofrece una amplia gama de widgets, pero en su núcleo, estos se dividen en dos categorías principales: Stateless y Stateful.

#### ¿Qué es Flutter?

Flutter es un framework de código abierto creado por Google para desarrollar aplicaciones multiplataforma con una única base de código. Permite crear interfaces nativas tanto para iOS como Android de manera eficiente y rápida.
Flutter es un framework potente que optimiza el desarrollo de aplicaciones móviles al ofrecer un flujo de trabajo rápido, interfaces de alta calidad y la capacidad de trabajar con múltiples plataformas desde un solo código.

**Principales ventajas de Flutter:**

    **Lenguaje Dart:**
    Flutter utiliza Dart, un lenguaje moderno y eficiente que combina la simplicidad de la sintaxis de C con características orientadas a objetos. Dart puede compilarse tanto en código nativo como en JavaScript, lo que lo hace versátil.

    **Hot Reload:**
    La función de Hot Reload permite ver cambios en el código de manera instantánea sin recompilar toda la aplicación, lo que acelera el desarrollo, facilita la depuración y mejora las pruebas.

    **Multiplataforma:**
    Con Flutter, puedes crear aplicaciones para iOS y Android con una sola base de código, reduciendo significativamente el tiempo y esfuerzo de desarrollo.

    **Interfaz de Usuario Personalizable:**
    Flutter permite modificar cada píxel en pantalla gracias al soporte para Material Design de Google y Cupertino de Apple, brindando flexibilidad total para crear interfaces complejas y atractivas.

#### Ventajas en usar flutter

Flutter reduce los costes de desarrollo hasta en un 40% y acelera el tiempo para comercializar con una base de código única para aplicaciones móviles, web y de escritorio.
También reduce los costos de mantenimiento y simplifica las actualizaciones de la plataforma cruzada.
Además, Flutter facilita la expansión a nuevas plataformas y llega a un público más amplio sin esfuerzo adicional.

#### ¿Qué es Dart?

Dart es un lenguaje de programación de código abierto, orientado a objetos y multiplataforma creado por Google para el desarrollo de aplicaciones móviles, web y de escritorio sofisticadas de alto rendimiento. Tiene un gran conjunto de APIs, lo que hace que sea sencillo crear aplicaciones iOS y Android y las extensas bibliotecas permiten a los desarrolladores acceder a la base de datos y otros servicios externos con relativa facilidad. 

#### ListView Separated widget

En Flutter, el widget de ListView Separated se utiliza para mostrar una lista de artículos de desplazamiento, donde cada elemento está separado por un widget de divider especificado. Este widget es particularmente útil cuando desea mostrar una lista con separación visual entre sus elementos, como líneas o separadores personalizados.

ListView Separated es similar al widget regular ListView, pero inserta automáticamente divisores entre sus hijos. Esto lo hace conveniente para mostrar listas de datos con separadores consistentes sin tener que gestionar manualmente el espaciado entre elementos.

#### Widget STATELESS
Los widgets Stateless, como su nombre indica, son aquellos que no almacenan estado. Estos widgets son inmutables, lo que significa que sus propiedades no pueden cambiar durante su ciclo de vida. Se utiliza para mostrar texto en la aplicación y su contenido no cambia a menos que se reconstruya el widget con diferentes datos. 

#### Widget STATEFUL
A diferencia de los widgets Stateless, los widgets Stateful mantienen un estado que puede cambiar durante su ciclo de vida. Estos widgets son cruciales para partes de la interfaz de usuario que deben responder a eventos de usuario o cambios de datos. Un widget Stateful consta de dos clases: una para el widget en sí y otra para su estado.

Un ejemplo clásico de un widget Stateful es un formulario con campos de entrada de texto, como TextField, donde el usuario puede introducir datos. Otro ejemplo sería un botón cuyo aspecto cambia cuando se presiona, como cambiar de color o tamaño.

#### MaterialApp: Utilizado para aplicaciones que siguen las directrices de diseño Material de Google.
#### CupertinoApp: Utilizado para aplicaciones con estilo iOS, siguiendo las directrices de diseño de Cupertino.

#### Diferencias entre `SliverAppBar, SliverList, SliverGrid, GridView y CustomScrollView` en Flutter

**SliverAppBar**
Es una versión especial de AppBar que se comporta como un sliver, es decir, puede expandirse, contraerse o permanecer fija en función del desplazamiento (scroll) de la vista.
Un AppBar que se comporta como una sliver. Puede expandirse, colapsarse y permanecer fija según el scroll.

**SliverList**
Crea una lista desplazable de manera eficiente, organizando los widgets en una única columna, ideal para listas largas con elementos dinámicos.
Crea una lista que se puede desplazar de forma eficiente, con widgets dispuestos en una columna.  

**SliverGrid**
Similar a SliverList, pero organiza los widgets en un formato de cuadrícula (grid), permitiendo distribuir los elementos en filas y columnas dentro de una vista desplazable.
Similar a `SliverList` pero organiza los elementos en un formato de cuadrícula.

**GridView**
Es un widget independiente que organiza elementos en una cuadrícula. Aunque también es desplazable, no está optimizado como los slivers para trabajar en conjunto con otros widgets desplazables.
Un widget que organiza elementos en una cuadrícula y es parte del árbol de scroll.   

**CustomScrollView**
Es un contenedor que permite combinar varios slivers (como SliverList, SliverGrid y SliverAppBar) en una única vista desplazable, ofreciendo control total sobre cómo se manejan las transiciones y el comportamiento de los widgets durante el scroll.
Un widget que permite usar múltiples slivers para crear un efecto de desplazamiento complejo con diferentes tipos de listas, grids y widgets en una sola vista.


### Resumen de uso:
- **SliverAppBar**: Encabezados que se expanden/colapsan.
- **SliverList**: Listas largas dentro de un `CustomScrollView`.
- **SliverGrid**: Cuadrículas dentro de un `CustomScrollView`.
- **GridView**: Cuadrículas sin la necesidad de combinar múltiples slivers.
- **CustomScrollView**: Scroll avanzado con múltiples componentes (listas, grids, app bars).

#### Widget ClipRRect
ClipRRect es un widget en Flutter que permite recortar su hijo con bordes redondeados, utilizando un BorderRadius especificado. Esto es útil para crear interfaces más estéticas al suavizar los bordes de los widgets, como imágenes o contenedores.

Caso de Uso:
Se utiliza comúnmente para mostrar imágenes con esquinas redondeadas, lo que mejora la apariencia visual en aplicaciones. Por ejemplo, al mostrar una lista de fotos, puedes envolver cada Image en un ClipRRect para que las imágenes se vean más atractivas y modernas.

   return ClipRRect(
     borderRadius: BorderRadius.circular(15), // Ajusta el valor del radio
     child: Container(
       width: 350,
       margin: const EdgeInsets.symmetric(horizontal: 5), // Espaciado entre imágenes
       child: Image.asset(
         imgList[index],
         fit: BoxFit.cover, // Ajusta la imagen
       ),
     ),
   );


#### List.generate
Te permite crear una lista con un número determinado de elementos, y cada elemento se crea mediante una función que se llama para cada índice de la lista.

#### Ejemplo 1
    List<String>.generate(1000,(counter) => "Item $counter");

#### Crear una lista de números del 1 al 10
    List<int> numbers = List.generate(10, (index) => index + 1);
    print(numbers); // [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

#### Ejemplo 2: Crear una lista de strings con los días de la semana
    List<String> days = List.generate(7, (index) => ['Lunes', 'Martes', 'Miércoles', 'Jueves', 'Viernes', 'Sábado', 'Domingo'][index]);
    print(days); // [Lunes, Martes, Miércoles, Jueves, Viernes, Sábado, Domingo]

#### Ejemplo 3: Crear una lista de objetos personalizados
    class Persona {
      String nombre;
      int edad;
    
      Persona(this.nombre, this.edad);
    }
    
    List<Persona> personas = List.generate(5, (index) => Persona('Persona $index', index * 10));
    print(personas); // [Persona(nombre: Persona 0, edad: 0), Persona(nombre: Persona 1, edad: 10), ...]
    

#### ¿Qué es TextStyle?
TextStyle es una clase en Flutter que permite personalizar la apariencia del texto, incluyendo propiedades como el tamaño de fuente, el color, el grosor, el estilo (negrita, cursiva), y otros atributos de estilo.

    Text(
      'Hola, mundo!',
      style: TextStyle(
        fontSize: 24,
        fontWeight: FontWeight.bold,
        color: Colors.blue,
      ),
    )

#### ¿Qué es Icons?
Icons es una clase en Flutter que contiene una serie de íconos de Material Design listos para usar. Proporciona acceso a un conjunto de íconos que puedes utilizar en tu aplicación.

    Icon(
      Icons.home, // Icono de inicio.
      color: Colors.blue,
      size: 30,
    )

#### Comando:
- Este comando descarga e instala todas las dependencias especificadas en el archivo pubspec.yaml del proyecto.
      flutter pub get
  
- Este comando compila la aplicación Flutter en un archivo APK para distribución en modo release, optimizado para rendimiento.
    flutter build apk --release

- Este comando elimina los archivos generados automáticamente y las carpetas de caché, ayudando a resolver problemas de compilación y a limpiar el proyecto.
    flutter clean

- Este comando compila y ejecuta la aplicación Flutter en un emulador o dispositivo conectado, iniciando la depuración en modo de desarrollo.
    flutter run

- Este comando añade el paquete 'shared_preferences' a las dependencias del proyecto y lo incluye en el archivo pubspec.yaml.
    flutter pub add nombre-del-paquete
    
#### Widget Scaffold
El **Scaffold** es el armazón de tu aplicación Flutter. Proporciona la estructura básica para la mayoría de las aplicaciones móviles, incluyendo elementos como barras de navegación, cajones de navegación (drawers) y barras de estado. Esencialmente, es el lienzo en el que pintas tu interfaz de usuario.
    
    @override
    Widget build(BuildContext context) {
        return Scaffold(
            appBar: AppBar(
            title: Text('Ejemplo Scaffold'),
            ),

            body: Center(
            child: Text('Contenido Principal'),
            ),
        );
    }

    +------------------------------------------+
    |        AppBar (barra de aplicación)      |
    |  +------------------------------------+  |
    |  |           Ejemplo Scaffold         |  |
    |  +------------------------------------+  |
    |                                          |
    |              Contenido Principal         |
    |              (Texto centrado)            |
    |                                          |
    |                                          |
    |                                          |
    +------------------------------------------+

## Propiedades del widget Scaffold

    Scaffold(
      appBar: AppBar( // Barra superior de la app que generalmente contiene el título y acciones.
        title: Text('Mi App'), // El título que se mostrará en el AppBar.
        backgroundColor: Colors.blue, // El color de fondo del AppBar.
      ),
      body: Center( // El contenido principal que se mostrará en la pantalla.
        child: Text('Hola Mundo!'), // Un texto centrado en el cuerpo del Scaffold.
      ),
      floatingActionButton: FloatingActionButton( // Botón flotante generalmente usado para acciones primarias.
        onPressed: () {}, // Función que se ejecutará al presionar el botón.
        child: Icon(Icons.add), // Icono dentro del botón flotante.
      ),
      drawer: Drawer( // Un menú lateral (drawer) que aparece al deslizar o presionar el icono de menú.
        child: ListView(
          children: <Widget>[
            DrawerHeader( // Encabezado del drawer, donde suele ir la info del usuario o app.
              child: Text('Encabezado del Drawer'),
              decoration: BoxDecoration(
                color: Colors.blue, // Color de fondo del encabezado.
              ),
            ),
            ListTile(
              title: Text('Opción 1'), // Elemento del menú con texto.
              onTap: () {}, // Acción al seleccionar el elemento del menú.
            ),
          ],
        ),
      ),
      bottomNavigationBar: BottomNavigationBar( // Barra de navegación en la parte inferior con varias opciones.
        items: [
          BottomNavigationBarItem( // Opción individual de la barra inferior.
            icon: Icon(Icons.home), // Icono de la opción.
            label: 'Inicio', // Texto asociado a la opción.
          ),
          BottomNavigationBarItem(
            icon: Icon(Icons.person),
            label: 'Perfil',
          ),
        ],
        currentIndex: 0, // El índice del elemento seleccionado actualmente.
        onTap: (index) { // Acción que se ejecuta al seleccionar un elemento de la barra.
          print('Seleccionado: $index');
        },
      ),
      backgroundColor: Colors.grey[200], // Color de fondo de todo el Scaffold.
      floatingActionButtonLocation: FloatingActionButtonLocation.centerDocked, // Ubicación del botón flotante.
      persistentFooterButtons: [ // Lista de botones que permanecen visibles en la parte inferior.
        ElevatedButton(
          onPressed: () {}, 
          child: Text('Botón 1'),
        ),
        ElevatedButton(
          onPressed: () {},
          child: Text('Botón 2'),
        ),
      ],
    )




## Widget ListView
**ListView** es el widget diseñado para mostrar una lista de elementos desplazables. Es ideal para situaciones donde necesitas mostrar una lista de datos, como una lista de correos electrónicos o contactos.

    ListView(
        children: <Widget>[
            ListTile(
            leading: Icon(Icons.map),
            title: Text('Mapa'),
            ),
            ListTile(
            leading: Icon(Icons.photo),
            title: Text('Álbum'),
            ),
        ],
    )

    +------------------------------------------+
    |            ListView (lista)              |
    |  +------------------------------------+  |
    |  |  [Icono de mapa]   Mapa            |  |
    |  +------------------------------------+  |
    |  |  [Icono de foto]   Álbum           |  |
    |  +------------------------------------+  |
    |                                          |
    |         (Posibles más elementos)         |
    |                                          |
    +------------------------------------------+

## ListView.builder
Es un widget en Flutter que se utiliza para crear listas de manera eficiente cuando los elementos de la lista son generados dinámicamente o cuando la lista tiene muchos elementos. En lugar de crear todos los widgets de la lista de una vez (lo que podría consumir mucha memoria), ListView.builder solo crea los widgets visibles en la pantalla y genera los otros bajo demanda, lo que mejora el rendimiento.

Propósito de ListView.builder

- Es útil cuando tienes una lista larga o infinita de elementos y quieres cargarlos bajo demanda.
- Acepta un índice que se puede usar para construir cada elemento de la lista dinámicamente.

Sintaxis

  ListView.builder(
    itemCount: <número de elementos>,
    itemBuilder: (BuildContext context, int index) {
      return <widget para cada elemento>;
    },
  );

#### Ejemplo prectico

      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          home: Scaffold(
            appBar: AppBar(
              title: const Text('Ejemplo de ListView.builder'),
            ),
            body: MiLista(),
          ),
        );
      }

    
    class MiLista extends StatelessWidget {
      final List<String> nombres = [
        'Carlos',
        'Ana',
        'Luis',
        'María',
        'Pedro',
        'Sofía',
        'Fernando',
        'Javier',
        'Luisa',
        'Carlos',
        'Alejandro',
        'Sara',
        'Díana',
        'Carmen',
        'Brenda',
        'Lucía',
        'Carolina',
        'Estela',
        'Cristina',
        'Carmen',
      ];
    
      MiLista({super.key});
    
      @override
      Widget build(BuildContext context) {
        return ListView.builder(
          itemCount: nombres.length, // Número de elementos
          itemBuilder: (BuildContext context, int index) {
            return ListTile(
              title: Text(nombres[index]), // Muestra el nombre según el índice
            );
          },
        );
      }
    }

    
## Widget Container
El ***Container** es quizás el widget más versátil en Flutter. Puede usarse para crear un rectángulo visual que puede ser decorado con BoxDecoration, como un borde, un fondo, etc. También se utiliza para agregar márgenes, relleno y restricciones a los elementos de la interfaz de usuario.

    Container(
        margin: EdgeInsets.all(10.0),
        color: Colors.blue,
        width: 48.0,
        height: 48.0,
    )

    +------------------------------------------+
    |                                          |
    |              (Margen 10px)               |
    |     +----------------------------+      |
    |     |                            |      |
    |     |                            |      |
    |     |      +---------------+     |      |
    |     |      |               |     |      |
    |     |      |  Contenedor   |     |      |
    |     |      |   48x48px     |     |      |
    |     |      +---------------+     |      |
    |     |                            |      |
    |     |                            |      |
    |     +----------------------------+      |
    |                                          |
    +------------------------------------------+

## Widgets Column y Row
**Column** y **Row** son widgets de diseño que permiten crear interfaces flexibles y reactivas. Column organiza los widgets verticalmente, mientras que Row los organiza horizontalmente.

    Column(
        children: <Widget>[
            Text('Primero'),
            Text('Segundo'),
            Text('Tercero'),
        ],
    )

## Widget Column
El widget **Column** en Flutter organiza sus hijos en una disposición vertical. Funciona alineando widgets uno debajo del otro, permitiendo personalizar su alineación y distribución a lo largo del eje vertical. Es útil para crear interfaces que requieren componentes apilados verticalmente. Además, admite personalización de espaciamiento, alineación y expansión dentro de su contenedor.


    Column(
    mainAxisAlignment: MainAxisAlignment.center, // Alinea los elementos en el centro verticalmente.
    crossAxisAlignment: CrossAxisAlignment.stretch, // Estira los elementos horizontalmente para que ocupen todo el ancho.
    children: <Widget>[
      Container(
        margin: EdgeInsets.all(8.0), // Añade margen alrededor del contenedor.
        padding: EdgeInsets.all(16.0), // Añade espacio dentro del contenedor.
        color: Colors.blueAccent, // Color de fondo del contenedor.
        child: Text(
          'Primero', 
          style: TextStyle(color: Colors.white), // Color del texto dentro del contenedor.
          textAlign: TextAlign.center, // Centra el texto.
        ),
      ),
      Container(
        margin: EdgeInsets.all(8.0),
        padding: EdgeInsets.all(16.0),
        color: Colors.greenAccent,
        child: Text(
          'Segundo', 
          style: TextStyle(color: Colors.white),
          textAlign: TextAlign.center,
        ),
      ),
      Container(
        margin: EdgeInsets.all(8.0),
        padding: EdgeInsets.all(16.0),
        color: Colors.redAccent,
        child: Text(
          'Tercero', 
          style: TextStyle(color: Colors.white),
          textAlign: TextAlign.center,
        ),
      ),
    ],
    )


    +------------------------------------------+
    |              Column (vertical)           |
    |  +------------------------------------+  |
    |  |            Primero                 |  |
    |  +------------------------------------+  |
    |  |            Segundo                 |  |
    |  +------------------------------------+  |
    |  |            Tercero                 |  |
    |  +------------------------------------+  |
    |                                          |
    +------------------------------------------+


## Row
El widget **Row** es muy similar a Column, excepto que el eje en el que se colocan los widgets hijos ya no es vertical, sino horizontal. Le permite integrar una lista de widgets hijos (children). No se pretende crear un desplazamiento horizontal, sino simplemente distribuir estos hijos en el espacio que se le asigna. 

    +------------------------------------------+
    |              Row (horizontal)            |
    |  +-----------+-----------+-----------+   |
    |  |   Primero |  Segundo  |  Tercero  |   |
    |  +-----------+-----------+-----------+   |
    |                                          |
    +------------------------------------------+

## Cómo funcionan las propiedades "CrossAxisAlignment" y "MainAxisAlignment"?
Antes de sumergirnos en ejemplos específicos de Column y Row, es esencial entender estas dos propiedades, ya que son fundamentales para la alineación y distribución de widgets.

- **MainAxisAlignment:** Alineación del eje principal. Esta propiedad define cómo se alinearán los hijos a lo largo del eje principal del widget. En el caso de Column, el eje principal es vertical, mientras que en Row, es horizontal.
Algunos de los valores que puedes usar incluyen start, end, center, spaceBetween, spaceAround y spaceEvenly.
- **CrossAxisAlignment:** Alineación Del Eje Cruzado. Es una propiedad que define cómo se alinearán los hijos a lo largo del eje transversal, que es perpendicular al eje principal. Para Column, el eje transversal es horizontal, mientras que para Row, es vertical.
Los valores comunes son start, end, center y stretch.


## Diferencia entre ListView vs GridView

**ListView** y **GridView** son dos formas comunes de presentar datos en interfaces de usuario. La principal diferencia radica en cómo organizan y visualizan los elementos.

**listView:**
    **Organización:** Presenta los elementos en una lista vertical, uno debajo del otro, Se organiza en una sola columna.
    **Uso:*** Ideal para listas de elementos que requieren una descripción detallada, Mostrar una lista de mensajes en un chat, como listas de contactos, productos o elementos de una base de datos,
    Una aplicación de correo electrónico podría usar un listView para mostrar una lista de mensajes, con el remitente, asunto y fecha como elementos principales. historial de compras,  o resultados de búsqueda.


**GridView:**
    **Organización:** Organiza los elementos en una cuadrícula, dispuestos en filas y columnas.
    **Uso:** Perfecto para presentar elementos visuales, como galeria de imágenes, productos en una tienda en línea, iconos o miniaturas, donde la apariencia es importante.
    Una aplicación de fotos podría usar un GridView para mostrar una galería de imágenes en miniatura, permitiendo al usuario desplazarse rápidamente por ellas y seleccionar la que desee ver a tamaño completo.

#### Cuándo usar cada uno

    **listView:**
        Cuando la prioridad es mostrar información textual detallada y jerárquica.
        Cuando se necesita una navegación secuencial a través de los elementos.
        Ideal para listas largas donde el desplazamiento vertical es común.
    **GridView:**
        GridView es un widget que muestra una cuadrícula de elementos, organizando los ítems en varias columnas y filas.
        Cuando se quiere destacar elementos visuales y facilitar la comparación rápida entre ellos.
        Mostrar imágenes o fotos en un álbum.
        Disposición de productos en una tienda en línea.
        Se organiza en múltiples columnas.
        Ideal para mostrar contenido visualmente atractivo en un formato de cuadrícula.

#### Resumen de diferencias:

    **Orientación:** ListView es una lista vertical; GridView es una cuadrícula de varias columnas.
    **Uso:** ListView es ideal para listas de texto; GridView es mejor para contenido visual denso.


    ListView(
    children: <Widget>[
        ListTile(title: Text('Elemento 1')),
        ListTile(title: Text('Elemento 2')),
        ListTile(title: Text('Elemento 3')),
    ],
    );


    GridView.count(
    crossAxisCount: 2, // Dos columnas
    children: <Widget>[
        Container(color: Colors.red, height: 100),
        Container(color: Colors.green, height: 100),
        Container(color: Colors.blue, height: 100),
        Container(color: Colors.yellow, height: 100),
    ],
    );

    
## Widget Stack
El widget **Stack** te permite superponer widgets sobre otros. Es útil cuando quieres colocar widgets encima de otro, como un texto sobre una imagen.

    Stack(
        alignment: Alignment.center,
        children: <Widget>[
            CircleAvatar(
            backgroundImage: NetworkImage('URL de la imagen'),
            radius: 100,
            ),
            Text(
            'Nombre',
            style: TextStyle(color: Colors.white),
            ),
        ],
    )

    +------------------------------------------+
    |               Stack (superposición)      |
    |  +------------------------------------+  |
    |  |          Imagen de Fondo           |  |
    |  |                                    |  |
    |  |  +------------------------------+  |  |
    |  |  |          Texto en la         |  |  |
    |  |  |        parte superior        |  |  |
    |  |  +------------------------------+  |  |
    |  |                                    |  |
    |  +------------------------------------+  |
    |                                          |
    +------------------------------------------+


## AppBar
Está creado para hacer que se represente una barra de aplicaciones. Este se trata de un espacio delimitado en el cual se pueden incluir otros muchos widgets. Aunque es muy simple es una barra que es clave para mantener una estructura básica en la aplicación. Estas siguen los principios del Flutter Material widget.

    class MyApp extends StatelessWidget {
      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          home: Scaffold(
            appBar: AppBar(
              title: Text('Ejemplo AppBar'),
              backgroundColor: Colors.blue,
            ),
            body: Center(
              child: Text('Contenido Principal'),
            ),
          ),
        );
      }
    }

    +------------------------------------------+
    |              AppBar (barra de app)       |
    |  +------------------------------------+  |
    |  |       Ejemplo AppBar              |  |
    |  |------------------------------------|  |
    |                                          |
    |           Contenido Principal            |
    |                                          |
    +------------------------------------------+


## Text
El widget **Text** ayuda a mostrar una línea o varias con un estilo determinado. Esto es así en lo que se refiere a tamaño, fuente, color… Es uno de los elementos clave para la creación de aplicaciones.

    class MyApp extends StatelessWidget {
      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          home: Scaffold(
            appBar: AppBar(
              title: Text('Ejemplo Text'),
            ),
            body: Center(
              child: Text(
                'Hola, Flutter!',
                style: TextStyle(
                  fontSize: 24,
                  fontWeight: FontWeight.bold,
                  color: Colors.blue,
                ),
              ),
            ),
          ),
        );
      }
    }

    +------------------------------------------+
    |              AppBar (barra de app)       |
    |  +------------------------------------+  |
    |  |          Ejemplo Text             |   |
    |  +------------------------------------+  |
    |                                          |
    |              Center                      |
    |        +------------------+              |
    |        |  Hola, Flutter!  |              |
    |        | (24pt, bold,      |             |
    |        |  color: blue)     |             |
    |        +------------------+              |
    |                                          |
    +------------------------------------------+


## Align

El widget **Align** en Flutter alinea su widget hijo dentro de su contenedor padre según una posición especificada. Funciona utilizando la propiedad alignment, que acepta valores predefinidos como Alignment.center, Alignment.topLeft, entre otros, o coordenadas personalizadas. Es útil para ajustar la posición de un widget dentro de un espacio más grande, dándole control sobre la ubicación exacta del contenido dentro de su padre.

    Align(
      alignment: Alignment.bottomRight, // Alinea el contenido en la esquina inferior derecha.
      child: Container(
        width: 100,
        height: 100,
        color: Colors.blue, // Contenedor azul de 100x100 píxeles.
        child: Text(
          'Alineado', 
          style: TextStyle(color: Colors.white), // Texto dentro del contenedor.
          textAlign: TextAlign.center, // Centra el texto dentro del contenedor.
        ),
      ),
    )


## Image
Si hablamos de los widgets básicos de Flutter no podemos dejar de lado la clase Image, que es la que hace posible que podamos mostrar una imagen. Principalmente, admite los siguientes formatos de imagen: JPEG, PNG, GIF, GIF animado, WebP, WebP animado, BMP y WBMP.

      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          home: Scaffold(
            appBar: AppBar(
              title: Text('Ejemplo Image'),
            ),
            body: Center(
              child: Image.asset(
                'assets/imagen.png',
                width: 100.0,
                height: 100.0,
              ),
            ),
          ),
        );
      }

    +------------------------------------------+
    |              AppBar (barra de app)       |
    |  +------------------------------------+  |
    |  |         Ejemplo Image              |  |
    |  +------------------------------------+  |
    |                                          |
    |               Center                     |
    |       +-----------------------+          |
    |       |      Imagen.png        |         |
    |       |   (100x100px)          |         |
    |       +-----------------------+          |
    |                                          |
    +------------------------------------------+

## Icon
El widget de tipo **Icon** se encarga de la representación de un icono gráfico. En Flutter se trata de iconos que no son interactivos, por lo que si este es tu deseo tendrás que recurrir a IconButton. Además, se entiende que el icono es cuadrado, por lo que si no lo son pueden no mostrarse de la manera correcta.

    class MyApp extends StatelessWidget {
      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          home: Scaffold(
            appBar: AppBar(
              title: Text('Ejemplo Icon'),
            ),
            body: Center(
              child: Icon(
                Icons.favorite,
                size: 50.0,
                color: Colors.red,
              ),
            ),
          ),
        );
      }
    }

    +------------------------------------------+
    |              AppBar (barra de app)       |
    |  +------------------------------------+  |
    |  |         Ejemplo Icon              |  |
    |  +------------------------------------+  |
    |                                          |
    |               Center                     |
    |       +-----------------------+          |
    |       |    (Corazón rojo)     |          |
    |       |     Icono tamaño 50px |          |
    |       +-----------------------+          |
    |                                          |
    +------------------------------------------+


## Widget FlatButton ahora conocido como TextButton 
Es un botón sin elevación que se utiliza comúnmente para acciones simples. Aunque FlatButton ha sido reemplazado por TextButton en versiones más recientes de Flutter, la descripción y el código siguen siendo útiles para entender cómo funcionan los botones en Flutter.

    class MyApp extends StatelessWidget {
      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          home: Scaffold(
            appBar: AppBar(
              title: Text('Ejemplo FlatButton'),
            ),
            body: Center(
              child: FlatButton(
                onPressed: () {
                  // Acción al presionar el botón
                  print('Botón presionado');
                },
                color: Colors.blue,
                textColor: Colors.white,
                padding: EdgeInsets.symmetric(horizontal: 16.0, vertical: 8.0),
                child: Text('Presionar'),
              ),
            ),
          ),
        );
      }
    }

    +------------------------------------------+
    |              AppBar (barra de app)       |
    |  +------------------------------------+  |
    |  |         Ejemplo FlatButton         |  |
    |  +------------------------------------+  |
    |                                          |
    |               Center                     |
    |       +--------------------------+       |
    |       |     [Presionar]          |       |
    |       |  (Botón azul sin borde)  |       |
    |       +--------------------------+       |
    |                                          |
    +------------------------------------------+

## IconButton 
Es un widget en Flutter que combina un ícono con una acción interactiva. Es útil para crear botones en la interfaz de usuario que responden a los toques o clics del usuario.
IconButton es un widget que muestra un ícono y permite al usuario interactuar con él, generalmente ejecutando una acción cuando se toca o se hace clic en el ícono.

    IconButton(
      icon: Icon(Icons.favorite, color: Colors.red),
      onPressed: () {
        // Acción a realizar cuando se toca el botón.
        print('Ícono de favorito tocado');
      },
    )


## NavigationBar
Es un widget en Flutter que proporciona una barra de navegación en la parte inferior de la pantalla, permitiendo a los usuarios navegar entre diferentes secciones de una aplicación. Es similar al BottomNavigationBar, pero ofrece una apariencia y funcionalidad más moderna.

      NavigationBar(
        destinations: [
          NavigationDestination(
            icon: Icon(Icons.home),
            label: 'Inicio',
          ),
          NavigationDestination(
            icon: Icon(Icons.search),
            label: 'Buscar',
          ),
          NavigationDestination(
            icon: Icon(Icons.notifications),
            label: 'Notificaciones',
          ),
          NavigationDestination(
            icon: Icon(Icons.account_circle),
            label: 'Perfil',
          ),
        ],
        onDestinationSelected: (int index) {
          // Acción a realizar al seleccionar un destino.
        },
      )


## Slider
Es un widget en Flutter que permite a los usuarios seleccionar un valor de un rango continuo moviendo un control deslizante. Es útil para ajustes que requieren un rango de valores, como volúmenes, brillo, o cualquier configuración numérica

    Slider(
      value: _currentValue, // Valor actual del slider.
      min: 0.0, // Valor mínimo.
      max: 100.0, // Valor máximo.
      divisions: 10, // Número de divisiones en el slider.
      label: _currentValue.round().toString(), // Etiqueta que muestra el valor actual.
      onChanged: (double value) {
        setState(() {
          _currentValue = value; // Actualiza el valor del slider.
        });
      },
    )

## SimpleDialog
Es un widget en Flutter que muestra un cuadro de diálogo sencillo con una lista de opciones o un mensaje. Es útil para presentar una selección de opciones o mostrar información sin necesidad de una interacción compleja.

    void _showDialog(BuildContext context) {
      showDialog(
        context: context,
        builder: (BuildContext context) {
          return SimpleDialog(
            title: Text('Selecciona una opción'),
            children: <Widget>[
              SimpleDialogOption(
                onPressed: () {
                  Navigator.pop(context, 'Opción 1');
                },
                child: Text('Opción 1'),
              ),
              SimpleDialogOption(
                onPressed: () {
                  Navigator.pop(context, 'Opción 2');
                },
                child: Text('Opción 2'),
              ),
            ],
          );
        },
      );
    }

## BottomSheet
Es un widget en Flutter que muestra una hoja deslizante desde la parte inferior de la pantalla. Se usa para presentar opciones adicionales, acciones o información de manera que el usuario pueda interactuar sin cambiar de pantalla.

      void _showBottomSheet(BuildContext context) {
        showModalBottomSheet(
          context: context,
          builder: (BuildContext context) {
            return Container(
              padding: EdgeInsets.all(16),
              child: Column(
                mainAxisSize: MainAxisSize.min,
                children: <Widget>[
                  Text('Opciones'),
                  ListTile(
                    leading: Icon(Icons.settings),
                    title: Text('Configuraciones'),
                    onTap: () {
                      Navigator.pop(context);
                      // Acción para configuraciones
                    },
                  ),
                  ListTile(
                    leading: Icon(Icons.info),
                    title: Text('Acerca de'),
                    onTap: () {
                      Navigator.pop(context);
                      // Acción para acerca de
                    },
                  ),
                ],
              ),
            );
          },
        );
      }


## TextField
Se utiliza para recibir texto del usuario. Es un campo de entrada de texto donde los usuarios pueden escribir datos. Puedes personalizar su apariencia y comportamiento según tus necesidades.

    class MyApp extends StatelessWidget {
      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          home: Scaffold(
            appBar: AppBar(
              title: Text('Ejemplo TextField'),
            ),
            body: Center(
              child: Padding(
                padding: const EdgeInsets.all(16.0),
                child: TextField(
                  decoration: InputDecoration(
                    border: OutlineInputBorder(),
                    labelText: 'Ingrese texto',
                  ),
                  onChanged: (text) {
                    print('Texto ingresado: $text');
                  },
                ),
              ),
            ),
          ),
        );
      }
    }

    +------------------------------------------+
    |              AppBar (barra de app)       |
    |  +------------------------------------+  |
    |  |        Ejemplo TextField           |  |
    |  +------------------------------------+  |
    |                                          |
    |               Center                     |
    |       +------------------------------+   |
    |       |  +------------------------+  |   |
    |       |  | Ingrese texto           | |   |
    |       |  +------------------------+  |   |
    |       +------------------------------+   |
    |                                          |
    +------------------------------------------+


## RaisedButton
Se usaba para crear botones elevados con sombra, pero ha sido reemplazado por ElevatedButton en versiones más recientes de Flutter. Aquí te presento un ejemplo de RaisedButton y su equivalente moderno, junto con una representación visual.

    class MyApp extends StatelessWidget {
      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          home: Scaffold(
            appBar: AppBar(
              title: Text('Ejemplo RaisedButton'),
            ),
            body: Center(
              child: RaisedButton(
                onPressed: () {
                  // Acción al presionar el botón
                  print('Botón presionado');
                },
                color: Colors.blue,
                textColor: Colors.white,
                padding: EdgeInsets.symmetric(horizontal: 16.0, vertical: 8.0),
                child: Text('Presionar'),
              ),
            ),
          ),
        );
      }
    }

    +------------------------------------------+
    |              AppBar (barra de app)       |
    |  +------------------------------------+  |
    |  |         Ejemplo RaisedButton       |  |
    |  +------------------------------------+  |
    |                                          |
    |               Center                     |
    |       +------------------------------+   |
    |       |  +------------------------+  |   |
    |       |  |    [Presionar]         |  |   |
    |       |  | (Botón azul elevado)   |  |   |
    |       |  +------------------------+  |   |
    |       +------------------------------+   |
    |                                          |
    +------------------------------------------+

## El FloatingActionButton (FAB) 
Es un widget en Flutter que muestra un botón flotante sobre el contenido de la interfaz de usuario. Generalmente, se usa para acciones primarias en una aplicación, como añadir un nuevo elemento o realizar una acción importante.

    class MyApp extends StatelessWidget {
      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          home: Scaffold(
            appBar: AppBar(
              title: Text('Ejemplo FloatingActionButton'),
            ),
            body: Center(
              child: Text('Presiona el botón flotante'),
            ),
            floatingActionButton: FloatingActionButton(
              onPressed: () {
                // Acción a realizar cuando se presione el botón
                print('Botón flotante presionado');
              },
              child: Icon(Icons.add), // Icono dentro del botón
              backgroundColor: Colors.blue, // Color de fondo del botón
            ),
          ),
        );
      }
    }

    +------------------------------------------+
    |              AppBar (barra de app)       |
    |  +------------------------------------+  |
    |  |      Ejemplo FloatingActionButton  |  |
    |  +------------------------------------+  |
    |                                          |
    |              Center                      |
    |                                          |
    |        +-----------------------+         |
    |        |  Presiona el botón    |         |
    |        |       flotante        |         |
    |        +-----------------------+         |
    |                                          |
    |                 +------ +                |
    |                 |  +   |                 |
    |                 |  +   |                 |
    |                 |  +   |                 |
    |                 +------ +                |
    |                                          |
    +------------------------------------------+


## ElevatedButton
Es un widget en Flutter que crea un botón elevado con sombra, proporcionando un efecto visual de profundidad. Se utiliza para realizar acciones o desencadenar eventos cuando el usuario interactúa con él. Ideal para botones que necesitan destacarse en la interfaz de usuario.

    class MyApp extends StatelessWidget {
      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          home: Scaffold(
            appBar: AppBar(
              title: Text('Ejemplo ElevatedButton'),
            ),
            body: Center(
              child: ElevatedButton(
                onPressed: () {
                  // Acción al presionar el botón
                  print('Botón presionado');
                },
                style: ElevatedButton.styleFrom(
                  primary: Colors.blue, // Color de fondo
                  onPrimary: Colors.white, // Color del texto
                  padding: EdgeInsets.symmetric(horizontal: 16.0, vertical: 8.0),
                ),
                child: Text('Presionar'),
              ),
            ),
          ),
        );
      }
    }

    +------------------------------------------+
    |              AppBar (barra de app)       |
    |  +------------------------------------+  |
    |  |       Ejemplo RaisedButton         |  |
    |  +------------------------------------+  |
    |                                          |
    |               Center                     |
    |       +------------------------------+   |
    |       |  +------------------------+  |   |
    |       |  |    [Presionar]         |  |   |
    |       |  | (Botón azul elevado)   |  |   |
    |       |  +------------------------+  |   |
    |       +------------------------------+   |
    |                                          |
    +------------------------------------------+

## Widget SliverList
Este widget se utiliza para crear una lista de elementos que se pueden desplazar dentro de un CustomScrollView. Funciona bien para listas grandes con rendimiento optimizado.

#### Explicación:

    **CustomScrollView:** Es un contenedor de scroll personalizado que permite combinar diferentes tipos de slivers.
    **SliverAppBar:** Un encabezado que se desplaza junto con la lista.
    **SliverList:** Un widget que muestra una lista de elementos que se generan dinámicamente con SliverChildBuilderDelegate.
    **SliverChildBuilderDelegate:** Se utiliza para construir cada elemento de la lista a medida que se desplaza.

      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          home: Scaffold(
            appBar: AppBar(
              title: Text('Ejemplo de SliverList'),
            ),
            body: CustomScrollView(
              slivers: [
                SliverAppBar(
                  pinned: true,
                  expandedHeight: 200.0,
                  flexibleSpace: FlexibleSpaceBar(
                    title: Text('SliverList Demo'),
                    background: Image.network(
                      'https://placekitten.com/800/400',
                      fit: BoxFit.cover,
                    ),
                  ),
                ),
                SliverList(
                  delegate: SliverChildBuilderDelegate(
                    (BuildContext context, int index) {
                      return Container(
                        padding: EdgeInsets.all(16.0),
                        margin: EdgeInsets.symmetric(vertical: 4.0),
                        color: Colors.blue[100 * (index % 9)],
                        child: Text(
                          'Elemento $index',
                          style: TextStyle(fontSize: 20),
                        ),
                      );
                    },
                    childCount: 20, // Número de elementos en la lista
                  ),
                ),
              ],
            ),
          ),
        );
      }

## Widget SliverAppBar 
El **SliverAppBar*** es un widget en Flutter que crea una barra de aplicaciones expansible y colapsable con el scroll. Sirve para mejorar la interfaz visual en pantallas con mucho contenido desplazable.
Se usa cuando necesitas una barra dinámica que cambie su tamaño o comportamiento al desplazarse. Ideal para apps con contenido largo, como tiendas o galerías.

#### SliverAppBar:
Es un AppBar flexible que puede expandirse y colapsarse mientras el usuario hace scroll. Los atributos importantes son:

    **pinned:** Si es true, la barra de aplicaciones permanece fija en la parte superior cuando se colapsa.
    **expandedHeight:** La altura máxima que tendrá el AppBar cuando esté expandido.
    **FlexibleSpaceBar:** Un widget flexible dentro del AppBar que puede incluir un título y una imagen de fondo.

#### SliverList: Después del SliverAppBar, tenemos una lista que se desplaza, generando 20 elementos dinámicamente.

      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          home: MyHomePage(),
        );
      }

    class MyHomePage extends StatelessWidget {
      @override
      Widget build(BuildContext context) {
        return Scaffold(
          body: CustomScrollView(
            slivers: [
              SliverAppBar(
                pinned: true, // Mantiene el AppBar en la parte superior
                expandedHeight: 200.0, // Altura cuando está expandido
                flexibleSpace: FlexibleSpaceBar(
                  title: Text('SliverAppBar Demo'),
                  background: Image.network(
                    'https://placekitten.com/800/400', // Imagen de fondo
                    fit: BoxFit.cover,
                  ),
                ),
              ),
              SliverList(
                delegate: SliverChildBuilderDelegate(
                  (BuildContext context, int index) {
                    return Container(
                      padding: EdgeInsets.all(16.0),
                      margin: EdgeInsets.symmetric(vertical: 4.0),
                      color: Colors.green[100 * (index % 9)],
                      child: Text(
                        'Elemento $index',
                        style: TextStyle(fontSize: 20),
                      ),
                    );
                  },
                  childCount: 20, // Número de elementos en la lista
                ),
              ),
            ],
          ),
        );
      }
    }


## Card
Es un widget en Flutter que proporciona una interfaz visual de contenedor con bordes redondeados y sombra, ideal para mostrar contenido agrupado, como información de un producto, una tarjeta de perfil, o cualquier otro conjunto de datos relacionado.

      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          home: Scaffold(
            appBar: AppBar(
              title: Text('Ejemplo Card'),
            ),
            body: Center(
              child: Card(
                elevation: 4.0,
                shape: RoundedRectangleBorder(
                  borderRadius: BorderRadius.circular(12.0),
                ),
                child: Padding(
                  padding: const EdgeInsets.all(16.0),
                  child: Column(
                    mainAxisSize: MainAxisSize.min,
                    children: <Widget>[
                      Text(
                        'Título de la Tarjeta',
                        style: TextStyle(fontSize: 20, fontWeight: FontWeight.bold),
                      ),
                      SizedBox(height: 10),
                      Text('Contenido de la tarjeta. Aquí puedes incluir más información.'),
                    ],
                  ),
                ),
              ),
            ),
          ),
        );
      }

    +------------------------------------------+
    |              AppBar (barra de app)       |
    |  +------------------------------------+  |
    |  |         Ejemplo Card              |   |
    |  +------------------------------------+  |
    |                                          |
    |               Center                     |
    |       +------------------------------+   |
    |       |  +------------------------+  |   |
    |       |  | Título de la Tarjeta   |  |   |
    |       |  |                        |  |   |
    |       |  | Contenido de la tarjeta |  |  |
    |       |  | (Texto más información) |  |  |
    |       |  +------------------------+  |   |
    |       +------------------------------+   |
    |                                          |
    +------------------------------------------+

## Propiedades del Card
    Card(
      color: Colors.blue, // Establece el color de fondo de la tarjeta.
      elevation: 8, // Define la sombra debajo de la tarjeta, mayor valor significa más profundidad.
      shape: RoundedRectangleBorder(
        borderRadius: BorderRadius.circular(15.0), // Establece el borde redondeado de la tarjeta con un radio de 15.
      ),
      margin: EdgeInsets.all(16.0), // Define el margen exterior de la tarjeta.
      borderOnForeground: false, // Indica si el borde debe estar en primer plano. Aquí está deshabilitado.
      clipBehavior: Clip.antiAlias, // Suaviza los bordes cuando el contenido se recorta dentro de la tarjeta.
      semanticContainer: true, // Añade etiquetas semánticas para mejorar la accesibilidad.
      shadowColor: Colors.red, // Establece el color de la sombra debajo de la tarjeta.
      shape: RoundedRectangleBorder(
        borderRadius: BorderRadius.circular(30.0), // (Duplicado) Bordes redondeados de 30, aunque esta propiedad está repetida.
      ),
      child: Text('This is a card'), // El contenido de la tarjeta, en este caso un texto simple.
    )
    

## SizedBox
Añade un espacio fijo entre los widgets. Puedes especificar el ancho y la altura del espacio.

    SizedBox(
      width: 20.0, // Ancho del espacio
      height: 20.0, // Altura del espacio
    )

## Widgets para generar espacios
**SizedBox:** Para un espacio fijo en ancho y/o alto
**Spacer:** Para espacio flexible y distribuido en Row o Column.
**Padding:** Para añadir relleno dentro de un widget.
**Margin:** Para añadir margen fuera de un widget, se utiliza dentro de Container.


## Spacer
Es un widget en Flutter que se utiliza dentro de un widget Row, Column, o Flex para crear espacio flexible entre los widgets hijos. A diferencia de Expanded, que expande el hijo para ocupar todo el espacio disponible, Spacer crea un espacio vacío flexible que puede ser utilizado para separar otros widgets de manera proporcional.

    class MyApp extends StatelessWidget {
      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          home: Scaffold(
            appBar: AppBar(
              title: Text('Ejemplo Spacer'),
            ),
            body: Row(
              children: <Widget>[
                Container(
                  color: Colors.red,
                  width: 100,
                  height: 100,
                  child: Center(
                    child: Text('Rojo', style: TextStyle(color: Colors.white)),
                  ),
                ),
                Spacer(),
                Container(
                  color: Colors.green,
                  width: 100,
                  height: 100,
                  child: Center(
                    child: Text('Verde', style: TextStyle(color: Colors.white)),
                  ),
                ),
              ],
            ),
          ),
        );
      }
    }

    +------------------------------------------+
    |              AppBar (barra de app)       |
    |  +------------------------------------+  |
    |  |           Ejemplo Spacer           |  |
    |  +------------------------------------+  |
    |                                          |
    |                Row                       |
    |  +-----------------+ +------------------+|
    |  |                 | |                 | |
    |  |        Rojo     | |       Verde     | |
    |  |                 | |                 | |
    |  +-----------------+ +------------------+|
    |                                          |
    +------------------------------------------+



## DropdownButton
Es un widget en Flutter que muestra un menú desplegable de opciones, permitiendo al usuario seleccionar una de las opciones disponibles. Es útil para casos en los que se necesita ofrecer múltiples opciones en un espacio reducido.

    class MyApp extends StatelessWidget {
      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          home: Scaffold(
            appBar: AppBar(
              title: Text('Ejemplo DropdownButton'),
            ),
            body: Center(
              child: DropdownButton<String>(
                value: 'Opción 1',
                onChanged: (String? newValue) {
                  // Acción al seleccionar una opción
                  print('Opción seleccionada: $newValue');
                },
                items: <String>['Opción 1', 'Opción 2', 'Opción 3']
                    .map<DropdownMenuItem<String>>((String value) {
                  return DropdownMenuItem<String>(
                    value: value,
                    child: Text(value),
                  );
                }).toList(),
              ),
            ),
          ),
        );
      }
    }

    +------------------------------------------+
    |              AppBar (barra de app)       |
    |  +------------------------------------+  |
    |  |       Ejemplo DropdownButton       |  |
    |  +------------------------------------+  |
    |                                          |
    |               Center                     |
    |       +------------------------------+   |
    |       | [Opción 1 v]                 |   |
    |       |                              |   |
    |       | (Menú desplegable)           |   |
    |       +------------------------------+   |
    |                                          |
    +------------------------------------------+

## Switch
Es un widget en Flutter que representa un control de encendido/apagado. Permite al usuario alternar entre dos estados, como activado y desactivado, proporcionando una forma intuitiva de encender o apagar una opción.

    import 'package:flutter/material.dart';

    void main() {
      runApp(MyApp());
    }

    class MyApp extends StatefulWidget {
      @override
      _MyAppState createState() => _MyAppState();
    }

    class _MyAppState extends State<MyApp> {
      bool _isSwitched = false;

      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          home: Scaffold(
            appBar: AppBar(
              title: Text('Ejemplo Switch'),
            ),
            body: Center(
              child: Switch(
                value: _isSwitched,
                onChanged: (bool value) {
                  setState(() {
                    _isSwitched = value;
                  });
                  print('Switch está ${_isSwitched ? "Activado" : "Desactivado"}');
                },
              ),
            ),
          ),
        );
      }
    }


    +------------------------------------------+
    |              AppBar (barra de app)       |
    |  +------------------------------------+  |
    |  |            Ejemplo Switch          |  |
    |  +------------------------------------+  |
    |                                          |
    |               Center                     |
    |       +------------------------------+   |
    |       |     [ ]                      |   |
    |       |    (Interruptor)            |    |
    |       |     [x]                      |   |
    |       +------------------------------+   |
    |                                          |
    +------------------------------------------+

## Checkbox
Es un widget en Flutter que permite al usuario seleccionar o deseleccionar una opción mediante una casilla de verificación. Es útil para opciones que permiten múltiples selecciones o para confirmar decisiones.

    import 'package:flutter/material.dart';
    void main() {
      runApp(MyApp());
    }

    class MyApp extends StatefulWidget {
      @override
      _MyAppState createState() => _MyAppState();
    }

    class _MyAppState extends State<MyApp> {
      bool _isChecked = false;

      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          home: Scaffold(
            appBar: AppBar(
              title: Text('Ejemplo Checkbox'),
            ),
            body: Center(
              child: Checkbox(
                value: _isChecked,
                onChanged: (bool? value) {
                  setState(() {
                    _isChecked = value ?? false;
                  });
                  print('Checkbox está ${_isChecked ? "Marcado" : "Desmarcado"}');
                },
              ),
            ),
          ),
        );
      }
    }

    +------------------------------------------+
    |              AppBar (barra de app)       |
    |  +------------------------------------+  |
    |  |           Ejemplo Checkbox         |  |
    |  +------------------------------------+  |
    |                                          |
    |               Center                     |
    |       +------------------------------+   |
    |       |  [ ]                         |   |
    |       | (Casilla de verificación)    |   |
    |       |  [x]                         |   |
    |       +------------------------------+   |
    |                                          |
    +------------------------------------------+

## Radio Widget

    import 'package:flutter/material.dart';
    
    class RadioExample extends StatefulWidget {
      @override
      _RadioExampleState createState() => _RadioExampleState();
    }
    
    class _RadioExampleState extends State<RadioExample> {
      int _radioValue = 1;
      List<String> _radioValues = ['Option 1', 'Option 2', 'Option 3'];
    
      @override
      Widget build(BuildContext context) {
        return Scaffold(
          appBar: AppBar(
            title: Text('Radio Example'),
          ),
          body: Container(
            child: Column(
              crossAxisAlignment: CrossAxisAlignment.start,
              children: _radioValues
                  .asMap()
                  .entries
                  .map((entry) => RadioListTile(
                        title: Text(entry.value),
                        value: entry.key,
                        groupValue: _radioValue,
                        onChanged: (value) {
                          setState(() {
                            _radioValue = value!;
                          });
                        },
                      ))
                  .toList(),
            ),
          ),
        );
      }
    }


## Padding
Es un widget en Flutter que permite agregar espacio adicional alrededor de un widget hijo. Se utiliza para proporcionar un margen interior, separando el contenido del borde del contenedor, lo que ayuda a mejorar la apariencia y la legibilidad.

    class MyApp extends StatelessWidget {
      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          home: Scaffold(
            appBar: AppBar(
              title: Text('Ejemplo Padding'),
            ),
            body: Center(
              child: Padding(
                padding: const EdgeInsets.all(16.0), // Espacio de 16 píxeles alrededor
                child: Container(
                  color: Colors.blue,
                  child: Text(
                    'Texto con Padding',
                    style: TextStyle(color: Colors.white, fontSize: 20),
                  ),
                ),
              ),
            ),
          ),
        );
      }
    }

    +------------------------------------------+
    |              AppBar (barra de app)       |
    |  +------------------------------------+  |
    |  |         Ejemplo Padding            |  |
    |  +------------------------------------+  |
    |                                          |
    |               Center                     |
    |       +------------------------------+   |
    |       |   +------------------------+   | |
    |       |   |                        |   | |
    |       |   |  Texto con Padding     |   | |
    |       |   |                        |   | |
    |       |   +------------------------+   | |
    |       +------------------------------+   |
    |                                          |
    +------------------------------------------+

## Flexible
Se utiliza para adaptar el tamaño de sus hijos en un contenedor flexible, como una fila (Row) o una columna (Column). Te permite definir cómo debe expandirse o contraerse un hijo en relación con otros hijos dentro de un contenedor flexible.
El primer Flexible tiene un flex de 2, lo que significa que ocupará el doble del espacio disponible en comparación con el segundo Flexible.
El segundo Flexible tiene un flex de 1, así que ocupará la mitad del espacio en comparación con el primer Flexible.

La suma de los flex se usa para dividir el espacio disponible entre los widgets Flexible, ajustándose dinámicamente según el tamaño total disponible en el contenedor.

    class MyApp extends StatelessWidget {
      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          home: Scaffold(
            appBar: AppBar(
              title: Text('Ejemplo de Flexible'),
            ),
            body: Column(
              children: <Widget>[
                Container(
                  color: Colors.red,
                  height: 100,
                  child: Center(
                    child: Text(
                      'No Flexible',
                      style: TextStyle(color: Colors.white),
                    ),
                  ),
                ),
                Flexible(
                  flex: 2,
                  child: Container(
                    color: Colors.green,
                    child: Center(
                      child: Text(
                        'Flexible 2',
                        style: TextStyle(color: Colors.white),
                      ),
                    ),
                  ),
                ),
                Flexible(
                  flex: 1,
                  child: Container(
                    color: Colors.blue,
                    child: Center(
                      child: Text(
                        'Flexible 1',
                        style: TextStyle(color: Colors.white),
                      ),
                    ),
                  ),
                ),
                Container(
                  color: Colors.orange,
                  height: 100,
                  child: Center(
                    child: Text(
                      'No Flexible',
                      style: TextStyle(color: Colors.white),
                    ),
                  ),
                ),
              ],
            ),
          ),
        );
      }
    }


## Expanded
Es un widget en Flutter que se utiliza dentro de un widget Row, Column o Flex para hacer que su hijo ocupe el espacio disponible en el eje principal. Esto es útil para crear interfaces flexibles y adaptativas, donde el tamaño de los widgets hijos se ajusta en función del espacio disponible.

    class MyApp extends StatelessWidget {
      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          home: Scaffold(
            appBar: AppBar(
              title: Text('Ejemplo Expanded'),
            ),
            body: Row(
              children: <Widget>[
                Expanded(
                  child: Container(
                    color: Colors.red,
                    height: 100,
                    child: Center(
                      child: Text('Expandido 1', style: TextStyle(color: Colors.white)),
                    ),
                  ),
                ),
                Expanded(
                  child: Container(
                    color: Colors.green,
                    height: 100,
                    child: Center(
                      child: Text('Expandido 2', style: TextStyle(color: Colors.white)),
                    ),
                  ),
                ),
              ],
            ),
          ),
        );
      }
    }

    +------------------------------------------+
    |              AppBar (barra de app)       |
    |  +------------------------------------+  |
    |  |          Ejemplo Expanded          |  |
    |  +------------------------------------+  |
    |                                          |
    |                Row                       |
    |   +-------------------------+            |
    |   |                         |            |
    |   |      Expandido 1        |            |
    |   |                         |            |
    |   +-------------------------+            |
    |   +-------------------------+            |
    |   |                         |            |
    |   |      Expandido 2        |            |
    |   |                         |            |
    |   +-------------------------+            |
    |                                          |
    +------------------------------------------+


## GridView
Es un widget en Flutter que muestra una cuadrícula de elementos desplazables. Es ideal para presentar una colección de elementos en una disposición de varias columnas y filas, similar a una cuadrícula de imágenes o ítems en una tienda.

    class MyApp extends StatelessWidget {
      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          home: Scaffold(
            appBar: AppBar(
              title: Text('Ejemplo GridView'),
            ),
            body: GridView.count(
              crossAxisCount: 3, // Número de columnas
              children: <Widget>[
                Container(
                  color: Colors.red,
                  child: Center(child: Text('Item 1', style: TextStyle(color: Colors.white))),
                ),
                Container(
                  color: Colors.green,
                  child: Center(child: Text('Item 2', style: TextStyle(color: Colors.white))),
                ),
                Container(
                  color: Colors.blue,
                  child: Center(child: Text('Item 3', style: TextStyle(color: Colors.white))),
                ),
                Container(
                  color: Colors.orange,
                  child: Center(child: Text('Item 4', style: TextStyle(color: Colors.white))),
                ),
                Container(
                  color: Colors.purple,
                  child: Center(child: Text('Item 5', style: TextStyle(color: Colors.white))),
                ),
                Container(
                  color: Colors.cyan,
                  child: Center(child: Text('Item 6', style: TextStyle(color: Colors.white))),
                ),
              ],
            ),
          ),
        );
      }
    }

    +------------------------------------------+
    |              AppBar (barra de app)       |
    |  +------------------------------------+  |
    |  |           Ejemplo GridView         |  |
    |  +------------------------------------+  |
    |                                          |
    |               GridView                   |
    |   +--------+--------+--------+           |
    |   |  Item 1|  Item 2|  Item 3|           |
    |   +--------+--------+--------+           |
    |   |  Item 4|  Item 5|  Item 6|           |
    |   +--------+--------+--------+           |
    |                                          |
    +------------------------------------------+


## Widget GridView.builder
***GridView.builder** es un widget en Flutter que crea una cuadrícula de elementos de manera perezosa, generando solo los elementos visibles en pantalla. Funciona usando un itemBuilder para construir cada celda bajo demanda. Es útil para mostrar colecciones grandes o dinámicas en una cuadrícula eficiente en cuanto a memoria.

**GridView.builder** crea una cuadrícula de elementos que se generan de forma perezosa (solo los visibles son construidos).
SliverGridDelegateWithFixedCrossAxisCount define el diseño de la cuadrícula con un número fijo de columnas (crossAxisCount).
**itemCount** especifica el número total de elementos en la cuadrícula.
**itemBuilder** construye cada elemento de la cuadrícula con un color y texto dinámico.
    
    class MyApp extends StatelessWidget {
      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          home: Scaffold(
            appBar: AppBar(title: Text('GridView.builder Example')),
            body: GridView.builder(
              gridDelegate: SliverGridDelegateWithFixedCrossAxisCount(
                crossAxisCount: 3, // Número de columnas en el grid.
                crossAxisSpacing: 10.0, // Espacio horizontal entre los elementos.
                mainAxisSpacing: 10.0, // Espacio vertical entre los elementos.
              ),
              itemCount: 30, // Número total de elementos en el grid.
              itemBuilder: (context, index) {
                return Container(
                  color: Colors.teal[(index % 9 + 1) * 100], // Color dinámico para cada elemento.
                  child: Center(
                    child: Text(
                      'Item $index',
                      style: TextStyle(color: Colors.white, fontSize: 18),
                    ),
                  ),
                );
              },
            ),
          ),
        );
      }
    }

## Diferencia entre GridView.builder vs ListView.builder

**GridView.builder:** Organiza los elementos en una cuadrícula (grid) con múltiples columnas y filas.
**ListView.builder:** Organiza los elementos en una lista vertical (o horizontal) con una sola columna.

**Uso:**

    Usa GridView.builder cuando necesites una disposición en cuadrícula, como en galerías de imágenes o catálogos de productos.
    Usa ListView.builder para listas verticales o horizontales, como listas de correos electrónicos o elementos de menú.

### Diferencia GridView.builder
    
    class MyApp extends StatelessWidget {
      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          home: Scaffold(
            appBar: AppBar(title: Text('GridView.builder Example')),
            body: GridView.builder(
              gridDelegate: SliverGridDelegateWithFixedCrossAxisCount(
                crossAxisCount: 3,
                crossAxisSpacing: 10.0,
                mainAxisSpacing: 10.0,
              ),
              itemCount: 30,
              itemBuilder: (context, index) {
                return Container(
                  color: Colors.teal[(index % 9 + 1) * 100],
                  child: Center(
                    child: Text(
                      'Grid $index',
                      style: TextStyle(color: Colors.white),
                    ),
                  ),
                );
              },
            ),
          ),
        );
      }
    }

### Diferencia ListView.builder

    class MyApp extends StatelessWidget {
      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          home: Scaffold(
            appBar: AppBar(title: Text('ListView.builder Example')),
            body: ListView.builder(
              itemCount: 30,
              itemBuilder: (context, index) {
                return ListTile(
                  leading: Icon(Icons.star),
                  title: Text('Item $index'),
                  subtitle: Text('Subtitle $index'),
                );
              },
            ),
          ),
        );
      }
    }

## Widget SingleChildScrollView
Ees un widget en Flutter que permite que su único hijo sea desplazable (scrollable) cuando su contenido excede las dimensiones de su contenedor, ya sea horizontal o verticalmente. Es útil cuando el contenido de una vista no cabe en pantalla, pero no es lo suficientemente extenso para usar widgets optimizados como ListView.

Explicación:

    **SingleChildScrollView:** Permite desplazamiento vertical o horizontal para el contenido que no cabe en la pantalla.
    **child:** Aquí se coloca cualquier widget como hijo, en este caso un Column con varios contenedores.
    **List.generate(20, ...):** Genera 20 elementos para mostrar en una columna desplazable.

Este ejemplo muestra una lista vertical de contenedores que se pueden desplazar usando el SingleChildScrollView.

  import 'package:flutter/material.dart';

  void main() {
    runApp(MyApp());
  }

  class MyApp extends StatelessWidget {
    @override
    Widget build(BuildContext context) {
      return MaterialApp(
        home: Scaffold(
          appBar: AppBar(title: Text('SingleChildScrollView Example')),
          body: SingleChildScrollView(
            child: Column(
              children: List.generate(20, (index) {
                return Container(
                  margin: EdgeInsets.all(10),
                  color: Colors.blueAccent,
                  height: 100,
                  child: Center(
                    child: Text(
                      'Item $index',
                      style: TextStyle(color: Colors.white, fontSize: 24),
                    ),
                  ),
                );
              }),
            ),
          ),
        ),
      );
    }
  }


## listView.builder con desplazamiento horizontal 
Explicación:

    **ListView.builder:** Crea una lista con desplazamiento horizontal.
    **scrollDirection:** Axis.horizontal: Define la dirección del scroll como horizontal.
    **itemCount: 10:** Establece 10 elementos en la lista.
    **itemBuilder:** Genera cada elemento, con un Container para cada item, donde se personaliza el contenido (texto en este caso).
Este ejemplo mostrará una lista horizontal con 10 contenedores, cada uno con un texto dentro

  import 'package:flutter/material.dart';

  void main() {
    runApp(MyApp());
  }

  class MyApp extends StatelessWidget {
    @override
    Widget build(BuildContext context) {
      return MaterialApp(
        home: Scaffold(
          appBar: AppBar(title: Text('Horizontal ListView')),
          body: HorizontalListView(),
        ),
      );
    }
  }

  class HorizontalListView extends StatelessWidget {
    @override
    Widget build(BuildContext context) {
      return Padding(
        padding: const EdgeInsets.all(8.0),
        child: Container(
          height: 150, // Altura fija para el ListView horizontal
          child: ListView.builder(
            scrollDirection: Axis.horizontal, // Desplazamiento horizontal
            itemCount: 10, // Número de elementos en la lista
            itemBuilder: (context, index) {
              return Container(
                width: 150, // Ancho fijo para cada elemento
                margin: EdgeInsets.all(8),
                color: Colors.blueAccent,
                child: Center(
                  child: Text(
                    'Item $index',
                    style: TextStyle(color: Colors.white, fontSize: 20),
                  ),
                ),
              );
            },
          ),
        ),
      );
    }
  }

## Una alternativa a ListView.builder para crear una lista horizontal
En Flutter es usar el widget SingleChildScrollView con la dirección de desplazamiento configurada a horizontal y un Row para disponer los elementos.

Explicación:

    **SingleChildScrollView:** Este widget permite desplazamiento, en este caso configurado para ser horizontal con scrollDirection: Axis.horizontal.
    **Row:** Dentro del **SingleChildScrollView** usamos un Row para disponer los elementos en línea horizontal.
    **List.generate:** Crea una lista de contenedores, similar a itemBuilder en ListView.builder, pero dentro del Row.

Esta alternativa es útil cuando no necesitas optimización avanzada para listas largas y quieres algo más sencillo para pocos elementos.

  import 'package:flutter/material.dart';

  void main() {
    runApp(MyApp());
  }

  class MyApp extends StatelessWidget {
    @override
    Widget build(BuildContext context) {
      return MaterialApp(
        home: Scaffold(
          appBar: AppBar(title: Text('Horizontal ScrollView')),
          body: HorizontalScrollView(),
        ),
      );
    }
  }

  class HorizontalScrollView extends StatelessWidget {
    @override
    Widget build(BuildContext context) {
      return SingleChildScrollView(
        scrollDirection: Axis.horizontal, // Desplazamiento horizontal
        child: Row(
          children: List.generate(10, (index) {
            return Container(
              width: 150, // Ancho fijo para cada elemento
              margin: EdgeInsets.all(8),
              color: Colors.greenAccent,
              child: Center(
                child: Text(
                  'Item $index',
                  style: TextStyle(color: Colors.black, fontSize: 20),
                ),
              ),
            );
          }),
        ),
      );
    }
  }



## Divider
Es un widget en Flutter que se utiliza para dividir visualmente el contenido en una lista o en un contenedor.
Generalmente se utiliza para separar elementos de una lista o para crear una línea de separación entre secciones de la interfaz de usuario.

    class MyApp extends StatelessWidget {
      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          home: Scaffold(
            appBar: AppBar(
              title: Text('Ejemplo Divider'),
            ),
            body: Column(
              children: <Widget>[
                ListTile(
                  title: Text('Elemento 1'),
                ),
                Divider(), // Línea de separación
                ListTile(
                  title: Text('Elemento 2'),
                ),
                Divider(), // Línea de separación
                ListTile(
                  title: Text('Elemento 3'),
                ),
              ],
            ),
          ),
        );
      }
    }

    +------------------------------------------+
    |              AppBar (barra de app)       |
    |  +------------------------------------+  |
    |  |           Ejemplo Divider          |  |
    |  +------------------------------------+  |
    |                                          |
    |         +-------------------------+      |
    |         |       Elemento 1        |      |
    |         +-------------------------+      |
    |         +-------------------------+      |
    |         |          Divider        |      |
    |         +-------------------------+      |
    |         +-------------------------+      |
    |         |       Elemento 2        |      |
    |         +-------------------------+      |
    |         +-------------------------+      |
    |         |          Divider        |      |
    |         +-------------------------+      |
    |         +-------------------------+      |
    |         |       Elemento 3        |      |
    |         +-------------------------+      |
    |                                          |
    +------------------------------------------+

## ListTile
**ListTile** es un widget de Flutter para crear filas en listas, con soporte para íconos, texto y acciones. Úsalo dentro de ListView para mostrar elementos de manera uniforme y funcional. Es ideal para menús, configuraciones, o listas de opciones que requieran interacción.

**leading:** Un ícono o widget que aparece al principio del ListTile.
**title:** El texto principal del ListTile.
**subtitle:** Un texto secundario que aparece debajo del title.
**trailing:** Un ícono o widget que aparece al final del ListTile.
**onTap:** Una función que se ejecuta cuando el ListTile es tocado.

```
  import 'package:flutter/material.dart';

  void main() => runApp(const MyApp());

  class MyApp extends StatelessWidget {
    const MyApp({super.key});

    @override
    Widget build(BuildContext context) {
      return MaterialApp(
        home: Scaffold(
          appBar: AppBar(
            title: const Text('Ejemplo de ListTile'),
          ),
          body: ListView(
            children: [
              ListTile(
                leading: Icon(Icons.star, color: Colors.blue),
                title: const Text('Elemento 1'),
                subtitle: const Text('Descripción del elemento 1'),
                trailing: Icon(Icons.arrow_forward),
                onTap: () {
                  // Acción al tocar el ListTile
                  print('Elemento 1 tocado');
                },
              ),
              ListTile(
                leading: Icon(Icons.favorite, color: Colors.red),
                title: const Text('Elemento 2'),
                subtitle: const Text('Descripción del elemento 2'),
                trailing: Icon(Icons.arrow_forward),
                onTap: () {
                  // Acción al tocar el ListTile
                  print('Elemento 2 tocado');
                },
              ),
            ],
          ),
        ),
      );
    }
  }
```

## SafeArea 
Es un widget de Flutter que evita que el contenido se superponga con áreas no visibles de la pantalla, como el notch o las barras de estado. Sirve para asegurar que el contenido se muestre dentro de una zona segura y visible. Úsalo siempre que quieras evitar que el contenido se oculte detrás de elementos del sistema operativo.

      import 'package:flutter/material.dart';
      void main() => runApp(const MyApp());
    
      class MyApp extends StatelessWidget {
        const MyApp({super.key});
    
        @override
        Widget build(BuildContext context) {
          return MaterialApp(
            home: Scaffold(
              appBar: AppBar(
                title: const Text('Ejemplo de SafeArea'),
              ),
              body: SafeArea(
                child: Column(
                  children: [
                    Container(
                      color: Colors.blue,
                      height: 200,
                      child: const Center(child: Text('Contenido Seguro', style: TextStyle(color: Colors.white))),
                    ),
                    Expanded(
                      child: Container(
                        color: Colors.red,
                        child: const Center(child: Text('Más Contenido', style: TextStyle(color: Colors.white))),
                      ),
                    ),
                  ],
                ),
              ),
            ),
          );
        }
      }


## Widget GestureDetector
**GestureDetector** es un widget en Flutter que detecta gestos del usuario, como toques, deslizamientos o pulsaciones largas. Funciona capturando gestos definidos (como onTap, onDoubleTap, etc.) y ejecutando una acción. Es útil para hacer interactivos los widgets, permitiendo responder a eventos táctiles en la interfaz.

    GestureDetector(
      onTap: () { // Función que se ejecuta al tocar el widget.
        print('Contenedor tocado!');
      },
      onDoubleTap: () { // Función que se ejecuta al hacer doble tap.
        print('Doble tap en el contenedor!');
      },
      onLongPress: () { // Función que se ejecuta al mantener presionado.
        print('Presionado por largo tiempo!');
      },
      child: Container(
        width: 200,
        height: 200,
        color: Colors.blue, // Contenedor azul.
        child: Center(
          child: Text(
            'Toca aquí', 
            style: TextStyle(color: Colors.white, fontSize: 18),
          ),
        ),
      ),
    )

## InkResponse 
Es un widget en Flutter que detecta gestos y proporciona una retroalimentación visual, como un efecto de onda (ripple) al ser tocado. Funciona como un detector de gestos, similar a GestureDetector, pero con animaciones visuales integradas. Es útil para crear botones interactivos con efectos táctiles. Además, permite personalizar la respuesta visual al interactuar.
    
    InkResponse(
      onTap: () { // Función que se ejecuta al tocar el widget.
        print('InkResponse tocado!');
      },
      onLongPress: () { // Función que se ejecuta al mantener presionado.
        print('Mantener presionado!');
      },
      radius: 50.0, // Radio del área donde se muestra el efecto ripple.
      child: Container(
        width: 150,
        height: 150,
        color: Colors.blue, // Contenedor azul.
        child: Center(
          child: Text(
            'Toca aquí', 
            style: TextStyle(color: Colors.white, fontSize: 18),
          ),
        ),
      ),
    )


## Navegar entre páginas en Flutte

#### 1. Crear dos pantallas
Primero, define dos pantallas (widgets) entre las que quieras navegar.
FirstPage.dart
    
    import 'package:flutter/material.dart';
    class FirstPage extends StatelessWidget {
      @override
      Widget build(BuildContext context) {
        return Scaffold(
          appBar: AppBar(
            title: Text('Primera Página'),
          ),
          body: Center(
            child: ElevatedButton(
              onPressed: () {
                // Navegar a la segunda página
                Navigator.push(
                  context,
                  MaterialPageRoute(builder: (context) => SecondPage()),
                );
              },
              child: Text('Ir a la Segunda Página'),
            ),
          ),
        );
      }
    }

#### Archivo SecondPage.dart
    
      @override
      Widget build(BuildContext context) {
        return Scaffold(
          appBar: AppBar(
            title: Text('Segunda Página'),
          ),
          body: Center(
            child: ElevatedButton(
              onPressed: () {
                // Volver a la primera página
                Navigator.pop(context);
              },
              child: Text('Volver a la Primera Página'),
            ),
          ),
        );
      }

## Configurar la navegación en tu main.dart
    
    class MyApp extends StatelessWidget {
      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          title: 'Flutter Navigation Example',
          theme: ThemeData(
            primarySwatch: Colors.blue,
          ),
          home: FirstPage(),
        );
      }
    }

### Notas:

    // Paquete de Flutter para construir interfaces de usuario
    import 'package:flutter/material.dart'; 
    
    /**
     * 
     * La función void main() Es el punto de entrada de una aplicación en Dart y Flutter. Es donde el programa comienza a ejecutarse.
     * main es la funcion principal de la app en Flutter que no puede ser sobrescrita por otras clases y ademas no devuelve ningun valor.
     */
    void main() {
      // runApp es la función que se encarga de iniciar la app
      runApp( const MiWidget()); // Punto de entrada de la app, ejecuta el widget principal
    }
    
    /**
     * En Flutter, dentro de main() normalmente se llama a runApp(), que inicia la aplicación y construye la interfaz de usuario.
      Ejemplo básico:
      void main() {
        runApp(MyApp()); // Inicia la app de Flutter
      }
      - main(): Siempre debe estar presente en todo programa de Dart.
      - runApp(): Arranca la aplicación Flutter.
     */
    
    
    /**
     * class MiWidget extends StatefulWidget define una clase que extiende de la clase StatefulWidget.
     * extends StatefulWidget: Significa que la clase MiWidget hereda de la clase StatefulWidget.
     * Esto quiere decir que MiWidget es un widget que puede tener estado y puede cambiar su apariencia o comportamiento durante la ejecución de la app.
     * En resumen, MiWidget es un widget con estado.
     */
    class MiWidget extends StatefulWidget {
      // Constructor de la clase MiWidget
      const MiWidget({super.key});
      /**
       * const MiWidget({super.key});
       * Crea una instancia inmutable del widget. 
       * Pasa la clave (key) al constructor de la clase padre (StatefulWidget), lo que ayuda a Flutter a identificar el widget en el árbol de widgets.
       */
    
    
    /**
     * override indica que la clase MiWidget es una clase heredada de la clase StatefulWidget
     * Es una anotación en Dart que indica que un método en una clase hija está reemplazando un método con el mismo nombre en la clase padre.
     Sirve para asegurar que se está sobreescribiendo correctamente un método y no creando uno nuevo accidentalmente.
     */
      @override
      /*
      * La línea _MiWidgetState createState() => _MiWidgetState(); 
      * Crea una instancia del estado _MiWidgetState asociado con el widget MiWidget. Este estado es el que gestionará el comportamiento y la apariencia del widget mientras está en uso.
      */
      _MiWidgetState createState() => _MiWidgetState(); // Crea el estado para este widget
    }
    
    
    /**
     * class _MiWidgetState extends State<MiWidget> define una clase privada _MiWidgetState que extiende la clase State de Flutter. 
     * Esta clase gestiona el estado del widget MiWidget, permitiendo que el widget se actualice y reconstruya cuando cambian sus datos internos.
     */
    class _MiWidgetState extends State<MiWidget> {
      bool _isExpanded = false; // Variable privada para controlar si está expandido o no
    
    /**
     * Es una funcion privada que alterna el valor de _isExpanded y actualiza la UI
     * void: Indica que la función no devuelve ningún valor.
     * _toggleExpansion: Nombre de la función y que es privada.
     * (): Paréntesis para los parámetros de la función (vacíos en este caso).
     * {}: Cuerpo de la función, donde se define su comportamiento.
     */
      void _toggleExpansion() {
        setState(() {
          _isExpanded =
              !_isExpanded; // Alterna el valor de _isExpanded y actualiza la UI
        });
      }
    
      /**
       * Widget build(BuildContext context) es un método que se llama cada vez que el estado del widget cambia.
       * El método Construye y devuelve la interfaz de usuario del widget utilizando el contexto actual de la aplicación
       */
      Widget build(BuildContext context) {
        return GestureDetector(
          onTap: _toggleExpansion, // Detecta el toque y llama a _toggleExpansion
          child: Text(_isExpanded
              ? 'Contraer'
              : 'Expandir'), // Muestra texto según _isExpanded
        );
      }
    }


#### Definir funciones  y llamarlas
    // Una función que suma dos números y devuelve el resultado
    int sumar(int a, int b) {
      return a + b;
    }
    /**
     * int: Tipo de valor que la función devolverá (en este caso, un entero).
     * sumar: Nombre de la función.
     * (int a, int b): Parámetros de la función, que son dos enteros.
     * { return a + b; }: Cuerpo de la función que realiza la suma y devuelve el resultado.
     */

#### Puedes llamar a esta función en tu código así
    void main() {
      int resultado = sumar(5, 3);
      print(resultado); // Imprime 8
    
      // Llama a la función saludar y muestra su resultado
      String saludo = saludar('Juan');
      print(saludo); // Imprime "Hola, Juan!"
    
      imprimirMensaje('¡Hola, mundo!');
      // Imprime "¡Hola, mundo!" en la consola
    }


####  Función que devuelve una cadena de texto
    /**
     * Una función que recibe un nombre y devuelve un saludo personalizado
     * String: Tipo de valor que la función devolverá (una cadena de texto).
     * saludar: Nombre de la función.
     * (String nombre): Parámetro de la función, que es una cadena de texto.
     * { return 'Hola, $nombre!'; }: Cuerpo de la función que devuelve un saludo personalizado usando interpolación de cadenas.
     */
    String saludar(String nombre) {
      return 'Hola, $nombre!';
    }


#### Función que no devuelve un valor
    /**
     * Una función que imprime un mensaje en la consola
     * void: La función no devuelve ningún valor.
     * imprimirMensaje: Nombre de la función.
     * (String mensaje): Parámetro de la función, que es una cadena de texto.
     * { print(mensaje); }: Cuerpo de la función que imprime el mensaje en la consola.
     */
    void imprimirMensaje(String mensaje) {
      print(mensaje);
    }


