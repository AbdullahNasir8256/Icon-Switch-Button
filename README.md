# Icon-Switch-Button


import 'package:flutter/material.dart';

class CounterView extends StatefulWidget {
  const CounterView({super.key});

  @override
  State<CounterView> createState() => _CounterViewState();
}

class _CounterViewState extends State<CounterView> {
  int counter = 0;
  bool isChange = false;

  @override
  Widget build(BuildContext context) {
    return Scaffold(
        backgroundColor: const Color.fromARGB(235, 157, 240, 161),
        appBar: AppBar(
          backgroundColor: const Color.fromARGB(255, 17, 180, 17),
          centerTitle: true,
          title: const Text("---  ICON SWITCH  ---", style: TextStyle(fontSize: 30)),
        ),
                body: Center(
            child: Column(
                crossAxisAlignment: CrossAxisAlignment.center,
                mainAxisAlignment: MainAxisAlignment.center,
                children: [
              Container(
                color: const Color.fromARGB(108, 59, 57, 57),
                height: 200,
              ),
              Text("Numbers"),
              Text("$counter", style: TextStyle(fontSize: 30)),
              IconButton(
                onPressed: () {
                  setState(() {
                    isChange = !isChange;
                  });
                },
                icon: Icon(
                  Icons.favorite,
                  size: 50,
                  color: isChange ? Colors.red : Colors.black,
                ),
              ),
            ]
     )
    )
      );
  }
}
