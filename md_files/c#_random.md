## Randon number
[Back to Mainp page](https://github.com/Dokidok1/new1000)

### *This lecture will teach how to generate a random number within a given range*

the source found be found **[here](https://stackoverflow.com/questions/2706500/how-do-i-generate-a-random-int-number)**

* There are two method I use a lot 
  * random.next()
  * guild.newguild()
  
 ### *random.next()*
 
 ```c#
 internal static class RandomNumber
{
    private static Random r = new Random();
    private static object l = new object();
    private static Random globalRandom = new Random();
    [ThreadStatic]
    private static Random localRandom;
    public static int GenerateNewRandom(int min, int max)
    {
        return new Random().Next(min, max);
    }
    public static int GenerateLockedRandom(int min, int max)
    {
        int result;
        lock (RandomNumber.l)
        {
            result = RandomNumber.r.Next(min, max);
        }
        return result;
    }
    public static int GenerateRandom(int min, int max)
    {
        Random random = RandomNumber.localRandom;
        if (random == null)
        {
            int seed;
            lock (RandomNumber.globalRandom)
            {
                seed = RandomNumber.globalRandom.Next();
            }
            random = (RandomNumber.localRandom = new Random(seed));
        }
        return random.Next(min, max);
    }
}
```


### *guild.newguild()*

```
public int GenerateRandom(int min, int max)
{
    var seed = Convert.ToInt32(Regex.Match(Guid.NewGuid().ToString(), @"\d+").Value);
    return new Random(seed).Next(min, max);
}
```

[Back to Mainp page](https://github.com/Dokidok1/new1000)

[last page](https://github.com/Dokidok1/new1000/blob/master/md_files/c%23_class.md)

[next lecture](https://github.com/Dokidok1/new1000/blob/master/md_files/recursion.md)
