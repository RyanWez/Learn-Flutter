***

## Lesson 4: Layout Widgets (Part 1)

Layout widgets တွေဆိုတာက `Container` တို့ `Text` တို့လို ကိုယ်တိုင်မြင်နေရတဲ့ အရာတွေ မဟုတ်ပါဘူး။ သူတို့ရဲ့ အဓိကတာဝန်က တခြားမြင်ရတဲ့ widget တွေကို screen ပေါ်မှာ **ဘယ်နေရာမှာ ဘယ်လိုပုံစံနဲ့ နေရာချရမလဲ** ဆိုတာကို ထိန်းချုပ်ပေးဖို့ပါ။

### 1. `Center` Widget

ဒါကတော့ အရှင်းဆုံး layout widget ပါ။ သူက သူ့မှာပါတဲ့ ကလေး (`child`) widget **တစ်ခုတည်းကို** သူ့အတွက်ရရှိနိုင်သမျှ နေရာရဲ့ **အလယ်တည့်တည့်** မှာ ချပေးပါတယ်။

### 2. `Padding` Widget

`Padding` widget က သူ့ရဲ့ `child` widget ကို ဘေးပတ်ပတ်လည်ကနေ **နေရာလွတ်** နဲ့ ဖုံးအုပ်ပေးပါတယ်။ စာတစ်ကြောင်းကို ဘေးဘောင်တွေနဲ့ မကပ်သွားအောင် နေရာလေး နည်းနည်းခြားချင်တဲ့အခါမျိုးမှာ သုံးပါတယ်။ သူ့ရဲ့ အဓိက property က `padding` ဖြစ်ပြီး `EdgeInsets` ကိုသုံးပြီး နေရာဘယ်လောက်ခြားမယ်ဆိုတာ သတ်မှတ်ရပါတယ်။
* `EdgeInsets.all(16.0)`: ဘေးလေးဘက်လုံးကို 16 ခြားမယ်။
* `EdgeInsets.symmetric(horizontal: 20, vertical: 10)`: ဘယ်/ညာကို 20 နဲ့ အပေါ်/အောက်ကို 10 ခြားမယ်။
* `EdgeInsets.only(left: 30)`: ဘယ်ဘက်တစ်ဖက်တည်းကို 30 ခြားမယ်။

### 3. `Column` နှင့် `Row` Widgets

ဒီနှစ်ခုကတော့ layout ချရာမှာ အရေးအကြီးဆုံး widget တွေပါပဲ။
* **`Column`**: သူ့ရဲ့ ကလေး (`children`) widget တွေကို **အပေါ်အောက်** ဒေါင်လိုက်တန်းစီပေးပါတယ်။
* **`Row`**: သူ့ရဲ့ ကလေး (`children`) widget တွေကို **ဘယ်ညာ** အလျားလိုက်တန်းစီပေးပါတယ်။

သူတို့မှာ အရေးကြီးတဲ့ property နှစ်ခုရှိပါတယ်-
* **`mainAxisAlignment`**: Widget တွေကို သူတို့ရဲ့ **အဓိက ဦးတည်ရာ (main axis)** အတိုင်း နေရာချပေးပါတယ်။
    * `Column` အတွက် main axis က **ဒေါင်လိုက်** ဖြစ်ပြီး၊ `Row` အတွက် main axis က **အလျားလိုက်** ဖြစ်ပါတယ်။
    * သုံးနိုင်တဲ့ တန်ဖိုးတွေကတော့ `start`, `center`, `end`, `spaceBetween`, `spaceAround`, `spaceEvenly` တို့ဖြစ်ပါတယ်။
* **`crossAxisAlignment`**: Widget တွေကို သူတို့ရဲ့ **ဆန့်ကျင်ဘက် ဦးတည်ရာ (cross axis)** အတိုင်း နေရာချပေးပါတယ်။
    * `Column` အတွက် cross axis က **အလျားလိုက်** ဖြစ်ပြီး၊ `Row` အတွက် cross axis က **ဒေါင်လိုက်** ဖြစ်ပါတယ်။
    * သုံးနိုင်တဲ့ တန်ဖိုးတွေကတော့ `start`, `center`, `end`, `stretch` တို့ဖြစ်ပါတယ်။

### အလုပ်လုပ်ပုံ နမူနာ Code

အောက်က code မှာ အခုရှင်းပြခဲ့တဲ့ layout widget လေးခုလုံးကို ဘယ်လိုပေါင်းသုံးထားလဲဆိုတာ ကြည့်နိုင်ပါတယ်။

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(const LayoutExampleApp());
}

