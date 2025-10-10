#include <stdint.h>
#include <stdio.h>
#include <stdlib.h>

struct header {
  uint64_t size;
  struct header *next;
  int id;
};

void initialize_block(struct header *block, uint64_t size, struct header *next,
                      int id) {
  block->size = size;
  block->next = next;
  block->id = id;
}

int find_first_fit(struct header *free_list_ptr, uint64_t size) {

  // Traverse the headers until there is a block with enough space
  struct header *curr = free_list_ptr->next;

  // Check if provided header is null
  if (curr == NULL) {
    return 1;
  }

  while (curr->next != NULL) {
    if (curr->size > size) {
      return curr->id;
    }
    curr = curr->next;
  }

  return -1;
}

int find_best_fit(struct header *free_list_ptr, uint64_t size) {
  int best_fit_id = -1;
  int prev_dif = -1;
  int difference = -1;

  // Traverse the list
  struct header *curr = free_list_ptr;
  while (curr->next != NULL) {
    // Check if current block size is closer to the desired
    // size than previously listed closest size
    difference = curr->size - size;

    // If current blk size better then save it
    if (difference < prev_dif && difference >= 0) {
      best_fit_id = curr->id;
    }

    // Update the prev_dif to be the current one and move to next blk
    prev_dif = difference;
    curr = curr->next;
  }

  return best_fit_id;
}

int find_worst_fit(struct header *free_list_ptr, uint64_t size) {
  int worst_fit_id = -1;
  int prev_dif = -1;
  int difference = -1;

  // Traverse the blocks in heap
  struct header *curr = free_list_ptr;
  while (curr->next != NULL) {

    // Check if current size is farther off than the previously
    // provided difference
    difference = curr->size - size;
    if (difference > prev_dif && difference >= 0) {
      worst_fit_id = curr->id;
    }

    // Update the prev_dif to be the current one and move to the next blk
    prev_dif = difference;
    curr = curr->next;
  }

  return worst_fit_id;
}

int main(void) {

  struct header *free_block1 = (struct header *)malloc(sizeof(struct header));
  struct header *free_block2 = (struct header *)malloc(sizeof(struct header));
  struct header *free_block3 = (struct header *)malloc(sizeof(struct header));
  struct header *free_block4 = (struct header *)malloc(sizeof(struct header));
  struct header *free_block5 = (struct header *)malloc(sizeof(struct header));

  initialize_block(free_block1, 6, free_block2, 1);
  initialize_block(free_block2, 12, free_block3, 2);
  initialize_block(free_block3, 24, free_block4, 3);
  initialize_block(free_block4, 8, free_block5, 4);
  initialize_block(free_block5, 4, NULL, 5);

  struct header *free_list_ptr = free_block1;

  int first_fit_id = find_first_fit(free_list_ptr, 7);
  int best_fit_id = find_best_fit(free_list_ptr, 7);
  int worst_fit_id = find_worst_fit(free_list_ptr, 7);

  // Print out the IDs
  printf("The ID for First-Fit algorithm is: %d\n", first_fit_id);
  printf("The ID for Best-Fit algorithm is: %d\n", best_fit_id);
  printf("The ID for Worst-Fit algorithm is: %d\n", worst_fit_id);

  return 0;
}

/*
// Assume we have the linked list of all free memory locations in heap
// with a newly freed block in the list
// handle merging free blocks in the linked list with 3 cases:
// 1. free block behind z
// 2. free block infront z
// 3. free block both behind and infront of z
//
//--------------------------------------------------------------------
//
// 1. Insert the newly freed block into head->next's position


// 2. Toggle bool variables if there is freed blocks behind or infront
// of the newly freed block


// 3. If there is only a free block behind, merge them

      // Increase the size of the newly freed block by the size of the        //
one behind it


      // Remove the block behind the newly freed one from linked list


// 4. If there is only a free block infront, merge them

      // Increase the size of the blk infront of the newly freed blk
      // by the size of the freed block


      // Remove the newly freed blk node from linked list


// 5. If there is free block behind and infront, merge both to
// the block infront

      // Increase the size of the blk infront of the newly freed
      // blk by the blk itself and the one behind it


      // Remove the newly freed blk and the one behind it

// 6. Else, if no blocks are free behind or infront of the newly
// freed block, do nothing
*/
