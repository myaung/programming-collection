## How Operating System work - for dummies pov

OS ဆုိတာက Computer Science မွာ most complex software ပါပဲ။အဲ့ေတာ့သူ.ရဲ. function ေတြလုပ္ပံုေတြကို တခုခ်င္းဆီလိုက္ေရး ရင္ေတာ့ ႏွစ္ေပါက္ပါလိမ့္မယ္။အကုန္ေရးႏုိင္စြမ္းလဲ မရိွပါဘူး။ ဒါေပသိ dummy point of view လုိ.ဆုိေတာ့ နည္းနည္းပဲေပါ့။

OS ဆုိတာ ဘာလဲဆုိေတာ့ ကြန္ပ်ဴတာတလံုးမွာ မရိွမၿဖစ္ ပါရမဲ့ software ေပါ့။ ၿမင္သာေအာင္ေၿပာရရင္ Window, Linux , Mac ဆုိတာေတြက OS ေတြပါပဲ။ တခုနဲ.တခုေတာ့မတူၾကေပမဲ့ OS တခုခ်င္းဆီ ေပးရတဲ့ service ေတြ လုပ္ပံုကိုင္ပံုေတြကေတာ့ အေတာ္ဆင္ၾကပါတယ္။ OS ကိုဘာလုိ.သံုးရလဲဆုိေတာ့ User program နဲ. Hardware ၾကားမွာ interface (ၾကားခံအေနနဲ.သံုးတာေပါ့)။ User program ဆုိတာ OS ေပၚမွာ run လို.ရသမွ် program ေတြေပါ့။ ဥပမာ word processing ေတြ , compiler ေတြ JVM ေတြ browser ေတြေပါ့။ ဆုိခ်င္တာက အဲ့ဒီ user program ေတြ run လို.ရေအာင္ managment ေတြ process managmenet , memory management, IO management, hardware management အစရိွတာေတြကို OS ကလုပ္ေပးရပါတယ္။

ၿမင္သာေအာင္ေၿပာရရင္ဟုိး ေအာက္ဆံုးမွာ hardware ရိွတယ္။ သူ.အေပၚမွာ OS က run တယ္။ OS အေပၚမွာမွ ေစာနက user program ေတြသည္ run တယ္။ OS ကိုေလ့လာမယ္ဆုိရင္ hardware architecture ေတြကိုေသခ်ာနားလည္ရပါမယ္။ ဥပမာ Intel ကထုတ္တဲ့ CPU ေတြက နားလည္တဲ့instruction set နဲ. တၿခား CPU ေတြရဲ. Instruction set မတူပါဘူး။ OS ေတြက user program ေတြမွာ ပါတဲ့ machine code instruction ေတြကို CPU ေပၚမွာတင္ၿပီးေတာ့ run ေပးတယ္ manage လုပ္ေပးတယ္ အဲ့အလုပ္ေတြကိုလုပ္ရတာပါ။

သူူ.ရဲ. Major function ေတြကေတာ့ဒါေတြပါပါတယ္

 - Process Management  
 - Main Memory Management  
 - File Management  
 - I/O System Management  
 - Secondary Management  
 - Protection System  
 - Interprocess Communication  
 - Networking

အဲ့တာေတြပါရတယ္။

