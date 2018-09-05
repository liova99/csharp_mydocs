# jagged array kata

[codewars](https://www.codewars.com/kata/cure-cancer/train/java)

Now you are a doctor.

You are working with a patient's **body** which has many cells.

The patient's body is a matrix where every row represents a cell.

Each cell contains just uppercase and lowercase letters,

and every cell in the body should be the same.

Oh no! It seems that one of the cells have mutated!

It is your job to locate the mutation so that the chemo specialists can fix it!

return the location [i,j] within the matrix...

before it's too late! :(

example:

```
cellscellscellscodecodecells
cellscellscellscodecodecells
cellscellscellscodecodecells
cellscellscellscodecodecells
cellscellscellscodecodecells
cellscellscellscodecodecells
cellscellscellscodecodecells
cellscellscellscodecodecells
cellscellscellscodecodecells
cellscellscellscodecadecells <- here it is! [9, 20]
cellscellscellscodecodecells
cellscellscellscodecodecells
cellscellscellscodecodecells
cellscellscellscodecodecells
```

no bodies will have less than 3 cells.

if the diagnose was a false alarm, return an empty array.



```c#
import java.util.Arrays;

class JomoPipi {
    public static int[] mutationLocation(char[][] body) {
        for (int x = 1 ; x < body.length ; x++)
            if (!Arrays.equals(body[0], body[x]))
                for (int y=0 ; y < body[0].length ; y++)
                    if( body[0][y] != body[x][y]) {
                        if (x>1) return new int[] {x,y};
                        else     return new int[] {Arrays.equals(body[0], body[2]) ? 1:0, y};
                    }
        return new int[0];
    }
}
```









