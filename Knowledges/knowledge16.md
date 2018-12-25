## How JavaScript + operator work

>ဘာရယ္မဟုတ္ဘူး ေရးသမွ်နားမလည္ဘူးဆုိလို. နားလည္လြယ္ေလာက္တဲ့အေပါင္းအေၾကာင္း ရွင္းမလားလုိ.။ နားလည္ၿပီးသားဆုိရင္လဲ ေက်ာ္သြားေပါ့ဗ်ာ။ 

JavaScript က အေပါင္းေပါ့ဗ်ာ။သူက Dynamic language ၿဖစ္ေလေတာ့ static language ကအေပါင္းေတြလို မရိုးဘူးဗ်။ ECMA specification အရဆုိရင္ေတာ့ JavaScript + operator သည္ semantic ၂မ်ိဳးရိွတယ္။   
 - string concatenation 
 - arithmetic addition

String concatenation က priority ပိုၿမင့္တယ္။ ဥပမာ a + b ဆုိတဲ့ expression ေပါ့. သူ.မွာ a ဒါမွမဟုတ္ b တခုခု ေသာ္လည္းေကာင္း ၂ ခုလံုးေသာ္လည္းေကာင္း string သုိ.မဟုတ္ string-like object ၿဖစ္မယ္ဆုိရင္ string concatenation ကိုလုပ္္မယ္။ 
  
```var result = 1 + 'Hello';```

 ဒီ expression မွာ result သည္ '1Hello' ဆုိတဲ့ *string* ရမယ္ ဘာလို.လဲဆုိေတာ့ operand တစ္ခုက Hello ဆုိတဲ့ string ၿဖစ္ေနလို. *string concatenation* ကုိလုပ္တယ္။ ဒီေနရာမွာ concatenation မလုပ္ခင္ 1ကုိ string အေနနဲ.ေၿပာငး္တယ္ ဘယ္လိုေၿပာင္းလဲဆုိရင္ *primitive to string convertion algorithm* ကုိသံုးၿပီးေၿပာင္းတယ္။ ၿပီးေတာ့မွ ရလာတဲ့ string '1' နဲ. 'Hello' ကို *concatenation* လုပ္ၿပီး string အသစ္ရတာ။ 

*Primitive to string convertion algorithm* အလုပ္လုပ္ပံုက ဒီလို။ undefined ဆုိရင္ "undefined" null ဆုိရင္ "null" boolean literal ဆုိရင္ value က true ၿဖစ္ေနရင္ "true" မဟုတ္ဘူးဆုိရင္ "false" Number ဆုိရင္ ToNumber conversion algorithm ကိုသံုး string literal ဆုိရင္ string ကုိပဲၿပန္၊ Object ဆုိရင္ ToPrimitive ကိုသံုးၿပီး primitive ေၿပာင္းၿပီးမွ ရလာတဲ့ primitive ကေန string ကိုေၿပာင္း အဲ့လိုေၿပာင္းရတယ္။ Object ကို string ေၿပာင္းရင္ valueOf ကိုအရင္ေခၚၿပီး primitive ကုိယူရတယ္ အဲ့ကေနမွ primitive တန္ဖုိးကို string ကုိေၿပာင္းတယ္။ ဥပမာ ေအာက္က Object ကို string ေၿပာင္းရင္ ဒီလိုရမယ္။ 

```var obj = { valueOf: function() { return 1; } }; console.log(obj+"Hello"); ```

console မွာ ေပၚမွာသည္ '1Hello' ဆုိတဲ့ string ၿဖစ္တယ္ ဘာလုိ.လဲဆုိေတာ့ Object ကို string ေၿပာင္းရင္ valueOf ကိုရွာတယ္ မရိွရင္ toString ကိုေခၚတယ္ သူကေနရလာတဲ့ ေကာင္ကိုမွ string ၿပန္ေၿပာင္းတယ္။ ဒီေနရာမွာ built in object ၿဖစ္တဲ့ Date က်ေတာ့ေၿပာင္းၿပန္ toString() ကုိေခၚတယ္ အဲ့ကေန string ကိုရမယ္။ အေပၚက ေကာင္က string concatenation အေၾကာင္းေၿပာတာ။ Arithmetic addition ကုိေတာ့ဒီလိုလုပ္တယ္။ Operand တခုခုသည္ string သုိ.မဟုတ္ string-like object မဟုတ္ေတာ့ဘဘူးဆုိရင္ ေအာက္က အဆင့္ေတြလုပ္၇တယ္။ Operand တခုခုသည္ object ၿဖစ္ေနရင္ object to primiitve conversion လုပ္ရတယ္။ ထြက္လာတဲ့ primitive type သည္ string ၿဖစ္ေနရင္ string concatenation ကုိလုပ္ၿပန္တယ္။ မဟုတ္ရင္ေတာ့ Object to primitive ကေနရလာတဲ့ ေကာင္ကို number ေၿပာင္းတယ္။ ဒီလိုဆင့္သြားမယ္။ 

