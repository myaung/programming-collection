## Programming Languages & their Execution Environment

ကဲ ဒီတခါေတာ့ languages ေတြနဲ. သူတုိ. ဘယ္လို execute လုပ္သလဲ ဘာေတြသံုးၿပီးေတာ့ သူတုိ. အလုပ္လုပ္သလဲဆုိတာကိုေၿပာၾကရေအာင္ပါ။

**Execution Environment ဆုိတာဘာလဲ**

သူ.ကုိေၿပာရမယ္ဆုိရင္ေတာ့ Language တခု execution လုပ္ရာမွာ ကူညီပါ၀င္တဲ့ ပတ္၀န္းက်င္ အဲလိုပဲေၿပာရမွာပါ

ၿမန္မာလို ဆုိေတာ့ ဘာသာၿပန္ရလဲခက္သားဗ်။ ဘာကိုဆုိလုိခ်င္တာလဲ ဆုိေတာ့ programming language ေတြဟာ သူတုိ.ရဲ. source code သုိ.မဟုတ္

byte code, object code , exe code အဲဒါေတြကို ဘယ္လို execute လုပ္ၾကလဲ ။ ဘယ္အေပၚမွာ လုပ္ၾကသလဲဆုိတာေပါ့။

အဲဒါေတြကိုသိထားရင္ ဒီ language ကို ဘယ္လို အသံုးခ်ရင္ သင့္ေတာ္မလဲ ဘာေတြလုပ္လုိ.ရမလဲဆုိတာ သိႏုိင္မွာပါ။ ဒီေနရာမွာ သံုးခု ခြဲၿပီးေၿပာရမွာပါ။

C, C++ အစရိွတာ က တစ္အုပ္စု၊ ဒီ အုပ္စု က သူတုိ.ေတြဟာ exe code ကုိတခါတည္းထုတ္ပါတယ္ ဒါေၾကာင့္သူတုိ.ေတြဟာ OS ကေနတဆင့္ physical machine ေပၚမွာ တန္းၿပီးေတာ့ run ပါတယ္။ ေနာက္တအုပ္စုကေတာ့ C#, [VB.NET](http://VB.NET/), Java အစရိွတဲ့ Virtual Machine သံုးတဲ့အုပ္စုေပါ့ သူတုိ.ကေတာ့ exe code မထုတ္ပဲ ၾကားခံ intermediate code ထုတ္ပါတယ္ ၿပီးေတာ့ physical computer မဟုတ္ပဲနဲ. software သုိ.မဟုတ္ hardware နဲ. virtual instruction set ကုိ simulated လုပ္ထားတဲ့ machine (ဒါေၾကာင့္မို.လုိ. VM လို.ေခၚတာပါ) အေပၚမွာ run တဲ့ အုပ္စု။ ဒီေနရာမွာ Virtual Machine လုိ.ေၿပာတဲ့ေနရာမွာ လင္းစရာတခုရိွပါတယ္။ ကြ်န္ေတာ္ေၿပာေနတာ programming language ေတြအတြက္သံုးတဲ့ virtual machine ကုိေၿပာတာပါ။ OS အတြက္သံုးတဲ့ VMWare တို.လုိ virtual machine မ်ိဳး မဟုတ္ပါဘူး။ ဒီႏွစ္ခု က ဆင္သလုိရိွေပမဲ့ မတူၾကပါဘူး။ ေနာက္တစ္စုကေတာ့ Interpreter ေတြေပါ့ သူတုိ.ဘယ္လုိ run ၾကသလဲဆုိေတာ ေၿပာမွာပါ။

**Execution Environment For C, C++**

