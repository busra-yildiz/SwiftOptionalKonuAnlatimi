# SwiftOptionalKonuAnlatimi
Swift dilindeki optional kavramını anlatalım. Swift, programlamanın hata yapma potansiyelini azaltmaya yardımcı olan 
güçlü bir güvenlik sistemine sahiptir ve "optional" (isteğe bağlı) bu sistemlerden biridir.

Optional Nedir?
Optional, Swift'te bir değişkenin veya sabitin değerinin olabileceği veya hiçbir değere sahip olmayabileceği anlamına gelir. 
Yani, bir optional değeri ya bir değere sahip olur ya da nil değerine sahiptir (hiçbir değer).

Optional, Swift'te birçok farklı durum için kullanılabilir, özellikle de bir değerin olup olmadığını belirsiz olduğu durumlarda 
veya bir değerin eksik olabileceği durumlarda.

Optional Nasıl Tanımlanır?
Optional bir değer tanımlamak için değer tipinin adının sonuna bir soru işareti (?) eklenir. Örnekler:
var yas: Int? // Bir optional tam sayı (Int)
var isim: String? // Bir optional dize (String)
Optional bir değişken veya sabit, ilk başta nil değerine sahiptir. Değere sahip olmadığınızda veya bilmediğinizde bu tür bir değer kullanışlı olabilir.

Optional Değerler Nasıl Kullanılır?
Optional değerleri kullanırken güvenli bir şekilde erişmelisiniz, çünkü optional bir değer nil (boş) olabilir. Optional değeri açmak için 
iki yaygın yol vardır: optional binding ve nil coalescing.

Optional Binding (İsteğe Bağlı Çözme): Optional değeri, değere erişmek ve kullanmak için güvenli bir yol sağlar. Bu, if let veya guard let 
ifadesi ile yapılır. Örnek:
var isim: String? = "John"

if let kullaniciAdi = isim {
    print("Kullanıcı adı: \(kullaniciAdi)")
} else {
    print("Kullanıcı adı yok.")
}
Nil Coalescing (Nil Birleştirme): Bu, optional değeri açmak yerine, optional değer nil ise varsayılan bir değeri kullanmanıza olanak tanır. 
?? operatörü ile yapılır. Örnek:
var isim: String? = nil
var varsayilanIsim = "Bilinmiyor"

let kullaniciAdi = isim ?? varsayilanIsim
print("Kullanıcı adı: \(kullaniciAdi)")

Optional Değerleri İşlerken Dikkat Edilmesi Gerekenler:

Optional değerleri güvenli bir şekilde açmalısınız, zorla açma (forced unwrapping) işlemlerinden kaçınmalısınız, çünkü bu tür işlemler 
değerin nil olma olasılığını göz ardı eder ve hata riski taşır.
Nil birleştirme (nil coalescing) gibi kullanışlı operatörleri kullanarak optional değerlerle çalışabilirsiniz.
Nil değerine sahip olabilen bir değeri optional olarak tanımladığınızda, programınızın daha güvenli ve hatasız olmasına yardımcı olabilirsiniz.
Swift'teki optional kavramı, özellikle değeri olmayan veya bilinmeyen durumları temsil etmek için güçlü bir araçtır ve Swift'in güvenli 
ve istikrarlı bir dil olmasına katkıda bulunur.
