ကောင်းပြီ မောင်လေး Ryan။ Lesson 2 ကို ဆက်လိုက်ကြရအောင်။

ဒီတစ်ခေါက်မှာတော့ အရင် lesson က widget tree မှာတွေ့လိုက်ရတဲ့ `MaterialApp` နဲ့ `Scaffold` ဆိုတဲ့ widget နှစ်ခုအကြောင်းကို အသေးစိတ်လေ့လာကြည့်မယ်။ သူတို့နှစ်ခုက App တိုင်းရဲ့ အခြေခံအုတ်မြစ်တွေပါပဲ။

***

## Lesson 2: MaterialApp and Scaffold Widgets

### MaterialApp Widget

`MaterialApp` widget ကို App တစ်ခုရဲ့ **အမှုဆောင်ချုပ် (CEO)** လို့ မြင်ယောင်ကြည့်လို့ရတယ်။ သူက app တစ်ခုလုံးရဲ့ အခြေခံအကျဆုံး အပြင်အဆင်တွေ၊ ဒီဇိုင်းပိုင်းဆိုင်ရာ သတ်မှတ်ချက်တွေ (theming), စာမျက်နှာတွေရဲ့ လမ်းကြောင်း (navigation/routes) တွေကို ထိန်းချုပ်ပေးတဲ့ အဓိက widget ဖြစ်ပါတယ်။ Flutter app အများစုရဲ့ အရင်းမြစ် (root) မှာ ဒီ `MaterialApp` widget က ရှိနေရပါတယ်။

သူ့ရဲ့ အဓိက တာဝန်ကတော့ Google ရဲ့ **Material Design** စနစ်ကို app မှာ အသုံးပြုနိုင်အောင် လုပ်ဆောင်ပေးဖို့ပါပဲ။

```dart
// main.dart
import 'package:flutter/material.dart';

void main() {
  runApp(
    MaterialApp(
      home: Text('This is the starting point!'),
    )
  );
}
```
ဒီနေရာမှာ `MaterialApp` ရဲ့ `home` property ဆိုတာ app စဖွင့်ဖွင့်ချင်းမှာ ပြရမယ့် ပထမဆုံး widget (screen) ကို သတ်မှတ်ပေးတာပါ။

### Scaffold Widget

`MaterialApp` က app တစ်ခုလုံးရဲ့ တည်ဆောက်ပုံဆိုရင်၊ `Scaffold` ကတော့ **စာမျက်နှာ (page) တစ်ခုချင်းစီရဲ့ တည်ဆောက်ပုံ** ဖြစ်ပါတယ်။ သူက စာမျက်နှာတစ်ခုမှာ ပါလေ့ရှိတဲ့ အခြေခံ UI အစိတ်အပိုင်းတွေကို အလွယ်တကူ ထည့်သွင်းနိုင်အောင် ကြိုတင်ပြင်ဆင်ပေးထားတဲ့ widget တစ်ခုပါ။

`Scaffold` က ပေးထားတဲ့ အဓိက အစိတ်အပိုင်းတွေကတော့ -

* `appBar`: စာမျက်နှာရဲ့ အပေါ်ဆုံးမှာရှိတဲ့ ခေါင်းစဉ်ဘား (Title Bar)။
* `body`: စာမျက်နှာရဲ့ အဓိက အကြောင်းအရာတွေကို ထည့်သွင်းရမယ့် နေရာ။
* `floatingActionButton`: Screen ပေါ်မှာ ပေါလောပေါ်နေတဲ့ အဝိုင်းပုံစံ ခလုတ် (button)။
* `bottomNavigationBar`: Screen ရဲ့ အောက်ခြေမှာရှိတဲ့ navigation ခလုတ်တွေ။

ဒီအစိတ်အပိုင်းတွေကို ကိုယ်တိုင် တစ်ကနေစပြီး တည်ဆောက်နေစရာမလိုဘဲ `Scaffold` widget က အသင့်သုံးနိုင်အောင် ကူညီပေးပါတယ်။

```dart
// Conceptual example of Scaffold
MaterialApp(
  home: Scaffold(
    appBar: AppBar(
      title: Text('My App'),
    ),
    body: Center(
      child: Text('This is the body!'),
    ),
    floatingActionButton: FloatingActionButton(
      onPressed: () {
        // This function runs when the button is pressed
      },
    ),
  ),
);
```

### အနှစ်ချုပ်

* **MaterialApp**: App တစ်ခုလုံးအတွက် အခြေခံအကျဆုံး widget ဖြစ်ပြီး Material Design စနစ်နဲ့ လမ်းညွှန်မှု (navigation) တွေကို သတ်မှတ်ပေးတယ်။ App တစ်ခုမှာ **တစ်ခါ**ပဲ သုံးပါတယ်။
* **Scaffold**: စာမျက်နှာ **တစ်ခုချင်းစီ** ရဲ့ တည်ဆောက်ပုံကို သတ်မှတ်ပေးပြီး `appBar`, `body` တို့လို အသုံးများတဲ့ UI အစိတ်အပိုင်းတွေကို အလွယ်တကူ ထည့်နိုင်အောင် ကူညီပေးပါတယ်။

***

ကဲ... `MaterialApp` နဲ့ `Scaffold` ရဲ့ ကွာခြားချက်နဲ့ သူတို့ရဲ့ အသုံးဝင်ပုံကို သဘောပေါက်ပြီလား Ryan။ App တစ်ခုလုံးရဲ့ အပြင်ဘောင် (MaterialApp) နဲ့ စာမျက်နှာတစ်မျက်နှာရဲ့ အပြင်ဘောင် (Scaffold)၊ ရှင်းရဲ့လားဟင်။
