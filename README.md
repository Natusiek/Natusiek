```dart
import 'package:flutter/material.dart';

class Profile extends StatelessWidget {

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: Column(mainAxisAlignment: MainAxisAlignment.center, children: [
        ClipOval(
          child: Image.asset("assets/profile/avatar.png"),
        ),
        // NOTE: Basic information
        const ProfileInfo(title: "Name:", description: "Alan Pypno"),
        const ProfileInfo(title: "Location:", description: "Poland, Cracow"),
        const ProfileInfo(title: "Email:", description: "alanpypno@gmail.com"),
        // NOTE: Experience
        const ProfileInfo(title: "Experience:", description: "3 years"),
        const ProfileInfo(title: "Languages:", description: "Dart, Kotlin"),
        // NOTE: Portfolio
        const ProfileInfo(
            title: "Linkedin:",
            description: "www.linkedin.com/in/alan-pypno-14b795278"),
        const ProfileInfo(
            title: "Github:",
            description: "www.github.com/Natusiek"),

        // TODO: Implement the application I'm working on and establish a startup
      ]),
    );
  }

}

class ProfileInfo extends StatelessWidget {
  final String title;
  final String description;

  const ProfileInfo({
    required this.title,
    required this.description,
  });
  
  @override
  Widget build(BuildContext context) {
    return Row(mainAxisSize: MainAxisSize.min, children: [
      Text(
        title,
        style: const TextStyle(fontSize: 14, fontWeight: FontWeight.bold),
      ),
      Padding(
        padding: const EdgeInsets.only(left: 10),
        child: Text(description),
      )
    ]);
  }

}
```
