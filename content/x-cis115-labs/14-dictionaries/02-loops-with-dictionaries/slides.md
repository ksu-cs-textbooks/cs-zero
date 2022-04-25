---
type: "reveal"
hidden: true
---

<section>
    <h3>Loops - Keys</h3>
    <pre><code style="font-size: 50px; line-height: 60px" class="language-python stretch">dict_3 = {
    "cat": "mammal",
    "lizard": "reptile",
    "goldfish": "fish",
    "chickadee": "bird"
}</code></pre>
	<pre class="fragment"><code style="font-size: 50px; line-height: 60px" class="language-python stretch">for key in dict_3:
    print("{}: {}".format(key, dict_3[key]))</code></pre>
</section>

<section>
	<img class="stretch plain" src="/images/lab14/output1.png">
</section>

<section>
    <h3>Loops - Keys & Values</h3>
    <pre><code style="font-size: 50px; line-height: 60px" class="language-python stretch">dict_3 = {
    "cat": "mammal",
    "lizard": "reptile",
    "goldfish": "fish",
    "chickadee": "bird"
}</code></pre>
	<pre class="fragment"><code style="font-size: 50px; line-height: 60px" class="language-python stretch">for key, value in dict_3.items():
    print("{}: {}".format(key, value))</code></pre>
</section>

<section>
	<img class="stretch plain" src="/images/lab14/output1.png">
</section>