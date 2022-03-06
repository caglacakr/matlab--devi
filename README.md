# matlab-homework
matlab-sf-59-examples


################ 3.1 ###################




>> a=24.4 * 365

a =

        8906

>> b=cos(pi/4)

b =

    0.7071

>> c= 45^(1/3)

c =

    3.5569

>> d=exp(-0.6)

d =

    0.5488
>> e=(4.6)^5

e =

   2.0596e+03

f=
>> syms i x
>> y=symsum((i^2-3),i,1,6)
 
y =
 
73


################ 3.2 ###################




a= Kayan noktalı değişkenler, yani tek veya çift üzerindeki hesaplamalar, bu değişkenlerin nasıl görüntülendiğine bakılmaksızın uygun kayan nokta kesinliğinde yapılır. Tamsayı değişkenleri üzerindeki hesaplamalar doğal olarak tamsayı olarak yapılır. Bu işlem için eps() komutu kullanılır.

b=Komut penceresinde kayan nokta hesaplamasının sonucunu görüntülemek için kullanılan varsayılan ondalık basamak sayısı hexadecimal'dirÖrneğin ; 400921fb54442d18 .

c= format short yolu ile farklı sayıda ondalık basamağa çevirebiliriz




################ 3.3 ###################





>> a=exp((sin(3*pi/4))^3-(log10(45.8))^(1.2))

a =

    0.2266
>> b=(345.88)^2-sqrt(4*(log10(45.8))+(sin(3*pi/4)))

b =

   1.1963e+05
>> c=(345.88-log10(45.8))/((sin(3*pi/4))+5*log10(45.8))

c =

   38.1980






################ 3.4 ###################




>> X=[4,5,1;0,2,4;3,4,1]

X =

     4     5     1
     0     2     4
     3     4     1

>> Y=[-7,6,-1;3,-2,0;13,-4,1]

Y =

    -7     6    -1
     3    -2     0
    13    -4     1

>> Z=[0,7,1;0,2,-5;3,3,-1]

Z =

     0     7     1
     0     2    -5
     3     3    -1

>> a=3*X+2*Y-Z

a =

    -2    20     0
     6     0    17
    32     1     6

>> b=X^2-Y^3

b =

   469  -366    73
  -204   214   -12
  -705   683   -58

 
>> c=X'*Y'

c =

   -31    12    55
   -27    11    61
    16    -5    -2

>> d=(X*Y)^(-1)

d =

    0.4444    0.0556   -0.5556
    3.6667    0.3333   -4.8333
   11.8889    1.1111  -16.1111
   
   
   

################ 3.5 ###################





a = log(x) , e tabanında doğal logaritma (ln) fonksiyonudur. 
    log10(x) , 10 tabanında logaritma fonksiyonudur.

b = rand(), 0 ile 1 arasında rastgele değerler döndürür. Rastgele değerler düzgün bir dağılım izler ve dolayısıyla ortalama değer 0,5 olur.
    randn() , -sonsuz ve +sonsuz arasında rastgele değerler döndürür. Rastgele değerler, ortalama değeri 0 ve standart sapması 1 olan normal bir dağılımı izleyecektir.

c = matris gücü

C = A^B, A'yı B gücüne hesaplar ve sonucu C'ye döndürür.

Öğe bazında güç

C = A.^B, A'nın her öğesini B'deki karşılık gelen güçlere yükseltir. A ve B'nin boyutları aynı veya uyumlu olmalıdır.


d = Çıkarma
C = A - B, karşılık gelen öğeleri çıkararak B dizisini A dizisinden çıkarır.
A ve B boyutları aynı veya uyumlu olmalıdır.

tekli eksi
C = -A, A'nın öğelerini olumsuzlar ve sonucu C'de saklar.




################ 3.6 ###################




lookfor fonksiyonu, MATLAB arama yolunda bulunan tüm M dosyalarındaki yardım metninin ilk yorum satırında (H1 satırı) dize konusunu arar.
Bir eşleşmenin gerçekleştiği tüm dosyalar için lookfor fonksiyonu, H1 satırını görüntüler.



Örneğin ;

 lookfor inverse 

"ters hiperbolik kosinüs", "iki boyutlu ters FFT" ve "sözde ters" içeren H1 çizgileri dahil en az bir düzine eşleşme bulur. 
Bunu şununla karşılaştır

which inverse 

yada 

what inverse

Bu işlevler daha hızlı çalışır, ancak MATLAB'ın ters bir işlevi olmadığı için muhtemelen hiçbir şey bulamaz.

Özetle, belirli bir dizindeki işlevleri listeleyen, belirli bir işlevi veya dosyayı içeren dizini bulan ve arayan, tüm dizinlerdeki belirli bir anahtar kelimeyle ilgisi olabilecek tüm işlevleri bulur.




################ 3.7 ###################





which fonksiyonu argüman fonksiyonu için tam yol adını görüntüler.Eğer bir fonksiyon 

MATLAB yolundaki bir M, P veya MDL dosyasındaki MATLAB işlevi veya Simulink modeli, ardından ilgili dosya için tam yol adını görüntüler.



Örneğin ;

Aşağıdaki ifade, pinv'nin MATLAB'ın matfun dizininde olduğunu gösterir.

which pinv
matlabroot\toolbox\matlab\matfun\pinv.m

MATLAB serial sınıf nesnelerinde kullanılan fopen işlevini bulmak için

which serial/fopen
matlabroot\toolbox\matlab\iofun\@serial\fopen.m  % serial method

Java Frame sınıfının nesnelerinde kullanılan setTitle yöntemini bulmak için öncelikle sınıfın MATLAB'a yüklenmesi gerekir. Sınıfın bir örneğini oluşturduğunuzda sınıf yüklenir:

frameObj = java.awt.Frame;

which setTitle
java.awt.Frame.setTitle  % Frame method

Bir hücre dizisini değişkene döndüren bir çıktı değişkeni belirttiğinizde. Tüm bağımsız değişkenleri parantez ve tek tırnak içine alarak işlev biçimini kullanmalısınız:

s = which('private/stradd','-all');
whos s
  Name      Size         Bytes  Class
  s         3x1            562  cell array
Grand total is 146 elements using 562 bytes

