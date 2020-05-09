## Recurssion
[Back to Main page](https://github.com/Dokidok1/new1000)

*This lecture will teach the basic **recursion** we might be use in our c# projects, the source could be found in [here](https://code-maze.com/csharp-basics-recursion/)*

* the recursion could be used in the following situation
   * calculates the sum of all the numbers from n to m recursively
   * Create an application which prints out how many times the number can be divided by 2 evenly
 
### *calculate the sum of all the number from n to m*

```c#
public static int CalculateSumRecursively(int n, int m)
    {
        int sum = n;
 
        if(n < m)
        {
            n++;
            return sum += CalculateSumRecursively(n, m);
        }
 
        return sum;
   }
 
    static void Main(string[] args)
    {
        Console.WriteLine("Enter number n: ");
        int n = Convert.ToInt32(Console.ReadLine());
 
        Console.WriteLine("Enter number m: ");
        int m = Convert.ToInt32(Console.ReadLine());
 
        int sum = CalculateSumRecursively(n, m);
 
        Console.WriteLine(sum);
 
        Console.ReadKey();
    }
```

### *Create an application which prints out how many times the number can be divided by 2 evenly*
```c#
 public static int CountDivisions(double number)
    {
        int count = 0;
 
        if(number > 0 && number % 2 == 0)
        {
            count++;
            number /= 2;
 
            return count += CountDivisions(number);
        }
 
        return count;
    }
 
    static void Main(string[] args)
    {
        Console.WriteLine("Enter your number: ");
        double number = Convert.ToDouble(Console.ReadLine());
 
        int count = CountDivisions(number);
        Console.WriteLine($"Total number of divisions: {count}");
 
        Console.ReadKey();
    }
```
** This is the illustration of how does recursion works**
![recursion](https://github.com/Dokidok1/new1000/blob/master/images/34-RecursionGraph.png)


[Back to Main page](https://github.com/Dokidok1/new1000)

[last lecture](https://github.com/Dokidok1/new1000/blob/master/md_files/c%23_random.md)

[back to poforlio](https://github.com/Dokidok1/new1000/blob/master/md_files/me.md)
