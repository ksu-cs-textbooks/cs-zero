---
type: "reveal"
hidden: true
---
<section>
    <pre><code style="font-size: 30px; line-height: 40px" class="language-python stretch">def square_sum(one, two):
    one = one * one
    two = two * two
    total = one + two
    return total<br><br>
def main():
    text_one = input("Enter the first number: ")
    one = int(text_one)
    text_two = input("Enter the second number: ")
    two = int(text_two)
    total = square_sum(one, two)
    print("The sum of squares of {} and {} is {}".format(one, two, total))<br><br>
main()
</code></pre>
</section>
<section>
    <pre><code style="font-size: 30px; line-height: 40px" class="language-python stretch">def square_sum(one, two):
    <mark>one = one * one</mark>
    <mark>two = two * two</mark>
    <mark>total = one + two</mark>
    <mark>return total</mark><br><br>
def main():
    text_one = input("Enter the first number: ")
    one = int(text_one)
    text_two = input("Enter the second number: ")
    two = int(text_two)
    total = square_sum(one, two)
    print("The sum of squares of {} and {} is {}".format(one, two, total))<br><br>
main()
</code></pre>
</section>
<section>
    <pre><code style="font-size: 30px; line-height: 40px" class="language-python stretch">def square_sum(one, two):
    <mark>return (one * one) + (two * two)</mark><br><br>
def main():
    text_one = input("Enter the first number: ")
    one = int(text_one)
    text_two = input("Enter the second number: ")
    two = int(text_two)
    total = square_sum(one, two)
    print("The sum of squares of {} and {} is {}".format(one, two, total))<br><br>
main()
</code></pre>
</section>
<section>
    <pre><code style="font-size: 30px; line-height: 40px" class="language-python stretch">def square_sum(one, two):
    return (one * one) + (two * two)<br><br>
def main():
    <mark>text_one = input("Enter the first number: ")</mark>
    <mark>one = int(text_one)</mark>
    <mark>text_two = input("Enter the second number: ")</mark>
    <mark>two = int(text_two)</mark>
    total = square_sum(one, two)
    print("The sum of squares of {} and {} is {}".format(one, two, total))<br><br>
main()
</code></pre>
</section>
<section>
    <pre><code style="font-size: 30px; line-height: 40px" class="language-python stretch">def square_sum(one, two):
    return (one * one) + (two * two)<br><br>
def main():
    <mark>one = int(input("Enter the first number: "))</mark>
    <mark>two = int(input("Enter the second number: "))</mark>
    total = square_sum(one, two)
    print("The sum of squares of {} and {} is {}".format(one, two, total))<br><br>
main()
</code></pre>
</section>
<section>
    <pre><code style="font-size: 30px; line-height: 40px" class="language-python stretch">def square_sum(one, two):
    return (one * one) + (two * two)<br><br>
def main():
    one = int(input("Enter the first number: "))
    two = int(input("Enter the second number: "))
    <mark>total = square_sum(one, two)</mark>
    print("The sum of squares of {} and {} is {}".format(one, two, <mark>total</mark>))<br><br>
main()
</code></pre>
</section>
<section>
    <pre><code style="font-size: 26px; line-height: 40px" class="language-python stretch">def square_sum(one, two):
    return (one * one) + (two * two)<br><br>
def main():
    one = int(input("Enter the first number: "))
    two = int(input("Enter the second number: "))
    print("The sum of squares of {} and {} is {}".format(one, two, <mark>square_sum(one, two)</mark>))<br><br>
main()
</code></pre>
</section>
<section>
    <pre><code style="font-size: 26px; line-height: 40px" class="language-python stretch">def square_sum(one, two):
    return (one * one) + (two * two)<br><br>
def main():
    one = int(input("Enter the first number: "))
    two = int(input("Enter the second number: "))
    print("The sum of squares of {} and {} is {}".format(one, two, square_sum(one, two)))<br><br>
main()
</code></pre>
</section>
<section>
    <h3>Style</h3>
    <ul>
        <li>More lines and variables?<br>Simpler?</li>
        <li>Fewer lines and variables?<br>More Complex?</li>
    </ul>
    <br><br>
    <h4>&nbsp;</h4>
</section>
<section>
    <h3>Style</h3>
    <ul>
        <li>More lines and variables?<br>Simpler?</li>
        <li>Fewer lines and variables?<br>More Complex?</li>
    </ul>
    <br><br>
    <h4>Focus on Readability!</h4>
</section>