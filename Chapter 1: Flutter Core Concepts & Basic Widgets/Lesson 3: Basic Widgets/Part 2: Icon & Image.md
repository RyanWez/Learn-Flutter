ကဲ ဒါဆိုရင် အခြေခံ Widget သင်ခန်းစာရဲ့ ဒုတိယပိုင်း (Part 2) ကို ဆက်လိုက်ကြရအောင်။ ဒီနေ့တော့ `Icon` နဲ့ `Image` widget တွေအကြောင်း လေ့လာကြမယ်။

***

## Lesson 3: Basic Widgets (Part 2: Icon & Image)

### 1. `Icon` Widget

`Icon` widget ကတော့ Flutter မှာ ကြိုတင်သတ်မှတ်ထားတဲ့ icon ပုံလေးတွေကို အလွယ်တကူ ဖော်ပြဖို့ သုံးပါတယ်။ `Icons` ဆိုတဲ့ class ထဲမှာ `Icons.home`, `Icons.settings`, `Icons.favorite` စသဖြင့် icon ပေါင်းများစွာ ပါဝင်ပြီးသားပါ။ `color` နဲ့ `size` property တွေသုံးပြီး အရောင်နဲ့ အရွယ်အစားကို ထိန်းချုပ်နိုင်ပါတယ်။

### 2. `Image` Widget

`Image` widget ကတော့ App ထဲမှာ ပုံတွေထည့်ဖို့သုံးပါတယ်။ အဓိကအားဖြင့် ပုံတွေကို ရယူတဲ့နေရာပေါ်မူတည်ပြီး နည်းလမ်းနှစ်မျိုးရှိပါတယ်။

* **`Image.network()`**: Internet ပေါ်က ပုံတစ်ပုံရဲ့ URL ကိုသုံးပြီး တိုက်ရိုက်ဖော်ပြတာပါ။ ဒီနည်းလမ်းက လွယ်ကူပေမယ့် user မှာ အင်တာနက် connection ရှိဖို့တော့ လိုအပ်ပါတယ်။
* **`Image.asset()`**: App ရဲ့ project folder ထဲမှာ ကိုယ်တိုင်ထည့်သွင်းထားတဲ့ ပုံတွေကို ဖော်ပြတာပါ။ ဒီနည်းလမ်းက internet မလိုတဲ့အတွက် ပိုစိတ်ချရပါတယ်။ ဒါပေမယ့် setting နည်းနည်းလုပ်ပေးဖို့ လိုပါတယ်။

### `Image.asset` အတွက် ပြင်ဆင်ခြင်း (Setup)

Project ထဲက ပုံကိုသုံးဖို့ အဆင့် (၃) ဆင့် လုပ်ရပါမယ်။ ဒါက အရမ်းအရေးကြီးတဲ့အတွက် သေချာလိုက်လုပ်ဖို့လိုတယ်နော် Ryan။

1.  **`assets` Folder တည်ဆောက်ပါ**: Flutter project ရဲ့ အပေါ်ဆုံးအလွှာ (root directory) မှာ `assets` ဆိုတဲ့ folder တစ်ခု တည်ဆောက်ပါ။
2.  **ပုံထည့်ပါ**: အဲ့ဒီ `assets` folder ထဲကို ကိုယ်သုံးချင်တဲ့ ပုံကို ထည့်ပါ။ ဥပမာ `my_image.png` ဆိုပါစို့။
3.  **`pubspec.yaml` မှာ ကြေညာပါ**: project ရဲ့ `pubspec.yaml` file ကိုဖွင့်ပြီး `flutter:` ဆိုတဲ့ section အောက်မှာ အောက်ကအတိုင်း ကိုယ့်ရဲ့ assets folder ကို ထည့်ပြီး ကြေညာပေးရပါမယ်။ **(အရေးကြီး: `assets:` ဆိုတဲ့စာသားက `uses-material-design` နဲ့ တစ်တန်းတည်းဖြစ်နေရပါမယ်။ YAML file မှာ space တွေရဲ့ အထားအသိုက အရမ်းအရေးကြီးပါတယ်။)**

    ```yaml
    flutter:
      uses-material-design: true
    
      # To add assets to your application, add an assets section, like this:
      assets:
        - assets/
    ```

### အလုပ်လုပ်ပုံ နမူနာ Code

