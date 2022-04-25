---
type: "reveal"
hidden: true
---

<section>
    <pre><code style="font-size: 35px; line-height: 40px" class="language-python stretch">def add_score(scores):
    name = input("Enter a name: ")
    score = int(input("Enter a score: "))
    scores[name] = score
<br>
def average_score(scores):
    total = 0
    for key, value in scores.items():
        total = total + value
    return total / len(scores)
<br>
def main():
    scores = {}
    for i in range(4):
        add_score(scores)
    print(average_score(scores))
<br>
main()</code></pre>
</section>


<section>
	<img class="stretch plain" src="/images/lab14/tutor14_6.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab14/tutor14_7.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab14/tutor14_8.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab14/tutor14_9.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab14/tutor14_12.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab14/tutor14_13.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab14/tutor14_14.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab14/tutor14_36.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab14/tutor14_37.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab14/tutor14_40.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab14/tutor14_49.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab14/tutor14_50.png">
</section>