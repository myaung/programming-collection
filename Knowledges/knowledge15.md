# Zero in programming languages

Zero ဆုိတာ သုညေပါ့ဗ်ာ။ ဘာလုိ. 0 အေၾကာင္းရွည္ရွည္ေ၀းေ၀းေၿပာလဲဆုိေတာ့ မသိတာေတြရိွမယ္ထင္လုိ.ေပါ့ဗ်ာ။ သိတယ္ဆုိလဲေက်ာ္သြားေပါ့။ သခ်ာၤမွာ သုညဆုိတာ sign မရိွဘူးဆုိၿပိးသံုးၾကပါတယ္။ Programming က သခ်ာၤမဟုတ္ေတာ့ zero က programming language အကုန္လံုးနီးပါး တိတိက်က်ေၿပာရရင္ floating point represenation ကုိ IEEE 754 format ကုိလုိက္နာ.တဲ့ language မွန္သမွ်မွာ သံုးမ်ိးရိွတယ္လုိ.ေၿပာရမွာပါ။ 

အဲ့ေကာင္ေတြက ေတာ့

integral type zero ဒါကေတာ့ရိုးရုိး floating point (float,double) မဟုတ္တဲ့ zero ေပါ့.  
positive floating point zero (0)  
negative floating point zero (-0)

အဲ့ေတာ့ negative zero ဆုိတာရိွတယ္လို. ေၿပာခ်င္တာပါ။ ဥပမာ ေအာက္က JavaScript code ကို run ရင္

    var a = -0;  
    console.log(1/a);

-Infinity ဆုိၿပီးထြက္မွာပါ ဘာလုိ.လဲဆုိေတာ့ a က negative zero ၿဖစ္ေနလို.ပါပဲ။ Positive zero နဲ. negative zero ဘာကြာလဲဆုိေတာ့ math operation ေတြလုပ္တဲ့ေနရာမွာ sign အေပၚမူတည္တဲ့ operation ေတြဆုိ effect ရိွပါတယ္။ ခုနက အေပၚက example လို.ေပါ့ Infinity မထြက္ဘူး -Infinity ထြက္မယ္။ ဒါေပမဲ့ ဘယ္ language မွာပဲၿဖစ္ၿဖစ္ positive zero နဲ. negative zero ကုိညီသလားစစ္ရင္ေတာ့ ညီတယ္ဆိုတဲ့အေၿဖပဲရမွာပါ။

Java C# မွာဆုိရင္ေတာ့ integer type (int,long etc) 0 ကို number တခုခုနဲ.စားရင္ division by zero error exception မ်ိဳးတတ္ပါတယ္။ Floating point zero ကုိ စားရင္ေတာ့ Infinity ,Minus Infinity တခုခုထြက္ပါတယ္။

ေအာက္က Java code ကုိ

    double b = -0;  
    System.out.println(1/b);

run မယ္ဆုိရင္ Infinity ရမွာပါ။ -Infinity မဟုတ္ပါဘူး။ C# မွာလဲဒီလိုပါပဲ။ ဘာလုိ.လဲဆုိေတာ့ Java C# compiler က optimization လုပ္လုိ.ပါပဲ။ zero အေရွ.မွာ negation ခံလဲ zero ပဲဆုိၿပီး compiler ကေန bytecode ထုတ္တဲ့ေနရာမွာ — ကိုၿဖဳတ္ပစ္ပါတယ္။ ဒါ့အၿပင္ သူတုိ. byte code မွာ load_zero ဆုိတဲ့ opcode ပဲရိွပါတယ္။ load_negative_zero ဆုိတဲ့ opcode မရွိပါဘူး။ ဒါဆုိရင္ခုနက code ကိုဒီလိုၿပန္ေရးရင္ေရာ။

    double b = 0;  
    System.out.println(1/-b);

-Infinity ထြက္ပါလိမ့္မယ္။ ဒါက ေတာ့ expression ထဲမွာၿဖစ္ေနတဲ့အတြက္ negation ကုိလုပ္သြားတာပါ။

Python Ruby PHP တုိ.မွာေတာ့ number တခုခုကို zero နဲ.စားရင္သူတုိ.က divide by zero error exception ကိုပဲၿပပါလိ့မ္မယ္။

Ruby ရဲ. negative zero ကုိ represent လုပ္ပံုသတ္မွတ္ပံုကေတာ့ ဂဏာန္းတလံုးဟာ negative ၿဖစ္မယ္ သူ.တန္ဖုိးက floating point အေနနဲ. represent လုပ္ဖုိ.ေသးလြန္းမယ္ဆုိရင္ negative zero နဲ.သတ္မွတ္ပါတယ္။

ဒီေနရာမွာ တခုသတိထားရမွာက floating point computation ေတြဟာ သခ်ာၤလိုအတိအက် မတြက္ႏိုင္ဘူး floating pointer number ေတြကို computer ကတိတိက်က် ကြက္တိ represent မလုပ္ႏုိင္ဘူးဆုိတာေပါ့။

ဘာေၾကာင့္ programming language ေတြမွာ negative zero positive zero ေပးထားရသလဲဆုိေတာ့ တခ်ိဳ. computation ေတြမွာ approximation နဲ.ပိုနီးစပ္တဲ့အတြက္ (ေသခ်ာေအာင္ထပ္ရွင္းရရင္ limit ေတြပါလာမွာ)ထဲ့ေပးထားရတာပါ။

ဒါေၾကာင့္ ဒီ language လဲ for do while ေနာက္ langauge လဲ for do while တူတူပါပဲကြာ ဆုိတာ မတူဘူး လို.ခနခနေၿပာရတာေပါ့ဗ်ာ။

ကဲဘာပဲၿဖစ္ၿဖစ္ zero အေၾကာငး္နားလည္ေတာ့ နည္းလား
