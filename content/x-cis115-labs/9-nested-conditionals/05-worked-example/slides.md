---
type: "reveal"
hidden: true
---

<section>
    <h3>Problem Statement</h3>
    <p style="font-size: 50px">Three players each guess a positive integer greater than 0, and then share them simultaneously. The winner is chosen following this formula:</p>
    <ul style="font-size: 50px">
        <li>If any two players have chosen the same number, the game is a tie.</li>
        <li>If all players have chosen even numbers, or all players have chosen odd numbers, then the smallest number wins.</li>
        <li>Otherwise, the largest number wins.</li>
    </ul>
</section>

<section>
    <pre><code style="font-size: 25px; line-height: 28px" class="language-python stretch">def main():
    p1 = int(input("Enter a positive integer for player 1: "))
    p2 = int(input("Enter a positive integer for player 2: "))
    p3 = int(input("Enter a positive integer for player 3: "))<br>
    # debugging statements
    print("player 1 chose {}".format(p1))
    print("player 2 chose {}".format(p2))
    print("player 3 chose {}".format(p3))
<br>
main()
</code></pre>
</section>

<section>
	<img class="stretch plain" src="/images/lab9/output1.png">
</section>

<section>
    <h3>Conditions to Check</h3>
    <ul>
        <li>Are the numbers all even?<ul>
            <li>If so, which number is smallest?</li>
        </ul></li>
        <li>Are the numbers all odd?<ul>
            <li>If so, which number is smallest?</li>
        </ul></li>
        <li>Are the numbers not all even or odd<ul>
            <li>If so, which number is the largest?</li>
        </ul></li>
        <li class="fragment fade-in">Are all numbers greater than 0?</li>
    </ul>
</section>

<section>
    <pre><code style="font-size: 25px; line-height: 28px" class="language-python stretch">def main():
    p1 = int(input("Enter a positive integer for player 1: "))
    p2 = int(input("Enter a positive integer for player 2: "))
    p3 = int(input("Enter a positive integer for player 3: "))<br>
    <mark>if p1 <= 0 or p2 <= 0 or p3 <= 0:
        print("Error")
    else:
        print("All numbers are greater than 0")</mark>
<br>
main()
</code></pre>
</section>

<section>
    <pre><code style="font-size: 25px; line-height: 28px" class="language-python stretch">def main():
    p1 = int(input("Enter a positive integer for player 1: "))
    p2 = int(input("Enter a positive integer for player 2: "))
    p3 = int(input("Enter a positive integer for player 3: "))<br>
    if p1 <= 0 or p2 <= 0 or p3 <= 0:
        print("Error")
    else:
        <mark>if p1 == p2 or p2 == p3 or p3 == p1:
            print("Tie")
        else:
            print("Not a Tie")</mark>
<br>
main()
</code></pre>
</section>

<section>
    <pre><code style="font-size: 25px; line-height: 28px" class="language-python stretch">def main():
    p1 = int(input("Enter a positive integer for player 1: "))
    p2 = int(input("Enter a positive integer for player 2: "))
    p3 = int(input("Enter a positive integer for player 3: "))<br>
    if p1 <= 0 or p2 <= 0 or p3 <= 0:
        print("Error")
    else:
        if p1 == p2 or p2 == p3 or p3 == p1:
            print("Tie")
        <mark>elif p1 % 2 == 0 and p2 % 2 == 0 and p3 % 2 == 0:
            print("All numbers are even")
        elif p1 % 2 != 0 and p2 % 2 != 0 and p3 % 2 != 0:
            print("All numbers are odd")
        else:
            print("Numbers are both even and odd")</mark>
<br>
main()
</code></pre>
</section>

<section>
    <pre><code style="font-size: 25px; line-height: 28px" class="language-python stretch">def main():
    p1 = int(input("Enter a positive integer for player 1: "))
    p2 = int(input("Enter a positive integer for player 2: "))
    p3 = int(input("Enter a positive integer for player 3: "))<br>
    if p1 <= 0 or p2 <= 0 or p3 <= 0:
        print("Error")
    else:
        if p1 == p2 or p2 == p3 or p3 == p1:
            print("Tie")
        elif p1 % 2 == 0 and p2 % 2 == 0 and p3 % 2 == 0:
            <mark>if p1 < p2 and p1 < p3:
                print("Player 1 wins")
            elif p2 < p1 and p2 < p3:
                print("Player 2 wins")
            else:
                print("Player 3 wins")</mark></p3:>
        elif p1 % 2 != 0 and p2 % 2 != 0 and p3 % 2 != 0:
            print("All numbers are odd")
        else:
            print("Numbers are both even and odd")
