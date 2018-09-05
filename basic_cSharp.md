# C# Basics

### Visual Studio

ctrl +k, d = align The selectet code

### Compiling process

![1532025181121](C:\Users\levan\Dropbox\cSharp_docs\compiling)

> Photo [ Turing Informatik](https://www.youtube.com/channel/UCPOv6aROWBSxBNXXTDIHf2w)  



### Notes

**We used camelCase for the private fields and PascalCase for the public**

```c#
private string connectionString;
public  string ConnectionString
```







### Data types

The following table lists the available value types in C# 2010 −

| Type    | Represents                                                   | Range                                                   | Default Value |
| ------- | ------------------------------------------------------------ | ------------------------------------------------------- | ------------- |
| bool    | Boolean value                                                | True or False                                           | False         |
| byte    | 8-bit unsigned integer                                       | 0 to 255                                                | 0             |
| char    | 16-bit Unicode character                                     | U +0000 to U +ffff                                      | '\0'          |
| decimal | 128-bit precise decimal values with 28-29 significant digits | (-7.9 x 1028 to 7.9 x 1028) / 100to 28                  | 0.0M          |
| double  | 64-bit double-precision floating point type                  | (+/-)5.0 x 10-324 to (+/-)1.7 x 10308                   | 0.0D          |
| float   | 32-bit single-precision floating point type                  | -3.4 x 1038 to + 3.4 x 1038                             | 0.0F          |
| int     | 32-bit signed integer type                                   | -2,147,483,648 to 2,147,483,647                         | 0             |
| long    | 64-bit signed integer type                                   | -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 | 0L            |
| sbyte   | 8-bit signed integer type                                    | -128 to 127                                             | 0             |
| short   | 16-bit signed integer type                                   | -32,768 to 32,767                                       | 0             |
| uint    | 32-bit unsigned integer type                                 | 0 to 4,294,967,295                                      | 0             |
| ulong   | 64-bit unsigned integer type                                 | 0 to 18,446,744,073,709,551,615                         | 0             |
| ushort  | 16-bit unsigned integer type                                 | 0 to 65,535                                             | 0             |

ref [tutorialspoint.com](https://www.tutorialspoint.com/csharp/csharp_data_types.htm)

### Hello World
```c#
Console.WriteLine("hello World");
```

```c#
Console.ReadKey();
```

### Import from user

```c#
static void Main(string[] args)
        {
            string name;
            int age;

            Console.WriteLine("Your name is.. ");
            name = Console.ReadLine();

            Console.WriteLine("your age is.. ");
            // convert String to int
            age = Convert.ToInt32(Console.ReadLine());

            Console.WriteLine(" ");
            // for that the window will not closed
            Console.ReadKey();
        }
```

#### Convert import to int

```c#
age = Convert.ToInt32(Console.ReadLine());
```

###  Including variables within strings

```c#
string name = "Scott";
string output = String.Format("Hello {0}", name);

//Or directly pint it 

string name = "Leo";
Console.WriteLine("my name is {0}", name);
```

### Arrays

> When you know how many items will be in the array

#### Print an Array int[]

```c#
int[] array = new int[] { 1, 2, 3 };
foreach(var item in array)
{
    Console.WriteLine(item.ToString());
}
```

If you don't want to have every item on a separate line use `Console.Write`:

```c#
int[] array = new int[] { 1, 2, 3 };
foreach(var item in array)
{
    Console.Write(item.ToString());
}
```

or `string.Join<T>` (in .NET Framework 4 or later):

```c#
int[] array = new int[] { 1, 2, 3 };
Console.WriteLine(string.Join(",", array));
```

###  Jagged Arrays[][]

[docs.microsoft.com](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/arrays/jagged-arrays)

```c#
int jaggedArray = new int3;

jaggedArray[0] = new int[5];
jaggedArray[1] = new int[4];
jaggedArray[2] = new int[2];

//or
jaggedArray[0] = new int[] { 1, 3, 5, 7, 9 };
jaggedArray[1] = new int[] { 0, 2, 4, 6 };
jaggedArray[2] = new int[] { 11, 22 };

```



### ArrayList

```c#
using System.Collections; 

ArrayList arrayList = new ArrayList() { 100, "Two", 12.5, 200 };
```

More info [tutorialsteacher.com](http://www.tutorialsteacher.com/csharp/csharp-arraylist)


### Generic List \<T>

The List\<T> collection is the same as an ArrayList except that List\<T> is a generic collection whereas ArrayList is a non-generic collection. 

Example: Generic List\<T> Initialization



```c#
using System.Collections.Generic; // List

List<int> intList = new List<int>();

//Or

IList<int> intList = new List<int>();
```

#### length 

 ```C#
 int listLenght = myList.Count();
 ```

#### Accessing

```c#
int elem = intList[1];
```

More info [tutorialsteacher.com](http://www.tutorialsteacher.com/csharp/csharp-list)

#### ConvertAll() items of a List

```c#
List<String> lowerCase = alphaList.Select(x => x.ToLower()).ToList();
            List<String> lower = alphaList.ConvertAll(y => y.ToLower()).ToList();
```



### Looping

#### foreach

```C#
String alpha = "A B C D E F G H I J K L M N O P Q R S T U V W X Y Z";

public void myString()
        {
            foreach (var i in alpha)
            {
                if (i.ToString() != " "){

                    Console.Write(" \"{0}\", ", i);

                }
            }

        }

//Returns
"A",  "B",  "C",  "D",  "E",  "F",  "G",  "H",  "I",
 "J",  "K",  "L",  "M",  "N",  "O",  "P",  "Q",  "R",
"S",  "T",  "U",  "V",  "W",  "X",  "Y",  "Z",
```

or

```C#

myList.ForEach(Console.WriteLine);
```



### String to int

```c#
int numVal = Int32.Parse("-105");
Console.WriteLine(numVal);
// Output: -105
```

more [docs.microsoft.com](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/types/how-to-convert-a-string-to-a-number)

### Check DVD after debuging

i just disable DVD in the device manager. 

### print out n the debuging mode

```c#
using System.Diagnostics;

Debug.Print(myString);
```

[Stackoverflow](https://stackoverflow.com/questions/18871505/what-is-the-difference-between-debug-print-and-console-writeline-in-net)



### Properties / Get und set

Encapsulation means having one class hide information from another. It helps you prevent bugs in your programs  (C# 227)  

> And just like chess, there are an almost unlimited number of possible encapsulation strategies!    

**What fields require some processing or calculation to happen when they’re set?**
 Those are prime candidates for encapsulation. If someone writes a method later that changes the value in any one of them, it could cause problems for the work your program is trying to do. 

**Only make fields and methods public if you need to**

 **We used camelCase for the private fields and PascalCase for the public**

#### Farmer app example

we make a basic program 

```C#
private int numOfCows;

// we need 30bags of feed for each cow
public const int FeefMultiplier = 30;

// we add a method to give other classe a way to get the number of cows
public int GetNumberOfcows()
{
    return numberOfCows;
}

public void SetNumOfCows(int newNumberOfCows)
{
    numberOfCows = newNumberOfCows;
    // numOfCows is private, so camelCase
    BagsOfFeed = numOfCows * FeedMultiplier;
}
```

Then we use **Properties**, Properties make encapsulation easier.
You can use properties, which are methods that look just like fields to other objects. A property can be used to get or set a backing field, which is just a name for a field set by a property.

```c#
// This will become the backing field for the NumberOfCows
private int numberOfCows;

// Often we use properties by combining them with a normal field declaration.
public int NumberOfCows
{
/*	 	This is a get accessor. It’s a method that’s run any time
        the NumberOfCows property is read. It has a return value
        that matches the type of the variable—in this case it
        returns the value of the private numberOfCows property
*/    
    get
    {
    	return numberOfCows;
    }
/*		This is a set accessor that’s called every time the
        NumberOfCows property is set. Even though the method
        doesn’t look like it has any parameters, it actually has one
        called value that contains whatever value the field was set to.
*/
	set
    {
    	numberOfCows = value;
    	BagsOfFeed = numberOfCows * feedMultiplier
    }
	
}
```

You use get and set accessors exactly like fields. Here’s code for a button that sets the number of cows and then gets the bags of feed:    

```c#
private void button_Click(object sender, EventArgs e) {
    Farmer myFarmer = new Farmer();
    
/*  
        When this line sets NumberOfCows to 10, the
        set accessor sets the private numberOfCows field
        and then updates the public BagsOfFeed field.
*/    
    myFarmer.NumberOfCows = 10;
    
    //Since the NumberOfCows set accessor updated BagsOfFeed, now you can get its value.
    int howManyBags = myFarmer.BagsOfFeed;
/*    
            Even though the code treats NumberOfCows like a field,
            it runs the set accessor, passing it 20.
            And when it queries the BagsOfFeed field it runs 
            the get accessor, which returns 20*30=600.
*/
    myFarmer.NumberOfCows = 20;
    howManyBags = myFarme.BagsOfFeed;
}
```



### Add content of a CheckBox to a TextBox

```xaml
<CheckBox Checked="CheckBox_Checked" Content="Weld"/>
<TextBox x:Name="LengthTextBox" Padding="3"  Margin="0 0 0 10" />
```

```c#
 private void CheckBox_Checked(object sender, RoutedEventArgs e)
        {
            //           cast String, cast sender as CheckBox and take the content
            this.LengthTextBox.Text += (string)((CheckBox)sender).Content;
        }
```







