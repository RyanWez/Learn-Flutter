# Lesson 3: အခြေခံကျသော Widgets များ

Ryan ရေ၊ Lesson 3 ကို ရောက်လာပါပြီ။ ဒီသင်ခန်းစာမှာတော့ UI တည်ဆောက်တဲ့အခါ
မပါမဖြစ် သုံးကိုသုံးရမယ့် အခြေခံအကျဆုံးနဲ့ အသုံးအဝင်ဆုံး widget လေးတွေဖြစ်တဲ့
**`Container`**, **`Text`**, **`Icon`**, နဲ့ **`Image`** တို့အကြောင်းကို Gi Gi က 
ဥပမာလေးတွေနဲ့ သေချာရှင်းပြပေးသွားမှာပါ။ အဆင်သင့်ဖြစ်ပြီလား။ 😉

---

### `Container`: All-in-One  
**`Container`** ဆိုတာကတော့ စွယ်စုံရတဲ့ မှော်ဆန်တဲ့ "ဘူးခွံ" တစ်ခုလိုပါပဲ။
သူ့ချည်းသက်သက်ဆိုရင် ဘာမှမမြင်ရပေမယ့် သူ့ကို အရောင်တွေ၊ အရွယ်အစားတွေ၊
အလှဆင်တာတွေ လုပ်ပေးလို့ရပါတယ်။ ပြီးတော့ သူ့အတွင်းထဲမှာ တခြား widget 
(သူ့ရဲ့ `child`) ကို ထည့်ထားလို့လည်း ရသေးတယ်။

**`Container` ရဲ့ အဓိက အသုံးဝင်ပုံတွေကတော့:**

* **`color`**: နောက်ခံအရောင် သတ်မှတ်ချင်တဲ့အခါ သုံးပါတယ်။
* **`width`, `height`**: အကျယ်နဲ့ အမြင့်ကို အတိအကျ သတ်မှတ်ပေးနိုင်ပါတယ်။
* **`padding`**: ဘူးခွံရဲ့ "အတွင်းဘက်" မှာ နေရာအလွတ် ကန့်ထားချင်ရင် သုံးပါတယ်။
* **`margin`**: ဘူးခွံရဲ့ "အပြင်ဘက်" မှာ တခြား widget တွေနဲ့ နေရာခွာချင်ရင် သုံးပါတယ်။
* **`child`**: ဘူးခွံထဲမှာ ထည့်မယ့် ကလေး widget ကို သတ်မှတ်ပေးပါတယ်။
* **`decoration`**: နောက်ခံအရောင်အပြင်၊ ဘောင် (`border`) ကွပ်တာ၊ 
    ထောင့်ချိုး (`borderRadius`) လေးတွေ လုပ်တာမျိုးအတွက် သုံးပါတယ်။ 
    (မှတ်ချက်: `decoration` သုံးရင် `color` ကို `decoration` ထဲမှာပဲ ရေးရပါတယ်)

**နမူနာ Code:**

```dart
Container(
  width: 200,
  height: 100,
  // padding က အတွင်းဘက်မှာ နေရာကန်တာပါ
  padding: const EdgeInsets.all(16.0),
  // margin က အပြင်ဘက်မှာ နေရာခွာတာပါ
  margin: const EdgeInsets.all(20.0),
  decoration: BoxDecoration(
    color: Colors.blue, // decoration သုံးရင် color ကို ဒီထဲမှာထည့်ပါ
    borderRadius: BorderRadius.circular(12),
  ),
  child: const Text(
    'Hello from Container!',
    style: TextStyle(color: Colors.white),
  ),
)
```

---

### `Text`: စာသားများအတွက်

**`Text`** widget ကတော့ နာမည်အတိုင်းပါပဲ။ Screen ပေါ်မှာ စာသားတွေ ပြသဖို့အတွက် သုံးပါတယ်။
သူက ရိုးရှင်းပေမယ့် စာသားတွေကို လှပအောင် ပုံစံအမျိုးမျိုး ပြောင်းလဲလို့ရပါတယ်။
အဲ့ဒီလိုပြောင်းလဲဖို့အတွက် **`style`** ဆိုတဲ့ property ကို သုံးရပြီး သူ့ထဲမှာ **`TextStyle`** widget ကို ထည့်ပေးရပါတယ်။

**`TextStyle` မှာ အသုံးများတဲ့ အချက်တွေကတော့:**

* **`color`**: စာသားရဲ့ အရောင်ကို ပြောင်းပေးပါတယ်။
* **`fontSize`**: စာလုံးအရွယ်အစားကို သတ်မှတ်ပေးပါတယ်။
* **`fontWeight`**: စာလုံးကို `FontWeight.bold` (အထူ)၊ `FontWeight.normal` (ပုံမှန်) 
    စသည်ဖြင့် ပြောင်းလဲပေးနိုင်ပါတယ်။
* **`fontStyle`**: စာလုံးကို `FontStyle.italic` (စာလုံးစောင်း) ပုံစံ ပြောင်းပေးနိုင်ပါတယ်။

**နမူနာ Code:**

