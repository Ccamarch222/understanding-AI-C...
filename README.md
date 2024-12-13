# Understanding-AI-C...
## Messages
parameter ail list hoti hai jisme har item aik dictionary hota hai.Har dictionary aik message ko represent karta hai jo conversation meain exchange ho rha hota hai. Har message ka do main hisay hote hain:
### 1. Role: 
ye bhtaata hai ke message kis ka taraf se hai.Ye**"system"**,**"user"**,** "assistant"** ho sakta hai.
 **System:**
messaage wo hota hai jo assistant ki persona ya behavior se karta hai.Matlab ye bataata hai ke assistant ko kis tarah se jawab dena chahiye.
**User:**
messages wo hotay hain jisme user apna sawal ya instruction deta hai.
**Assistant:**
message wo hote hain jo model ki taraf se diye gaye jawab hote hain.
### 2. Content:
ye wo text hota hai jo message ke andar diya gaya hota hai, jaise koi question ya instruction.

 Ye structured conversation history bohot zaroori hoti hai taake model ko har new request ka context samajh aaye. Isse model ko ye samahne mein madaf milti hai ke kis type ka jawab dena chahiye based on previous messages.
## Model
model parameter wo model specify karta hai jo app response genrate karne ke liy use karna chahte hain.
 Har model ki apni capabilities , strengths, our costs hoti hain.Is liye, shai model ka intekhab performance our cost optimization ke liye bohat zaroori hai.
 Misahl ke taur par,**gpt-3.5-turno** aik acha general-purpose model hai jo kaafi tasks handle kar sakta hai,Jabke dosser models kuch specific tasks mein behtar ho sakte hain,jaise creatibve writing ya complelx reasoning.

## Max Completion Tokens
parameter wo limit se karta hai jo model apne response mein genrate kar sakta har.
**Tokens**
wo chhoe tukde hote hai jo words ya unke hisso ko represent karte hain.Is parameter ki madad se genrate hone wale textki length ko control kar sakte hai.
Limit kam karne se response incomplete ho sakta hai .Or zada karne se unnecessarily ho shkta hai ,Jis se cost zayada kar sakta hai.

## n
**n** parameter ye determine karta hai ke API ek hi prompt ke liye kitne alag-alag respnses generate karegi.
Ager n=1  se karte hain, to sirf ek response milega.Agar n=3 to three response milen gean.is se alag-alag responses campare karke sabse bhtareen response choose kar sakte hain.

## Stream
parameter jab True set kiya jata hai,to API partial responses ko real-time mein genrate karte hue user ko bhejti hai.
Isse user ko interatice experience milta hai,kyunke wo response ko step-by-step dekh sakte hain jab wo generrate ho rha ho,iske bajaye ke poora responce complete hone ka wait karna pade.

## Temperature
parameter model ke output ki randomness ko control karta hai.
Agar temperature zada ho (e.g.,0.8), to  responses zada creative our unexpected hote hain.Jabke agar temperature kam ho (e.g.,0.2),to model ka jawab focused our predictable hota hai.Agar temperature 0 set kiya jaye,to model hamesha sabse zada probable token ko select karega.

## Top_P(Nucleus Sampling)
parameter,temperature sampling ka aik alternative hai.
Top_p wo chhoti set of tokens ko consider karta hai jinki cumulatice probility probability 'p' ko exceed karti hai.Isse model ka output zyada likely tokens par focus hota hai, lekin thodi si randommness bhi rehti hai.

## Tools
Ye hume external tools specify karne ka moka dete haim jo model apne response generate karne ke liye use kar skta hai.Misal ke taur pe, aap tools enable kar sakte hain jo search engine,specific code interpreter,ya database ko access kar sakein.Is se model ki capabilities expand hoti hain our ye apni initial training data se aage jakar information access our process kar sakta hai
