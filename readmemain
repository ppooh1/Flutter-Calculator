import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Calculator',
      debugShowCheckedModeBanner: false,
      home: Calculator(),
    );
  }
}

class Calculator extends StatefulWidget {
  @override
  _CalculatorState createState() {
    return _CalculatorState();
  }
}

class _CalculatorState extends State<Calculator> {
  final TextEditingController firstNumberController = TextEditingController();
  final TextEditingController secondNumberController = TextEditingController();
  String output = '';

  void plusFunction() {
    int firstNumber = int.parse(firstNumberController.text);
    int secondNumber = int.parse(secondNumberController.text);
    int result = firstNumber + secondNumber;
    setState(() {
      output = result.toString();
    });
  }

  void minusFunction() {
    int firstNumber = int.parse(firstNumberController.text);
    int secondNumber = int.parse(secondNumberController.text);
    int result = firstNumber - secondNumber;
    setState(() {
      output = result.toString();
    });
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Calculator'),
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
            TextField(
              controller: firstNumberController,
              decoration: InputDecoration(hintText: 'Enter first number'),
              textAlign: TextAlign.center,
            ),
            TextField(
              controller: secondNumberController,
              decoration: InputDecoration(hintText: 'Enter second number'),
              textAlign: TextAlign.center,
            ),
            SizedBox(height: 16), // Add 16px of vertical space
            Row(
              mainAxisAlignment: MainAxisAlignment.center,
              children: [
                ElevatedButton(
                  onPressed: plusFunction,
                  child: Text('+'),
                ),
                SizedBox(width: 16), // Add 16px of horizontal space
                ElevatedButton(
                  onPressed: minusFunction,
                  child: Text('-'),
                ),
              ],
            ),
            SizedBox(height: 16), // Add 16px of vertical space
            Text(
              'Output: $output',
              style: TextStyle(fontSize: 20),
            ),
          ],
        ),
      ),
    );
  }
}
