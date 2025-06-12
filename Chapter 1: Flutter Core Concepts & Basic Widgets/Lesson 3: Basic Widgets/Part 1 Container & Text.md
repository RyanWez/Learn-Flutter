Lesson 3 ကို စလိုက်ကြရအောင်။ ဒီနေ့တော့ App တစ်ခုရဲ့ UI ကိုတည်ဆောက်တဲ့နေရာမှာ မရှိမဖြစ်လိုအပ်တဲ့ အခြေခံအကျဆုံး widget လေးတွေအကြောင်းကို လေ့လာသွားမှာပါ။

အရင်ဆုံး `Container` နဲ့ `Text` widget နှစ်ခုကိုစပြီး လေ့လာကြည့်ကြမယ်။

***

## Lesson 3: Basic Widgets (Part 1: Container & Text)

### 1. `Container` Widget

`Container` ဆိုတာက နာမည်အတိုင်းပဲ "ထည့်စရာဘူး" တစ်ခုလိုပါပဲ။ သူက ဘာမှမရှိတဲ့ လေးထောင့်ပုံစံနေရာလေးတစ်ခု ဖန်တီးပေးပါတယ်။ အဲ့ဒီနေရာလေးကို ကိုယ်ကြိုက်သလို အရောင် (`color`)၊ အကျယ် (`width`)၊ အမြင့် (`height`) တွေ သတ်မှတ်နိုင်တယ်။ သူ့ရဲ့အတွင်းဘက်မှာ တခြား widget တွေ (child) ကိုလည်း ထည့်လို့ရပါတယ်။ Flutter မှာ အရမ်းအသုံးဝင်ပြီး ဘက်စုံသုံးလို့ရတဲ့ widget တစ်ခုပါ။

### 2. `Text` Widget

`Text` widget ကတော့ အရမ်းရှင်းပါတယ်။ သူ့ရဲ့အဓိကတာဝန်က စာသား (`String`) တွေကို screen ပေါ်မှာ ဖော်ပြပေးဖို့ပါပဲ။ စာသားရဲ့ပုံစံကို ပြင်ချင်တယ်ဆိုရင်တော့ `style` ဆိုတဲ့ property ကိုသုံးပြီး `TextStyle` widget နဲ့ အရောင်၊ စာလုံးအရွယ်အစား (font size) စတာတွေကို ပြောင်းလဲနိုင်ပါတယ်။

### အလုပ်လုပ်ပုံ နမူနာ Code

အောက်မှာ `Container` နဲ့ `Text` widget တွေကို ဘယ်လိုတွဲသုံးလဲဆိုတာ ကြည့်နိုင်ဖို့ ပြည့်စုံတဲ့ code နမူနာကို ပေးထားပါတယ်။ ဒီ code တစ်ခုလုံးကို copy ကူးပြီး ကိုယ့်ရဲ့ `main.dart` file ထဲမှာ ထည့်ပြီး run ကြည့်လိုက်ရုံပါပဲ။

```dart
// 1. Flutter Material Design package ကို import လုပ်ခြင်း
import 'package:flutter/material.dart';

// 2. App ကို စတင်မောင်းနှင်တဲ့ main function
void main() {
  runApp(const MyApp());
}

// 3. App ရဲ့ class Widget
class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    // 4. MaterialApp widget ကို အသုံးပြုခြင်း
    return MaterialApp(
      // 5. Scaffold widget ဖြင့် စာမျက်နှာကို တည်ဆောက်ခြင်း
      home: Scaffold(
        appBar: AppBar(
          title: const Text('Lesson 3: Container & Text'),
        ),
        // 6. စာမျက်နှာရဲ့ body ကို အလယ်မှာထားရန် Center widget ကိုသုံးခြင်း
        body: Center(
          // 7. Container widget ကို ဖန်တီးခြင်း
          child: Container(
            width: 300,  // Container ၏ အကျယ်
            height: 200, // Container ၏ အမြင့်
            color: Colors.lightBlue, // Container ၏ နောက်ခံအရောင်
            // 8. Container ၏ child အဖြစ် Text widget ကိုထည့်သွင်းခြင်း
            child: const Center(
              child: Text(
                'Hello Ryan!', // ပြသမည့် စာသား
                style: TextStyle( // စာသား၏ ပုံစံ
                  color: Colors.white, // စာသား၏ အရောင်
                  fontSize: 24, // စာလုံး အရွယ်အစား
                ),
              ),
            ),
          ),
        ),
      ),
    );
  }
}
```

### Code အလုပ်လုပ်ပုံ ရှင်းလင်းချက်

1.  **`import 'package:flutter/material.dart';`**
    * Flutter ရဲ့ Material Design widget တွေ (MaterialApp, Scaffold, Container, Text စသည်ဖြင့်) ကို သုံးနိုင်အောင် လိုအပ်တဲ့ package ကို import လုပ်တာပါ။ ဒီတစ်ကြောင်းက မပါမဖြစ်ပါ။

