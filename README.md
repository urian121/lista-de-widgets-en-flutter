# <img width="48" height="48" src="https://miro.medium.com/v2/resize:fit:720/format:webp/0*Y37daFMFwerE_zUr.jpg" alt="logo flutter"/> Lista de Widgets en Flutter 😲

#### Los widgets de Flutter son los bloques de construcción fundamentales para crear interfaces de usuario interactivas y visualmente atractivas en las aplicaciones. En Flutter, todo es un widget.

#### Tipos de Widgets en Flutter
Flutter ofrece una amplia gama de widgets, pero en su núcleo, estos se dividen en dos categorías principales: Stateless y Stateful.

#### Qué es Flutter?

Flutter es un marco de código abierto creado por Google que permite una base de código único para crear interfaces de usuario complejas en múltiples dispositivos, independientemente de si se trata de un sistema operativo Android o iOS. La función Flutter-reload-hot-reload permite a los desarrolladores introducir cambios en tiempo casi real haciéndolo eficiente, y Googles Material Design permite a los desarrolladores modificar todos y cada uno de los píxeles en pantalla usando .widgets para crear diseños de IU consistentes para todas las plataformas durante el desarrollo multiplataforma. Los fans del desarrollo de aplicaciones móviles multiplataforma arrebatan a Flutter por su increíble rendimiento, arquitectura lógica y documentación exhaustiva. 

#### ventajas

Flutter reduce los costes de desarrollo hasta en un 40% y acelera el tiempo para comercializar con una base de código única para aplicaciones móviles, web y de escritorio.
También reduce los costos de mantenimiento y simplifica las actualizaciones de la plataforma cruzada.
Además, Flutter facilita la expansión a nuevas plataformas y llega a un público más amplio sin esfuerzo adicional.


#### Qué es Dart?

Dart es un lenguaje de programación de código abierto, orientado a objetos y multiplataforma creado por Google para el desarrollo de aplicaciones móviles, web y de escritorio sofisticadas de alto rendimiento. Tiene un gran conjunto de APIs, lo que hace que sea sencillo crear aplicaciones iOS y Android y las extensas bibliotecas permiten a los desarrolladores acceder a la base de datos y otros servicios externos con relativa facilidad. Las aplicaciones de Flutter están programadas usando Dart que puede compilarse tanto en AOT como en JIT (ver más abajo) y tiene una sintaxis bien definida, lo que facilita el desarrollo y mantenimiento de código. Todas estas cosas permiten a los desarrolladores crear aplicaciones el doble de rápido que las producidas usando otros marcos de desarrollo multiplataforma.


#### Qué es Flutter?

Flutter es un marco de código abierto, multiplataforma utilizado para el desarrollo de aplicaciones móviles, basado en interfaces nativas de iOS y Android. Fue presentado en 2018 y se exhibió en una de las conferencias de Google para desarrolladores. Las principales razones por las que Flutter se ha vuelto tan popular entre los desarrolladores son:

Lengua de Dar, un lenguaje de programación moderno, conciso y orientado. Dart se basa en el estilo/sintaxis de C, que se puede compilar en JavaScript;
Función de descarga caliente, gracias a ella, el proceso de desarrollo de la aplicación es más rápido porque los programadores tienen la posibilidad de previsualizar cambios en el código sobre la marcha sin tener que recompilar la aplicación. Esto permite la fijación de errores más rápido, pruebas y la verificación de varios elementos de código, interfaces de usuario;

#### ListView Separated widget

En Flutter, el widget de ListView Separated se utiliza para mostrar una lista de artículos de desplazamiento, donde cada elemento está separado por un widget de divider especificado. Este widget es particularmente útil cuando desea mostrar una lista con separación visual entre sus elementos, como líneas o separadores personalizados.

ListView Separated es similar al widget regular ListView, pero inserta automáticamente divisores entre sus hijos. Esto lo hace conveniente para mostrar listas de datos con separadores consistentes sin tener que gestionar manualmente el espaciado entre elementos.



#### WIDGETS STATELESS
Los widgets Stateless, como su nombre indica, son aquellos que no almacenan estado. Estos widgets son inmutables, lo que significa que sus propiedades no pueden cambiar durante su ciclo de vida. Se utiliza para mostrar texto en la aplicación y su contenido no cambia a menos que se reconstruya el widget con diferentes datos. 

#### WIDGETS STATEFUL
A diferencia de los widgets Stateless, los widgets Stateful mantienen un estado que puede cambiar durante su ciclo de vida. Estos widgets son cruciales para partes de la interfaz de usuario que deben responder a eventos de usuario o cambios de datos. Un widget Stateful consta de dos clases: una para el widget en sí y otra para su estado.

Un ejemplo clásico de un widget Stateful es un formulario con campos de entrada de texto, como TextField, donde el usuario puede introducir datos. Otro ejemplo sería un botón cuyo aspecto cambia cuando se presiona, como cambiar de color o tamaño.