C, C++ Compiler ဟာ C, C++ source program ကုိလက္ခံၿပီးေတာ့ exe code ကုိ directly ထုတ္ေပးပါတယ္ ။ Library file ေတြကိုေတာ့ object code အေနနဲ.သိမ္းထားပါတယ္ ၊ကုိသံုးမဲ့ library ေတြကိုပါ exe ဖုိင္ထဲမွာ တြဲထည့္ေပးတာပါ။ သူ.ကို run မယ္ဆုိရင္ exe ဖိုင္မွာ ရိွတဲ့ content အားလံုးကို memory ေပၚေခၚတင္ရပါတယ္ ။ အဲလုိ ကုိယ္သံုးမဲ့အရာအားလံုး source program + library function ေတြကို တခါတည္း တန္းၿပီးေခၚတင္ (load) လုပ္ရတဲ့အတြက္ C,C++ ကုိ static linking language လို.ေခၚပါတယ္။ ေၿပာခ်င္တာကေတာ့ object code ေတြကို program မ run ခင္ compile time (static) ၿဖစ္ေနတံုးမွာ ေခၚတင္ရတဲ့အတြက္ static linking language ေပါ့။ C,C++ exe code ေတြဟာ OS ကတဆင့္ physical hardware ေပၚမွာ တန္းၿပီး run ပါတယ္။ အဲေတာ့ သူတုိ.ဟာ low level function ေတြၿဖစ္တဲ့ direct memory access လုပ္တာမ်ိုး register ေတြကို access လုပ္တာမ်ိဳးအစရိွတဲ့ function ေတြကို လုပ္ခြင့္ရပါတယ္။ ဒါေၾကာင့္လဲ C,C++ ကုိ OS ေတြေရးတဲ့ေနရာမ်ိဳးေတြ low level device ေတြကို လွမ္းထိန္းရမဲ့ code မ်ိဳးေတြ ဥပမာ (Networking library) လိုေနရာမ်ိဳးမွာသံုးၾကတာေပါ့။ Static Linking ရဲ.မေကာင္းတဲ့အခ်က္က အားလံုးကုိ memory ေပၚမွာတင္ေနရတာပဲ သံုးမသံဳးေပ့ါ။ ေကာင္းတဲ့အခ်က္ကေတာ့ သူတုိ.ေတြဟာ modern language ေတြၿဖစ္တဲ့ Java, C# ထက္ၿမန္တယ္ဆုိတာပါပဲ။ ၿပီးေတာ့ memory ကိုတုိက္ရုိက္ထိန္းလုိ.ရတယ္ ။ ေနာက္တခုမေကာင္းတာက ကိုယ္တုိင္ထိန္းရတဲ့ အတြက္ memory မွာ က်န္တဲ့ garbage ေတြအတြက္ programmer က memory ကုိ သပ္သပ္ garbage collection လုပ္ရပါတယ္။ Modern programming language ေတြမွာေတာ့ လုပ္စရာမလုိဘူးေပါ့။ တကယ္လုိ. window platform ဆုိရင္ static linking ကုိရွင္းဖုိ.ရာအတြက္ dll ဖုိင္ေတြသံုးရင္ရပါတယ္ ဒါကလဲ microsoft ကေပးထားတာပါ library ေတြကို dll အေနနဲ.သိမ္းၿပီး လုိအပ္မွ memory ေပၚေခၚတင္ေပါ့။.

**Execution Environment for C#, VB.NET, Java**

