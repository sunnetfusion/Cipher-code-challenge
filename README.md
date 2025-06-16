Explanation: How the Code Works
Goal:
To reverse a permutation cipher applied to fixed-size blocks of a message string using a known key.

Step-by-step:
Understand the Key:

key = [2, 0, 3, 1] tells us how the original characters were shuffled into the encoded block.

For example, in an original block abcd, if key = [2, 0, 3, 1], then:

'a' goes to index 2

'b' goes to index 0

'c' goes to index 3

'd' goes to index 1

We reverse this to place characters back to their original positions.

Block Processing:

Split the message into blocks using key.length.

For each block, reverse the permutation using the key.

Reversing Logic:

Use an original[] array to place each character from the encoded block into the position defined by key.

original[key[j]] = block[j] reverses the shuffle.

Output:

Join the corrected blocks to form the full decoded message.