#### Widget Scaffold
El Scaffold es el armazón de tu aplicación Flutter. Proporciona la estructura básica para la mayoría de las aplicaciones móviles, incluyendo elementos como barras de navegación, cajones de navegación (drawers) y barras de estado. Esencialmente, es el lienzo en el que pintas tu interfaz de usuario.
    
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

## Widget ListView
ListView es el widget diseñado para mostrar una lista de elementos desplazables. Es ideal para situaciones donde necesitas mostrar una lista de datos, como una lista de correos electrónicos o contactos.

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

## ListView.builder es un widget en Flutter que se utiliza para crear listas de manera eficiente cuando los elementos de la lista son generados dinámicamente o cuando la lista tiene muchos elementos. En lugar de crear todos los widgets de la lista de una vez (lo que podría consumir mucha memoria), ListView.builder solo crea los widgets visibles en la pantalla y genera los otros bajo demanda, lo que mejora el rendimiento.
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
    import 'package:flutter/material.dart';
    
    void main() {
      runApp(const MyApp());
    }
    
    class MyApp extends StatelessWidget {
      const MyApp({super.key});
    
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
El Container es quizás el widget más versátil en Flutter. Puede usarse para crear un rectángulo visual que puede ser decorado con BoxDecoration, como un borde, un fondo, etc. También se utiliza para agregar márgenes, relleno y restricciones a los elementos de la interfaz de usuario.

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
Column y Row son widgets de diseño que permiten crear interfaces flexibles y reactivas. Column organiza los widgets verticalmente, mientras que Row los organiza horizontalmente.

    Column(
        children: <Widget>[
            Text('Primero'),
            Text('Segundo'),
            Text('Tercero'),
        ],
    )

## Widget Column
El widget Column en Flutter organiza sus hijos en una disposición vertical. Funciona alineando widgets uno debajo del otro, permitiendo personalizar su alineación y distribución a lo largo del eje vertical. Es útil para crear interfaces que requieren componentes apilados verticalmente. Además, admite personalización de espaciamiento, alineación y expansión dentro de su contenedor.

```
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
```



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
El widget Row es muy similar a Column, excepto que el eje en el que se colocan los widgets hijos ya no es vertical, sino horizontal. Le permite integrar una lista de widgets hijos (children). No se pretende crear un desplazamiento horizontal, sino simplemente distribuir estos hijos en el espacio que se le asigna. 

    +------------------------------------------+
    |              Row (horizontal)            |
    |  +-----------+-----------+-----------+   |
    |  |   Primero |  Segundo  |  Tercero  |   |
    |  +-----------+-----------+-----------+   |
    |                                          |
    +------------------------------------------+

## Widget Stack
El widget Stack te permite superponer widgets sobre otros. Es útil cuando quieres colocar widgets encima de otro, como un texto sobre una imagen.
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
El widget Text ayuda a mostrar una línea o varias con un estilo determinado. Esto es así en lo que se refiere a tamaño, fuente, color… Es uno de los elementos clave para la creación de aplicaciones.

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

El widget Align en Flutter alinea su widget hijo dentro de su contenedor padre según una posición especificada. Funciona utilizando la propiedad alignment, que acepta valores predefinidos como Alignment.center, Alignment.topLeft, entre otros, o coordenadas personalizadas. Es útil para ajustar la posición de un widget dentro de un espacio más grande, dándole control sobre la ubicación exacta del contenido dentro de su padre.

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

    import 'package:flutter/material.dart';

    void main() {
      runApp(MyApp());
    }

    class MyApp extends StatelessWidget {
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
El widget de tipo Icon se encarga de la representación de un icono gráfico. En Flutter se trata de iconos que no son interactivos, por lo que si este es tu deseo tendrás que recurrir a IconButton. Además, se entiende que el icono es cuadrado, por lo que si no lo son pueden no mostrarse de la manera correcta.

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


## FlatButton
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


## Card
Es un widget en Flutter que proporciona una interfaz visual de contenedor con bordes redondeados y sombra, ideal para mostrar contenido agrupado, como información de un producto, una tarjeta de perfil, o cualquier otro conjunto de datos relacionado.


    class MyApp extends StatelessWidget {
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

## SizedBox
Añade un espacio fijo entre los widgets. Puedes especificar el ancho y la altura del espacio.

    SizedBox(
      width: 20.0, // Ancho del espacio
      height: 20.0, // Altura del espacio
    )

## Widgets para generar espacios
SizedBox: Para un espacio fijo en ancho y/o alto
Spacer: Para espacio flexible y distribuido en Row o Column.
Padding: Para añadir relleno dentro de un widget.
Margin: Para añadir margen fuera de un widget, se utiliza dentro de Container.


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

    import 'package:flutter/material.dart';

    void main() {
      runApp(MyApp());
    }

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


## Divider
Es un widget en Flutter que se utiliza para dividir visualmente el contenido en una lista o en un contenedor. Generalmente se utiliza para separar elementos de una lista o para crear una línea de separación entre secciones de la interfaz de usuario.

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