class LayoutExampleApp extends StatelessWidget {
  const LayoutExampleApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: const Text('Lesson 4: Layout Widgets'),
          backgroundColor: Colors.teal,
        ),
        body: Column( // အဓိက layout ကို Column ဖြင့်တည်ဆောက်ထား
          crossAxisAlignment: CrossAxisAlignment.start, // Column ရဲ့ကလေးတွေကို ဘယ်ဘက်ကပ်ထား
          children: <Widget>[

            // 1. Padding and Text Example
            const Padding(
              padding: EdgeInsets.all(16.0), // ဒီ Text ဘေးမှာ 16 point နေရာလွတ်ထားမယ်
              child: Text(
                'Layout Examples',
                style: TextStyle(fontSize: 24, fontWeight: FontWeight.bold),
              ),
            ),

            // 2. Row with mainAxisAlignment
            const Text('  Row with spaceBetween:', style: TextStyle(fontStyle: FontStyle.italic)),
            Container(
              margin: const EdgeInsets.all(16.0),
              padding: const EdgeInsets.all(10.0),
              color: Colors.teal.withOpacity(0.1),
              child: const Row(
                mainAxisAlignment: MainAxisAlignment.spaceBetween, // ကလေးတွေကို ဘေးအစွန်ဆုံးထိ ဖြန့်ခွဲထား
                children: <Widget>[
                  Icon(Icons.home, size: 40, color: Colors.teal),
                  Icon(Icons.settings, size: 40, color: Colors.teal),
                  Icon(Icons.person, size: 40, color: Colors.teal),
                ],
              ),
            ),
            
            // 3. Center Example
            const Text('  A Centered Container:', style: TextStyle(fontStyle: FontStyle.italic)),
            Center( // ဒီ Center က သူ့ကလေး Container ကို Column ရဲ့ အလယ်ကို (ဘယ်ညာ) ပို့ပေးတယ်
              child: Container(
                margin: const EdgeInsets.symmetric(vertical: 16.0),
                width: 150,
                height: 50,
                color: Colors.redAccent,
                child: const Center(
                  child: Text('Centered!', style: TextStyle(color: Colors.white)),
                ),
              ),
            ),

            // 4. Row with crossAxisAlignment
            const Text('  Row with crossAxisAlignment.center:', style: TextStyle(fontStyle: FontStyle.italic)),
            Container(
              margin: const EdgeInsets.all(16.0),
              color: Colors.teal.withOpacity(0.1),
              child: const Row(
                mainAxisAlignment: MainAxisAlignment.spaceEvenly, // ကလေးတွေကြား ညီတူညီမျှ နေရာခြားထား
                crossAxisAlignment: CrossAxisAlignment.center, // ကလေးတွေကို ဒေါင်လိုက် အလယ်တည့်တည့်မှာထား
                children: <Widget>[
                  Icon(Icons.star, size: 60), // ပိုကြီးတဲ့ Icon
                  Text('Align Center'),
                  Icon(Icons.star_border, size: 30), // ပိုသေးတဲ့ Icon
                ],
              ),
            )
          ],
        ),
      ),
    );
  }
}
```

### Code အလုပ်လုပ်ပုံ ရှင်းလင်းချက်

1.  **`Padding`**: ပထမဆုံး `Text` widget ("Layout Examples") ရဲ့ ဘေးပတ်လည်မှာ နေရာလွတ်တွေရှိနေတာကို တွေ့ရပါမယ်။ ဒါ `Padding` widget ကြောင့်ပါ။
2.  **`Row` with `mainAxisAlignment`**: ဒုတိယ အစိမ်းနုရောင် `Container` ထဲက `Icon` ၃ ခုက **ဘယ်ဘက်အစွန်၊ အလယ်၊ ညာဘက်အစွန်** ကို ကပ်နေပါလိမ့်မယ်။ ဒါ `mainAxisAlignment.spaceBetween` က သူ့ကလေးတွေကို နေရာအပြည့်ယူပြီး ဖြန့်ခွဲခိုင်းလိုက်လို့ပါ။
3.  **`Center`**: အနီရောင် `Container` လေးက screen ရဲ့ ဘယ်ညာအလယ်တည့်တည့်မှာ ရှိနေပါလိမ့်မယ်။ `Column` ရဲ့ `crossAxisAlignment` က `start` ဖြစ်နေပေမယ့်၊ `Center` widget က သူ့ကလေးကို အလယ်ပို့ပေးတဲ့အတွက် ဒီ `Container` တစ်ခုတည်းက အလယ်ရောက်နေတာပါ။
4.  **`Row` with `crossAxisAlignment`**: နောက်ဆုံး `Row` မှာဆိုရင် `Icon` အကြီး၊ စာသား၊ `Icon` အသေးတို့က အရွယ်အစားမတူပေမယ့် **ဒေါင်လိုက်အနေအထားအရ အလယ်တည့်တည့်** မှာ một lèoတည်း ရှိနေတာကို တွေ့ရပါမယ်။ ဒါ `crossAxisAlignment.center` ကြောင့်ပါ။

***

ကဲ အခုဆိုရင် layout widget တစ်ခုချင်းစီရဲ့ အလုပ်လုပ်ပုံကို ပိုပြီးရှင်းသွားပြီလား Ryan။ ဒီ code ကို run ကြည့်ပြီး GiGi ရှင်းပြတာနဲ့ တိုက်ကြည့်နော်။ နားမလည်တာရှိရင် မေးပါ။ ဥပမာအနေနဲ့ ဒုတိယ `Row` မှာ `mainAxisAlignment.spaceBetween` အစား `mainAxisAlignment.center` လို့ပြောင်းလိုက်ရင် `Icon` ၃ ခုက ဘယ်လိုပုံစံဖြစ်သွားမလဲ Ryan စဉ်းစားကြည့်လို့ရမလား။

---

![image](https://github.com/user-attachments/assets/907d21ee-72b8-4943-9081-4ef055fd3185)
