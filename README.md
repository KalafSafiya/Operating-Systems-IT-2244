# Operating Systems IT 2244  
## Day 06 Practical  
**Date:** 04/04/2025  

---

### 1) Astrology Based on Life Path Number (Using `case`)

```bash
echo "Enter your birth date"
read date
a=$(($date % 10))
b=$(($date / 10))
c=$(($a + $b))

case $c in
    1) echo "Luck" ;;
    2) echo "Carefully do your work" ;;
    3) echo "Stronger" ;;
    4) echo "Happy" ;;
    5) echo "Can get help" ;;
    6) echo "Doubt" ;;
    7) echo "Sad" ;;
    8) echo "Like" ;;
    9) echo "Courage" ;;
    *) echo "Invalid Input" ;;
esac
```

---

### 2) Summation and Multiplication Using `for` Loop

```bash
sum=0
product=1

for x in 1 2 3 4 5
do
    sum=$(($sum + $x))
    product=$(($product * $x))
done

echo "Summation: $sum"
echo "Multiplication: $product"
```

---

### 3) Print Integers from 1 to 10 Using `while` Loop

```bash
count=1

while [ $count -le 10 ]
do
    echo $count
    count=$(($count + 1))
done
```

---

### 4) Pattern Printing Using Nested Loops

#### i) Increasing Stars

```bash
echo "Enter number of rows:"
read rows

for ((i = 1; i <= rows; i++))
do
    for ((j = 1; j <= i; j++))
    do
        echo -n "*"
    done
    echo ""
done
```

---

#### ii) Decreasing Stars

```bash
for ((i = 7; i >= 1; i--))
do
    for ((j = 1; j <= i; j++))
    do
        echo -n "*"
    done
    echo ""
done
```

---

#### iii) Repeating Row Numbers

```bash
for ((i = 1; i <= 6; i++))
do
    for ((j = 1; j <= i; j++))
    do
        echo -n "$i"
    done
    echo ""
done
```

---

#### iv) Increasing Number Sequence

```bash
for ((i = 1; i <= 6; i++))
do
    for ((j = 1; j <= i; j++))
    do
        echo -n "$j"
    done
    echo ""
done
```

---

#### v) Pyramid Star Pattern

```bash
echo "Enter number of rows:"
read rows

for ((i = 1; i <= rows; i++))
do
    for ((j = i; j < rows; j++))
    do
        echo -n " "
    done
    for ((k = 1; k <= i; k++))
    do
        echo -n "* "
    done
    echo ""
done
```
