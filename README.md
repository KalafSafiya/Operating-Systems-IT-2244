#!/bin/bash

# ----------------------------------------
# 1. Fibonacci Series
# ----------------------------------------
# Example Output: 0 1 1 2 3 5 8 13 21 34 55

echo "Fibonacci Series"
read -p "Enter the number: " num

a=0
b=1
for ((i=0; i<=num; i++))
do
  echo -n "$a "
  c=$((a + b))
  a=$b
  b=$c
done

echo -e "\n"  # New line for clarity

# ----------------------------------------
# 2. Factorial Calculation
# ----------------------------------------
# Example Output: Factorial of 5 is: 120

echo "Factorial Calculator"
read -p "Enter a number for factorial: " num

fact=1
for ((i=1; i<=num; i++))
do
  fact=$((fact * i))
done

echo "Factorial of $num is: $fact"
echo ""

# ----------------------------------------
# 3. Multiples of 3 between 1 and 50
# ----------------------------------------
# Example Output: 3 6 9 12 15 ... 48

echo "Multiples of 3 from 1 to 50 (Method 1)"
for ((i=1; i<=50; i++))
do
  if (( i % 3 == 0 )); then
    echo -n "$i "
  fi
done

echo -e "\n"

echo "Multiples of 3 from 1 to 50 (Method 2)"
for ((i=1; i<=50; i++))
do
  c=$((i * 3))
  if (( c <= 50 )); then
    echo -n "$c "
  fi
done

echo -e "\n"
