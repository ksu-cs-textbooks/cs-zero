---
type: "reveal"
hidden: true
---
<section>
    <pre><code style="font-size: 45px; line-height: 50px" class="language-plaintext stretch">PROCEDURE positive_input()
{
    DISPLAY("Enter a positive number: ")
    x <- NUMBER(INPUT())
    REPEAT WHILE(x <= 0)
    {
        DISPLAY("Invalid Input!\n")
        DISPLAY("Enter a positive number: ")
        x <- NUMBER(INPUT())
    }
    RETURN x
}
</code></pre>
</section>

<section>
	<img class="stretch plain" src="/images/lab10/trace12_1.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab10/trace12_2.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab10/trace12_3.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab10/trace12_4.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab10/trace12_5.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab10/trace12_6.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab10/trace12_7.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab10/trace12_8.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab10/trace12_9.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab10/trace12.gif">
</section>

<section>
    <pre><code style="font-size: 45px; line-height: 50px" class="language-plaintext stretch">PROCEDURE main()
{
    a <- positive_input()
    b <- positive_input()
    c <- (a + b) / 2
    DISPLAY("The midpoint is " + c)
}
</code></pre>
</section>