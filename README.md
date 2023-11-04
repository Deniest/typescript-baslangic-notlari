
# Giriş

Merhaba sevgili arkadaşlar, bu yazdığım ilk şahsi yardımcı makalem ***(acemice olabilir)*** o yüzden bu makaleyi okurken bunları göz önünde bulundurmanızı tavsiye ederim.***Büyük oranda typescriptin resmi dökümantasyonundan ilerleyeceğim.***

Not: Makaleyi zaman buldukça güncelleyeceğim o yüzden sürekli gelişen ve hataların giderildiği bir yazı olacak.

Eğer makalemi beğendiyseniz ***star*** atabilirsiniz :)

Detaylara girmeden önce typescript hakkında ufak bir sözel detaylarına bakalım.

# Typescript Nedir? 

TypeScript, Microsoft tarafından geliştirilen bir programlama dili ve açık kaynak bir projedir. TypeScript, JavaScript tabanlı bir dil olup, JavaScript kodlarına tip güvenliği ekleyen, statik bir tip sistemine sahip bir dildir. JavaScript'in tüm özelliklerini içerir ve bu nedenle mevcut JavaScript projelerini kolayca genişletebilir veya geliştirebilirsiniz.

![Uygulama Ekran Görüntüsü](https://d2ms8rpfqc4h24.cloudfront.net/uploads/2021/12/Understand-Typescript.jpg)

Kullanım alanlarına ufaktan değinecek olursak typeScript, web uygulamaları, sunucu tarafı uygulamalar, oyun geliştirme ve daha birçok alanda kullanılabilir ve hızla gelişen bir dil olan TypeScript, geliştiricilere daha güvenli ve okunabilir kodlar oluşturma fırsatı sunar.

Typescript hakkında biraz bilgi edindiğimize göre biraz javascript hakkında bilgi edinelim çünkü typescripti daha iyi anlamamız için javascripti iyi anlamamız gerektiğine inanıyorum.

## Javascript(ECMAScript olarakta bilinir)
Javascript, java ile karıştırılmamalıdır. Javascript o zamanlarda Netscape'te ve şimdilerde Mozilla'da çalışan ***Brendan Eich*** tarafından 1995'in Mayısında 10 günde üretildi. Javascript her zaman Javascript olarak bilinmedi, orjinal adı Netscape'in kurucusu Marc Andreessen tarafından seçilen ***Mocha***ydı bla bla bla. Çok uzatmaya gerek yok bu bilgiler gerçek hayatta işimize yaramayacak sadece arkadaş çevresinde kullanılabilir

Daha önemli yerlere değinelim,

## ECMASCRIPT
ECMAScript, javascriptin temel belirtisini oluşturan ve dilin nasıl çalışması gerektiği konusunda rehberlik eden bir standarttır. Javascript bu standartı uygulayan bir dil olarak kabul edilir ve tarayıcılar ve diğer platformlar bu standarta uygun javascript motorlarını kullanarak javascript kodunu çalıştırırlar. 

## TypeScript'in Tür Atama Özelliği: Değişken Oluşturma ve Otomatik Tür Belirleme.
TypeScript, JavaScript dilini bilir ve birçok durumda türleri otomatik olarak oluşturur. Örneğin, bir değişken oluştururken ve ona belirli bir değer atarken, TypeScript bu değeri anlayacak ve tipini ona göre belirtecektir.

Örnek : 
```typescript
let selamDunya = "Selam Dünya"
//let selamDunya:string olarak typescript tarafından tip atanacaktır.
```

## TypeScript'te Tür Belirlemeleri
Özet: Bu rehberde, TypeScript'te tür belirlemeleri hakkında bilgi edineceksiniz.

TypeScript, değişkenler, fonksiyonlar, nesneler vb. gibi tanımlayıcılar için türleri açıkça belirtmek için tip belirteçlerini kullanır ve bu sayede program hataları önlenir.


TypeScript, tür belirlemesi olarak bir değişkenin sonrasında :type sözdizimini kullanır, bu tür herhangi bir geçerli tür olabilir, örnek olarak :
```typescript
let sayi:number 
let isim:string 
let obje:object 
```

Bir değişken bir türle belirtildiğinde, yalnızca o tür olarak kullanılabilir. Eğer değişken farklı bir tür olarak kullanılırsa, TypeScript derleyicisi bir hata verecektir. Örnek :

```typescript
let isim:string = "Can"
isim = 30 //Burada hata verecektir çünkü string tipine number atamaya calısıyoruz.
```

Bu kodu javascriptte yazsaydık herhangi bir hata almayacaktık.

## Sayılar (Numbers)
Bu bölümde typsecriptte kulanılan number tipine bakacağız

TypeScript'te "number" türü, sayıları temsil etmek için kullanılan bir veri türüdür. Bu tür, hem tam sayıları hem de ondalık (kayan noktalı) sayıları ifade eder. Yani, tamsayılar (örneğin, 42) ve ondalık sayılar (örneğin, 3.14) "number" türünün bir parçasıdır.


```typescript
let tamSayi: number = 42;
let ondalikSayi: number = 3.14;
```

"number" türü, matematiksel işlemler, hesaplamalar ve sayısal verilerle çalışmak için kullanılır. TypeScript'te, bu türün kullanılması sayıların türünün belirtilmesini sağlar. 
### Sekizlik Sayılar (Octal Numbers)

TypeScript'te "octal numbers," sekizlik sayıları ifade eder. Sekizlik sayılar, sekiz farklı rakamla (0-7) temsil edilir. Genellikle "0" öneki ile başlarlar. Örneğin, "034" bir sekizlik sayıdır.

Ancak TypeScript ve modern JavaScript dilinde, sekizlik sayıların kullanımı artık önerilmez ve büyük ölçüde terkedilmiştir. Sekizlik sayıları yerine ondalık (10 tabanında) sayılar veya hexadecimal (16 tabanında) sayılar kullanılması daha yaygındır.

Eski tarayıcılar ve JavaScript uygulamaları için uyumluluk nedeniyle bazı durumlarda hala sekizlik sayılarla karşılaşılabilir, ancak genel olarak bu tür kullanımı sınırlıdır ve modern TypeScript ve JavaScript kodlamalarında pek yaygın değildir.

```typescript
let sekizlikSayi: number = 0o10;
```

### Hexadecimal Sayılar (Onaltılık Sayılar)
16 farklı rakamla (0-9 ve A-F veya a-f) temsil edilen bir sayı sistemidir. TypeScript ve diğer birçok programlama dilinde, onaltılı sayıları ifade etmek için öneki "0x" veya "0X" kullanılır.
Örneğin, "0x1A" bir onaltılı sayıdır. Bu, onaltılı bir sayının ondalık eşdeğeri olan 26'ya karşılık gelir.
Onaltılı sayıların kullanımı özellikle bellek adresleri, renk kodları ve diğer özellikle sayısal değerlerle çalışırken yaygındır. Örneğin, HTML ve CSS'de renk kodları onaltılı formatta kullanılır (örneğin, "#FF0000" kırmızı rengi temsil eder).

Örnek TypeScript kullanımı:
```typescript
let onaltılıSayi: number = 0x1A; // "0x" ile başlayan bir değer onaltılı bir sayıyı temsil eder
```
Onaltılı sayılar, özellikle düşük seviyeli programlamada ve donanım etkileşimlerinde kullanılırlar, ancak günlük yazılım geliştirmelerinde daha az yaygın olarak karşımıza çıkarlar.

### Büyük Sayılar (Big Integers)

Büyük tam sayılar, 2^53 ve 1'den daha büyük olan tam sayıları temsil eder. sayının sonuna "n" karakterini ekleyerek oluşturulur. Peki neden böyle bir şey var ? 
bigInt, özellikle büyük ve hassas tam sayı işlemlerine ihtiyaç duyulan durumlarda işe yarar. 

Örnek:

```typescript
let büyükTamSayı: bigint = 9007199254740991n;
```

# String Nedir ? 
"string" ifadesi metin veya metin verilerini temsil eden bir veri türünü ifade eder. Bir "string" değişkeni, metinsel karakterlerin bir dizisini saklar, 
Peki bir stringi nasıl tanımlarız? ***" "*** çift tırnak veya tek tırnak ***' '*** veya ***` `**** içinde kullanarak metinsel ifademizi oluşturuabiliriz. Bir kaç örnek yapalım ve konu daha iyi anlaşılsın.

```typescript
let isim: string = "Can";
//Bu şekilde isim değişkeni oluşturduk ve tipini string değerinide "Can" olarak atadık.
//String Değerleri Kullanma:
//Şimdi "string" değişkeninizi kullanabilirsiniz. Örneğin, bir "console.log" ifadesi kullanarak değeri görüntüleyebilirsiniz:
console.log(isim);
//Ekran çıktısı : Can
```

### Stringleri birleştirme işlemleri : 
"string" verileri üzerinde çeşitli işlemler yapabilirsiniz. Örneğin, metin birleştirme (concatenation) işlemi yapabilirsiniz:
```typescript
let isim:string = "Can";
let soyisim: string = "Mert";
let tamAd: string = isim + " " + soyisim;
console.log(tamAd); // "Can Mert" şeklinde konsol çıktısını alacağız.
```

### Stringleri metodları : 
Metodlara bu bölümde deyinmeyeceğim çünkü yeni başladığınızı varsayıyorum ve yüzlerce metodu bir anda öprenmenizi istemiyorum o yüzden tek bir örnekle gideceğim.
Makalemin diğer bölümlerinde string metodlarına tamamen değieneceğim eğer dilerseniz o bölüme gidebilirsiniz.

Örneğin, bir metnin uzunluğunu öğrenmek için "length" özelliğini kullanabilirsiniz:

```typescript
let metin: string = "Merhaba, Dünya!";
let uzunluk: number = metin.length; //metin değişkeninin uzunluğunu almamıza yarayan property
console.log(uzunluk); // 13
```

Bir metod yapalım : 
```typescript
const orijinalMetin = "Can";
const tersCevir = orijinalMetin.reverse()
console.log(tersCevir) //Bu şekilde ekrana yazdırdığımızda "Nac" değerini alacağız.
//Reverse metodu anladığımız üzere değeri tersine çevirmeye yarayan bir string metodudur.
```
### String interpolasyon (String interpolations)
TypeScript ve diğer modern programlama dillerinde, bir string ifadesi içinde değişkenleri veya ifadeleri yerleştirmek için kullanılan bir tekniktir. TypeScript'te string interpolasyonu, template literals (şablon literal) olarak da adlandırılır ve genellikle `` (ters tırnak) karakterleri ile oluşturulur. Bu teknik, daha okunaklı ve esnek string oluşturmayı sağlar.

```typescript
const isim = "Can";
const yas = 24;

const mesaj = `Merhaba, benim adım ${isim} ve ${yas} yaşındayım.`;

console.log(mesaj);
// Çıktı: "Merhaba, benim adım Can ve 24 yaşındayım"

```

### String indeksleri
Bir stringin belirli karakterlerine erişmek için kullanılan bir işlemdir. Stringler, karakter dizilerinden oluşur ve her karakterin bir sırası (indeksi) vardır. Bu indeksleri kullanarak string içindeki belirli karakterlere veya alt dizilere erişebilirsiniz.

Peki bir metnin herhangi bir elemanına ulaşmak için nasıl bir yöntem izleriz? Örneklere  bakalım.

Mesela bir string içindeki belirli karaktere erişmek için indeks kullanabilirsiniz. İndeksler sıfırdan başlar ve 0, ilk karakteri temsil eder.
```typescript
const metin = "Merhaba, Dünya!";
const ilkKarakter = metin[0]; // İlk karakteri alır (M)
const ikinciKarakter = metin[1]; // İkinci karakteri alır (e)
console.log(ilkKarakter); // M
console.log(ikinciKarakter); // e
```
Bu şekilde metnin içindeki belirli karakterlere erişebildik.
Peki, ya birden çok karaktere erişmek istersem nasıl yapardım?
Çözümü basit, javascriptin içinde bulunan ve stringlere ait olan slice metodu ile bu sorunu çözebiliriz.

not: slice metodunun ayrıntısına metodlara özel yapılan bölümde değinilecektir.

```typescript
const metin = "Merhaba, Dünya!";
const altDizi = metin.slice(0, 7); // İndeks 0'dan başlayarak 7. indekse kadar olan karakterleri alır
console.log(altDizi); // "Merhaba"
```

### Tersten indeksleme 
Stringlerde negatif indeksler kullanarak sondan başlayarak karakterlere erişebilirsiniz. -1 son karakteri temsil eder.
```typescript
const metin = "Merhaba, Dünya!";
const sonKarakter = metin[metin.length - 1]; // Son karaktere erişir (a)
const sondanIkinciKarakter = metin[metin.length - 2]; // Sondan ikinci karaktere erişir (ı)
console.log(sonKarakter); // a
console.log(sondanIkinciKarakter); // ı
```
