---
type: "reveal"
hidden: true
---

<section>
	<img class="stretch plain" src="/images/lab9/rps.svg">
    <p class="imagecredit">Image Credit: <a href="https://commons.wikimedia.org/w/index.php?title=File:Rock-paper-scissors.svg&oldid=513212597">Wikimedia</a></p>
</section>

<section>
    <pre><code style="font-size: 30px; line-height: 35px" class="language-python stretch">def main():
    p1 = input("Enter 'rock', 'paper', or 'scissors' for player 1: ")
    p2 = input("Enter 'rock', 'paper', or 'scissors' for player 2: ")<br>
    # determine the winner
<br>
main()
</code></pre>
</section>

<section>
<table style="font-size: 50px">
<thead>
<tr>
<th style="text-align:center">Player 1</th>
<th style="text-align:center">Player 2</th>
<th style="text-align:center">Output</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:center">rock</td>
<td style="text-align:center">rock</td>
<td style="text-align:center">tie</td>
</tr>
<tr>
<td style="text-align:center">rock</td>
<td style="text-align:center">paper</td>
<td style="text-align:center">player 2 wins</td>
</tr>
<tr>
<td style="text-align:center">rock</td>
<td style="text-align:center">scissors</td>
<td style="text-align:center">player 1 wins</td>
</tr>
<tr>
<td style="text-align:center">paper</td>
<td style="text-align:center">rock</td>
<td style="text-align:center">player 1 wins</td>
</tr>
<tr>
<td style="text-align:center">paper</td>
<td style="text-align:center">paper</td>
<td style="text-align:center">tie</td>
</tr>
<tr>
<td style="text-align:center">paper</td>
<td style="text-align:center">scissors</td>
<td style="text-align:center">player 2 wins</td>
</tr>
<tr>
<td style="text-align:center">scissors</td>
<td style="text-align:center">rock</td>
<td style="text-align:center">player 2 wins</td>
</tr>
<tr>
<td style="text-align:center">scissors</td>
<td style="text-align:center">paper</td>
<td style="text-align:center">player 1 wins</td>
</tr>
<tr>
<td style="text-align:center">scissors</td>
<td style="text-align:center">scissors</td>
<td style="text-align:center">tie</td>
</tr>
</tbody>
</table>
</section>

<section>
	<img class="stretch plain" src="/images/lab9/linear.svg">
</section>

<section>
    <pre><code style="font-size: 30px; line-height: 35px" class="language-python stretch">def main():
    p1 = input("Enter 'rock', 'paper', or 'scissors' for player 1: ")
    p2 = input("Enter 'rock', 'paper', or 'scissors' for player 2: ")<br>
    if p1 == "rock" and p2 == "rock":
        print("tie")
    if p1 == "rock" and p2 == "paper":
        print("player 2 wins")
    if p1 == "rock" and p2 == "scissors":
        print("player 1 wins")
    if p1 == "paper" and p2 == "rock":
        print("player 1 wins")
    if p1 == "paper" and p2 == "paper":
        print("tie")
    if p1 == "paper" and p2 == "scissors":
        print("player 2 wins")
    if p1 == "scissors" and p2 == "rock":
        print("player 2 wins")
    if p1 == "scissors" and p2 == "paper":
        print("player 1 wins")
    if p1 == "scissors" and p2 == "scissors":
        print("tie")
    if (not (p1 == "rock" or p1 == "paper" or p1 == "scissors") and
                not (p2 == "rock" or p2 == "paper" or p2 == "scissors")):
        print("error")
<br>
main()
</code></pre>
</section>

<section>
    <pre><code style="font-size: 28px; line-height: 35px" class="language-python stretch">def main():
    p1 = input("Enter 'rock', 'paper', or 'scissors' for player 1: ")
    p2 = input("Enter 'rock', 'paper', or 'scissors' for player 2: ")<br>
    if ((p1 == "rock" and p2 == "rock") or 
            (p1 == "paper" and p2 == "paper") or 
            (p1 == "scissors" and p2 == "scissors")):
        print("tie")
    if ((p1 == "rock" and p2 == "paper") or 
            (p1 == "paper" and p2 == "scissors") or 
            (p1 == "scissors" and p2 == "rock")):
        print("player 2 wins")
    if ((p1 == "rock" and p2 == "scissors") or 
            (p1 == "paper" and p2 == "rock") or 
            (p1 == "scissors" and p2 == "paper")):
        print("player 1 wins")
    if (not (p1 == "rock" or p1 == "paper" or p1 == "scissors") and 
            not (p2 == "rock" or p2 == "paper" or p2 == "scissors")):
        print("error")
<br>
main()
</code></pre>
</section>
