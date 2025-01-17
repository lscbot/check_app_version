# Check App Version

A plugin that allows you to check the **version** of the app installed with a hypothetical version of the app published on the PlayStore / AppStore.

## About

The plugin compares two version codes:
- The code for the app **installed** on the device.
- Code for a new version of the app compiled using **JSON**.

In fact the package acquires the necessary information for the comparison between the two versions, 
through a JSON file compiled by the user himself.

Example of a JSON file at this [link](https://github.com/enzo-desimone/check_app_version/blob/master/example/example.json).

| Key           |       Value |
| ------------- | ------------- |
| app_name  | the name of the app  |
| new_app_version  | the new app version  |
| new_app_code  | the new app code  |
| app_package  | android app package name  |
| bundle_id_ios  | ios bundle identify  |
| ios_app_id  | iOS app id number  |

## Install


### Import the Check App Version package
To use the Check App Version package, follow the [plugin installation instructions](https://pub.dev/packages/check_app_version/install).

### Use the package

Add the following import to your Dart code:
```dart
import 'package:check_app_version/show_dialog.dart';
```

We now have the option to use the method **ShowDialog(jsonUrl: 'my url').checkVersion();** 
to check the version and show a message dialog, remember to replace **'my link'** with the link that 
refers to our previously created and customized JSON file

```dart
    ShowDialog(
        context: context,
        jsonUrl: 'https://besimsoft.com/example.json',
        ).checkVersion();
```

### Customize the message dialog

In the **ShowDialog()** method we have many properties to be able to **customize** massage dialog.


| Property           |       Function |
| ------------- | ------------- |
| **jsonUrl**  | **the JSON Link**  |
| dialogRadius  | the message dialog border radius value  |
| backgroundColor  | the message dialog background color  |
| title  | the dialog message title  |
| titleColor  | the dialog message title color  |
| body  | the dialog message body  |
| bodyColor  | the dialog message body color  |
| barrierDismissible  | if is TRUE you can dismiss the message dialog by tapping the modal barrier  |
| onWillPop  | if is TRUE the message dialog it will disappear using only the action keys (default: TRUE)   |
| updateButtonText  | the update button text  |
| updateButtonTextColor  | the update button text color  |
| updateButtonColor  | the update button text color  |
| updateButtonRadius  | the update button text border radius value  |
| laterButtonText  | the later button text  |
| laterButtonColor  | the later button color  |
| laterButtonEnable  | if is FALSE the later button is not visible (default: FALSE)  |
| cupertinoDialog  | if is TRUE you can use Cupertino Style for iOS and Material Style for Android (default: TRUE)  |

