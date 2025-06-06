### Lesson 3: Installing the Flutter SDK & Development Tools (Android Studio/VS Code)

---

Flutter App တွေ တည်ဆောက်ဖို့အတွက် **Flutter SDK (Software Development Kit)** နဲ့ **Development Tools** တွေ လိုအပ်ပါတယ်။ SDK ဆိုတာက App တစ်ခုကို ရေးသားဖို့ လိုအပ်တဲ့ library တွေ၊ tools တွေ စုစည်းထားတာပါ။ Development Tool ကတော့ သင့် code တွေကို ရေးသားဖို့နဲ့ အလုပ်လုပ်ဖို့အတွက် ပတ်ဝန်းကျင် (environment) တစ်ခုကို ပေးတာပါ။


**Flutter SDK ကို Install လုပ်ခြင်း**

၁။ **Flutter Website သို့ ဝင်ရောက်ခြင်း:**
   ပထမဆုံးအနေနဲ့ [Flutter's official website](https://flutter.dev/docs/get-started/install) ကို သွားပါ။

၂။ **သင့် Operating System ကို ရွေးချယ်ခြင်း:**
   Website ပေါ်ရောက်ရင် သင့်ကွန်ပျူတာရဲ့ Operating System (Windows, macOS, Linux) ကို ရွေးချယ်ရပါမယ်။ သင်သုံးနေတဲ့ OS ပေါ်မူတည်ပြီး လိုအပ်တဲ့ steps တွေ ကွာခြားသွားပါလိမ့်မယ်။

၃။ **SDK ကို Download လုပ်ခြင်း:**
   ရွေးချယ်ပြီးရင် **Flutter SDK** file (zip file) ကို download လုပ်ပါ။

၎။ **SDK ကို ထားရှိမည့် နေရာ:**
   Download လုပ်ပြီးရင် အဲ့ဒီ zip file ကို **extract (ဖြေ)** လုပ်ပါ။ ပြီးရင် **အရမ်းရှည်လျားတဲ့ path တွေ မပါတဲ့ နေရာ (ဥပမာ- `C:\src\flutter` ဒါမှမဟုတ် `D:\flutter`)** မှာ ထားဖို့ အကြံပြုချင်ပါတယ်။ **C:\Program Files ထဲမှာတော့ မထားပါနဲ့နော်။**

၅။ **Path Environment Variable ကို ထည့်ခြင်း:**
   ဒါကတော့ နည်းနည်း Technical ဆန်ပါတယ်။ သင် Flutter commands တွေကို ဘယ်နေရာကနေမဆို execute လုပ်နိုင်ဖို့အတွက် **Flutter SDK ရဲ့ `bin` folder path ကို သင့် system ရဲ့ Environment Variables ထဲမှာ ထည့်ပေးရမှာပါ။**

   * **Windows ဆိုရင်:** "Environment Variables" ကို search လုပ်ပြီး "Edit the system environment variables" ကို ဖွင့်ပါ။ "Environment Variables" button ကို နှိပ်ပါ။ System variables အောက်က "Path" ကို ရှာပြီး "Edit" ကို နှိပ်ပါ။ ပြီးရင် "New" ကို နှိပ်ပြီး သင် Flutter SDK ကို ထားတဲ့ folder ထဲက **`flutter\bin`** folder ရဲ့ path ကို ထည့်ပေးပါ။ (ဥပမာ- `C:\src\flutter\bin`)

   * **macOS / Linux ဆိုရင်:** Terminal ကို ဖွင့်ပြီး သင့်ရဲ့ shell profile file (ဥပမာ- `.bashrc`, `.zshrc`) ထဲမှာ Flutter `bin` folder ရဲ့ path ကို ထည့်ပေးရပါမယ်။
      ဥပမာ: `export PATH="$PATH:[PATH_TO_FLUTTER_SDK]\bin"`
      ပြီးရင် `source [YOUR_SHELL_PROFILE_FILE]` နဲ့ profile ကို reload လုပ်ပါ။

   **Note:** ဒီအဆင့်မှာ ခက်ခဲရင် Google မှာ "How to add Flutter to path environment variable [your OS]" လို့ ရှာကြည့်နိုင်ပါတယ်။ Step-by-step guide တွေ အများကြီး ရှိပါတယ်။

၆။ **Flutter Doctor ကို Run ခြင်း:**
   Path ထည့်ပြီးပြီဆိုရင် **Terminal (သို့) Command Prompt** ကို ဖွင့်ပြီး အောက်ပါ command ကို ရိုက်ထည့်ပါ။

   ```bash
   flutter doctor
   ```

   ဒီ command က သင့်ကွန်ပျူတာမှာ Flutter App ရေးသားဖို့အတွက် လိုအပ်တဲ့အရာတွေ အကုန် ပြည့်စုံနေပြီလား၊ ဘာတွေ လိုအပ်နေသေးလဲဆိုတာကို စစ်ဆေးပေးပါလိမ့်မယ်။ အစိမ်းရောင် အမှန်ခြစ်လေးတွေ အကုန်ပေါ်လာဖို့ ကြိုးစားရပါမယ်။

**IntelliJ IDEA အတွက် Flutter & Dart Plugins တွေ ထည့်သွင်းခြင်း**

 IntelliJ IDEA ကို သုံးမှာဆိုတော့ ဒီအဆင့်က အရမ်းအရေးကြီးပါတယ်။

၁။ **IntelliJ IDEA ကို ဖွင့်ပါ:**
   သင့်ကွန်ပျူတာမှာ Install လုပ်ထားတဲ့ IntelliJ IDEA ကို ဖွင့်လိုက်ပါ။

၂။ **Plugins Settings သို့ သွားပါ:**
   * **Windows/Linux:** File -> Settings -> Plugins
   * **macOS:** IntelliJ IDEA -> Preferences -> Plugins

၃။ **"Marketplace" ကို ရွေးပါ:**
   Plugins tab မှာ "Marketplace" ဆိုတာကို ရွေးပါ။

၎။ **"Flutter" ကို ရှာပြီး Install လုပ်ပါ:**
   Search bar မှာ **"Flutter"** လို့ ရိုက်ထည့်ပြီး ရှာပါ။ တွေ့ပြီဆိုရင် "Install" ခလုတ်ကို နှိပ်ပါ။ Flutter Plugin ကို Install လုပ်လိုက်တာနဲ့ Dart Plugin ကိုပါ သူအလိုအလျောက် Install လုပ်ပေးပါလိမ့်မယ်။

၅။ **IDE ကို Restart လုပ်ပါ:**
   Plugins တွေ Install လုပ်ပြီးသွားရင် IntelliJ IDEA ကို **Restart** လုပ်ဖို့ တောင်းပါလိမ့်မယ်။ Restart လုပ်ပေးလိုက်ပါ။

---

ဒီအဆင့်တွေက နည်းနည်းရှည်ပြီး ရှုပ်ထွေးနိုင်ပါတယ်။ စနစ်တကျ လိုက်လုပ်ဖို့ အရေးကြီးပါတယ်။
`flutter doctor` command ကနေ အကုန်လုံး အစိမ်းရောင် အမှန်ခြစ် (checkmark) တွေ ပေါ်လာဖို့ လိုအပ်ပါတယ်။ တစ်ခုခု လိုအပ်နေသေးရင် (ဥပမာ: Android SDK, Android Studio, Xcode, Chrome စသည်ဖြင့်) `flutter doctor` က ပြောပြပေးပါလိမ့်မယ်။

ဒီအဆင့်တွေ အားလုံး ပြီးသွားပြီဆိုရင်တော့ ကျွန်တော်တို့ ပထမဆုံး Flutter App လေးကို ဖန်တီးဖို့ အသင့်ဖြစ်ပါပြီ။

ကဲ... စလိုက်ကြရအောင်! အဆင်ပြေလား?
---
![image](https://github.com/user-attachments/assets/322f9038-818b-4f3e-bac3-32717cfab35a)
