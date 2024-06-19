```c
#include <stdio.h>
#include <sys/types.h>
int main() {
  u_int8_t *a1;
  u_int8_t **a2;
  u_int8_t ***a3;
  u_int8_t ****a4;

  printf("%ld %ld %ld %ld\n", sizeof(a1), sizeof(a2), sizeof(a3), sizeof(a4));
  printf("%ld %ld %ld %ld\n", sizeof(*a1), sizeof(**a2), sizeof(***a3),
         sizeof(****a4));

  u_int32_t *b1;
  u_int32_t **b2;
  u_int32_t ***b3;
  u_int32_t ****b4;

  printf("%ld %ld %ld %ld\n", sizeof(b1), sizeof(b2), sizeof(b3), sizeof(b4));
  printf("%ld %ld %ld %ld\n", sizeof(*b1), sizeof(**b2), sizeof(***b3),
         sizeof(****b4));

  return 0;
}
```

Output
```
8 8 8 8
1 1 1 1
8 8 8 8
4 4 4 4
```
