---
type: "reveal"
hidden: true
---

<section>
    <pre><code style="font-size: 35px; line-height: 40px" class="language-python stretch">def positive_input():
    x = int(input("Enter a positive integer: "))
    while x <= 0:
        print("Invalid input!")
        x = int(input("Enter a positive integer: "))
    return x
<br>
def main():
    x = positive_input()
    y = positive_input()
    while y <= x:
        for i in range(x - y):
            print("*", end="")
            y = y + 2
        print("")
    print("Complete!")
<br>
main()
</code></pre>
</section>

<section>
	<img class="stretch plain" src="/images/lab12/output2.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab12/output3.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab12/output4.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab12/output5.png">
</section>

<section>
    <pre><code style="font-size: 35px; line-height: 40px" class="language-python stretch">def positive_input():
    x = int(input("Enter a positive integer: "))
    while x <= 0:
        print("Invalid input!")
        x = int(input("Enter a positive integer: "))
    return x
<br>
def main():
    x = positive_input()
    y = positive_input()
    while <mark>y <= x</mark>:
        for i in range(<mark>x - y</mark>):
            print("*", end="")
            y = y + 2
        print("")
    print("Complete!")
<br>
main()
</code></pre>
</section>