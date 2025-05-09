Merhabalar,
Elimden geldiğince Bus Jam'e benzetmeye çalıştım.
-Personların karşılarındaki değil en öndeki Busa binmesini sağlayamadım sadece karşılarındakilere biniyorlar.
-Level Editor'de save prototip halinde mevcut
-Personlar array ile atandı rastgele spawn olmuyorlar.
-Person ve bus prefablarını github'dan aldım öyle kullandım.
-Simulator -> İphone 12 Max'a göre yaptım oyunu runlarken hep o ekran üzerinde çalıştım.
-Personların box colliderı üst üste binmemesi için direkt kafalarının en üstüne basılırsa değil biraz daha alt kısma basılırsa click alınıyor. Bu nedenle scale'den arttırarak daha net clickler ile yaptım. Clicklenen bölge de console'da debug kullanarak printleniyor nereye tıklandığı. Eğer personun önünde bir başka person varsa ona çarpıp duruyor ve yürüyen halde kalıyor. Stuck oluyor iki karakter de.
Scene'ler ve genel özellikleri şu şekilde:

------------
Start Scene:
-Start Game ile GameScene'e Level Editor ile LevelEditorScene'e geçiş yapıyor.
------------
Game Scene:
-2D Array ile konum atadığım person prefablarını oluşturuyor.
-ObjectPooling yapmaya çalıştım
-Orta hattakiler karşısındaki en ön otobüse binip otobüsü götürebiliyor, ancak sol taraftakiler sadece önlerindeki otobüse 
(en öndeki otobüse değil) biniyor, sağdakiler ise yürümeye devam ediyor.
-Otobüse binen karakterler inactive moda dönüyor.
-Timer bittiğinde EndScene'e geçiş oluyor.
------------
Level Editor: 
-Add Bus tuşu ile sırayla otobüs ekleniyor
-Add person ile sırayla gride person ekleniyor.
-İstenilen yere eklenme mevcut değil sıra ile ekleniyor.
-Save Level tuşu .json olarak kaydetme mottolu ama şuan sadece debug ile level saved bilgisini console'da yazdırıyor, save yapmıyor.
-Main Menu tuşuyla StartScene'e dönüyor.
------------
End Scene: 
- Main Menu tuşuyla StartScene'e Level Editor tuşuyla LevelEditorScene'e dönüyor
-Try again tuşuyla GameScene'i tekrar çalıştırıyor.