ခုနက C, C++ တုိ.ဟာ physical machine အေပၚမွာ run ပါတယ္ ။ သူတုိ.ဆီက ထုတ္တဲ့ code က executable ၿဖစ္ပါတယ္ ။ ဆုိခ်င္တာက သူတုိ.ထုတ္လုိက္တာဟာ သက္ဆုိင္ရာ OS နဲ. Physical hardware အေပၚမူတည္တဲ့ code ေတြပါပဲ။ ဒါဟာ ဘာၿဖစ္သလဲဆုိေတာ့ portable program မၿဖစ္ေတာ့ပါဘူး။ ဆုိခ်င္တာက microsoft အတြက္ ထုတ္ထားတဲ့ C++ exe code ဟာ linux အေပၚမွာ run ဖုိ.အဆင္မေၿပပါဘူး။ ဘာေၾကာင့္လဲဆုိေတာ သူတုိ.ေတြဟာ platform specific code ၿဖစ္လို.ပါပဲ။ အဲေတာ့ သင္ေရးထားတဲ့ window ေပၚက C++ program တစ္ပုဒ္ကုိ Linux သုိ.မဟုတ္ တၿခား platform မွာ run မယ္ဆုိရင္ recompile သုိ.မဟုတ္ တၿခားၿပင္စရာေတြလုိအပ္လာမွာပါ။ program ေသးရင္ေတာ့ၿပႆနာမရိွေပမဲ့ program ကၾကီးလာရင္ ဒီၿပႆနာကေတာ္ေတာ္ၾကီးလာေရာ ။ ကဲ ဘယ္လိုလုပ္ၾကမလဲေပါ့။ အဲဒီေတာ့ researcher ၾကီးေတြက ဘာလုပ္တံုးဆုိ ေတာ့ဗ်ာ ၊ programming language တစ္ခု က machine code or executable code ထုတ္မယ္ ဆုိရင္ သူက အဲ့ machine အေပၚမွာ ပဲ run ႏုိင္မယ္ အဲေတာ့ သူတုိ.က ၾကားခံ intermediate code ထုတ္မယ္ အဲ့ code ကို run ဟာ ဘယ္ platform ကိုမွ မမူတည္တဲ့ virtual instruction set ၿဖစ္ရမယ္။ အဲ့ဒီ instruction set ကို က်ေတာ့ physical hardware က နားမလည္ဘူး ။ အဲေတာ့ virtual instruction set ေတြကို ဘယ္လုိ execute လုပ္မလဲ ။ အဲဒီမွာ virtual machine ဆုိတာကိုထုတ္လိုက္ေလ သတည္းေပါ့။ Programming language တခုက virtual instruction set ကိုထုတ္မယ္ သူ.ကို platform အလုိက္ ေရးထားတဲ့ virtual machine ေတြက execute လုပ္ေပါ့ ။ အဲဒီနည္းကို C#, VB.Net, Java အစရိွတဲ့ programming language ေတြကသံုးပါတယ္။ Java program တစ္ပုဒ္ေရးလုိက္တယ္ ၿပီးေတာ့ Compile လုပ္လုိက္ရင္ .class ဖုိင္ဆုိတာ ထြက္လာပါတယ္ အဲ့ဖုိင္ဟာ တကယ္ေတာ့ physical machine ေပၚမွာ မ run ႏုိင္ပါဘူး ။ သူ.ကုိ byte code လုိ.ေခၚပါတယ္ အဲ့အထဲမွာ JVM (Java Virtual Machine) ကပဲနားလည္တဲ့ instruction set ေတြ ပါပါတယ္။ ခုနက ထုတ္လိုက္တဲ့ .class (byte code) ေတြဟာ software သုိ.မဟုတ္ hardware နဲ. implement လုပ္ထားတဲ့ JVM အေပၚမွာ run ပါတယ္။ ကဲ ေနာက္တခါ အဲဒီ bytecode ကုိ Linux ကုိေရြ.မယ္ဆုိပါေတာ့ Linux အေပၚမွာ ရိွတဲ့ JVM က အဲ့ဒီ bytecode ကုိနားလည္ၿပီး execute လုပ္ေပးပါလိမ့္မယ္ ။ အဲဒီေတာ့ဗ်ာ ဘာၿဖစ္လာလဲဆုိေတာ့ platform independent ဆုိတာၾကီး ၿဖစ္လာေရာ ။ ဆုိခ်င္တာက Java ဟာ ၾကိဳက္တဲ့ေနရာမွာ run လုိ.ရပါတယ္ေပါ့ အဲ JVM ေတာ့ ရိွရမေပါ့ေလ။

ဒီေနရာမွာ Microsoft အၾကံ႔ၾကီးပံုထပ္ေၿပာဖုိ.လိုပါၿပီ Java က C++ ကိုေလ်ာ့သင့္တာေလ်ာ့ ၿဖည့္သင့္တာၿဖည့္ၿပီးေတာ့ platform independent လုပ္ပလိုက္ေရာ။ အဲေတာ့ Microsoft ကလဲ အမွီလုိက္ရ ေရာေပါ့ေလ ။ သူကလဲ C#, VB.NETစတာေတြကုိထုတ္လုိက္ပါတယ္ ၿပီးေတာ့ သူတုိ.ကုိ run ဖုိ. CLR (Common Language Runtime) ကုိထုတ္လုိက္ပါတယ္ ။ C#, VB.NET အၿပင္ တၿခားေသာ language ေတြဟာလဲ CLR အေပၚမွာ run ႏုိင္ပါတယ္ ။ CLR ဆုိတာ လည္း Virtual Machine တစ္ခုပါပဲ ။ C#, VB.NET အၿပင္ တၿခားေသာ CLR target language ေတြဟာ MSIL (Microsoft Intermediate Language) ကုိထုတ္ပါတယ္။ ၿပီးေတာ့ MSIL ဟာ CLR အေပၚမွာ run ေပါ့ ။ ဒီနည္းနဲ. Microsoft programming language ေတြဟာ လဲ Unix အေပၚမွာ run လုိ.ရပါတယ္ Mono project လို.ေခၚပါတယ္ ။ Unix, Linux တုိ.အေပၚမွာ CLR language ေတြကို run ဖုိ.အတြက္ လုပ္တဲ့ project ပါ။ ကဲ Java ထက္ ဘာတကြက္ အသာယူသြားလဲဆုိေတာ့ သူက platform independent အၿပင္မကပဲ Cross language Interoperability ပါရသြားပါတယ္ ဆုိခ်င္တာက VB.NET ကလဲ MSIL ကုိထုတ္တယ္ C# ကလဲ MSIL ထုတ္ေတာ့ VB.NET နဲ.ေရးထားတဲ့ Class တစ္ခုကို C# ကေနယူသံုးလုိ.ရသြားပါတယ္။ အဲဒီေတာ့ Project တစ္ခုမွာ programmer ေတြဟာ ၾကိဳက္တဲ့ language နဲ.သုံုးလုိ.ရသြားပါတယ္။

