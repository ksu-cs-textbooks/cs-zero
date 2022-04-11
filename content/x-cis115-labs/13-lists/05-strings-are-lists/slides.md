---
type: "reveal"
hidden: true
---

<section>
    <pre><code style="font-size: 30px; line-height: 33px" class="language-python stretch">import random
import string
<br>
def encode(secret, step):
    output = ""
    for i in secret:
        output = output + i
        for j in step:
            output = output + random.choice(string.ascii_lowercase)
    return output
<br>
def decode(code, step):
    return code[::step]
<br>
def main():
    secret = input("Enter a secret word")
    step = int(input("Enter a positive integer"))
    code = encode(secret, step)
    print("Your code is:")
    print(code)
    print()
    decoded = decode(code, step)
    print("I can decode it back to:")
    print(decoded)
<br>
main()
</code></pre>
</section>

<section>
	<img class="stretch plain" src="/images/lab13/tutor12_7.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab13/tutor12_8.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab13/tutor12_10.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab13/tutor12_12.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab13/tutor12_13.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab13/tutor12_14.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab13/tutor12_15.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab13/tutor12_16.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab13/tutor12_17.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab13/tutor12_24.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab13/tutor12_102.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab13/tutor12_104.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab13/tutor12_107.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab13/tutor12_109.png">
</section>

<section>
	<img class="stretch plain" src="/images/lab13/tutor12_111.png">
</section>