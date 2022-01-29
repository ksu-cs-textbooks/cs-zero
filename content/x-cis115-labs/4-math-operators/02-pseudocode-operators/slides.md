---
type: "reveal"
hidden: true
---
<section>
    <h3>Mathematical Operators</h3>
    <br>
    <pre><code style="font-size:60px; line-height: 70px" class="language-plaintext stretch">&lt;expression> &lt;operator> &lt;expression>
</code></pre>
    <br>
</section>
<section>
    <h3>Addition</h3>
    <pre><code style="font-size:100px; line-height: 120px" class="language-plaintext stretch">a <- 5
b <- 7
c <- a + b
DISPLAY(c)</code></pre>
    <p><i>displays</i></p>
    <pre><code style="font-size:100px; line-height: 120px" class="language-plaintext stretch">12</code></pre>
    <br>
</section>
<section>
    <h3>Subtraction</h3>
    <pre><code style="font-size:100px; line-height: 120px" class="language-plaintext stretch">x <- 24
y <- 10
z <- x - y
DISPLAY(z)</code></pre>
    <p><i>displays</i></p>
    <pre><code style="font-size:100px; line-height: 120px" class="language-plaintext stretch">14</code></pre>
    <br>
</section>
<section>
    <h3>Multiplication</h3>
    <pre><code style="font-size:100px; line-height: 120px" class="language-plaintext stretch">a <- 6
b <- 7
c <- a * b
DISPLAY(c)</code></pre>
    <p><i>displays</i></p>
    <pre><code style="font-size:100px; line-height: 120px" class="language-plaintext stretch">42</code></pre>
    <br>
</section>
<section>
    <h3>Division (Whole Number)</h3>
    <pre><code style="font-size:100px; line-height: 120px" class="language-plaintext stretch">x <- 27
y <- 3
z <- x / y
DISPLAY(z)</code></pre>
    <p><i>displays</i></p>
    <pre><code style="font-size:100px; line-height: 120px" class="language-plaintext stretch">9</code></pre>
    <br>
</section>
<section>
    <h3>Division (Decimal)</h3>
    <pre><code style="font-size:100px; line-height: 120px" class="language-plaintext stretch">a <- 19
b <- 5
c <- a / b
DISPLAY(c)</code></pre>
    <p><i>displays</i></p>
    <pre><code style="font-size:100px; line-height: 120px" class="language-plaintext stretch">3.8</code></pre>
    <br>
</section>
<section>
    <h3>Modulo (Remainder)</h3>
    <pre><code style="font-size:100px; line-height: 120px" class="language-plaintext stretch">x <- 19
y <- 5
z <- x MOD y
DISPLAY(z)</code></pre>
    <p><i>displays</i></p>
    <pre><code style="font-size:100px; line-height: 120px" class="language-plaintext stretch">4</code></pre>
    <br>
</section>
<section>
    <h3>Order of Operations</h3>
    <ol>
        <li>Parentheses</li>
        <li>Multiplication, Division, Modulo</li>
        <li>Addition, Subtraction</li>
    </ol>
</section>
<section>
    <pre><code style="font-size:60px; line-height: 70px" class="language-plaintext stretch">x <- 8 / 4 + 5 * (3 + 1) - 7 MOD 4
<br><br><br></code></pre>
</section>
<section>
    <pre><code style="font-size:60px; line-height: 70px" class="language-plaintext stretch">x <- 8 / 4 + 5 * <mark>(3 + 1)</mark> - 7 MOD 4
<br><br><br></code></pre>
</section>
<section>
    <pre><code style="font-size:60px; line-height: 70px" class="language-plaintext stretch">x <- 8 / 4 + 5 * (3 + 1) - 7 MOD 4
x <- 8 / 4 + 5 *    4    - 7 MOD 4<br><br><br></code></pre>
</section>
<section>
    <pre><code style="font-size:60px; line-height: 70px" class="language-plaintext stretch">x <- 8 / 4 + 5 * (3 + 1) - 7 MOD 4
x <- <mark>8 / 4</mark> + <mark>5 *    4</mark>    - <mark>7 MOD 4</mark><br><br><br></code></pre>
</section>
<section>
    <pre><code style="font-size:60px; line-height: 70px" class="language-plaintext stretch">x <- 8 / 4 + 5 * (3 + 1) - 7 MOD 4
x <- 8 / 4 + 5 *    4    - 7 MOD 4
x <-   2   +    20       -    3<br><br></code></pre>
</section>
<section>
    <pre><code style="font-size:60px; line-height: 70px" class="language-plaintext stretch">x <- 8 / 4 + 5 * (3 + 1) - 7 MOD 4
x <- 8 / 4 + 5 *    4    - 7 MOD 4
x <-   <mark>2   +    20       -    3</mark><br><br></code></pre>
</section>
<section>
    <pre><code style="font-size:60px; line-height: 70px" class="language-plaintext stretch">x <- 8 / 4 + 5 * (3 + 1) - 7 MOD 4
x <- 8 / 4 + 5 *    4    - 7 MOD 4
x <-   2   +    20       -    3
x <- 19</code></pre>
</section>