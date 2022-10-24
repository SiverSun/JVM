# JVM
Задача 1 (обязательная)
Просмотрите код ниже и опишите (текстово или с картинками) каждую строку с точки зрения происходящего в JVM

int i = 1;                      // 1
Создается переменная примитивного типа int и ей присваивается значение 1. Затем она помещается во фрейм main в Stack Memory.

Object o = new Object();        // 2
Создается ссылка o на объект Object. В heap выделяется память для объекта класса Object, а ссылка о помещается во фрейм main в Stack Memory

Integer ii = 2;                 // 3
Создается переменная ссылочного типа Integer ii и ей присаивается знаение 2. В heap выделяется память для объекта класса Integer, а ссылка ii помещается во фрейм main в Stack Memory

 printAll(o, i, ii);             // 4
 В Stack Memory создается новый фрейм для метода printAll и туда помещаются все его параметры: i, ii, o
 
 Integer uselessVar = 700;                   // 5
 Создается переменная ссылочного типа Integer uselessVar и ей присаивается знаение 700. В heap выделяется память для объекта класса Integer, а ссылка uselessVar помещается во фрейм main в Stack Memory
 
 System.out.println(o.toString() + i + ii);  // 6
 Вызывается метод печати toString для объекта o и переменных i и ii. В Stack Memory создается новый фрейм, куда передаются ссылки
  
  System.out.println("finished"); // 7
  В heap выделяется память для метода println со значением типа String "finished"
  Удаляется из памяти неиспользованная переменная uselessVar
