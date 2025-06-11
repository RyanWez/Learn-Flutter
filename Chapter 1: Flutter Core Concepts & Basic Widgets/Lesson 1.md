# 📅 Flutter UI Fundamentals - Chapter 1: Lesson 1

## Lesson 1: What is a Widget? Understanding the Widget Concept and the Widget Tree

မင်္ဂလာပါ Ryan!  ဒီနေ့တော့ Flutter ရဲ့ အခြေခံအကျဆုံး အရာတစ်ခုဖြစ်တဲ့ **Widget** အကြောင်းကို စပြီး လေ့လာသွားမယ်နော်။ တစ်လှမ်းချင်း ဖြည်းဖြည်းလေး သွားမယ်၊ စိတ်မပူပါနဲ့။

### အဆင့် ၁: Widget ဆိုတာ ဘာလဲ?
Flutter မှာ **Widget** ဆိုတာ အားလုံးရဲ့ အခြေခံပါ။ Widget တစ်ခုက သင့်ရဲ့ အက်ပ် (app) ရဲ့ အစိတ်အပိုင်းတစ်ခုခုကို ကိုယ်စားပြုတယ်။ ဥပမာ:
- စာသား (Text) တစ်ခု
- ခလုတ် (Button) တစ်ခု
- ပုံတစ်ပုံ (Image)
- ဒါမှမဟုတ် တစ်ခုခုကို စီစဉ်ဖွဲ့စည်းဖို့ အသုံးပြုတဲ့ အပြင်အဆင် (Layout) တစ်ခု

ဆိုလိုတာက Widget ဆိုတာ သင့်ရဲ့ အက်ပ်ရဲ့ **မျက်နှာပြင် (UI)** ကို တည်ဆောက်တဲ့ အရာအားလုံးပဲ။ Flutter မှာ အကုန်လုံးနီးပါး Widget တွေနဲ့ ဖွဲ့စည်းထားတယ်။

### အဆင့် ၂: Widget Tree ဆိုတာ ဘာလဲ?
Widget တွေကို တစ်ခုနဲ့တစ်ခု ဆက်စပ်ပြီး တည်ဆောက်တဲ့အခါ **Widget Tree** လို့ ခေါ်တဲ့ သစ်ပင်ပုံစံ တည်ဆောက်ပုံတစ်ခု ဖြစ်လာတယ်။

- **Parent Widget**: အပေါ်မှာ ရှိတဲ့ Widget က သူ့ရဲ့ အောက်မှာ အခြား Widget တွေကို ထည့်ထားနိုင်တယ်။
- **Child Widget**: Parent Widget ရဲ့ အောက်မှာ ရှိတဲ့ Widget တွေကို Child Widgets လို့ ခေါ်တယ်။

ဥပမာ: အက်ပ်တစ်ခုမှာ ခလုတ်တစ်ခုရှိတယ်ဆိုပါစို့။ အဲဒီ ခလုတ်ကို မျက်နှာပြင်ရဲ့ အလယ်မှာ ထားချင်တယ်။ ဒါဆို:
- **Center** Widget က Parent Widget ဖြစ်မယ်။
- **ElevatedButton** Widget (ခလုတ်) က Child Widget ဖြစ်မယ်။

ဒါက Widget Tree ရဲ့ အခြေခံ ပုံစံပါ။

