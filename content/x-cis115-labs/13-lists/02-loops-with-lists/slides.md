---
type: "reveal"
hidden: true
---

<section>
	<h3>For Loop</h3>
    <pre><code style="font-size: 45px; line-height: 50px" class="language-python stretch">def main():
    nums = [3, 1, 4, 1, 5, 9, 2]
    print("The first seven digits of pi are...")
    for i in nums:
        print(i)
<br>
main()
</code></pre>
</section>

<section>
	<img class="stretch plain" src="/images/lab13/output1.png">
</section>

<section>
	<h3>While Loop</h3>
    <pre><code style="font-size: 45px; line-height: 50px" class="language-python stretch">def main():
    nums = [3, 1, 4, 1, 5, 9, 2]
    print("The first seven digits of pi are...")
    i = 0
    while i < len(nums):
        print(nums[i])
        i = i + 1
<br>
main()
</code></pre>
</section>
