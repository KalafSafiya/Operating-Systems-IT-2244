Operating-Systems-IT-2244 Day 08
Day 08 Practical

SHELL SCRIPTING PRACTICE – Fibonacci, Factorial, and Multiples of 3
01. Fibonacci Series

read -p "Enter the number:" num
a=0
b=1
for ((i=0; i<=num; i++))
do
  echo $a
  c=$(($a + $b))
  a=$b
  b=$c
done

Sample Output:
Enter the number: 10
0
1
1
2
3
5
8
13
21
34
55


02. Factorial of a Number
Command:
read -p "Enter a number of fact:" num
fact=1
for ((i=1; i<=num; i++))
do
  fact=$((fact * i))
done
echo "Factorial of $num is" $fact

Sample Output:
read -p "Enter a number of fact:" num
fact=1
for ((i=1; i<=num; i++))
do
  fact=$((fact * i))
done
echo "Factorial of $num is" $fact

Sample Output:

Enter a number of fact: 5
Factorial of 5 is 120

03. Multiples of 3 Between 1 to 50

for ((i=1; i<=50; i++))
do
  c=$(($i % 3))
  if [ "$c" -eq 0 ]; then
    echo $i
  fi
done

Sample Output:

3
6
9
12
15
18
21
24
27
30
33
36
39
42
45
48








