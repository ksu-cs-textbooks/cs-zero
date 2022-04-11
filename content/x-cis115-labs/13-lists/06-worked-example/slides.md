---
type: "reveal"
hidden: true
---

<section>
    <h3>Problem Statement</h3>
    <p style="font-size: 55px">Write a program to construct and print Pascal’s Triangle for a given number of rows. The user should be prompted to enter a positive integer indicating the number of rows, and if the user provides an invalid input the program should prompt for additional input until valid input is received.</p>
</section>

<section>
    <pre><code style="font-size: 70px; line-height: 75px" class="language-plaintext stretch">    1
   1 1
  1 2 1
 1 3 3 1
1 4 6 4 1
</code></pre>
</section>

<section>
	<h3>Handling Input</h3>
    <pre><code style="font-size: 40px; line-height: 45px" class="language-python stretch">def main():
<br>
main()
</code></pre>
</section>

<section>
	<h3>Handling Input</h3>
    <pre><code style="font-size: 40px; line-height: 45px" class="language-python stretch">def positive_input():
    x = int(input("Enter a positive integer: "))
    while x <= 0:
        print("Invalid input!")
        x = int(input("Enter a positive integer: "))
    return x
<br>
def main():
<br>
main()
</code></pre>
</section>

<section>
	<h3>Handling Input</h3>
    <pre><code style="font-size: 40px; line-height: 45px" class="language-python stretch">def positive_input():
    x = int(input("Enter a positive integer: "))
    while x <= 0:
        print("Invalid input!")
        x = int(input("Enter a positive integer: "))
    return x
<br>
def main():
    n = positive_input()
<br>
main()
</code></pre>
</section>

<section>
	<h3>Initial Setup</h3>
    <pre><code style="font-size: 40px; line-height: 45px" class="language-python stretch">def main():
    n = positive_input()
    row = [1]
    print(row)
</code></pre>
</section>

<section>
	<h3>Initial Setup</h3>
    <pre><code style="font-size: 40px; line-height: 45px" class="language-python stretch">def main():
    n = positive_input()
    row = [1]
    print(row)
    for i in range(1, n):
        # update row
        print(row)
</code></pre>
</section>

<section>
	<h3>Next Row</h3>
    <pre><code style="font-size: 40px; line-height: 45px" class="language-python stretch">def update_row(row):
</code></pre>
</section>

<section>
	<h3>Next Row</h3>
    <pre><code style="font-size: 40px; line-height: 45px" class="language-python stretch">def update_row(row):
    i = 0
    while i < len(row):
        # use list elements
        i = i + 1
</code></pre>
</section>

<section>
	<h3>Next Row</h3>
    <pre><code style="font-size: 40px; line-height: 45px" class="language-python stretch">def update_row(row):
    i = 0
    new_row = [1]
    while i < len(row):
        # use list elements
        i = i + 1
</code></pre>
</section>

<section>
	<h3>Next Row</h3>
    <pre><code style="font-size: 40px; line-height: 45px" class="language-python stretch">def update_row(row):
    i = 0
    new_row = [1]
    while i < len(row):
        new_row.append(row[i] + row[i + 1])
        i = i + 1
</code></pre>
</section>

<section>
	<h3>Next Row</h3>
    <pre><code style="font-size: 40px; line-height: 45px" class="language-python stretch">def update_row(row):
    i = 0
    new_row = [1]
    while i < len(row):
        new_row.append(row[i] + row[i + 1])
        i = i + 1
    new_row.append(1)
    return new_row
</code></pre>
</section>


<section>
	<h3>Final Program</h3>
    <pre><code style="font-size: 29px; line-height: 32px" class="language-python stretch">def positive_input():
    x = int(input("Enter a positive integer: "))
    while x <= 0:
        print("Invalid input!")
        x = int(input("Enter a positive integer: "))
    return x
<br>
def update_row(row):
    i = 0
    new_row = [1]
    while i < len(row):
        new_row.append(row[i] + row[i + 1])
        i = i + 1
    new_row.append(1)
    return new_row
<br>
def main():
    n = positive_input()
    row = [1]
    print(row)
    for i in range(1, n):
        row = update_row(row)
        print(row)
<br>
main()
</code></pre>
</section>

<section>
	<h3>Logic Error</h3>
	<img class="stretch plain" src="/images/lab13/error1.png">
</section>

<section>
	<h3>Logic Error</h3>
    <pre><code style="font-size: 40px; line-height: 45px" class="language-python stretch">def update_row(row):
    i = 0
    new_row = [1]
    while i < len(row):
        new_row.append(row[i] + <mark>row[i + 1]</mark>)
        i = i + 1
    new_row.append(1)
    return new_row
</code></pre>
</section>

<section>
	<h3>Logic Error</h3>
    <pre><code style="font-size: 40px; line-height: 45px" class="language-python stretch">def update_row(row):
    i = 0
    new_row = [1]
    while <mark>i < len(row) - 1</mark>:
        new_row.append(row[i] + <mark>row[i + 1]</mark>)
        i = i + 1
    new_row.append(1)
    return new_row
</code></pre>
</section>

<section>
	<h3>Logic Error Fixed!</h3>
	<img class="stretch plain" src="/images/lab13/output3.png">
</section>

<section>
	<h3>Final Program</h3>
    <pre><code style="font-size: 29px; line-height: 32px" class="language-python stretch">def positive_input():
    x = int(input("Enter a positive integer: "))
    while x <= 0:
        print("Invalid input!")
        x = int(input("Enter a positive integer: "))
    return x
<br>
def update_row(row):
    i = 0
    new_row = [1]
    while i < len(row) - 1:
        new_row.append(row[i] + row[i + 1])
        i = i + 1
    new_row.append(1)
    return new_row
<br>
def main():
    n = positive_input()
    row = [1]
    print(row)
    for i in range(1, n):
        row = update_row(row)
        print(row)
<br>
main()
</code></pre>
</section>