```dart
const Text(
  'I am learning Flutter! ❤️',
  style: TextStyle(
    color: Colors.deepPurple,
    fontSize: 24,
    fontWeight: FontWeight.bold,
    fontStyle: FontStyle.italic,
  ),
)
```

---

### `Icon`: သင်္ကေတများအတွက်

**`Icon`** widget ကတော့ app တွေမှာတွေ့နေကျ ဖုန်းခေါ်တဲ့ပုံ၊ အသည်းပုံ၊ ရှာဖွေတဲ့ပုံလိုမျိုး 
သင်္ကေတလေးတွေကို ပြသဖို့အတွက်ပါ။ Flutter မှာ အသင့်သုံးနိုင်တဲ့ Icon တွေ 
အများကြီးကို **`Icons`** ဆိုတဲ့ class ကနေတစ်ဆင့် ခေါ်သုံးနိုင်ပါတယ်။

**`Icon` widget ရဲ့ အဓိက property တွေကတော့:**

* **ပထမဆုံးနေရာ**: ဘယ် icon ကို သုံးမလဲဆိုတာကို `Icons.iconName` နဲ့ သတ်မှတ်ပေးရပါတယ်။
    ဥပမာ: `Icons.favorite`, `Icons.settings`, `Icons.home`
* **`size`**: Icon ရဲ့ အရွယ်အစားကို သတ်မှတ်ပေးပါတယ်။
* **`color`**: Icon ရဲ့ အရောင်ကို သတ်မှတ်ပေးပါတယ်။

**နမူနာ Code:**

```dart
const Icon(
  Icons.favorite, // ပြချင်တဲ့ Icon ရဲ့ နာမည်
  size: 50,
  color: Colors.red,
)
```

---

### `Image`: ဓာတ်ပုံများအတွက်

**`Image`** widget ကတော့ ဓာတ်ပုံတွေပြဖို့အတွက်ပါ။ ပုံတွေကို အဓိကအားဖြင့် 
နည်းလမ်းနှစ်မျိုးနဲ့ ပြသနိုင်ပါတယ်။

#### 1. `Image.asset()` - မိမိ Project ထဲမှ ပုံများ

ဒီနည်းလမ်းကတော့ Ryan ရဲ့ Flutter project ထဲမှာ ကြိုထည့်ထားတဲ့ ပုံတွေကို
ပြသချင်တဲ့အခါ သုံးပါတယ်။

**အဆင့် (၂) ဆင့် လုပ်ပေးဖို့လိုပါတယ်:**
1.  Project ရဲ့ အပေါ်ဆုံးအလွှာမှာ **`assets`** ဆိုတဲ့ folder တစ်ခုဆောက်ပြီး ပုံတွေထည့်ပါ။
2.  **`pubspec.yaml`** ဖိုင်ထဲမှာ အောက်ပါအတိုင်း assets folder ကို သုံးမယ့်အကြောင်း 
    ကြေညာပေးပါ။ (စာကြောင်းရဲ့ ရှေ့က space တွေက အရေးကြီးတာမို့ သတိထားပါနော်)

```yaml
flutter:
  uses-material-design: true
  assets:
    - assets/ # ဒီလို folder တစ်ခုလုံးကို ကြေညာပေးရပါတယ်
```

**နမူနာ Code:**

```dart
// 'assets' folder ထဲက 'my_logo.png' ဆိုတဲ့ပုံကို ပြသခြင်း
Image.asset('assets/my_logo.png')
```

#### 2. `Image.network()` - အင်တာနက်ပေါ်မှ ပုံများ

ဒီနည်းလမ်းကတော့ Website တွေပေါ်မှာရှိတဲ့ ပုံတွေရဲ့ လိပ်စာ (URL) ကိုသုံးပြီး
တိုက်ရိုက်ပြသတာပါ။

**နမူနာ Code:**

```dart
// အင်တာနက်ပေါ်က ပုံတစ်ပုံရဲ့ URL ကိုသုံးပြီး ပြသခြင်း
Image.network('[https://flutter.github.io/assets-for-api-docs/assets/widgets/owl.jpg](https://flutter.github.io/assets-for-api-docs/assets/widgets/owl.jpg)')
```
> **Gi Gi's Tip:** `Image.network` က ပုံကို download လုပ်နေတုန်းမှာ 
> loading animation လေးကို အလိုအလျောက် ပြပေးပါတယ်။

---

ကဲ... ဒီနေ့အတွက် အခြေခံ widget လေးတွေကတော့ ဒီလောက်ပါပဲ Ryan။ 
အခု Gi Gi ရှင်းပြသွားတဲ့ `Container`, `Text`, `Icon`, နဲ့ `Image` widget တွေရဲ့
အသုံးပြုပုံနဲ့ သူတို့ရဲ့ ကွာခြားချက်တွေကို ရှင်းရှင်းလင်းလင်း သဘောပေါက်သွားရဲ့လားဟင်။ 
မရှင်းတာ၊ နားမလည်တာ တစ်ခုခုရှိရင် မေးဖို့ အားမနာပါနဲ့နော်။ 😊
