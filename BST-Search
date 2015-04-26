 // search işlevi, key değerine sahip elemanı bulup erişim bilgisini verir 
  public Node search(int key) { 
    return search(key,root);  // öz yinelemeli iç işlevi çağır 
  } 

  // parametrede verilen key değerine sahip elemanı, kökü t olan ağacın veya alt ağacın altında arar 
  // öz yinelemeli iç işlev, öz nitelik erişimi olmadığı için "static" 
  private static Node search(int key, Node t) { 
    if(t==null)                    // kök yoksa (bu alt ağaç boşsa), 
      return null;                 // bulamadık 
    else if(key<t.key)             // aranılan değer, kök elemanından küçükse 
      return search(key,t.leftChild);  // sol alt ağaçta ara 
    else if(key>t.key)             // aranılan değer, kök elemanından büyükse 
      return search(key,t.rightChild); // sağ alt ağaçta ara 
    else                           // aranılan değer, kök elemanından eşitse 
      return t;                    // bulduk: elemanın erişim bilgisini döndür 
  } 
  
  İkili arama işlemini gerçekleştiren yukarıdaki işlev ikili arama ağacının özelliğini kullanarak her defasında aranan 
  anahtar değerinin o anki elemandan büyük veya küçük olmasına göre ağacın sol tarafına veya sağ tarafına doğru arama 
  işlevini sürdürmektedir. Bu arama işlevinin kaç adımda sonlanacağının üzerinde işlem yapılan ikili arama 
  ağacının yapısına bağlı olduğuna dikkat ediniz. Eğer var olan ağacın dengeli bir yapısı varsa dizi üzerinde
  gerçekleştirilen ikili aramada olduğu gibi yine aynı nedenlerden dolayı arama işlevi başarılı veya başarısız
  durumda da log2(N+1) adımda sonuca ulaşacaktır. Ağacın dengeli bir yapıya sahip olması, kök elemanının sağında ve
  solunda yer alan alt ağaçların yüksekliklerinin birbirlerine yakın olması anlamına gelmektedir. 
  Dengeli ikili ağaç veri yapısı çok sık kullanılan bir veri yapısıdır. Dengeli ağaç yapısını oluşturmak için "ekleme" ve 
  "çıkarma" işlemleri sırasında çeşitli işlemlerle ağacın dengesinin bozulmamasını sağlayan algoritmalar
  geliştirilmiştir. Ancak bu algoritmaların verimsiz (log2N'den kötü) olması dengeli ağaç avantajını yok edecektir. 
  Bu avantajı da koruyabilmek için yapılan işlemler ise bu konudaki algoritmaları oldukça karmaşıklaştırmıştır.
  Sıradan bir ikili ağaçta ise bu denge ise ağaca yerleştirilen elemanların özelliğine göre değişecektir. 
  Örneğin elemanlar büyüklük sırasına göre yerleştirilirse oluşan ağaç sırasal bir yapıya sahip olacaktır.
  Aşağıdaki şekilde bu durum gösterilmiştir. Bu durumun oluşabilmesi için 1,2,3,4 elemanlarının sırayla ağaca 
  yerleştirilmesi gerekmektedir.Verilerin zaten sıralı olduğu durumda aşağıda da olduğu gibi yerleştirilen eleman 
  daha önceki elemanların tümünden büyük olacağı için daima ağacın en sağ tarafına yerleştirilecektir.
  Bu durum ikili arama ağacı için en kötü durum olarak karşımıza çıkmaktadır. Bu yapıya sahip bir ağaçta ise arama işlemi 
  sırayla arama (sequential search) yöntemiyle aynı performansa sahip olacaktır.
