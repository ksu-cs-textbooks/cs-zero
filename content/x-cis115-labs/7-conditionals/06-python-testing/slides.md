---
type: "reveal"
hidden: true
---
<section>
    <h3>Testing</h3>
    <pre><code style="font-size: 35px; line-height: 45px" class="language-python stretch">def main():
    a = int(input("Enter a number: "))
    b = int(input("Enter a number: "))
    if a // b >= 5:
        # Branch 1
        print("{} goes into {} at least 5 times".format(b, a))
    else:
        # Branch 2
        print("{} is less than 5 times {}".format(a, b))
    if a % b == 0:
        # Branch 3
        print("{} evenly divides {}".format(b, a))
    else:
        # Branch 4
        print("{} / {} has a remainder".format(a, b))<br><br>
main()
</code></pre>
</section>
<section>
    <h3>a = 25 | b = 5</h3>
    <pre><code style="font-size: 35px; line-height: 45px" class="language-python stretch">def main():
    a = int(input("Enter a number: "))
    b = int(input("Enter a number: "))
    if a // b >= 5:
        <mark># Branch 1</mark>
        print("{} goes into {} at least 5 times".format(b, a))
    else:
        # Branch 2
        print("{} is less than 5 times {}".format(a, b))
    if a % b == 0:
        <mark># Branch 3</mark>
        print("{} evenly divides {}".format(b, a))
    else:
        # Branch 4
        print("{} / {} has a remainder".format(a, b))<br><br>
main()
</code></pre>
</section>
<section>
    <h3>a = 21 | b = 5</h3>
    <pre><code style="font-size: 35px; line-height: 45px" class="language-python stretch">def main():
    a = int(input("Enter a number: "))
    b = int(input("Enter a number: "))
    if a // b >= 5:
        # Branch 1
        print("{} goes into {} at least 5 times".format(b, a))
    else:
        <mark># Branch 2</mark>
        print("{} is less than 5 times {}".format(a, b))
    if a % b == 0:
        # Branch 3
        print("{} evenly divides {}".format(b, a))
    else:
        <mark># Branch 4</mark>
        print("{} / {} has a remainder".format(a, b))<br><br>
main()
</code></pre>
</section>
<section>
    <h3>Branch Coverage</h3>
    <ul>
        <li>a = 25 | b = 5 -> Branches 1 & 3</li>
        <li>a = 21 | b = 5 -> Branches 2 & 4</li>
    </ul>
</section>
<section>
    <h3>a = 31 | b = 5</h3>
    <pre><code style="font-size: 35px; line-height: 45px" class="language-python stretch">def main():
    a = int(input("Enter a number: "))
    b = int(input("Enter a number: "))
    if a // b >= 5:
        <mark># Branch 1</mark>
        print("{} goes into {} at least 5 times".format(b, a))
    else:
        # Branch 2
        print("{} is less than 5 times {}".format(a, b))
    if a % b == 0:
        # Branch 3
        print("{} evenly divides {}".format(b, a))
    else:
        <mark># Branch 4</mark>
        print("{} / {} has a remainder".format(a, b))<br><br>
main()
</code></pre>
</section>
<section>
    <h3>a = 20 | b = 5</h3>
    <pre><code style="font-size: 35px; line-height: 45px" class="language-python stretch">def main():
    a = int(input("Enter a number: "))
    b = int(input("Enter a number: "))
    if a // b >= 5:
        # Branch 1
        print("{} goes into {} at least 5 times".format(b, a))
    else:
        <mark># Branch 2</mark>
        print("{} is less than 5 times {}".format(a, b))
    if a % b == 0:
        <mark># Branch 3</mark>
        print("{} evenly divides {}".format(b, a))
    else:
        # Branch 4
        print("{} / {} has a remainder".format(a, b))<br><br>
main()
</code></pre>
</section>
<section>
    <h3>Path Coverage</h3>
    <ul>
        <li>a = 25 | b = 5 -> Branches 1 & 3</li>
        <li>a = 21 | b = 5 -> Branches 2 & 4</li>
        <li>a = 31 | b = 5 -> Branches 1 & 4</li>
        <li>a = 20 | b = 5 -> Branches 2 & 3</li>
    </ul>
</section>
<section>
    <h3>Edge Cases</h3>
    <pre><code style="font-size: 35px; line-height: 45px" class="language-python stretch">def main():
    a = int(input("Enter a number: "))
    b = int(input("Enter a number: "))
    if <mark>a // b >= 5</mark>:
        # Branch 1
        print("{} goes into {} at least 5 times".format(b, a))
    else:
        # Branch 2
        print("{} is less than 5 times {}".format(a, b))
    if <mark>a % b == 0</mark>:
        # Branch 3
        print("{} evenly divides {}".format(b, a))
    else:
        # Branch 4
        print("{} / {} has a remainder".format(a, b))<br><br>
main()
</code></pre>
</section>
<section>
    <h3>Path Coverage & Edge Cases</h3>
    <ul>
        <li>a = 25 | b = 5 -> Branches 1 & 3</li>
        <li>a = 21 | b = 5 -> Branches 2 & 4</li>
        <li>a = 31 | b = 5 -> Branches 1 & 4</li>
        <li>a = 20 | b = 5 -> Branches 2 & 3</li>
    </ul>
</section>
