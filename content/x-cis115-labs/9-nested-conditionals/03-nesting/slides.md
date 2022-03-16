---
type: "reveal"
hidden: true
---

<section>
	<img class="stretch plain" src="/images/lab9/nested.svg">
</section>

<section>
    <pre><code style="font-size: 25px; line-height: 28px" class="language-python stretch">def main():
    p1 = input("Enter 'rock', 'paper', or 'scissors' for player 1: ")
    p2 = input("Enter 'rock', 'paper', or 'scissors' for player 2: ")<br>
    if p1 == "rock":
        if p2 == "rock":
            print("tie")
        elif p2 == "paper":
            print("player 2 wins")
        elif p2 == "scissors":
            print("player 1 wins")
        else:
            print("error") 
    elif p1 == "paper":
        if p2 == "rock":
            print("player 1 wins")
        elif p2 == "paper":
            print("tie")
        elif p2 == "scissors":
            print("player 2 wins")
        else:
            print("error")
    elif p1 == "scissors":
        if p2 == "rock":
            print("player 2 wins")
        elif p2 == "paper":
            print("player 1 wins")
        elif p2 == "scissors":
            print("tie")
        else:
            print("error")
    else:
        print("error") 
<br>
main()
</code></pre>
</section>

<section>
    <pre><code style="font-size: 25px; line-height: 28px" class="language-python stretch">def main():
    p1 = input("Enter 'rock', 'paper', or 'scissors' for player 1: ")
    p2 = input("Enter 'rock', 'paper', or 'scissors' for player 2: ")<br>
    if (not (p1 == "rock" or p1 == "paper" or p1 == "scissors") or 
            not (p2 == "rock" or p2 == "paper" or p2 == "scissors")):
        print("error")
    else:
        if p1 == "rock":
            if p2 == "rock":
                print("tie")
            elif p2 == "paper":
                print("player 2 wins")
            else:
                print("player 1 wins")
        elif p1 == "paper":
            if p2 == "rock":
                print("player 1 wins")
            elif p2 == "paper":
                print("tie")
            else:
                print("player 2 wins")
        else:
            if p2 == "rock":
                print("player 2 wins")
            elif p2 == "paper":
                print("player 1 wins")
            else:
                print("tie")
<br>
main()
</code></pre>
</section>

<section>
    <pre><code style="font-size: 30px; line-height: 33px" class="language-python stretch">def main():
    p1 = input("Enter 'rock', 'paper', or 'scissors' for player 1: ")
    p2 = input("Enter 'rock', 'paper', or 'scissors' for player 2: ")<br>
    if (not (p1 == "rock" or p1 == "paper" or p1 == "scissors") or 
            not (p2 == "rock" or p2 == "paper" or p2 == "scissors")):
        print("error")
    else:
        if p1 == p2:
            print("tie")
        elif p1 == "rock":
            if p2 == "paper":
                print("player 2 wins")
            else:
                print("player 1 wins")
        elif p1 == "paper":
            if p2 == "rock":
                print("player 1 wins")
            else:
                print("player 2 wins")
        else:
            if p2 == "rock":
                print("player 2 wins")
            else:
                print("player 1 wins")
<br>
main()
</code></pre>
</section>