<br>
main()
</code></pre>
</section>

<section>
    <pre><code style="font-size: 25px; line-height: 28px" class="language-python stretch">def main():
    p1 = int(input("Enter a positive integer for player 1: "))
    p2 = int(input("Enter a positive integer for player 2: "))
    p3 = int(input("Enter a positive integer for player 3: "))<br>
    if p1 <= 0 or p2 <= 0 or p3 <= 0:
        print("Error")
    else:
        if p1 == p2 or p2 == p3 or p3 == p1:
            print("Tie")
        elif p1 % 2 == 0 and p2 % 2 == 0 and p3 % 2 == 0:
            if p1 < p2 and p1 < p3:
                print("Player 1 wins")
            elif p2 < p1 and p2 < p3:
                print("Player 2 wins")
            else:
                print("Player 3 wins")
        elif p1 % 2 != 0 and p2 % 2 != 0 and p3 % 2 != 0:
            <mark>if p1 < p2 and p1 < p3:
                print("Player 1 wins")
            elif p2 < p1 and p2 < p3:
                print("Player 2 wins")
            else:
                print("Player 3 wins")</mark>
        else:
            print("Numbers are both even and odd")
<br>
main()
</code></pre>
</section>

<section>
	<img class="stretch plain" src="/images/lab9/output2.png">
</section>

<section>
    <pre><code style="font-size: 25px; line-height: 28px" class="language-python stretch">def smallest(p1, p2, p3):
    if p1 < p2 and p1 < p3:
        print("Player 1 wins")
    elif p2 < p1 and p2 < p3:
        print("Player 2 wins")
    else:
        print("Player 3 wins")
<br>
def main():
    p1 = int(input("Enter a positive integer for player 1: "))
    p2 = int(input("Enter a positive integer for player 2: "))
    p3 = int(input("Enter a positive integer for player 3: "))<br>
    if p1 <= 0 or p2 <= 0 or p3 <= 0:
        print("Error")
    else:
        if p1 == p2 or p2 == p3 or p3 == p1:
            print("Tie")
        elif p1 % 2 == 0 and p2 % 2 == 0 and p3 % 2 == 0:
            <mark>smallest(p1, p2, p3)</mark>
        elif p1 % 2 != 0 and p2 % 2 != 0 and p3 % 2 != 0:
            <mark>smallest(p1, p2, p3)</mark>
        else:
            print("Numbers are both even and odd")
<br>
main()
</code></pre>
</section>

<section>
    <pre><code style="font-size: 25px; line-height: 27px" class="language-python stretch">def smallest(p1, p2, p3):
    if p1 < p2 and p1 < p3:
        print("Player 1 wins")
    elif p2 < p1 and p2 < p3:
        print("Player 2 wins")
    else:
        print("Player 3 wins")
<br>
def largest(p1, p2, p3):
    if p1 > p2 and p1 > p3:
        print("Player 1 wins")
    elif p2 > p1 and p2 > p3:
        print("Player 2 wins")
    else:
        print("Player 3 wins")
<br>
def main():
    p1 = int(input("Enter a positive integer for player 1: "))
    p2 = int(input("Enter a positive integer for player 2: "))
    p3 = int(input("Enter a positive integer for player 3: "))<br>
    if p1 <= 0 or p2 <= 0 or p3 <= 0:
        print("Error")
    else:
        if p1 == p2 or p2 == p3 or p3 == p1:
            print("Tie")
        elif p1 % 2 == 0 and p2 % 2 == 0 and p3 % 2 == 0:
            smallest(p1, p2, p3)
        elif p1 % 2 != 0 and p2 % 2 != 0 and p3 % 2 != 0:
            smallest(p1, p2, p3)
        else:
            <mark>largest(p1, p2, p3)</mark>
<br>
main()
</code></pre>
</section>

<section>
    <pre><code style="font-size: 35px; line-height: 38px" class="language-python stretch">def main():
    p1 = int(input("Enter a positive integer for player 1: "))
    p2 = int(input("Enter a positive integer for player 2: "))
    p3 = int(input("Enter a positive integer for player 3: "))<br>
    if p1 <= 0 or p2 <= 0 or p3 <= 0:
        print("Error")                          # -1, -1, -1
    else:
        if p1 == p2 or p2 == p3 or p3 == p1:
            print("Tie")                        # 1, 1, 1
        elif p1 % 2 == 0 and p2 % 2 == 0 and p3 % 2 == 0:
            smallest(p1, p2, p3)                # 2, 4, 6
        elif p1 % 2 != 0 and p2 % 2 != 0 and p3 % 2 != 0:
            smallest(p1, p2, p3)                # 1, 3, 5
        else:
            largest(p1, p2, p3)                 # 1, 2, 3
