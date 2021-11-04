# day14
import 'package:flutter/material.dart';

void main() => runApp(MyApp());

class MyApp extends StatefulWidget {
  @override
  MyAppState createState()=> MyAppState();
}
class MyAppState extends State<MyApp> {
  TextEditingController emailController = TextEditingController();
  TextEditingController nameController = TextEditingController();
  TextEditingController passwordCintroller = TextEditingController();

  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: Text('Text Faild'),),
        body: Padding(
          padding: EdgeInsets.all(20),
          child: Column(
            children: [
              Padding(
                padding: EdgeInsets.all(20),
                child: TextField(
                    controller: emailController,
                    decoration: InputDecoration(
                      border: OutlineInputBorder(),
                      labelText: 'Name',
                      hintText: 'pass',
                    )
                ),
              ),
              Padding(
                padding: EdgeInsets.all(20),
                child: TextField(
                  controller: emailController,
                  decoration: InputDecoration(
                      border: OutlineInputBorder(),
                      labelText: 'password',
                      hintText: 'Enter you password'
                  ),
                ),
              ),
              RaisedButton(
                textColor: Colors.black45,
                color: Colors.lightBlue,
                child: Text('Sing In'),
                onPressed: () {
                  testAlert(context);
                },
              )

            ],
          ),
        ),
      ),
    );
  }
  void testAlert(BuildContext context){
    var alert = AlertDialog(
      title: Text('Alert!!!'),
      content: Text(nameController.text),
    );
    showDialog(context: context, builder: (BuildContext context){
      return alert;
    });
  }

}
