```C#
using System;


namespace myGists
{
    class Program
    {
        // This is a comment 
        public int[] BubbleSort(int[] myList)
        {
            
            int n = myList.Length-1;

            for (int i = 0; i < n; i++)
            {
                for (int j = 0; j < n; j++)
                {
                    if (myList[j] > myList[j + 1])
                    {
                        int temp = myList[j];
                        myList[j] = myList[j + 1];
                        myList[j + 1] = temp;

                    }
                }
            }
            
            return myList;
        }

        static void Main(string[] args)
        {
            Program bubble = new Program();

            int[] myList = { 1, 2, 5, 6, 4, 3 };
            int[] result =  bubble.BubbleSort(myList);

            Console.WriteLine(string.Join(",", myList));
            Console.WriteLine(String.Join(",",result));
            Console.ReadKey();

        }
        
    }
}
```

