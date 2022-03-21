---
type: "reveal"
hidden: true
---
<section>
    <h3>Range Function</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-python stretch">range(stop)
</code></pre>
<pre><code style="font-size: 70px; line-height: 80px" class="language-python stretch">range(start, stop)
</code></pre>
<pre><code style="font-size: 70px; line-height: 80px" class="language-python stretch">range(start, stop, step)
</code></pre>
</section>

<section>
    <h3>For Loop</h3>
    <pre><code style="font-size: 65px; line-height: 70px" class="language-python stretch">for &lt;iterator variable> in &lt;list>:
    &lt;block of statements>
</code></pre>
</section>

<section>
    <pre><code style="font-size: 45px; line-height: 50px" class="language-python stretch">def main():
    x = int(input("Enter a number: "))
    line = ""
    for i in range(x):
        line = line + "*"
        print(line)
<br>
main()
</code></pre>
</section>

<section>
	<img class="stretch plain" src="/images/lab11/tutor8_1.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab11/tutor8_3.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab11/tutor8_4.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab11/tutor8_6.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab11/tutor8_7.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab11/tutor8_8.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab11/tutor8_9.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab11/tutor8_10.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab11/tutor8_12.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab11/tutor8_13.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab11/tutor8_15.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab11/tutor8_16.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab11/tutor8_18.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab11/tutor8_19.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab11/tutor8_21.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab11/tutor8.gif">
</section>

<section>
    <pre><code style="font-size: 45px; line-height: 50px" class="language-python stretch">def main():
    x = int(input("Enter a number: "))
    line = ""
    for i in range(x):
        line = line + "*"
        print(line)
</code></pre>
</section>

<section>
    <pre><code style="font-size: 45px; line-height: 50px" class="language-python stretch">def main():
    x = int(input("Enter a number: "))
    line = ""
    <mark>i = 0</mark>
    for i in range(x):
        line = line + "*"
        print(line)
</code></pre>
</section>

<section>
    <pre><code style="font-size: 45px; line-height: 50px" class="language-python stretch">def main():
    x = int(input("Enter a number: "))
    line = ""
    i = 0
    for i in range(x):
        line = line + "*"
        print(line)
        <mark>i = i + 1</mark>
</code></pre>
</section>

<section>
    <pre><code style="font-size: 45px; line-height: 50px" class="language-python stretch">def main():
    x = int(input("Enter a number: "))
    line = ""
    i = 0
    <mark>while i < x:</mark>
        line = line + "*"
        print(line)
        i = i + 1
</code></pre>
</section>