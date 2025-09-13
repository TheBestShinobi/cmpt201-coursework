// Title: Lab 1
// Name: Mitchell Verma
// Date: Sept 13, 2025

#define _POSIX_C_SOURCE 200809L
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main() {
  char *buffer = NULL;
  char *savedptr;
  char *tokens;
  size_t size = 0;
  int error;

  // Get input from user
  printf("Please enter some text: ", stdout);
  error = getline(&buffer, &size, stdin);

  if (error == -1) {
    perror("getline failed");
    exit(EXIT_FAILURE);
  }

  // Tokenize the input
  tokens = strtok_r(buffer, " ", &savedptr);

  // Print out tokenized input
  printf("Tokens:\n", stdout);
  while (tokens != NULL) {
    printf("  %s\n", tokens);
    tokens = strtok_r(NULL, " ", &savedptr);
  }

  free(buffer);

  return 0;
}
