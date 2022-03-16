---
type: "reveal"
hidden: true
---
<section>
    <h3>Block Scope</h3>
    <pre><code style="font-size: 30px; line-height: 35px" class="language-python stretch">def main():
    # main block
    x = int(input("Enter a number: "))
    if x > 5:
        # block A
        y = int(input("Enter a number: "))
        if y > 10: 
            # block B
            z = 10
        else:
            # block C
            z = 5
    elif x < 0:
        # block D
        a = -5
    else:
        # block E
        b = 0
    print("?")
<br>
main()
</code></pre>
</section>

<section>
    <h3>Main Block</h3>
    <pre><code style="font-size: 30px; line-height: 35px" class="language-python stretch">def main():
    <mark># main block
    x = int(input("Enter a number: "))
    if x > 5:
        # block A
        y = int(input("Enter a number: "))
        if y > 10: 
            # block B
            z = 10
        else:
            # block C
            z = 5
    elif x < 0:
        # block D
        a = -5
    else:
        # block E
        b = 0
    print("?")</mark>
<br>
main()
</code></pre>
</section>

<section>
    <h3>Block A</h3>
    <pre><code style="font-size: 30px; line-height: 35px" class="language-python stretch">def main():
    # main block
    x = int(input("Enter a number: "))
    if x > 5:
        <mark># block A
        y = int(input("Enter a number: "))
        if y > 10: 
            # block B
            z = 10
        else:
            # block C
            z = 5</mark>
    elif x < 0:
        # block D
        a = -5
    else:
        # block E
        b = 0
    print("?")
<br>
main()
</code></pre>
</section>

<section>
    <h3>Block B</h3>
    <pre><code style="font-size: 30px; line-height: 35px" class="language-python stretch">def main():
    # main block
    x = int(input("Enter a number: "))
    if x > 5:
        # block A
        y = int(input("Enter a number: "))
        if y > 10: 
            <mark># block B
            z = 10</mark>
        else:
            # block C
            z = 5
    elif x < 0:
        # block D
        a = -5
    else:
        # block E
        b = 0
    print("?")
<br>
main()
</code></pre>
</section>

<section>
    <h3>Block C</h3>
    <pre><code style="font-size: 30px; line-height: 35px" class="language-python stretch">def main():
    # main block
    x = int(input("Enter a number: "))
    if x > 5:
        # block A
        y = int(input("Enter a number: "))
        if y > 10: 
            # block B
            z = 10
        else:
            <mark># block C
            z = 5</mark>
    elif x < 0:
        # block D
        a = -5
    else:
        # block E
        b = 0
    print("?")
<br>
main()
</code></pre>
</section>

<section>
    <h3>Block D</h3>
    <pre><code style="font-size: 30px; line-height: 35px" class="language-python stretch">def main():
    # main block
    x = int(input("Enter a number: "))
    if x > 5:
        # block A
        y = int(input("Enter a number: "))
        if y > 10: 
            # block B
            z = 10
        else:
            # block C
            z = 5
    elif x < 0:
        <mark># block D
        a = -5</mark>
    else:
        # block E
        b = 0
    print("?")
<br>
main()
</code></pre>
</section>


<section>
    <h3>Block E</h3>
    <pre><code style="font-size: 30px; line-height: 35px" class="language-python stretch">def main():
    # main block
    x = int(input("Enter a number: "))
    if x > 5:
        # block A
        y = int(input("Enter a number: "))
        if y > 10: 
            # block B
            z = 10
        else:
            # block C
            z = 5
    elif x < 0:
        # block D
        a = -5
    else:
        <mark># block E
        b = 0</mark>
    print("?")
<br>
main()
</code></pre>
</section>

<section>
    <h3>Variable <code>x</code></h3>
    <pre><code style="font-size: 30px; line-height: 35px" class="language-python stretch">def main():
    # main block
    <mark>x = int(input("Enter a number: "))
    if x > 5:
        # block A
        y = int(input("Enter a number: "))
        if y > 10: 
            # block B
            z = 10
        else:
            # block C
            z = 5
    elif x < 0:
        # block D
        a = -5
    else:
        # block E
        b = 0
    print("?")</mark>
<br>
main()
</code></pre>
</section>

<section>
    <h3>Variable <code>y</code></h3>
    <pre><code style="font-size: 30px; line-height: 35px" class="language-python stretch">def main():
    # main block
    x = int(input("Enter a number: "))
    if x > 5:
        # block A
        <mark>y = int(input("Enter a number: "))
        if y > 10: 
            # block B
            z = 10
        else:
            # block C
            z = 5</mark>
    elif x < 0:
        # block D
        a = -5
    else:
        # block E
        b = 0
    print("?")
<br>
main()
</code></pre>
</section>

<section>
    <h3>Variable <code>z</code></h3>
    <pre><code style="font-size: 30px; line-height: 35px" class="language-python stretch">def main():
    # main block
    x = int(input("Enter a number: "))
    if x > 5:
        # block A
        y = int(input("Enter a number: "))
        if y > 10: 
            # block B
            <mark>z = 10</mark>
        else:
            # block C
            <mark>z = 5</mark>
    elif x < 0:
        # block D
        a = -5
    else:
        # block E
        b = 0
    print("?")
<br>
main()
</code></pre>
</section>

<section>
    <h3>Variable <code>a</code></h3>
    <pre><code style="font-size: 30px; line-height: 35px" class="language-python stretch">def main():
    # main block
    x = int(input("Enter a number: "))
    if x > 5:
        # block A
        y = int(input("Enter a number: "))
        if y > 10: 
            # block B
            z = 10
        else:
            # block C
            z = 5
    elif x < 0:
        # block D
        <mark>a = -5</mark>
    else:
        # block E
        b = 0
    print("?")
<br>
main()
</code></pre>
</section>

<section>
    <h3>Variable <code>b</code></h3>
    <pre><code style="font-size: 30px; line-height: 35px" class="language-python stretch">def main():
    # main block
    x = int(input("Enter a number: "))
    if x > 5:
        # block A
        y = int(input("Enter a number: "))
        if y > 10: 
            # block B
            z = 10
        else:
            # block C
            z = 5
    elif x < 0:
        # block D
        a = -5
    else:
        # block E
        <mark>b = 0</mark>
    print("?")
<br>
main()
</code></pre>
</section>

<section>
    <pre><code style="font-size: 30px; line-height: 35px" class="language-python stretch">def main():
    # main block
    # variable declarations in main block
    y = 0
    z = 0
    a = 0
    b = 0
    x = int(input("Enter a number: "))
    if x > 5:
        # block A
        y = int(input("Enter a number: "))
        if y > 10: 
            # block B
            z = 10
        else:
            # block C
            z = 5
    elif x < 0:
        # block D
        a = -5
    else:
        # block E
        b = 0
    print("?")
<br>
main()
</code></pre>
</section>

<section>
    <h3>Function Scope</h3>
    <pre><code style="font-size: 30px; line-height: 35px" class="language-python stretch">def main():
    # main block
    x = int(input("Enter a number: "))
    if x > 5:
        # block A
        y = int(input("Enter a number: "))
        if y > 10: 
            # block B
            z = 10
        else:
            # block C
            z = 5
    elif x < 0:
        # block D
        a = -5
    else:
        # block E
        b = 0
    print("?")
<br>
main()
</code></pre>
</section>

<section>
	<img class="stretch plain" src="/images/lab9/tutor.png">
</section>