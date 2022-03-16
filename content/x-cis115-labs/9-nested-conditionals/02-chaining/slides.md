---
type: "reveal"
hidden: true
---

<section>
	<img class="stretch plain" src="/images/lab9/chain.svg">
</section>

<section>
    <pre><code style="font-size: 22px; line-height: 25px" class="language-python stretch">def main():
    p1 = input("Enter 'rock', 'paper', or 'scissors' for player 1: ")
    p2 = input("Enter 'rock', 'paper', or 'scissors' for player 2: ")<br>
    if p1 == "rock" and p2 == "rock":
        print("tie")
    else:
        if p1 == "rock" and p2 == "paper":
            print("player 2 wins")
        else: 
            if p1 == "rock" and p2 == "scissors":
                print("player 1 wins")
            else:
                if p1 == "paper" and p2 == "rock":
                    print("player 1 wins")
                else:
                    if p1 == "paper" and p2 == "paper":
                        print("tie")
                    else:
                        if p1 == "paper" and p2 == "scissors":
                            print("player 2 wins")
                        else:
                            if p1 == "scissors" and p2 == "rock":
                                print("player 2 wins")
                            else:
                                if p1 == "scissors" and p2 == "paper":
                                    print("player 1 wins")
                                else:
                                    if p1 == "scissors" and p2 == "scissors":
                                        print("tie")
                                    else:
                                        if (not (p1 == "rock" or p1 == "paper" or p1 == "scissors") and 
                                                not (p2 == "rock" or p2 == "paper" or p2 == "scissors")):
                                            print("error")
<br>
main()
</code></pre>
</section>

<section>
    <pre><code style="font-size: 25px; line-height: 28px" class="language-python stretch">def main():
    p1 = input("Enter 'rock', 'paper', or 'scissors' for player 1: ")
    p2 = input("Enter 'rock', 'paper', or 'scissors' for player 2: ")<br>
    if ((p1 == "rock" and p2 == "rock") or 
            (p1 == "paper" and p2 == "paper") or 
            (p1 == "scissors" and p2 == "scissors")):
        print("tie")
    else:
        if ((p1 == "rock" and p2 == "paper") or 
                (p1 == "paper" and p2 == "scissors") or 
                (p1 == "scissors" and p2 == "rock")):
            print("player 2 wins")
        else:
            if ((p1 == "rock" and p2 == "scissors") or 
                    (p1 == "paper" and p2 == "rock") or 
                    (p1 == "scissors" and p2 == "paper")):
                print("player 1 wins")
            else:
                if (not (p1 == "rock" or p1 == "paper" or p1 == "scissors") and 
                        not (p2 == "rock" or p2 == "paper" or p2 == "scissors")):
                    print("error")
<br>
main()
</code></pre>
</section>

<section>
    <pre><code style="font-size: 25px; line-height: 28px" class="language-python stretch">def main():
    p1 = input("Enter 'rock', 'paper', or 'scissors' for player 1: ")
    p2 = input("Enter 'rock', 'paper', or 'scissors' for player 2: ")<br>
    if p1 == "rock" and p2 == "rock":
        print("tie")
    else:
        if p1 == "rock" and p2 == "paper":
            print("player 2 wins")
        else: 
            if p1 == "rock" and p2 == "scissors":
                print("player 1 wins")
            else:
                if p1 == "paper" and p2 == "rock":
                    print("player 1 wins")
                else:
                    if p1 == "paper" and p2 == "paper":
                        print("tie")
                    else:
                        if p1 == "paper" and p2 == "scissors":
                            print("player 2 wins")
                        else:
                            if p1 == "scissors" and p2 == "rock":
                                print("player 2 wins")
                            else:
                                if p1 == "scissors" and p2 == "paper":
                                    print("player 1 wins")
                                else:
                                    if p1 == "scissors" and p2 == "scissors":
                                        print("tie")
                                    else:
                                        # All other options have been checked
                                        print("error")
<br>
main()
</code></pre>
</section>


<section>
    <pre><code style="font-size: 30px; line-height: 35px" class="language-python stretch">def main():
    p1 = input("Enter 'rock', 'paper', or 'scissors' for player 1: ")
    p2 = input("Enter 'rock', 'paper', or 'scissors' for player 2: ")<br>
    if p1 == "rock" and p2 == "rock":
        print("tie")
    elif p1 == "rock" and p2 == "paper":
        print("player 2 wins")
    elif p1 == "rock" and p2 == "scissors":
        print("player 1 wins")
    elif p1 == "paper" and p2 == "rock":
        print("player 1 wins")
    elif p1 == "paper" and p2 == "paper":
        print("tie")
    elif p1 == "paper" and p2 == "scissors":
        print("player 2 wins")
    elif p1 == "scissors" and p2 == "rock":
        print("player 2 wins")
    elif p1 == "scissors" and p2 == "paper":
        print("player 1 wins")
    elif p1 == "scissors" and p2 == "scissors":
        print("tie")
    else:
        # All other options have been checked
        print("error")
<br>
main()
</code></pre>
</section>