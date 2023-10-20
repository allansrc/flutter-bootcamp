# flutter-bootcamp

Código Base inicial:

```
/// Flutter BootCamp 23: GDG João Pessoa

import 'package:english_words/english_words.dart';
import 'package:flutter/material.dart';
import 'package:provider/provider.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
        title: 'RandomApp',
        theme: ThemeData(
          useMaterial3: true,
          colorScheme: ColorScheme.fromSeed(seedColor: Colors.deepOrange),
        ),
        home: MyHomePage(),
    );
  }
}

class MyHomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {

    return Scaffold(
      appBar: AppBar(
        backgroundColor: Theme.of(context).colorScheme.inversePrimary,
        title: const Text("Random App"),
      ), // Final do AppBar
      body: Column(
        children: [
          // Lista de Widgets filhos do Column
          
          const Text('Uma ideia aleatória da hora:'),
          
        ],
      ),// Final do Column
    );// Final do Scaffold
  }
}

```


Add Botão >>>
```
ElevatedButton(
  onPressed: () {
    print('Botão pressionado!');
  },
  child: Text('Próximo'),
),
```
