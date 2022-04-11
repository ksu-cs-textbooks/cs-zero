---
type: "reveal"
hidden: true
---

<section>
    <h3>Problem Statement</h3>
    <p style="font-size: 55px">Write a program to print the sum of the first <code>n</code> prime numbers, where <code>n</code> is provided as input from the user. </p>
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
    n = positive_input()
<br>
main()
</code></pre>
</section>

<section>
	<h3>Prime Numbers</h3>
    <pre><code style="font-size: 40px; line-height: 45px" class="language-python stretch">def is_prime(n):
</code></pre>
</section>

<section>
	<h3>Prime Numbers</h3>
    <pre><code style="font-size: 40px; line-height: 45px" class="language-python stretch">def is_prime(n):
    for i in range(2, n):
</code></pre>
</section>

<section>
	<h3>Prime Numbers</h3>
    <pre><code style="font-size: 40px; line-height: 45px" class="language-python stretch">def is_prime(n):
    for i in range(2, n):
        if n % i == 0:
            # i equally divides n
</code></pre>
</section>

<section>
	<h3>Prime Numbers</h3>
    <pre><code style="font-size: 40px; line-height: 45px" class="language-python stretch">def is_prime(n):
    for i in range(2, n):
        if n % i == 0:
            return False
    # what if we don't return false?
</code></pre>
</section>

<section>
	<h3>Prime Numbers</h3>
    <pre><code style="font-size: 40px; line-height: 45px" class="language-python stretch">def is_prime(n):
    for i in range(2, n):
        if n % i == 0:
            return False
    return True
</code></pre>
</section>

<section>
	<h3>Main Function</h3>
    <pre><code style="font-size: 40px; line-height: 45px" class="language-python stretch">def main():
    n = positive_input()
    count = 0
    i = 2
    sum = 0
    while count < n:
        if is_prime(i):
            sum = sum + i
            count = count + 1
        i = i + 1
    print("The sum of the first {} prime numbers is {}".
           format(n, sum))
</code></pre>
</section>

<section>
	<h3>Full Program</h3>
    <pre><code style="font-size: 25px; line-height: 27px" class="language-python stretch">def positive_input():
    x = int(input("Enter a positive integer: "))
    while x <= 0:
        print("Invalid input!")
        x = int(input("Enter a positive integer: "))
    return x
<br>
def is_prime(n):
    for i in range(2, n):
        if n % i == 0:
            return False
    return True
<br>
def main():
    n = positive_input()
    count = 0
    i = 2
    sum = 0
    while count < n:
        if is_prime(i):
            sum = sum + i
            count = count + 1
        i = i + 1
    print("The sum of the first {} prime numbers is {}".format(n, sum))
<br>
main()
</code></pre>
</section>

<section>
	<h3>Testing</h3>
	<ul>
	    <li>Main Function</li>
		<li>Prime Function</li>
	</ul>
	<br><br>
	<p style="font-size: 60px;" class="fragment">2 + 3 + 5 + 7 + 11 + 13 + 17 + 19 + 23 = 100</p>
</section>

<section>
	<img class="stretch plain" src="/images/lab12/output6.png">
</section>