# Review of find_max

## Purpose
The function is intended to return the largest number in a list.

## Manual Trace
For the input:

find_max([3, 1, 9])

The list length is 3, so:

range(len(numbers) - 1)

becomes:

range(2)

This means the loop checks only:

- numbers[0] = 3
- numbers[1] = 1

It never checks numbers[2] = 9.

The function returns 3, but the correct result is 9.

## Bug
This is an off-by-one bug because the loop range is one element too short, causing the last element to be skipped.

There is also another edge-case bug. If the function receives an empty list, numbers[0] raises an IndexError.