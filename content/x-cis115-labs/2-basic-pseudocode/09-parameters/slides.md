---
type: "reveal"
hidden: true
---
<section>
    <b>parameters</b>: required inputs for a procedure<br>
    <b>arguments</b>: values in procedure calls stored as parameters
</section>
<section>
    <pre><code style="font-size: 50px; line-height: 60px" class="language-plaintext stretch">PROCEDURE hello_world(first_name, last_name)
{
    DISPLAY("Hello ")
    DISPLAY(first_name)
    DISPLAY(" ")
    DISPLAY(last_name)
}</code></pre>
</section>
<section>
    <pre><code style="font-size: 50px; line-height: 60px" class="language-plaintext">hello_world("Willie", "Wildcat")</code></pre>
    <br>
    <pre><code style="font-size: 50px; line-height: 60px" class="language-plaintext"> </code></pre>
    <br>
    <br>
</section>
<section>
    <pre><code style="font-size: 50px; line-height: 60px" class="language-plaintext">hello_world("Willie", "Wildcat")</code></pre>
    <br>
    <pre><code style="font-size: 50px; line-height: 60px" class="language-plaintext">Hello Willie Wildcat</code></pre>
    <br>
    <br>
</section>
<section>
    <pre><code style="font-size: 50px; line-height: 60px" class="language-plaintext stretch">PROCEDURE hello_world(first_name, last_name)
{
    DISPLAY("Hello ")
    DISPLAY(first_name)
    DISPLAY(" ")
    DISPLAY(last_name)
}<br>
PROCEDURE main()
{
    hello_world("Willie", "Wildcat")
}<br>
main()</code></pre>
</section>
<section>
	<img class="stretch plain" src="/cc110/images/lab2/trace5_1.png">
</section>
<section>
	<img class="stretch plain" src="/cc110/images/lab2/trace5_5.png">
</section>
<section>
	<img class="stretch plain" src="/cc110/images/lab2/trace5_6.png">
</section>
<section>
	<img class="stretch plain" src="/cc110/images/lab2/trace5_7.png">
</section>
<section>
	<img class="stretch plain" src="/cc110/images/lab2/trace5_8.png">
</section>
<section>
	<img class="stretch plain" src="/cc110/images/lab2/trace5_14.png">
</section>
<section>
	<img class="stretch plain" src="/cc110/images/lab2/trace5_15.png">
</section>
<section>
	<img class="stretch plain" src="/cc110/images/lab2/trace5.gif">
</section>
