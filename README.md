# Elixir List Modification Bug

This repository demonstrates an unexpected behavior when trying to modify a list within an `Enum.each` loop in Elixir.  Due to Elixir's immutable data structures, direct modification attempts fail to alter the original list.  The example illustrates this issue and provides a correct solution using `Enum.filter`.

## Bug

The `bug.ex` file contains code that iterates over a list and attempts to remove an element (3) if a condition is met.  However, because Elixir lists are immutable, the `List.delete` function creates a new list, leaving the original list unchanged.

## Solution

The `bugSolution.ex` file provides a corrected version of the code, utilizing `Enum.filter` to create a new list containing only the desired elements, effectively removing the element without attempting to modify the original list in place.