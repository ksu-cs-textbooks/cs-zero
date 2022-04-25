---
type: "reveal"
hidden: true
---

<section>
    <h3>Problem Statement</h3>
    <p style="font-size: 55px">Write a program that will compute the score of a given word in a game of <a href="https://en.wikipedia.org/wiki/Scrabble">Scrabble</a>. Assume that there are no special squares present. The program should prompt the user to input a string that only contains letters, and then compute the total score of that string by summing the value assigned to each letter. If the user inputs a string that contains invalid characters, the program should prompt for additional input until a valid word is received.</p>
</section>

<section>
	<h3>Handling Input</h3>
    <pre><code style="font-size: 40px; line-height: 45px" class="language-python stretch">def main():
<br>
main()
</code></pre>
</section>

<section>
	<h3>Handling Input</h3>
    <pre><code style="font-size: 40px; line-height: 45px" class="language-python stretch">def get_input():
<br>
def main():
    word = get_input()
<br>
main()
</code></pre>
</section>

<section>
	<h3>Handling Input</h3>
    <pre><code style="font-size: 40px; line-height: 45px" class="language-python stretch">def get_input():
    word = input("Enter a single word: ")
    while # word is not valid
        print("Error! Invalid Input!")
        word = input("Enter a single word: ")
    return word
<br>
def main():
    word = get_input()
<br>
main()
</code></pre>
</section>

<section>
	<h3>Handling Input</h3>
    <pre><code style="font-size: 40px; line-height: 45px" class="language-python stretch">def get_input():
    word = input("Enter a single word: ")
    while not word.isalpha():
        print("Error! Invalid Input!")
        word = input("Enter a single word: ")
    return word
<br>
def main():
    word = get_input()
<br>
main()
</code></pre>
</section>

<section>
	<h3>Computing Score</h3>
    <pre><code style="font-size: 40px; line-height: 45px" class="language-python stretch">def compute_score(word):<br>
</code></pre>
</section>

<section>
	<h3>Computing Score</h3>
    <pre><code style="font-size: 40px; line-height: 45px" class="language-python stretch">def compute_score(word):
    word = word.lower()
</code></pre>
</section>

<section>
	<h3>Computing Score</h3>
    <pre><code style="font-size: 40px; line-height: 45px" class="language-python stretch">def compute_score(word):
    word = word.lower()
    for letter in word:<br>
</code></pre>
</section>

<section>
	<h3>Computing Score</h3>
    <pre><code style="font-size: 40px; line-height: 45px" class="language-python stretch">def compute_score(word):
    word = word.lower()
    total = 0
    for letter in word:
        # add letter's score to total
    return total
</code></pre>
</section>

<section>
    <h3>Scrabble Scores</h3>
    <ul>
        <li>(1 point) - A, E, I, O, U, L, N, S, T, R</li>
        <li>(2 points) - D, G</li>
        <li>(3 points) - B, C, M, P</li>
        <li>(4 points) - F, H, V, W, Y</li>
        <li>(5 points) - K</li>
        <li>(8 points) - J, X</li>
        <li>(10 points) - Q, Z</li>
    </ul>
</section>

<section>
    <h3>Scrabble Scores</h3>
    <ul>
        <li><s>(1 point) - A, E, I, O, U, L, N, S, T, R</s></li>
        <li>(2 points) - D, G</li>
        <li>(3 points) - B, C, M, P</li>
        <li>(4 points) - F, H, V, W, Y</li>
        <li>(5 points) - K</li>
        <li>(8 points) - J, X</li>
        <li>(10 points) - Q, Z</li>
    </ul>
</section>

<section>
	<h3>Computing Score</h3>
    <pre><code style="font-size: 37px; line-height: 45px" class="language-python stretch">def compute_score(word):
    scores = {"d": 2, "g": 2, "b": 3, "c": 3, "m": 3, "p": 3, 
              "f": 4, "h": 4, "v": 4, "w": 4, "y": 4, "k": 5, 
              "j": 8, "x": 8, "q": 10, "z": 10}
    word = word.lower()
    total = 0
    for letter in word:
        # add letter's score to total
    return total
</code></pre>
</section>

<section>
	<h3>Computing Score</h3>
    <pre><code style="font-size: 37px; line-height: 45px" class="language-python stretch">def compute_score(word):
    scores = {"d": 2, "g": 2, "b": 3, "c": 3, "m": 3, "p": 3, 
              "f": 4, "h": 4, "v": 4, "w": 4, "y": 4, "k": 5, 
              "j": 8, "x": 8, "q": 10, "z": 10}
    word = word.lower()
    total = 0
    for letter in word:
        if letter in scores:
            total = total + scores[letter]
        else:
            total = total + 1
    return total
</code></pre>
</section>


<section>
    <pre><code style="font-size: 30px; line-height: 35px" class="language-python stretch">def get_input():
    word = input("Enter a single word: ")
    while not word.isalpha():
        print("Error! Invalid Input!")
        word = input("Enter a single word: ")
    return word
<br>
def compute_score(word):
    scores = {"d": 2, "g": 2, "b": 3, "c": 3, "m": 3, "p": 3, 
              "f": 4, "h": 4, "v": 4, "w": 4, "y": 4, "k": 5, 
              "j": 8, "x": 8, "q": 10, "z": 10}
    word = word.lower()
    total = 0
    for letter in word:
        if letter in scores:
            total = total + scores[letter]
        else:
            total = total + 1
    return total
<br>
def main():
    word = get_input()
    print(compute_score(word))
<br>
main()
</code></pre>
</section>

<section>
	<img class="stretch plain" src="/images/lab14/output2.png">
</section>



