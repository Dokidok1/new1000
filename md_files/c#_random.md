## Randon number
[Back to Mainp page](https://github.com/Dokidok1/new1000)

### *This lecture will teach how to generate a random number within a given range*

the source found be found **[here](https://stackoverflow.com/questions/2706500/how-do-i-generate-a-random-int-number)**

* There are two method I use a lot 
  * random.next()
  *guild.newguild()
  
 ### random.next()
 
 ```
 Random rnd = new Random();
int month  = rnd.Next(1, 13); 
int dice   = rnd.Next(1, 7);  
int card   = rnd.Next(52)
```


### guild.newguild()

```
public int GenerateRandom(int min, int max)
{
    var seed = Convert.ToInt32(Regex.Match(Guid.NewGuid().ToString(), @"\d+").Value);
    return new Random(seed).Next(min, max);
}
```

[Back to Mainp page](https://github.com/Dokidok1/new1000)

[next lecture](https://github.com/Dokidok1/new1000/blob/master/md_files/recursion.md)
