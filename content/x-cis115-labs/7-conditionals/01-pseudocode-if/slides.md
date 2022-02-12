---
type: "reveal"
hidden: true
---
<section>
    <h3>If Statement</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext stretch">IF(&lt;boolean expression>)
{
    &lt;block of statements>
}
</code></pre>
</section>
<section>
    <pre><code style="font-size: 50px; line-height: 60px" class="language-plaintext stretch">PROCEDURE main()
{
    DISPLAY("Enter a number: ")
    x <- NUMBER(INPUT())
    IF(x = 42)
    {
        DISPLAY("You found the secret!\n")
    }
    DISPLAY("Thanks for playing!\n")
}<br>
main()
</code></pre>
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace8_1.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace8_2.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace8_3.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace8_4.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace8_5.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace8_6.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace8_7.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace8_8.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace8_1.gif">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace8_4.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace8_9.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace8_10.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace8_11.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace8_12.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace8_13.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace8_14.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace8_2.gif">
</section>
<section>
    <h3>Flowchart</h3>
    <div style="float: right; width: 50%">
        <img class="stretch plain" src="/images/lab7/ifthen.png">
    </div>
    <div style="float: left; width: 50%">
                <pre class="language-plaintext stretch" style="font-size: 50px; line-height: 60px"><code>x <- NUMBER(INPUT())
IF(x > 0)
{
    DISPLAY(x)
}
DISPLAY("Goodbye")</code></pre>
    </div>
</section>