**Execution Environment for Ruby, Python, PHP**

ကဲဒီတမ်ိဳးကေတာ့ Interpreter ေတြသံုးတယ္ ဗ် သူတုိ.က source code ကုိဖတ္တယ္ ၿပီးတာ့ အထဲမွာ memory ေပၚမွာပဲ intermediate representation ေဆာက္ၿပီးေတာ့ အဲဒီအေပၚမွာ ပဲ Instruction ေတြ ကို execute လုပ္ပါတယ္ ။ VM ေတြနဲ.ကြာတာက သူတုိ.ဟာ byte code ကုိတုိက္ရုိက္ run ရတာမဟုတ္ပဲ source code ကုိ parse လုပ္ syntax error ေတြဘာေတြစစ္ အဲလုိလုပ္ၿပီးေတာ့မွ run ရတာပါ။ အဲေတာ့ ဘာၿဖစ္လဲဆုိေတာ့ မမွားတဲ့ line ဆီမေရာက္မခ်င္း run လုိ.ရပါတယ္ မွားတဲ့ line ေရာက္သြားရင္ ရပ္ေပ့ါ။ ဒါေၾကာင့္တခါတေလ ဒီလုိ language မ်ိဳးေတြကုိ safety critical application ေတြမွာမသံုးၾကပါဘူး ။ Static Language ေတြမွာ syntax error, ေနာက္ တၿခား semantic error အားလံုး မွန္ပါမွ Compile လုပ္လုိ.ရပါတယ္ အဲဒီေတာ့ error ကုိ program မ run ခင္ၾကိဳသိႏုိင္တာေပါ့ ။ Dynamic language ေတြၿဖစ္တဲ့ Ruby, Python,PHP က်ေတာ့အဲလိုမဟုတ္ဘူး line အားလံုး မမွန္လဲ Interpret လုပ္လုိ.ရတယ္ မမွန္တဲ့ line ဆုိ ရပ္သြားလိ့မယ္။ ဘာလုိ. နာမည္ၾကီးလာတာလဲေမးရင္ေတာ့ သူတုိ.ေတြက သင္ရတာလြယ္တယ္ ခု ေနာက္ပုိင္း Ruby ဆုိပိုဆုိးတယ္ သင္ရတာ Language syntax က တၿခား Language ေတြထက္နားလည္ရလြယ္ပါတယ္။ ဒါေၾကာင့္ metasploit ကို Ruby နဲ.ေရးထားတာၿဖစ္ပါတယ္။ Performance အေနနဲ.ေၿပာရရင္ေတာ့ Interpreter တုိ.ဟာ ေနာက္ဆံုးမွာပါ။ Compiled and native language ေတြၿဖစ္တဲ့ C, C++ က အၿမန္ဆံုးၿဖစ္ပါလိမ့္မယ္။ ၿပီးေတာ့ VM သံုးတဲ့ Language ေတြကေတာ့ အလယ္ေပါ့။ ေနာက္ဆံုးမွာေတာ့ Interpreter ေတြရိွတယ္ေပါ့ဗ်ာ။

ဆက္ပါဦးမယ္

Comments and Feedback မ်ားေမ်ာ္လင့္ေနပါတယ္ ေဆြးေႏြးမဲ့သူေတြကုိဖိတ္ေခၚပါတယ္

Ref - https://www.facebook.com/thet.khine.587/posts/10210002576900538