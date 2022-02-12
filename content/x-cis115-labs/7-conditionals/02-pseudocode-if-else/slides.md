---
type: "reveal"
hidden: true
---
<section>
    <h3>If-Else Statement</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext stretch">IF(&lt;boolean expression>)
{
    &lt;block of statements 1>
}
ELSE
{
    &lt;block of statements 2>
}
</code></pre>
</section>
<section>
    <pre><code style="font-size: 50px; line-height: 60px" class="language-plaintext stretch">PROCEDURE main()
{
    DISPLAY("Enter a number: ")
    x <- NUMBER(INPUT())
    IF(x MOD 2 = 0)
    {
        DISPLAY("Your number is even!\n")
    }
    ELSE
    {
        DISPLAY("Your number is odd!\n")
    }
    DISPLAY("Thanks for playing!\n")
}<br>        
main()
</code></pre>
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace9_1.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace9_2.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace9_3.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace9_4.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace9_5.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace9_6.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace9_7.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace9_8.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace9_9.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace9_10.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace9_1.gif">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace9_4.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace9_11.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace9_12.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace9_13.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace9_14.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace9_15.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace9_16.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab7/trace9_2.gif">
</section>
<section>
    <h3>Flowchart</h3>
    <div style="float: right; width: 50%">
        <img class="stretch plain" src="/images/lab7/ifthenelse.png">
    </div>
    <div style="float: left; width: 50%">
                <pre class="language-plaintext stretch" style="font-size: 50px; line-height: 60px"><code>x <- NUMBER(INPUT())
IF(x >= 0)
{
    DISPLAY(x)
}
ELSE
{
    DISPLAY(-1 * x)
}
DISPLAY("Goodbye")</code></pre>
</div>
</section>