2.  **`void main() { ... }`**
    * Dart programming language ရဲ့ ထုံးစံအတိုင်း ဒီ `main` function က app စစချင်းမှာ အရင်ဆုံးအလုပ်လုပ်တဲ့ နေရာပါ။ `runApp(const MyApp());` ဆိုတာက `MyApp` ဆိုတဲ့ widget ကို screen ပေါ်မှာ ပြသခိုင်းလိုက်တာပါ။

3.  **`class MyApp extends StatelessWidget { ... }`**
    * `MyApp` ဆိုပြီး ကိုယ်ပိုင် widget တစ်ခုကို တည်ဆောက်လိုက်တာပါ။ `StatelessWidget` ဆိုတာက အခြေအနေပြောင်းလဲမှုမရှိတဲ့ (static) widget တွေအတွက်သုံးပါတယ်။ လောလောဆယ်တော့ ဒါက app ရဲ့ အဓိကကိုယ်ထည်လို့ မှတ်ထားနိုင်ပါတယ်။

4.  **`MaterialApp`**
    * Lesson 2 မှာ သင်ခဲ့တဲ့အတိုင်း App တစ်ခုလုံးရဲ့ အခြေခံအုတ်မြစ်ပါ။

5.  **`Scaffold`**
    * စာမျက်နှာတစ်မျက်နှာရဲ့ layout ကို တည်ဆောက်ပေးပါတယ်။ ဒီမှာဆိုရင် ခေါင်းစဉ်အတွက် `appBar` နဲ့ အဓိက content အတွက် `body` ကို သုံးထားပါတယ်။

6.  **`Center`**
    * သူ့ရဲ့ `child` widget (ဒီဥပမာမှာတော့ `Container`) ကို screen ရဲ့ အလယ်တည့်တည့်ကို ပို့ပေးပါတယ်။

7.  **`Container`**
    * ဒါက ဒီနေ့သင်ခန်းစာရဲ့ အဓိက Hero ပါ။ ဒီမှာ `width` ကို 300, `height` ကို 200 သတ်မှတ်ပြီး `color` ကို `Colors.lightBlue` (အပြာနုရောင်) ပေးထားပါတယ်။ ဒါကြောင့် screen အလယ်မှာ အပြာနုရောင် လေးထောင့်ဘူးလေးတစ်ခု ပေါ်လာပါလိမ့်မယ်။

8.  **`Text`**
    * အဲ့ဒီအပြာရောင် `Container` ဘူးလေးရဲ့ အတွင်းထဲမှာ စာသားပြဖို့သုံးထားပါတယ်။ စာသားက "Hello Ryan!" ဖြစ်ပြီး `TextStyle` ကိုသုံးပြီး အရောင်ကို အဖြူ (`Colors.white`) နဲ့ စာလုံးအရွယ်အစားကို `24` သတ်မှတ်ထားပါတယ်။ `Text` widget ကို နောက်ထပ် `Center` တစ်ခုနဲ့ ထပ်ပြီးခြုံထားတဲ့အတွက် စာသားက အပြာရောင်ဘူးရဲ့ အလယ်တည့်တည့်မှာ ပေါ်နေပါလိမ့်မယ်။

### သင်ဒီ Code ကို Run ရင် ဘာမြင်ရမလဲ?

App ကို run လိုက်တဲ့အခါ "Lesson 3: Container & Text" လို့ရေးထားတဲ့ ခေါင်းစဉ်ဘား (AppBar) ကို အပေါ်မှာတွေ့ရပါမယ်။ စာမျက်နှာရဲ့ အလယ်တည့်တည့်မှာ အပြာနုရောင် လေးထောင့် `Container` တစ်ခုရှိနေပြီး၊ အဲ့ဒီလေးထောင့်ကွက်ရဲ့ အလယ်မှာ အဖြူရောင်စာလုံးကြီးကြီးနဲ့ "Hello Ryan!" ဆိုပြီး မြင်တွေ့ရမှာ ဖြစ်ပါတယ်။

***

ကဲ... `Container` က ဘူးတစ်လုံးလို အလုပ်လုပ်ပုံနဲ့ `Text` က စာသားပြတဲ့ပုံစံကို သဘောပေါက်ပြီလား Ryan။ ဥပမာအနေနဲ့ အဲ့ဒီအပြာရောင်ဘူးကို အစိမ်းရောင်ပြောင်းချင်ရင် code ရဲ့ ဘယ်နေရာကို ပြင်ရမလဲ သိလောက်ပြီလား။

---
![image](https://github.com/user-attachments/assets/47b6f91e-4698-458d-88b0-e36c0a25d2a7)