```Object-> Object to primitive-> primitive to number ```

Object to primitive ကိုေၿပာင္းရင္ ပထမဆံုး object မွာ valueOf ကို သံုးတယ္။ valueOf မရိွမွသာ toString ကိုသံုးတယ္။ Date ကေတာ့သီးသန္. သူကေတာ့ toString ကုိသံုးၿပီး ေၿပာင္းမယ္။ ဒါေၾကာင့္ ဒီလို code ဆုိရင္။ `var result = new Date () +1;` Date သည္ Object အဲ့ေတာ့ object to primitive conversion လုပ္မယ္။ ဒါေပမဲ့သူက valueOf ကိုမေခၚဘူး valueOf ကုိေခၚ၇င္ number တခုရမယ္ ဒါေၾကာင့္ထြက္လာတာသည္ number ၿဖစ္မယ္။ Date က special ၿဖစ္ေနတဲ့အတြက္ toString() ကိုေခၚမယ္ ရလာတာသည္ string type ၿဖစ္မယ္။ ဒါေၾကာင့္ string concatenation ကိုလုပ္တဲ့အခါ ေအာက္က ေကာင္လုိရမယ္။ `Sun Nov 20 2016 21:53:49 GMT+0630 (Myanmar Standard Time)1` ဆုိၿပီး။ Array လိုေကာင္ေတြဆုိ [] empty arry ကို primitive ေၿပာင္းရင္ empty string ရမယ္။ empty string ကုိ number ေၿပာင္းရင္ 0 ၇မယ္။ ဒါေၾကာင့္ ေအာက္က ေကာင္ဆုိရင္ `var arr = []; var res = 1+ arr; console.log(res); console` သည္ 1 ရမယ္။ ေနာက္ array မွာ တကယ္လုိ. single element ပဲရိွမယ္ဆုိရင္ valueOf သည္ အဲ့ဒီ element string ေၿပာင္းထားတာရမယ္။ အဲ့ေတာ့ 

```var arr = [2]; var res = arr +1; console.log(res);```


 ဒီလိုုိဆုိရင္ 21 ရမယ္။ Object ေတြကုိ convert လုပ္လုိ.ရလာတဲ့ operand ေတြသည္ string type မပါခဲ့ရင္ primivite to number conversion ကုိလုပ္တယ္။ အဲ့ေတာ့ ေအာက္က code 

```var b = new Boolean(true); var res = 1+b; console.log(res); ```

ဆုိရင္ 2 ရမယ္ ဘာလုိ.လဲဆုိေတာ့ Boolean true ကို primitive conversion ေၿပာင္းရင္ valueOf ကိုေခၚမယ္ အဲ့က်ရင္ true ကို return ၿပန္မယ္။ ဒါဆုိ 1+b သည္ 1+ true ၿဖစ္သြားၿပီ။ true သည္ string မဟုတ္တာေၾကာင့္ primitive to number conversion ကုိေၿပာင္းရင္ 1 ရမယ္။ ဒါဆုိ `1+b = 1+true = 1+1 = 2` ေနာက္ဆံုးမွာ 2 ရမယ္။ တကယ္လုိ. prmitive ေတြကေန number ေၿပာင္းၿပီးရင္ + ကုိ number အတိုင္း IEEE addtition rule အတိုင္း ဆက္လုပ္လုိ.ရၿပီ။ 
 >နားလည္ၿပီဟု ထင္ေသာေၾကာင့္ေတာ္ေလၿပီ ဆက္ရွင္းရင္ေတာ့ က်န္ေသးသဗ်
