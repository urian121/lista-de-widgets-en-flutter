# Widgets en Flutter

### Los widgets de Flutter son los bloques de construcción fundamentales para crear interfaces de usuario interactivas y visualmente atractivas en las aplicaciones. En Flutter, todo es un widget.

### Tipos de Widgets en Flutter
Flutter ofrece una amplia gama de widgets, pero en su núcleo, estos se dividen en dos categorías principales: Stateless y Stateful.

### WIDGETS STATELESS
Los widgets Stateless, como su nombre indica, son aquellos que no almacenan estado. Estos widgets son inmutables, lo que significa que sus propiedades no pueden cambiar durante su ciclo de vida. Se utiliza para mostrar texto en la aplicación y su contenido no cambia a menos que se reconstruya el widget con diferentes datos. 

### WIDGETS STATEFUL
A diferencia de los widgets Stateless, los widgets Stateful mantienen un estado que puede cambiar durante su ciclo de vida. Estos widgets son cruciales para partes de la interfaz de usuario que deben responder a eventos de usuario o cambios de datos. Un widget Stateful consta de dos clases: una para el widget en sí y otra para su estado.

Un ejemplo clásico de un widget Stateful es un formulario con campos de entrada de texto, como TextField, donde el usuario puede introducir datos. Otro ejemplo sería un botón cuyo aspecto cambia cuando se presiona, como cambiar de color o tamaño.

# Widget Scaffold
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

### Widget ListView
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

### Widget Container

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

### Widgets Column y Row
Column y Row son widgets de diseño que permiten crear interfaces flexibles y reactivas. Column organiza los widgets verticalmente, mientras que Row los organiza horizontalmente.
    Column(
        children: <Widget>[
            Text('Primero'),
            Text('Segundo'),
            Text('Tercero'),
        ],
    )
## Column
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
+------------------------------------------+
|              Row (horizontal)            |
|  +-----------+-----------+-----------+  |
|  |   Primero |  Segundo  |  Tercero  |  |
|  +-----------+-----------+-----------+  |
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
|               Stack (superposición)       |
|  +------------------------------------+  |
|  |          Imagen de Fondo           |  |
|  |                                    |  |
|  |  +------------------------------+  |  |
|  |  |          Texto en la         |  |  |
|  |  |        parte superior         |  |  |
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
|       |      Imagen.png        |          |
|       |   (100x100px)          |          |
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


## El widget FlatButton en Flutter es un botón sin elevación que se utiliza comúnmente para acciones simples. Aunque FlatButton ha sido reemplazado por TextButton en versiones más recientes de Flutter, la descripción y el código siguen siendo útiles para entender cómo funcionan los botones en Flutter.

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

## El widget TextField en Flutter se utiliza para recibir texto del usuario. Es un campo de entrada de texto donde los usuarios pueden escribir datos. Puedes personalizar su apariencia y comportamiento según tus necesidades.

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


## El widget RaisedButton en Flutter se usaba para crear botones elevados con sombra, pero ha sido reemplazado por ElevatedButton en versiones más recientes de Flutter. Aquí te presento un ejemplo de RaisedButton y su equivalente moderno, junto con una representación visual.

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

## ElevatedButton es un widget en Flutter que crea un botón elevado con sombra, proporcionando un efecto visual de profundidad. Se utiliza para realizar acciones o desencadenar eventos cuando el usuario interactúa con él. Ideal para botones que necesitan destacarse en la interfaz de usuario.
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
|       +------------------------------+    |
|       |  +------------------------+  |    |
|       |  |    [Presionar]         |  |    |
|       |  | (Botón azul elevado)   |  |    |
|       |  +------------------------+  |    |
|       +------------------------------+    |
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
|       +------------------------------+    |
|       | [Opción 1 v]                 |    |
|       |                              |    |
|       | (Menú desplegable)           |    |
|       +------------------------------+    |
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
|       +------------------------------+    |
|       |     [ ]                      |    |
|       |    (Interruptor)            |    |
|       |     [x]                      |    |
|       +------------------------------+    |
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
|       +------------------------------+    |
|       |  [ ]                         |    |
|       | (Casilla de verificación)    |    |
|       |  [x]                         |    |
|       +------------------------------+    |
|                                          |
+------------------------------------------+

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
|   +-----------------+ +-----------------+|
|   |                    | |              | |
|   |        Rojo        | |       Verde  | |
|   |                    | |              | |
|   +-----------------+ +-----------------+|
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