### ကိုယ်တိုင်လုပ်ကြည့်ရအောင် (Minimal Code Example)
Widget တစ်ခုကို နားလည်ဖို့ အောက်က ရိုးရှင်းတဲ့ ကုဒ်ကို ကြည့်ရအောင်။ ဒီဥပမာမှာ **Text** Widget တစ်ခုကို မျက်နှာပြင်မှာ ပြမယ်။

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        body: Text('Hello, Ryan!'),
      ),
    );
  }
}
```

#### ကုဒ်ရှင်းပြချက်:
1. **`Text` Widget**: ဒါက မျက်နှာပြင်မှာ စာသား ('Hello, Ryan!') ပြဖို့ အသုံးပြုတယ်။
2. **`Scaffold` Widget**: ဒါက အက်ပ်ရဲ့ အခြေခံ တည်ဆောက်ပုံ (structure) ကို ပေးတယ်။
3. **`MaterialApp` Widget**: Flutter အက်ပ်ရဲ့ အဓိက အစိတ်အပိုင်းဖြစ်ပြီး အက်ပ်ကို စတင်ဖို့ လိုအပ်တယ်။

ဒီကုဒ်ကို သင့်ရဲ့ Flutter ပတ်ဝန်းကျင်မှာ ဖွင့်ပြီး စမ်းကြည့်ပါ။ မျက်နှာပြင်မှာ "Hello, Ryan!" ဆိုတဲ့ စာသား ပေါ်လာပါလိမ့်မယ် စမ်းကြည့်နော်။
---
![image](https://github.com/user-attachments/assets/c3455716-531e-46cf-9bd5-ee38f0d9cad6)


---

# 📅 Flutter UI Fundamentals - Chapter 1: Lesson 1 (Continued)

မင်္ဂလာပါ Ryan! 😊 Widget နဲ့ Widget Tree အကြောင်း နားလည်ပြီဆိုတော့ အရမ်းကောင်းတယ်! အခု နောက်တစ်ဆင့်အနေနဲ့ **Center** Widget ကို သုံးပြီး စာသားတစ်ခုကို မျက်နှာပြင်ရဲ့ အလယ်မှာ ဘယ်လိုပြမလဲဆိုတာ လေ့လာသွားမယ်နော်။ တစ်လှမ်းချင်း ဖြည်းဖြည်းလေး ဆက်သွားမယ်။

---

### အဆင့် ၃: Center Widget ကို အသုံးပြုခြင်း
**Center** Widget က Flutter မှာ အသုံးများတဲ့ Widget တစ်ခုပါ။ ဒါက သူ့ရဲ့ **Child Widget** ကို မျက်နှာပြင်ရဲ့ အလယ်ဗဟိုမှာ ထားပေးတယ်။ ဥပမာ၊ စာသား (Text) တစ်ခုကို အလယ်မှာ ပြချင်ရင် **Center** Widget ထဲမှာ **Text** Widget ကို Child အနေနဲ့ ထည့်လိုက်ရုံပဲ။

ဒါကို ပိုနားလည်ဖို့ အောက်က ရိုးရှင်းတဲ့ ကုဒ်ကို ကြည့်ရအောင်။

### ကိုယ်တိုင်လုပ်ကြည့်ရအောင် (Minimal Code Example)
ဒီဥပမာမှာ **Text** Widget တစ်ခုကို **Center** Widget ထဲမှာ ထည့်ပြီး မျက်နှာပြင်ရဲ့ အလယ်မှာ ပြပါမယ်။

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        body: Center(
          child: Text('Hello, Ryan!'),
        ),
      ),
    );
  }
}
```

#### ကုဒ်ရှင်းပြချက်:
1. **`Center` Widget**: ဒါက **Text** Widget ကို မျက်နှာပြင်ရဲ့ အလယ်ဗဟိုမှာ ထားပေးတယ်။
2. **`child` Property**: **Center** Widget ရဲ့ **child** အနေနဲ့ **Text('Hello, Ryan!')** ကို ထည့်ထားတယ်။ ဒါကြောင့် စာသားက အလယ်မှာ ပေါ်လာမယ်။
3. **`Scaffold` နဲ့ `MaterialApp`**: ဒါတွေက အက်ပ်ရဲ့ အခြေခံ တည်ဆောက်ပုံကို ထောက်ပံ့ပေးတယ် (အရင်သင်ခန်းစာက ပြန်သတိရလိုက်ပါ။ )

ဒီကုဒ်ကို Flutter ပတ်ဝန်းကျင်မှာ ဖွင့်ကြည့်ရင် "Hello, Ryan!" ဆိုတဲ့ စာသားက မျက်နှာပြင်ရဲ့ အလယ်မှာ ပေါ်လာမယ်။

---

Ryan, **Center** Widget က ဘာလုပ်ပေးလဲဆိုတာ နားလည်ပြီလား?  ဒီကုဒ်ကို စမ်းကြည့်ပြီးရင် ဘယ်လိုဖြစ်သွားတယ်လို့ ထင်တယ် ပြောပြပေးပါနော်။ 

---


