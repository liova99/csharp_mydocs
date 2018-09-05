```C#
 class BinarySearch
    {

        public int  Binary(List<int> myList,int myNumber)
        {

            int listLenght = myList.Count();
            int low = 0;
            int hight = listLenght;
            int middle = listLenght/2;

            int iterator = 0;

            while (iterator < 10)// for list smaller than 1000 int
            {
                if (myNumber == myList[middle])
                {
                    Console.WriteLine("index " + middle);
                    return myNumber;
                }
                else if(myNumber < myList[middle])
                {
                    hight = middle;
                    middle = (low + hight) / 2;

                }
                else // Mynum > middle
                {
                    low = middle;
                    middle = (low + hight) / 2;
                }
                iterator++;
            }

            return -1;
        }

    }
```

