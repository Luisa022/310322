# 31/03/22

 import 'package:flutter/material.dart';

const Color darkBlue = Color.fromARGB(255, 18, 32, 47);

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      theme: ThemeData.dark().copyWith(
        scaffoldBackgroundColor: darkBlue,
      ),
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        body: Center(
          child: MyWidget(),
        ),
      ),
    );
  }
}

class MyWidget extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Column(children: [
      const Text('Cadastro NewUser'),
      const Padding(
        padding: EdgeInsets.all(10.0),
        child: TextField(
          decoration: InputDecoration(
            border: OutlineInputBorder(),
            labelText: 'Nome',
          ),
        ),
      ),
      const Padding(
        padding: EdgeInsets.all(10.0),
        child: TextField(
          decoration: InputDecoration(
            border: OutlineInputBorder(),
            labelText: 'Telefone',
          ),
        ),
      ),
      const Padding(
        padding: EdgeInsets.all(10.0),
        child: TextField(
          decoration: InputDecoration(
            border: OutlineInputBorder(),
            labelText: 'email',
          ),
        ),
      ),
      
      ElevatedButton (
      style: raisedButtonStyle,
        onPressed: () {},
        child: const Text('adicionar á Lista'),
      
      )
    ]);
  }
}

final ButtonStyle raisedButtonStyle = ElevatedButton.styleFrom(
onPrimary: Colors.black87,
  primary: Colors.red[300],
  minimumSize: const Size(88, 36),
  padding: const EdgeInsets.symmetric(horizontal: 300),
  shape: const RoundedRectangleBorder(
  borderRadius: BorderRadius.all(Radius.circular(5)),
  ),
);
