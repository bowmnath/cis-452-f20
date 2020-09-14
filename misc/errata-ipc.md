In the lecture on POSIX shared memory,
I incorrectly assumed in one of my examples that the length returned by
`strlen` would include the NUL (`'\0'`) character.
That is not the case,
and it changes how far the pointer would move after writing in that example.
