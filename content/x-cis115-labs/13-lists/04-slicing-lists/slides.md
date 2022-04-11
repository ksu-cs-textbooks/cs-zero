---
type: "reveal"
hidden: true
---
<section>
    <h3>List Slicing</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-python stretch">nums[start:end]</code></pre>
	<br>
	<pre class="fragment"><code style="font-size: 70px; line-height: 80px" class="language-python stretch">nums[start:end:step]</code></pre>
</section>

<section>
    <h3>List Slicing</h3>
    <ul>
		<li>Numbers can be Omitted</li>
		<li>Numbers can be Negative</li>
</section>

<section>
    <pre><code style="font-size: 35px; line-height: 40px" class="language-python stretch">def main():
    nums = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
    print(nums)<br>
    # simple slices
    print(nums[3:7])
    print(nums[5:])
    print(nums[:5])
    print(nums[::2])
    print(nums[1::2])<br>
    # negative numbers
    print(nums[-1])
    print(nums[-7:-3])
    print(nums[-3:])
    print(nums[:-3])
    print(nums[::-1])
<br>
main()
</code></pre>
</section>

<section>
	<img class="stretch plain" src="/images/lab13/output2.png">
</section>

<section>
    <h3>List from Range</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-python stretch">nums = range(10)
print(nums[3:7])</code></pre>
	<br>
	<pre class="fragment"><code style="font-size: 70px; line-height: 80px" class="language-plaintext stretch">range(3, 7)</code></pre>
</section>

<section>
    <h3>List from Range</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-python stretch">nums = list(range(10))
print(nums[3:7])</code></pre>
	<br>
	<pre class="fragment"><code style="font-size: 70px; line-height: 80px" class="language-plaintext stretch">[3, 4, 5, 6]</code></pre>
</section>