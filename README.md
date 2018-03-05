# HP-67-97-Prime-Finder
A prime number finder written for the vintage HP 67 and HP 97 calculators. Now you can find primes like it's 1976!

## The hardware

This code is written for the HP-67 and HP-97 calculators. Both calculators are functionally equivalent, except the HP-97 has a thermal printer built in.

More information can be found on [Wikipedia](https://en.wikipedia.org/wiki/HP-67/-97) or at the [HP museum](http://www.hpmuseum.org/hp6797.htm).

## The algorithm

The code uses the basic [Trial Division](https://en.wikipedia.org/wiki/Trial_division) algorithm to find primes, with some basic optimisations applied: Only check odd numbers for primeness, and only search up to the square root of a number.

## Pseudocode:

Some pseudocode that I wrote before implementing the algorithm in plain 67/97 instructions.

I plan to make this more pseudo at some stage. It's probably pretty hard to understand unless you know how the reverse polish notation stack works on HP calculators.


```
A:
        let i = 1;
B:
        incriment i;
        let j = round(sqrt(i));
C:
        recall i;
        push x to y;
        recall j;
        divide;
        push x to y;
        get integer componant;
        subtract;
        if x == 0
                goto D;
        decriment j;
        goto C;
D:
        decriment j
             goto E;
        goto B;

E:
        recall i;
        print x;
        goto B;
```

## Video Demonstration:

Currently TODO. I own both of these calculators and plan to record a video demonstrating them in action. The HP-97 actually prints each prime to the thermal paper (instead of just to the screen), so it's quite impressive to watch.
