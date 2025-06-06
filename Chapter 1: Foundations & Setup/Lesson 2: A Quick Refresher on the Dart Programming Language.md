### Lesson 2: A Quick Refresher on the Dart Programming Language

---

Flutter App တွေကို ရေးသားဖို့အတွက် **Dart** ဆိုတဲ့ Programming Language ကို အသုံးပြုရပါတယ်။ ဒါကြောင့် Flutter ကို မလေ့လာခင် Dart ရဲ့ အခြေခံလေးတွေကို နည်းနည်း ပြန်လေ့လာထားရင် ပိုပြီး အဆင်ပြေပါလိမ့်မယ်။

Dart ဟာ **object-oriented programming language** တစ်ခု ဖြစ်ပါတယ်။ Java, C++, JavaScript တို့နဲ့ ဆင်တူတဲ့ အစိတ်အပိုင်းတွေ အများကြီးရှိပါတယ်။ အကယ်၍ သင်က တခြား programming language တွေနဲ့ ရင်းနှီးပြီးသားဆိုရင် Dart ကို လေ့လာရတာ ပိုပြီး လွယ်ကူပါလိမ့်မယ်။

ဒီသင်ခန်းစာမှာ Dart ရဲ့ အခြေခံ အကျဆုံး အချက်လေးတွေကိုပဲ အမြန်ဆုံး ပြန်လည် ဆန်းစစ်ကြည့်ရအောင်နော်။ အသေးစိတ် မသင်သေးပါဘူး။

#### 1. Variables (ကိန်းရှင်များ)

Data တွေကို သိမ်းဆည်းဖို့အတွက် **Variables** တွေကို အသုံးပြုပါတယ်။

**Example:**

```dart
void main() {
  String name = 'Ryan Wez'; // Text data
  int age = 25;           // Whole number
  double height = 5.9;    // Decimal number
  bool isStudent = true;  // True or False value

  print('Name: $name');
  print('Age: $age');
  print('Height: $height feet');
  print('Is student: $isStudent');
}
```

ဒီ code လေးမှာ `String` (စာသား), `int` (ကိန်းပြည့်), `double` (ဒသမ ကိန်း), `bool` (မှန်/မှား) ဆိုပြီး variable အမျိုးအစား ၄ မျိုးကို မြင်တွေ့ရပါလိမ့်မယ်။ `print()` function ကတော့ console မှာ စာသားတွေ ထုတ်ပြဖို့အတွက်ပါ။ စာသားတွေထဲမှာ variable တွေကို ထည့်သွင်းပြသချင်ရင် `$` symbol ကို အသုံးပြုနိုင်ပါတယ်။

#### 2. Functions (လုပ်ဆောင်ချက်များ)

特定的 task တွေကို လုပ်ဆောင်ဖို့အတွက် **Functions** တွေကို အသုံးပြုပါတယ်။

**Example:**

```dart
void main() {
  sayHello('Ryan'); // Calling the function
  int result = addNumbers(10, 5);
  print('Sum: $result');
}

void sayHello(String name) { // Function with no return value
  print('Hello, $name!');
}

int addNumbers(int a, int b) { // Function that returns an integer
  return a + b;
}
```

ဒီမှာ `sayHello` နဲ့ `addNumbers` ဆိုတဲ့ function နှစ်ခုကို မြင်ရပါလိမ့်မယ်။ `sayHello` ကတော့ နာမည်တစ်ခုကို ယူပြီး နှုတ်ဆက်စာ ထုတ်ပြတာပါ။ `addNumbers` ကတော့ ဂဏန်းနှစ်လုံးကို ပေါင်းပြီး ရလဒ်ကို ပြန်ပေးတာပါ။ `void` ဆိုတာက ဘာမှ ပြန်မပေးတဲ့ function တွေအတွက် သုံးတာပါ။ `int` ဆိုတာကတော့ ကိန်းပြည့်တစ်လုံးကို ပြန်ပေးမယ်ဆိုတဲ့ အဓိပ္ပာယ်ပါ။

#### 3. Control Flow (အခြေအနေထိန်းချုပ်ခြင်း)

Code တွေ ဘယ်လိုအလုပ်လုပ်မယ်ဆိုတာကို ထိန်းချုပ်ဖို့အတွက် `if/else`, `for`, `while` စတာတွေကို အသုံးပြုပါတယ်။

**Example:**

```dart
void main() {
  int score = 75;

  // if-else statement
  if (score >= 60) {
    print('You passed!');
  } else {
    print('You failed.');
  }

  // for loop
  for (int i = 0; i < 3; i++) {
    print('Loop iteration: $i');
  }

  // while loop
  int count = 0;
  while (count < 2) {
    print('While loop count: $count');
    count++;
  }
}
```

ဒီဥပမာတွေကတော့ ရိုးရှင်းတဲ့ `if/else` အခြေအနေ စစ်ဆေးတာ၊ သတ်မှတ်ထားတဲ့ အကြိမ်အရေအတွက်အတိုင်း အလုပ်လုပ်တဲ့ `for loop` နဲ့ အခြေအနေတစ်ခုမှန်သရွေ့ အလုပ်လုပ်တဲ့ `while loop` ဥပမာတွေ ဖြစ်ပါတယ်။

---

ဒီလောက်ဆို Dart ရဲ့ အခြေခံလေးတွေဖြစ်တဲ့ Variables, Functions, Control Flow တွေကို ပြန်ပြီး သတိရသွားလောက်ပြီလို့ ထင်ပါတယ်။ Flutter ကို လေ့လာတဲ့အခါမှာ ဒီအခြေခံအချက်လေးတွေက အမြဲသုံးရမှာမို့လို့ပါ။
