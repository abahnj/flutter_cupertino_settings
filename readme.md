# flutter_cupertino_settings

![Pub badge](https://img.shields.io/pub/v/flutter_cupertino_settings.svg)  ![](https://img.shields.io/github/license/matthinc/flutter_cupertino_settings.svg)

A Flutter widget to create an iOS settings-table (static TableView).

[Get from Pub](https://pub.dartlang.org/packages/flutter_cupertino_settings#-installing-tab-)

- [x] Basic items (CSHeader, CSWidget, CSControl, CSButton, CSLink)
- [x] Support for icons
- [x] Item selection
- [X] Themes


```dart

import 'package:flutter_cupertino_settings/flutter_cupertino_settings.dart';

CSWidgetStyle brightnessStyle = const CSWidgetStyle(
    icon: const Icon(Icons.brightness_medium, color: Colors.black54)
);

CupertinoSettings(
    items: <Widget>[
        CSHeader('Brightness'),
        CSWidget(CupertinoSlider(value: 0.5), style: brightnessStyle),
        CSControl('Auto brightness', CupertinoSwitch(value: true), style: brightnessStyle,),
        CSHeader('Selection'),
        CSSelection(['Day mode','Night mode'], (index) {print(index);}, currentSelection: 0),
        CSDescription('Using Night mode extends battery life on devices with OLED display'),
        CSHeader(),
        CSControl('Loading...', CupertinoActivityIndicator()),
        CSButton(CSButtonType.DEFAULT, "Licenses", (){ print("It works!"); }),
        CSHeader(),
        CSButton(CSButtonType.DESTRUCTIVE, "Delete all data", (){})
    ]
);
```

![](https://abload.de/img/screenshot2018-05-02a00u3w.png)


![](https://abload.de/img/dark3xk0b.png)
![](https://abload.de/img/lightu5k1a.png)

Dark theme & example by [AppleEducate](https://github.com/appleeducate)
