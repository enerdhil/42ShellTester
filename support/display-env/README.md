# ./display_env

A binary that iterates on `**envp` and write each element on standard output.

```c
#include <unistd.h>
#include <string.h>
#include <stdio.h>

int main(int argc, char **argv, char **envp)
{
  (void)argc;
  (void)argv;
  int i = 0;
  write(1, "------------------------------\n", 31);
  while (envp[i])
  {
    write(1, envp[i], strlen(envp[i]));
    write(1, "\n", 1);
    i++;
  }
  write(1, "------------------------------\n", 31);
  printf("TOTAL ENVIRONMENT VARIABLES: %d\n", i);
  return (0);
}
```
