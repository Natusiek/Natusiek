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
        const ProfileInfoText(title: "Name:", description: "Alan Pypno"),
        const ProfileInfoText(title: "Location:", description: "Poland, Cracow"),
        const ProfileInfoText(title: "Experience:", description: "3 years"),
        const ProfileInfoText(title: "Languages:", description: "Dart, Kotlin"),
        const ProfileInfoText(
            title: "Linkedin:",
            description: "www.linkedin.com/in/alan-pypno-14b795278"),
        const ProfileInfoText(
            title: "Github:",
            description: "www.github.com/Natusiek"),
      ]),
    );
  }

}

class ProfileInfoText extends StatelessWidget {
  final String title;
  final String description;

  const ProfileInfoText({
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
