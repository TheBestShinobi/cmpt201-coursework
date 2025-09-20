#include <stdio.h>
#include <unistd.h>

int main() {

  int pid;

  for (int i = 0; i < 10; ++i) {
    pid = fork();
  }

  printf("Your PID: %d\n", pid);

  if (pid == 0) {
    printf("You are the child!\n");
  }

  else if (pid == -1) {
    printf("Somethings wrong!!!!!!!\n");
  }

  else {
    printf("You are a parent!!\n");
  }
}
