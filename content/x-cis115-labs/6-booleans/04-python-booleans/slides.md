---
type: "reveal"
hidden: true
---
<section>
    <h3>Booleans</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-python stretch">a = True
b = False
print(a)
print(type(b))
</code></pre>
<br>
<pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext"><br>
</code></pre>
</section>
<section>
    <h3>Booleans</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-python stretch">a = True
b = False
print(a)
print(type(b))
</code></pre>
<br>
<pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext">True
&lt;class 'bool'></code></pre>
</section>
<section>
    <h3>Conversion</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-python stretch">a = bool("True")
</code></pre><br>
    <ul>
        <li><code>False</code>, 0, <code>None</code> or 0 length : <code>False</code></li>
        <li>Any other value : <code>true</code></li>
    </ul>
</section>
<section>
    <h3>Conversion</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-python stretch">print(bool("True"))
print(bool("False"))
</code></pre>
<br>
<pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext"><br>
</code></pre>
</section>
<section>
    <h3>Conversion</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-python stretch">print(bool("True"))
print(bool("False"))
</code></pre>
<br>
<pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext">True
True
</code></pre>
</section>
<section>
    <h3>Conversion</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-python stretch">print(bool(0))
print(bool(1))
print(bool(""))
</code></pre>
<br>
<pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext"><br><br>
</code></pre>
</section>
<section>
    <h3>Conversion</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-python stretch">print(bool(0))
print(bool(1))
print(bool(""))
</code></pre>
<br>
<pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext">False
True
False
</code></pre>
</section>
