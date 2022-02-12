---
type: "reveal"
hidden: true
---
<section>
    <h3>Equal Comparator</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext stretch">x <- 5
y <- 3 + 2
DISPLAY(x = y)
</code></pre>
    <br>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext">
</code></pre>
</section>
<section>
    <h3>Equal Comparator</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext stretch">x <- 5
y <- 3 + 2
DISPLAY(x = y)
</code></pre>
    <br>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext">true
</code></pre>
</section>
<section>
    <h3>Equal Comparator</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext stretch">a <- "Hello " + "World"
b <- "hello " + "world"
DISPLAY(a = b)
</code></pre>
    <br>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext">
</code></pre>
</section>
<section>
    <h3>Equal Comparator</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext stretch">a <- "Hello " + "World"
b <- "hello " + "world"
DISPLAY(a = b)
</code></pre>
    <br>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext">false
</code></pre>
</section>
<section>
    <h3>Not Equal Comparator</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext stretch">x <- 5
y <- 5 + 0.000001
DISPLAY(x != y)
</code></pre>
    <br>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext">
</code></pre>
</section>
<section>
    <h3>Not Equal Comparator</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext stretch">x <- 5
y <- 5 + 0.000001
DISPLAY(x != y)
</code></pre>
    <br>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext">true
</code></pre>
</section>
<section>
    <h3>Less Than & Greater Than</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext stretch">a <- 5
b <- 6
DISPLAY(a < b)
DISPLAY("\n")
DISPLAY(a > b)
</code></pre>
    <br>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext"><br>
</code></pre>
</section>
<section>
    <h3>Less Than & Greater Than</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext stretch">a <- 5
b <- 6
DISPLAY(a < b)
DISPLAY("\n")
DISPLAY(a > b)
</code></pre>
    <br>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext">true
false
</code></pre>
</section>
<section>
    <h3>Less Than & Greater Than</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext stretch">x <- "test"
y <- "tent"
DISPLAY(x < y)
</code></pre>
    <br>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext">
</code></pre>
</section>
<section>
    <h3>Less Than & Greater Than</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext stretch">x <- "test"
y <- "tent"
DISPLAY(x < y)
</code></pre>
    <br>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext">false
</code></pre>
</section>
<section>
    <h3>Order of Operations</h3>
    <ol>
        <li>Mathematical Operators</li>
        <li>Boolean Comparators</li>
        <li><code>NOT</code> Operator</li>
        <li><code>AND</code> Operator</li>
        <li><code>OR</code> Operator</li>
    </ol>
</section>
<section>
    <pre><code style="font-size:50px; line-height: 60px" class="language-plaintext stretch">x <- 4 < 5 AND 3 * 5 > 12 OR NOT 7 MOD 3 = 1
<br><br><br><br><br></code></pre>
</section>
<section>
    <pre><code style="font-size:50px; line-height: 60px" class="language-plaintext stretch">x <- 4 < 5 AND <mark>3 * 5</mark> > 12 OR NOT <mark>7 MOD 3</mark> = 1
<br><br><br><br><br></code></pre>
</section>
<section>
    <pre><code style="font-size:50px; line-height: 60px" class="language-plaintext stretch">x <- 4 < 5 AND 3 * 5 > 12 OR NOT 7 MOD 3 = 1
x <- 4 < 5 AND  15   > 12 OR NOT    1    = 1
<br><br><br><br></code></pre>
</section>
<section>
    <pre><code style="font-size:50px; line-height: 60px" class="language-plaintext stretch">x <- 4 < 5 AND 3 * 5 > 12 OR NOT 7 MOD 3 = 1
x <- <mark>4 < 5</mark> AND  <mark>15   > 12</mark> OR NOT   <mark>1    = 1</mark>
<br><br><br><br></code></pre>
</section>
<section>
    <pre><code style="font-size:50px; line-height: 60px" class="language-plaintext stretch">x <- 4 < 5 AND 3 * 5 > 12 OR NOT 7 MOD 3 = 1
x <- 4 < 5 AND  15   > 12 OR NOT    1    = 1
x <- TRUE  AND    TRUE    OR NOT       TRUE
<br><br><br></code></pre>
</section>
<section>
    <pre><code style="font-size:50px; line-height: 60px" class="language-plaintext stretch">x <- 4 < 5 AND 3 * 5 > 12 OR NOT 7 MOD 3 = 1
x <- 4 < 5 AND  15   > 12 OR NOT    1    = 1
x <- TRUE  AND    TRUE    OR <mark>NOT       TRUE</mark>
<br><br><br></code></pre>
</section>
<section>
    <pre><code style="font-size:50px; line-height: 60px" class="language-plaintext stretch">x <- 4 < 5 AND 3 * 5 > 12 OR NOT 7 MOD 3 = 1
x <- 4 < 5 AND  15   > 12 OR NOT    1    = 1
x <- TRUE  AND    TRUE    OR NOT       TRUE
x <- TRUE  AND    TRUE    OR FALSE
<br><br></code></pre>
</section>
<section>
    <pre><code style="font-size:50px; line-height: 60px" class="language-plaintext stretch">x <- 4 < 5 AND 3 * 5 > 12 OR NOT 7 MOD 3 = 1
x <- 4 < 5 AND  15   > 12 OR NOT    1    = 1
x <- TRUE  AND    TRUE    OR NOT       TRUE
x <- <mark>TRUE  AND    TRUE</mark>    OR FALSE
<br><br></code></pre>
</section>
<section>
    <pre><code style="font-size:50px; line-height: 60px" class="language-plaintext stretch">x <- 4 < 5 AND 3 * 5 > 12 OR NOT 7 MOD 3 = 1
x <- 4 < 5 AND  15   > 12 OR NOT    1    = 1
x <- TRUE  AND    TRUE    OR NOT       TRUE
x <- TRUE  AND    TRUE    OR FALSE
x <-       TRUE           OR FALSE
<br></code></pre>
</section>
<section>
    <pre><code style="font-size:50px; line-height: 60px" class="language-plaintext stretch">x <- 4 < 5 AND 3 * 5 > 12 OR NOT 7 MOD 3 = 1
x <- 4 < 5 AND  15   > 12 OR NOT    1    = 1
x <- TRUE  AND    TRUE    OR NOT       TRUE
x <- TRUE  AND    TRUE    OR FALSE
x <-       TRUE           OR FALSE
x <- TRUE</code></pre>
</section>

