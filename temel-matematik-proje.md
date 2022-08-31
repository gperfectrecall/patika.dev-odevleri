# Matematik Proje Ödevi
## Mekansal Ağırlık Matrisi
Ekonometrinin özel bir alanı olarak ortaya çıkan mekansal ekonometri, gözlemler arasındaki mekansal ilişkilerin varlığını ve bunların ne kadar büyük olduğunu incelemektedir. Ağırlıklı olarak konut piyasası ve tarım arazileri üzerine yapılan çalışmalarda kullanılan bu yöntem, mekansal ağırlık matrisi verilen özel matrislerin oluşturulmasıyla mekansal ilişkinin varlığını ölçer. 

### Mekansal Ağırlık Matrisi Nasıl Oluşturulur?
Mekansal ilişkinin varlığının test edilmesinde gözlemler arasındaki komşuluk ilişkileri ve gözlemlerin birbirine olan yakınlığı ilk derecede önemlidir. $W$ değişkeni ile tanımlanan mekansal ağırlık matrisi, gözlemleri karşılayan $i$ ve $j$ değişkenlerini içeren $w_{ij}$ elemanlarını içerir. Burada $i$ ve $j$ değişkenleri arasındaki ilişkinin nasıl kurulmak istendiği matrisin elemanlarını belirler. 

Gözlemler arasındaki komşuluk ilişkisi ve bunlar arasındaki mesafeyi dikkate alan İki farklı mekansal ağırlık matrisi oluşturulabilir. GIS ArcView, GeoDa gibi programlar kullanılarak oluşturulan mekansal ağırlıklarla birlikte söz konusu komşuluklar ve iki gözlem arasındaki uzaklıklar kolaylıkla oluşturulabilmektedir. 

#### Komşuluk İlişkisine Göre Mekansal Ağırlık Matrisi 
Matris oluşturulurken komşuluk dikkate alınıyorsa bu durumda matris, $i$ ve $j$ değişkeninin komşu olduğu durumda matris elemanının 1 değerini alması, diğer durumda ise 0 değerini alması şeklinde oluşur. $n$ gözlem olduğu varsayılan bir matris $n*n$ boyutlarına sahip olur. Gözlemleirn satır ve sütunlara yerleştirildiği bu matriste, hangi gözlemler arasında komşuluk varsa o satır 1 değerini alır diğer bir deyişle. Satırlar standardize edilerek her bir satır için toplam rakamın 1 olması sağlanır. Böylece komşuluk ilişkisine sahip gözlemlerin ağırlıkları kesin olarak ortaya konur. 

#### Uzaklığa Göre Mekansal Ağırlık Matrisi
Uzaklık dikkate alınarak oluşturulan mekansal ağırlık matrisinde araştırmacının ölçmek istediği mekansal ilişkinin boyutuna bağlı olarak belirli bir uzaklığın seçilmesiyle elemanların oluşturulması mümkün olur. Çoğunlukla her bir gözlemin en az bir komşuluk ilişkisine sahip olacağı gözlemler arasındaki en düşük uzaklığa sahip olan mesafe seçilir. Burada matris elemanlarının oluşturulmasında mesafe belirlendikten sonra o mesafe ve altında kalan iki gözlem için matrise 1 değeri atanırken diğerleri için 0 değeri atanır. Yine benzer şekilde satır standardizasyonu yapılarak ağırlıklı ortalamalara sahip ağırlık matrisi oluşturulur. 

#### Mekansal Ağırlık Matrisleri Nasıl Kullanılır?
Mekansal ağırlık matrislerinin uzaklığa veya komşuluk ilişkilerine göre oluşturulmasının ardından mekansal ilişkinin ölçümünde mekansal regresyon aşamasına geçilir. Bu noktada mekansal lag modeli, mekansal error modeli gibi farklı modeller kullanılarak mekansal ilişkinin varlığı ve/veya ne düzeyde olduğu ortaya konur. En basit düzeyde tipik bir regresyon formülü içerisinde bu matris bir değişken olarak yerini alır ve böylece önündeki katsayı mekansal ilişkinin ne derecede anlamlı olduğunu gösterir. Bunlara ek olarak mekansal ilişkinin ortaya konmasında mekansal bağımlılığı gösteren Moran's $I$'s gibi ölçekler de kullanılır. 