အောက်က code မှာ `Icon`, `Image.network`, `Image.asset` တို့ကို `Column` ဆိုတဲ့ widget အသစ်တစ်ခုနဲ့ တွဲသုံးပြထားပါတယ်။ `Column` က သူ့ရဲ့ `children` (ကလေး widget) တွေကို အပေါ်အောက် တန်းစီပေးပါတယ်။

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: const Text("Lesson 3: Icon & Image"),
        ),
        body: Center(
          // Column widget က widget တွေကို အပေါ်အောက်တန်းစီပေးတယ်
          child: Column(
            // mainAxisAlignment ကိုသုံးပြီး Column ရဲ့ ကလေးတွေကို နေရာချနိုင်တယ်
            mainAxisAlignment: MainAxisAlignment.center,
            children: <Widget>[
              
              // 1. Icon Widget
              const Icon(
                Icons.favorite, // ပြသမည့် Icon
                color: Colors.red,  // Icon အရောင်
                size: 50.0,         // Icon အရွယ်အစား
              ),

              // 2. Image.network Widget
              Image.network(
                // Internet ပေါ်က ပုံတစ်ပုံရဲ့ URL
                'https://flutter.github.io/assets-for-api-docs/assets/widgets/owl.jpg',
                width: 150, // ပုံ၏ အကျယ်
              ),

              // 3. Image.asset Widget
              // ဒီ widget အလုပ်လုပ်ဖို့ pubspec.yaml မှာ assets folder ကို ကြေညာထားဖို့လိုပါတယ်
              Image.asset(
                'assets/my_image.png', // assets folder ထဲက ပုံ၏ လမ်းကြောင်း
                width: 150, // ပုံ၏ အကျယ်
              ),

            ],
          ),
        ),
      ),
    );
  }
}
```

### Code အလုပ်လုပ်ပုံ ရှင်းလင်းချက်

ဒီ code ကို run မယ်ဆိုရင် screen ရဲ့အလယ်မှာ အပေါ်အောက်တန်းစီနေတဲ့ အရာ ၃ ခုကို တွေ့ရပါမယ်။

1.  **`Icon`**: ပထမဆုံးအနေနဲ့ အရောင်အနီရောင်၊ အရွယ်အစား 50 ရှိတဲ့ နှလုံးသားပုံ `favorite` icon လေးကို တွေ့ရပါမယ်။
2.  **`Image.network`**: ဒုတိယတစ်ခုကတော့ ပေးထားတဲ့ URL ကနေ ဇီးကွက်ပုံလေးကို download ဆွဲပြီး ပြပေးပါလိမ့်မယ်။
3.  **`Image.asset`**: တတိယတစ်ခုကတော့ Ryan ကိုယ်တိုင် `assets` folder ထဲမှာထည့်ပြီး `pubspec.yaml` မှာ ကြေညာထားတဲ့ `my_image.png` ဆိုတဲ့ ပုံကို ပြပေးပါလိမ့်မယ်။ (ဒီအဆင့်ကို မလုပ်ရသေးရင် ဒီပုံနေရာမှာ error ပြနေပါလိမ့်မယ်)။

`Column` widget က သူတို့ကို အပေါ်အောက်တန်းစီပေးပြီး `mainAxisAlignment: MainAxisAlignment.center` ကတော့ အဲ့ဒီတန်းစီထားတဲ့ widget တွေကို column ရဲ့ အလယ်တည့်တည့်မှာ နေရာချပေးလိုက်တာပါ။

***

ကဲ အခုဆိုရင် `Icon` နဲ့ `Image` widget တွေကို ဘယ်လိုသုံးရလဲဆိုတာ ရှင်းလောက်ပြီထင်တယ် Ryan။ `Image.network` နဲ့ `Image.asset` ရဲ့ အဓိကကွာခြားချက်က ဘာဖြစ်မလဲ။ App က အင်တာနက်မရှိတဲ့အချိန်မှာတောင် ပုံတစ်ပုံကို မဖြစ်မနေပြပေးချင်ရင် ဘယ် `Image` widget အမျိုးအစားကို သုံးသင့်လဲဟင်။

---
![image](https://github.com/user-attachments/assets/0e1b89ad-de67-4ac5-994c-6ca349d3e10c)