**Process Management**  
Process ဆုိတာ computer ေပၚမွာလက္ရိွ run ေနတဲ့ Program ကိုဆုိလိုတာ။ Process တခု run ေတာ့မယ္ဆုိရင္ OS ကေန အဲ့ဒီ process ကို run ႏုိင္ေအာင္ memory ေပၚေခၚတင္ရမယ္ အဲ့ေတာ့ ပထမဆံုးသူကို Hard disk ကေန လွမ္းဖတ္မယ္။ ဘာနဲ.ဖတ္မလဲဆုိေတာ့ File management module သံုးၿပီးဖတ္ရတယ္။ ေကာင္းၿပီ ဥပမာ JVM run ေတာ့မယ္ဆုိပါစုိ.ဒါဆုိ အရင္ဆံုး JVM ၿဖစ္တဲ့ java.exe ကို hard disk ကေန လွမ္းဖတ္ဖုိ. File management ကိုေၿပာရတယ္။ File management ကေန တဆင့္ ဒီ java.exe ကေတာ့ harddisk ရဲ. ဘယ္ေနရာမွာရိွတယ္ ဘယ္ sector ဘယ္ track မွာရိွတယ္ဆုိတာကိသိတယ္။ ဖတ္ေတာ့မယ္ဆုိရင္ hard disk ရဲ. device driver ကိုလွမ္းခုိင္းတယ္။ ဒါသည္ IO management ကလုပ္တာ။အဲ့ေတာ့ ခုနက CPU ကဖုိင္ကို လွမ္းဖတ္ဖုိ. ေခၚေတာ့ နဂိုမူလက run ေနတဲ့ code ေလး ခနရပ္ၿပီးေတာ့ user mode ကေန kernel mode ကို ေၿပာင္းရတယ္။ User mode ဆုိတာ user program ေတြပဲ run လို.ရတယ္။ Hardware ကိုလွမ္းထိန္းတာ ဘာညာလုပ္လုိ.မရဘူး အဲ့ေတာ့ kernel mode ကိုေၿပာင္းတယ္။အဲ့ကေန hard disk ကေန file ကို ဖတ္ပါၿပီတဲ့။ ဒါဆုိရင္ ခုနက java.exe process သည္ ခနရပ္သြားမယ္ ဘာလို.ရပ္လဲဆုိေတာ့ IO သည္ ၾကာတယ္ CPU သည္ ၿမန္ေတာ့ ေစာင့္ေနရမယ္။ ဒါဆုိရင္ CPU သည္ ဘာမွမလုပ္ပဲထုိင္ေစာင့္ေနရမလားေပါ့.။ ဘယ္ဟုတ္မလဲ java.exe မဟုတ္ပဲ တၿခား run လို.ရတဲ့ process ေတြကို ဆက္ run ရမွာေပါ့။ ဒါဆုိဘယ္ေကာင္ကို. run ရမလဲ ဘယ္သူ.အလွည့္က်သလဲ ဒါကိုက်ေတာ့ process management ထဲက scheduling ကိုၾကည့္ၿပီးေတာ့ဆံုးၿဖတ္တယ္။ အဲ့လုိမွမဟုတ္ရင္ multiple process ေတြ run ေနၿပီး တေယာက္ကေတာ့ run ရတယ္ ေနာက္တေယာက္ကေတာ့ မ run ရမၿဖစ္ေအာင္ ခုနက scheduling algorithm ေတြနဲ.ထိန္းၿပီ။

အုိေက ဒါဆုိ ခုနက Process ေလး ရပ္ IO ေစာင့္ေနတုန္းမွာတၿခား process ေလး run မယ္ဒါဆုိ ခုနက run ဖုိ.အလွည့္က်တဲ့ process ေလးကို memory ေပၚမွာရိွၿပီးသားဆုိရင္ ၿပန္ယူယံုပဲ။ ဒါဆုိ ရင္ process switchingလုပ္ၿပီ။ Process တခုရဲ. state ကို သိမ္း တၿခား Process state တခုကို OS ကCPU register ေတြမွာတင္ၿပီး run ၿပီ ။အ ဲ့အပို္င္းေတြကို Process management ကလုပ္ရတယ္။

Process တခုသည္ သူ.ေနရာနဲ.သူ memory မွာေနရာယူရတယ္ ဘာလုိ.လဲဆိုေတာ့ တေယာက္နဲ.တေယာက္ overwriting ေတြ မၿဖစ္ေအာင္ရယ္ securityဘက္က protection ရေအာင္ရယ္ကာထားတာ။ အဲ့လို process တခုက memory address တခုထုတ္ေပးရင္ ဒါသည္ relative address ပဲ သူ.ကို hardware physical adress ၿဖစ္ေအာင္ေၿပာင္းရတယ္။ အဲ့တာသည္ memory manageemnt ကလုပ္ရတယ္။ ဒါနဲ. Memory ေလးက တင္ထားတာ 4GB ရယ္ ။မဆန္.ေတာ့ရင္ေရာ OS ကဘာလုပ္ေပးလဲ အဲ့တာဆုိရင္ OS က main memory ေပၚမွာ မဆန္.တာေတြကို physical memory (harddisk ေပါ့ဗ်ာ)သံုးၿပီး တင္ထားရတယ္။ ဒါဆုိရင္ ဘယ္ေကာင့္ကိုက် memory ေပၚမွာထားၿပီး ဘယ္ေကာင့္ကို harddisk physical memory မွာသိမ္းမလဲဆုိတာကိုက်ေတာ့ Algorithm ေတြသံုးၿပီးတြက္တယ္ေပါ့ဗ်ာ။ ခနခန သံုးတဲ့ေကာင္ေတြကုိေတာ့ သိမ္းထားမယ္ အသံုးနည္တးဲ့ေကာင္ေတြကိုေတာ့ ေြရ.ၿပစ္မယ္ေပါ့။

