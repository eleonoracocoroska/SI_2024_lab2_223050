Втора лабараториска по Софтверско Инженерство
Елеонора Чочороска,223050

2.Control Flow Graph

![hg](https://github.com/eleonoracocoroska/SI_2024_lab2_223050/assets/165606672/4840a0f5-fa49-4438-9d3a-4987d59812cf)


3.Цикломатска комплексност
М=Е-N+2P каде Е-број на рабови , N-број на јазли и P-број на поврзани компоненти 
М=48-40+2=10

4.Every Branch тест случаеви
Во првиот тест all items ќе биде null па ќе се фрли исклучок
Во вториот тест name=null и barcode=null тоагаш name=unknown а за barcode ќе се фрли исклучок
Во третиот тест name=item и barcode=012a тогаш name=item а за barcode ќе се фрли исклучок дека има невалиден карактер
Во четвриот случај name=item и barcode=0123 discount=0.5 и price=350 , payment=200 тогаш name=unknown а за barcode=0123 сумата ќе е 350*0.5=175 па ќе се намали за 30 и ќе биде 145 и е помал од payment па ќе врати true
Во петтиот случај name =item barcode=0123 discount =0 price=100 , payment=200 тогаш name=item barcode=0123 price=150 sum=150 , сумата е поголема од payment па ќе врати false

5.Multiple Condition
 if (item.getPrice() > 300 && item.getDiscount() > 0 && item.getBarcode().charAt(0) == '0')
 -Точно.точно,точно - price=350 , discount=0.5, barcode=0123 ќе врати точно
 -Точно,точно,неточно - price=350 ,discount=0.5 , barcode=012a последното е неточно па затоа ќе врати неточно
 -Точно,неточно,точно\неточно -price =350 ,dicscount=0, barcode нема ни да го гледа и ќе врати неточно
 -Неточно,точно\неточно,точно\неточно -price =100 ,dicscount и barcode нема ни да ги гледа и ќе врати неточно
 
