<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

   <h1>Proje 1 </h1>
   <p> <h3>[22, 27, 16, 2, 18, 6] <br>
    Sorting sıralama işlemidir. İlk elemandan ya da index 0 varsayalım. <br>
     index 0 daki eleman en küçük değer alacaktır. <br>
    Bunun için ilk olarak en küçük bulduğu değer ile index 0'daki değerin yerini değistirir. <br>
     Böylece index 0 da en küçük değer varken en küçük değerin çekildiği indexe de başlangıçtaki index 0'da rastgele bulunan değerimiz kaydedilir. 
    <br> Kısaca ilk değer en küçük değer ile yer değistirir. Sıra index 1'e yani ikinci elemana geçilir. İşlemler aynı mantık ile devam ettirilir.
    [22, 27, 16, 2, 18, 6] bize verilen sırasız dizide index 0 ile başlayalım.  <br>
    Dizide () içine alınacak değer en küçük olacak ve yer değiştirecektir.  <br>
      [22, 27, 16, <span style="color: red;">(2),</span> 18, 6]  <br>
          [2, 27, 16, 22, 18, 6] index 0 degerini aldı. Bunu yaparken n tane elemanın degerini kontrol!  <br>
            [2, 27, 16, 22, 18, <span style="color: red;">(6),</span>] Burada ikinci en küçük değer için n - 1 kontrol işlemi.  <br>
               [2, 6, 16, 22, 18, 27] index 1 değerini aldı.  <br>
                   [2, 6, <span style="color: red;">16</span>, 22, 18, 27] burada 3. eleman index 2 icin zaten en küçük degerdedir.  <br>
                      [2, 6, 16, 22, <span style="color: red;">(18)</span>, 27]  index 3 yani 4. eleman degerini alacaktır.  <br>
                          [2, 6, 16, 18, <span style="color: red;">(22)</span>, 27] index 4 için de değer en küçük olduğu için dizi sıralanmış oldu.  <br>
    
    <br>
    Big O gösterimi dizideki en küçük değer için n elemanlı dizide n tanesine tek tek bakacağı için n tane işlem yapılır. <br>
    <br> Artık 1. işlem yapıldı en küçük bulundu geriye kalanların en küçüğünü bulmak için yine tek tek bakar ancak 1. değer zaten bilindiği ve değerini aldığı için burada n - 1 tane kalan eleman arasından en küçüğe bakar. 
   <br> Dolayısıyla burda artık n - 1 işlem yapar. 3. eleman için n - 2, 4. eleman için n - 3 şeklinde gidilir. Son 1 eleman kalana kadar bu işlem devam edeceğinden Big O n + n - 1 + n - 2 + n - 3 + ... + 1 yani 1'den n'e kadar olan sayıların toplamıdır.  
    Bu da (n*n+1)/2 formülüne eşittir. Açarsak (n<sup>2</sup> + n)/2 den dominant n<sup>2</sup> olması sebebi ile
    O(n<sup>2</sup>)  Big O gösterimidir.</h3></p>
    
   <h3> Sıralanmış dizimiz [2, 6, 16, 18, 22, 27] Time Comp. için 18 sayısını <br>
    <br> 1. Avarage case ortada olması durumu ortalama olarak 18 elemanı 6 elemanın 4. elemanı olması sebebiyle avarage case girer.
    <br> 2. Worst case en kötü durum sonda olmasıdır ki 18 5 ve 6. eleman olmadığı için avarage daha yakındır.
   <br> 3. Best case en iyi durum olarak basta olmasıdır ki ballı diye tabir edebiliriz :) yani ilk sırada 18 4. eleman ilk sırada degil dolayısıyla Best case olamaz.
 <br>
   <br> [7, 3, 5, 8, 2, 9, 4, 15, 6]  
     <br> 1. Adım [2, 3, 5, 8, 7, 9, 4, 15, 6]  
       <br> 2. Adım [2, 3, 5, 8, 7, 9, 4, 15, 6] aynı kaldı çünkü en küçük yerinde zaten.  
          <br> 3. Adım [2, 3, 4, 8, 7, 9, 5, 15, 6]  
             <br> 4. Adım [2, 3, 4, 5, 7, 9, 8, 15, 6]  </h3>
    <br>
    <hr>
    <h1>Proje 2</h1>
    <h2>
    [16, 21, 11, 8, 12, 22]  <br>
    <img src="images/Notes_231006_004918.jpg" alt="">                
    
    <br>MergeSort için dizi önce ikiye parçalanır. Daha sonra parçalanan elemanlar tekrar ikiye parcalanır.
    <br> Bu parçalama eleman tek kalana kadar devam eder. 2'ye bölme işlemlerim bana logn sayısını ifade edecektir.
    <br> Birleşme işlemlerinde ise n tane elemanların kendi arasındaki küçüklüklerini okumam sebebi ile n işlem yapacağım.
    <br> Dolayısıyla Big O n*logn olacaktır. O(nlogn) olur.
</h2>
<hr>
<h1> Proje 3</h1>   
  <h2>  Binary Search Tree <br>
    [7, 5, 1, 8, 3, 6, 0, 9, 4, 2]   <br>
    root 6 alalım. <br>
    <img src="images/PENUP_20231005_231315.png" alt=""> 
    
    <br> root 6 sag agacında 8 var 6 dan buyuk 8 in iki childi var 7 küçük solunda 9 büyük sağında sağ taraf tamamlandı. 
   <br> Sol ağaçta 6 dan küçük ilk 4 aldık cünkü iki childın biri 4 den büyük 5 olacak peki küçük soluna ne yazzağım 2 cunku 2 nin childi büyügü 3 olacaktır. dolayısıyla 2 nin sagı 3 solu 1 kaldı ve tek elemanım 0 kaldı. o da 1 den küçük 1 in soluna aldım. böylelikle iyi bir agac dagıtımı yapmaya calıştık. 
</h2>
        
</body>
</html>
