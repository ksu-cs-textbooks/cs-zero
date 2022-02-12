---
type: "reveal"
hidden: true
---
<section>
    <h3>Return Statement</h3>
    <pre><code style="font-size: 45px; line-height: 50px" class="language-plaintext stretch">PROCEDURE mult_mod(value, multiply, modulo)
{
    value <- value * multiply
    value <- value MOD modulo
    RETURN(value)
}<br>
PROCEDURE main()
{
    DISPLAY("Enter a value: ")
    text <- INPUT()
    value <- NUMBER(text)
    answer <- mult_mod(value, 5, 3)
    DISPLAY(answer)
}<br>
main()
</code></pre>
</section>
<section>
    <h3>Return Statement</h3>
    <pre><code style="font-size: 45px; line-height: 50px" class="language-plaintext stretch">PROCEDURE mult_mod(value, multiply, modulo)
{
    value <- value * multiply
    value <- value MOD modulo
    <mark>RETURN(value)</mark>
}<br>
PROCEDURE main()
{
    DISPLAY("Enter a value: ")
    text <- INPUT()
    value <- NUMBER(text)
    answer <- mult_mod(value, 5, 3)
    DISPLAY(answer)
}<br>
main()
</code></pre>
</section>
<section>
	<img class="stretch plain" src="/images/lab4/trace8_1.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab4/trace8_3.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab4/trace8_5.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab4/trace8_6.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab4/trace8_7.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab4/trace8_8.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab4/trace8_10.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab4/trace8_11.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab4/trace8_12.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab4/trace8_13.png">
</section>
<section>
	<img class="stretch plain" src="/images/lab4/trace8.gif">
</section>