ဒီအခ်ိန္ ဟုိဘက္က IO ၾကီးက ၿပီးသြားၿပီ java.exe ၿပီးသြားၿပီဆုိရင္ ဘာလုပ္လဲဆုိေတာ့ hardrware ကေန trapလုပ္လုိက္တယ္။ အဲ့မွာ OS ကေန သိသြားၿပီး။ ဟ IO ေတာ့ၿပီးၿပီဆုိၿပီးေတာ့ ခုနက java.exe ကို memory ေပၚတင္လို.ရၿပီဆုိပါစို. သူ.ကိုrun ဖုိ. process အသစ္ create လုပ္ၿပီးေတာ့ runတယ္။ အဲ့မွာ တခ်ိဳ. process ေတြသည္ thread ေတြပါ run လို.ရတဲ့အတြက္ thread management ကိုလဲ OS ကလုပ္ေပးရေသးတယ္။ အဲ့လို JVM run ေနရင္းနဲ. java program ကေန file တခုကို ဖတ္ခ်င္ၿပီဆုိပါစုိ.။ဒါဆုိ Java class ကေန native C prgoram ကိုေခၚတယ္ ။C program exe code ကေန OS ရဲ. file ဖတ္တဲ့ system call ကိုလွမ္းေခၚတယ္။ System call ဆိုတာ OS ကေန user program ေတြသံုးလုိ.၇ေအာင္ ေပးထားတဲ့ API call ေတြပါပဲ။ window မွာဆုိ widow API ေပ့ါ.

အဲ့လို ဖုိင္ ဖတ္ေနရင္းနဲ. ဖိုင္ ကို write ပါလုပ္မယ္ေပါ့။ဒါဆုိ တၿခား process တခုခုက ဒီ file ကို ဖတ္ေနႏုိင္တယ္။ အဲ့လို မၿဖစ္ေရေအာင္ lock ခ်ရတယ္။ အဲ့ေတာ့ တေယာက္က write ေနရင္ ေနာက္တေယာက္က write ေတြ read ေတြ မၿဖစ္ေအာင္ ကာရတယ္။ အဲ့လိုကာရင္းနဲ. Process အခ်င္းခ်င္း မီးပြိဳင့္မွာ သူ.လဲ လမ္းမေပး ကို.လဲလမ္းမေပးပဲနဲ. ကားေတြ ေရွ.ဆက္တုိးလို.မရသလို deadlock ေတြ မၿဖစ္ေအာင္လဲ ထိန္းရေသးတယ္။ File ရိုက္တာေတြဘာေတြကေတာ့ IO Management နဲ. File Management ကလုပ္တယ္။

ေနာက္ ခုနက process တခုက file ကို ရိုက္ေနတုန္းဆုိရင္ ေနာက္တေယာက္က ေစာင့္ေနရတယ္။ ေကာင္းၿပီ ၿပီးသြားရင္ေရာ ဘယ္လုိအသိေပးလဲ ။ ဒါကိုက်ေတာ့ Process အခ်င္းခ်င္း communicate လုပ္ရတယ္။ တုိက္ရိုက္ commmunicate မလုပ္ၾကပဲနဲ. message passing နဲ.ပဲလုပ္ၾကတယ္။ Message passing ကဘာလဲဆုိေတာ့ ကိုပို.ခ်င္တဲ့ information ကို mail box လို central data ထဲထဲ့လိုက္တာပဲေပါ့။ အဲ့လိုမဟုတ္ပဲနဲ. TCP/IP networking ကိုသံုးၿပီးေတာ့လဲ process အခ်င္းခ်င္း communicate လုပ္ၾကတာလဲရိွေသးတယ္။Process intercommunication ကိုေတာ့Interprocess Communication ဆုိတဲ့ module ကေနလုပ္တယ္။

TCP/IP networking ကေတာ့ ဆုိ္င္ရာnetworking module ကလုပ္တယ္။ Security နဲ. Accounting moduleလဲရိွေသးတယ္။ ေတာ္ေသးဘီ

Notes : OS ဆိုတာ SE တတ္ရင္ေရးလို..ရတယ္ဆုိတာေတြ.လို. အံ့ၾသလို.ေရးလိုက္တာ။

