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
        const ProfileInfo(title: "Name:", label: "Alan Pypno"),
        const ProfileInfo(title: "Location:", label: "Poland, Cracow"),
        const ProfileInfo(title: "Email:", label: "alanpypno@gmail.com"),
        // NOTE: Experience
        const ProfileInfo(title: "Experience:", label: "3 years"),
        const ProfileInfo(title: "Languages:", label: "Dart, Kotlin"),
        // NOTE: Portfolio
        const ProfileInfo(
            title: "Linkedin:",
            label: "www.linkedin.com/in/alan-pypno-14b795278"),
        const ProfileInfo(
            title: "Github:",
            label: "www.github.com/Natusiek"),

        // TODO: Implement the application I'm working on and establish a startup
      ]),
    );
  }

}

class ProfileInfo extends StatelessWidget {
  final String title;
  final String label;

  const ProfileInfo({
    required this.title,
    required this.label,
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
        child: Text(label),
      )
    ]);
  }

}
```
