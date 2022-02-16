<!-- 
This README describes the package. If you publish this package to pub.dev,
this README's contents appear on the landing page for your package.

For information about how to write a good package README, see the guide for
[writing package pages](https://dart.dev/guides/libraries/writing-package-pages). 

For general information about developing packages, see the Dart guide for
[creating packages](https://dart.dev/guides/libraries/create-library-packages)
and the Flutter guide for
[developing packages and plugins](https://flutter.dev/developing-packages). 
-->

Flutter package for circle group widget

## Features

Make circle group widget shaped hexagon (limited 18 circles)

circle size is optimazed with parent widget size, inputted padding




## Usage

you can make circles up to 20 

```dart
class MyCircleGroup extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: Colors.yellow[50],
      appBar: AppBar(
        title: Text("Circle Group"),
      ),
      body: Container(
        padding: EdgeInsets.all(10),
        child: CircleGroup(
          origin: Offset(0, 0),
          elevation: 10,
          childPadding: 10,
          outPadding: 30,
          centerWidget: CircleAvatar(
            backgroundImage: NetworkImage(
                'https://flutter.github.io/assets-for-api-docs/assets/widgets/owl.jpg'),
          ),
          children: List.generate(
              3, (index) => Icon(Icons.accessibility_new_rounded)),
        ),
      ),
    );
  }
}
```

![Screenshot_1644995053](https://user-images.githubusercontent.com/10630330/154214004-40e31c79-615a-4365-abbc-1a719cc85ee3.png)

```dart
 children: List.generate(
              7, (index) => Icon(Icons.accessibility_new_rounded))
```
![Screenshot_1644995077](https://user-images.githubusercontent.com/10630330/154214091-b9d5aee8-2a5e-478f-ae33-b7a5c86d1de0.png)

## Additional information

**parameters**
```dart
required List<Widget> children,
Widget centerWidget,
double childPadding = 10.0,
double outPadding = 10.0,
Color backgroundColor,
Color childColor,
double elevation = 10.0,
Offset origin = Offset.zero,
```
