## C# class

 [Back to Main page](https://github.com/Dokidok1/new1000)

### The complete toturial could be found in **[here](https://www.tutorialspoint.com/csharp/csharp_classes.htm)** ![logo](https://www.tutorialspoint.com/csharp/images/logo.png)


* Two items need to notice in this lectue
  * class
  * constructor
  
*The class in c# is not that hard as what it looks like, to define a class, just need to type the following code*

```Live Demo
using System;

namespace BoxApplication {
   class Box {
      public double length;   // Length of a box
      public double breadth;  // Breadth of a box
      public double height;   // Height of a box
   }
   class Boxtester {
      static void Main(string[] args) {
         Box Box1 = new Box();   // Declare Box1 of type Box
         Box Box2 = new Box();   // Declare Box2 of type Box
         double volume = 0.0;    // Store the volume of a box here

         // box 1 specification
         Box1.height = 5.0;
         Box1.length = 6.0;
         Box1.breadth = 7.0;

         // box 2 specification
         Box2.height = 10.0;
         Box2.length = 12.0;
         Box2.breadth = 13.0;
           
         // volume of box 1
         volume = Box1.height * Box1.length * Box1.breadth;
         Console.WriteLine("Volume of Box1 : {0}",  volume);

         // volume of box 2
         volume = Box2.height * Box2.length * Box2.breadth;
         Console.WriteLine("Volume of Box2 : {0}", volume);
         Console.ReadKey();
      }
   }
}
```

notice the class must be define within **namespace**



 [Back to Main page](https://github.com/Dokidok1/new1000)
 [last lecture](https://github.com/Dokidok1/new1000/blob/master/md_files/me.md)
 
 [next lecture](https://github.com/Dokidok1/new1000/blob/master/md_files/c%23_random.md)

