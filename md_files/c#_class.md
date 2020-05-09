## C# class

### The complete toturial could be found in **[aa](https://www.tutorialspoint.com/csharp/csharp_classes.htm)** ![logo](https://www.tutorialspoint.com/csharp/images/logo.png)
 [Back to Mainp page](https://github.com/Dokidok1/new1000)

* Two items need to notice in this lectue
  * class
  * constructor
  
*The class in c# is not that hard as what it looks like, to define a class, just need to type the following code*

```

class Box {
      private double length;   // Length of a box
      private double breadth;  // Breadth of a box
      private double height;   // Height of a box
      
      public void setLength( double len ) {
         length = len;
      }
      public void setBreadth( double bre ) {
         breadth = bre;
      }
      public void setHeight( double hei ) {
         height = hei;
      }
      public double getVolume() {
         return length * breadth * height;
      }
   }
```

notice the class must be define within **namespace**



 [Back to Mainp page](https://github.com/Dokidok1/new1000)
 
 [next lecture](https://github.com/Dokidok1/new1000/blob/master/md_files/c%23_random.md)

