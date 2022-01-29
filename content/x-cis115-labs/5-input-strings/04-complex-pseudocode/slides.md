---
type: "reveal"
hidden: true
---
<section>
    <pre><code style="font-size: 55px; line-height: 65px" class="language-plaintext stretch">DISPLAY("Enter a number: ")
text <- INPUT()
number <- NUMBER(text)
square <- number * number
DISPLAY("The square of your input is ")
DISPLAY(square)
</code></pre>
</section>
<section>
    <pre><code style="font-size: 55px; line-height: 65px" class="language-plaintext stretch">DISPLAY("Enter a number: ")
<mark>text <- INPUT()
number <- NUMBER(text)</mark>
square <- number * number
DISPLAY("The square of your input is ")
DISPLAY(square)
</code></pre>
</section>
<section>
    <pre><code style="font-size: 55px; line-height: 65px" class="language-plaintext stretch">DISPLAY("Enter a number: ")
<mark>number <- NUMBER(INPUT())</mark>
square <- number * number
DISPLAY("The square of your input is ")
DISPLAY(square)
</code></pre>
</section>
<section>
    <pre><code style="font-size: 55px; line-height: 65px" class="language-plaintext stretch">DISPLAY("Enter a number: ")
number <- NUMBER(INPUT())
square <- number * number
<mark>DISPLAY("The square of your input is ")
DISPLAY(square)</mark>
</code></pre>
</section>
<section>
    <pre><code style="font-size: 40px; line-height: 50px" class="language-plaintext stretch">DISPLAY("Enter a number: ")
number <- NUMBER(INPUT())
square <- number * number
<mark>DISPLAY("The square of your input is " + STRING(square))</mark>
</code></pre>
</section>
<section>
    <pre><code style="font-size: 40px; line-height: 50px" class="language-plaintext stretch">DISPLAY("Enter a number: ")
number <- NUMBER(INPUT())
<mark>square <- number * number</mark>
DISPLAY("The square of your input is " + STRING(<mark>square</mark>))
</code></pre>
</section>
<section>
    <pre><code style="font-size: 35px; line-height: 45px" class="language-plaintext stretch">DISPLAY("Enter a number: ")
number <- NUMBER(INPUT())
DISPLAY("The square of your input is " + STRING(<mark>number * number</mark>))
</code></pre>
</section>
<section>
    <pre><code style="font-size: 35px; line-height: 45px" class="language-plaintext stretch">DISPLAY("Enter a number: ")
number <- NUMBER(INPUT())
DISPLAY("The square of your input is " + STRING(number * number))
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