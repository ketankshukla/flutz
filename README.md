# Flutter Demo Application

This is a simple Flutter demo application that demonstrates the basic structure and functionality of a typical Flutter app. The code consists of the following main components:

1. **Import statement**: This imports the `material.dart` package, which provides a rich set of pre-built widgets, styling, and utilities for building Material Design applications.

   ```dart
   import 'package:flutter/material.dart';
   ```

2. **Main function**: This is the entry point of the application. It initializes and runs the `MyApp` widget.

   ```dart
   void main() {
     runApp(const MyApp());
   }
   ```

3. **MyApp class**: This class extends `StatelessWidget` and represents the root widget of the application. It contains a `build` method that returns a `MaterialApp` widget.

   ```dart
   class MyApp extends StatelessWidget {
     const MyApp({super.key});

     @override
     Widget build(BuildContext context) {
       return MaterialApp(
         title: 'Flutter Demo',
         theme: ThemeData(
           primarySwatch: Colors.blue,
         ),
         home: const MyHomePage(title: 'Flutter Demo Home Page'),
       );
     }
   }
   ```

4. **MyHomePage class**: This class extends `StatefulWidget` and represents the home page of the application. It contains a `title` property and a `createState` method that returns a new instance of `_MyHomePageState`.

   ```dart
   class MyHomePage extends StatefulWidget {
     const MyHomePage({super.key, required this.title});

     final String title;

     @override
     State<MyHomePage> createState() => _MyHomePageState();
   }
   ```

5. **_MyHomePageState class**: This class extends `State<MyHomePage>` and represents the mutable state of the `MyHomePage` widget. It contains a private `_counter` property, a private `_incrementCounter` method, and a `build` method.

   ```dart
   class _MyHomePageState extends State<MyHomePage> {
     int _counter = 0;

     void _incrementCounter() {
       setState(() {
         _counter++;
       });
     }

     @override
     Widget build(BuildContext context) {
       return Scaffold(
         appBar: AppBar(
           title: Text(widget.title),
         ),
         body: Center(
           child: Column(
             mainAxisAlignment: MainAxisAlignment.center,
             children: <Widget>[
               const Text(
                 'You have pushed the button this many times:',
               ),
               Text(
                 '$_counter',
                 style: Theme.of(context).textTheme.headlineMedium,
               ),
             ],
           ),
         ),
         floatingActionButton: FloatingActionButton(
           onPressed: _incrementCounter,
           tooltip: 'Increment',
           child: const Icon(Icons.add),
         ),
       );
     }
   }
   ```

The app displays a simple counter on the screen. The counter is incremented every time the floating action button with a "+" icon is pressed.