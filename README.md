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
    return ChangeNotifierProvider(
      create: (context) => MyAppState(),
      child: MaterialApp(
        title: 'RandomApp',
        theme: ThemeData(
          useMaterial3: true,
          colorScheme: ColorScheme.fromSeed(seedColor: Colors.deepOrange),
        ),
        home: MyHomePage(),
      ),
    );
  }
}

class MyAppState extends ChangeNotifier {
  var current = WordPair.random();
}

class MyHomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    var appState = context.watch<MyAppState>();
    return Scaffold(
      appBar: AppBar(
        backgroundColor: Theme.of(context).colorScheme.inversePrimary,
        title: const Text("Random App"),
      ), // Final do AppBar
      body: Column(
        children: [
          const Text('Uma ideia aleatória da hora:'),
          Text(appState.current.asLowerCase),
          ElevatedButton(
            onPressed: () {
              print('botão pressionado!');
            },
            child: const Text('Próximo'),
          ),
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
