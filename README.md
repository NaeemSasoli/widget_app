# widget_app
import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        appBar: AppBar(title: const Text("Flutter Widgets Demo")),
        body: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            // Image Widget
            Image.network(
              'https://flutter.dev/assets/homepage/carousel/slide_1-bg-4e2fcef55a3a1b7b5bcf92421279d99050912cbf5d6b7a6a1351e7fbc2e8fc26.jpg',
              height: 200,
            ),

            // Row with Icons and Text
            Padding(
              padding: const EdgeInsets.all(20.0),
              child: Row(
                mainAxisAlignment: MainAxisAlignment.center,
                children: const [
                  Icon(Icons.favorite, color: Colors.red, size: 40),
                  SizedBox(width: 10),
                  Text(
                    "Flutter is awesome!",
                    style: TextStyle(fontSize: 18, fontWeight: FontWeight.bold),
                  ),
                ],
              ),
            ),

            // Elevated Button
            ElevatedButton(
              onPressed: () {
                print("Button Pressed");
              },
              child: const Text("Click Me"),
            ),
          ],
        ),
      ),
    );
  }
}
