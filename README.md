## Signed ints

### Max function

```C
int max(int a, int b)
{
    const int BITSIZE_INT = ((sizeof(int) << 3) - 1));
    return a - ((a - b) & (a - b) >> BITSIZE_INT);
}
```

### Min function

```C
int min(int a, int b)
{
    const int BITSIZE_INT = ((sizeof(int) << 3) - 1));
    return b + ((a - b) & (a - b) >> BITSIZE_INT);
}
```

### Abs function

```C
int abs(int x)
{
    const int BITSIZE_INT = ((sizeof(int) << 3) - 1));
    return x + ((x * (x >> BITSIZE_INT)) << 1);
}
```
 
## Unsigned ints