</code></pre>
</section>

<section>
    <pre><code style="font-size: 35px; line-height: 38px" class="language-python stretch">def smallest(p1, p2, p3):
    if p1 < p2 and p1 < p3:
        print("Player 1 wins")      # 2, 4, 6
    elif p2 < p1 and p2 < p3:
        print("Player 2 wins")      # 4, 2, 6
    else:
        print("Player 3 wins")      # 4, 6, 2
<br>
def largest(p1, p2, p3):
    if p1 > p2 and p1 > p3:
        print("Player 1 wins")      # 3, 1, 2
    elif p2 > p1 and p2 > p3:
        print("Player 2 wins")      # 1, 3, 2
    else:
        print("Player 3 wins")      # 1, 2, 3
</code></pre>
</section>


<section>
    <pre><code style="font-size: 25px; line-height: 27px" class="language-python stretch">def smallest(p1, p2, p3):
    if p1 < p2 and p1 < p3:
        print("Player 1 wins")      # 2, 4, 6
    elif p2 < p1 and p2 < p3:
        print("Player 2 wins")      # 4, 2, 6
    else:
        print("Player 3 wins")      # 4, 6, 2
<br>
def largest(p1, p2, p3):
    if p1 > p2 and p1 > p3:
        print("Player 1 wins")      # 3, 1, 2
    elif p2 > p1 and p2 > p3:
        print("Player 2 wins")      # 1, 3, 2
    else:
        print("Player 3 wins")      # 1, 2, 3
<br>
def main():
    p1 = int(input("Enter a positive integer for player 1: "))
    p2 = int(input("Enter a positive integer for player 2: "))
    p3 = int(input("Enter a positive integer for player 3: "))<br>
    if p1 <= 0 or p2 <= 0 or p3 <= 0:
        print("Error")                          # -1, -1, -1
    else:
        if p1 == p2 or p2 == p3 or p3 == p1:
            print("Tie")                        # 1, 1, 1
        elif p1 % 2 == 0 and p2 % 2 == 0 and p3 % 2 == 0:
            smallest(p1, p2, p3)                # 2, 4, 6
        elif p1 % 2 != 0 and p2 % 2 != 0 and p3 % 2 != 0:
            smallest(p1, p2, p3)                # 1, 3, 5
        else:
            largest(p1, p2, p3)                 # 1, 2, 3
<br>
main()
</code></pre>
</section>

<section>
    <pre><code style="font-size: 25px; line-height: 27px" class="language-python stretch">def smallest(p1, p2, p3):
    if p1 < p2 and p1 < p3:
        print("Player 1 wins")      # 2, 4, 6 and 1, 3, 5
    elif p2 < p1 and p2 < p3:
        print("Player 2 wins")      # 4, 2, 6 and 3, 1, 5
    else:
        print("Player 3 wins")      # 4, 6, 2 and 3, 5, 1
<br>
def largest(p1, p2, p3):
    if p1 > p2 and p1 > p3:
        print("Player 1 wins")      # 3, 1, 2
    elif p2 > p1 and p2 > p3:
        print("Player 2 wins")      # 1, 3, 2
    else:
        print("Player 3 wins")      # 1, 2, 3
<br>
def main():
    p1 = int(input("Enter a positive integer for player 1: "))
    p2 = int(input("Enter a positive integer for player 2: "))
    p3 = int(input("Enter a positive integer for player 3: "))<br>
    if p1 <= 0 or p2 <= 0 or p3 <= 0:
        print("Error")                          # -1, -1, -1
    else:
        if p1 == p2 or p2 == p3 or p3 == p1:
            print("Tie")                        # 1, 1, 1
        elif p1 % 2 == 0 and p2 % 2 == 0 and p3 % 2 == 0:
            smallest(p1, p2, p3)                # 2, 4, 6
        elif p1 % 2 != 0 and p2 % 2 != 0 and p3 % 2 != 0:
            smallest(p1, p2, p3)                # 1, 3, 5
        else:
            largest(p1, p2, p3)                 # 1, 2, 3
<br>
main()
</code></pre>
</section>