---
type: "reveal"
hidden: true
---

<section>
    <h3>Problem Statement</h3>
    <p style="font-size: 55px">The game begins with the first player choosing either 1, 2, or 3. Then, the second player chooses either 1, 2 or 3 and adds that number to the number chosen by the first player to establish a total. The game continues by alternating between players, each choosing to add either 1, 2 or 3 to the total. The game is over when the total reaches 21 or higher. The player who adds the number to the total that causes the game to end is the loser.</p>
</section>

<section>
    <pre><code style="font-size: 35px; line-height: 40px" class="language-plaintext stretch">PROCEDURE main()
{<br>
}<br>
main()
</code></pre>
</section>

<section>
    <pre><code style="font-size: 35px; line-height: 40px" class="language-plaintext stretch">PROCEDURE main()
{
    total <- 0
    REPEAT WHILE(total <= 21)
    {
        # players take turns
    }
    # game over
}<br>
main()
</code></pre>
</section>

<section>
    <pre><code style="font-size: 35px; line-height: 40px" class="language-plaintext stretch">PROCEDURE main()
{
    total <- 0
    player <- 1
    REPEAT WHILE(total <= 21)
    {
        # player's turn
        IF(player = 1)
        {
            player = 2
        }
        ELSE
        {
            player = 1
        }
    }
    # game over
}<br>
main()
</code></pre>
</section>

<section>
    <pre><code style="font-size: 35px; line-height: 40px" class="language-plaintext stretch">PROCEDURE read_input(player)
{
    DISPLAY("Enter 1, 2, or 3 for player " + player + ": ")
    x <- INPUT()
    REPEAT WHILE(x != "1" AND x != "2" AND x != "3")
    {
        DISPLAY("Invalid Input!\n")
        DISPLAY("Enter 1, 2, or 3 for player " + player + ": ")
        x <- INPUT()
    }
    RETURN NUMBER(x)
}
</code></pre>
</section>

<section>
    <pre><code style="font-size: 25px; line-height: 27px" class="language-plaintext stretch">PROCEDURE read_input(player)
{
    DISPLAY("Enter 1, 2, or 3 for player " + player + ": ")
    x <- INPUT()
    REPEAT WHILE(x != "1" AND x != "2" AND x != "3")
    {
        DISPLAY("Invalid Input!\n")
        DISPLAY("Enter 1, 2, or 3 for player " + player + ": ")
        x <- INPUT()
    }
    RETURN NUMBER(x)
}<br>
PROCEDURE main()
{
    total <- 0
    player <- 1
    REPEAT WHILE(total <= 21)
    {
        # player's turn
        total <- total + read_input(player)
        IF(player = 1)
        {
            player = 2
        }
        ELSE
        {
            player = 1
        }
    }
    # game over
    DISPLAY("Player " + player + " wins!")
}<br>
main()
</code></pre>
</section>

<section>
<table style="font-size: 30px">
<thead>
<tr>
<th style="text-align:center">Input</th>
<th style="text-align:center">Player</th>
<th style="text-align:center">Sum/Error</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:center"><code>&quot;1&quot;</code></td>
<td style="text-align:center">1</td>
<td style="text-align:center">1</td>
</tr>
<tr>
<td style="text-align:center"><code>&quot;2&quot;</code></td>
<td style="text-align:center">2</td>
<td style="text-align:center">3</td>
</tr>
<tr>
<td style="text-align:center"><code>&quot;3&quot;</code></td>
<td style="text-align:center">1</td>
<td style="text-align:center">6</td>
</tr>
<tr>
<td style="text-align:center"><code>&quot;0&quot;</code></td>
<td style="text-align:center">2</td>
<td style="text-align:center">error</td>
</tr>
<tr>
<td style="text-align:center"><code>&quot;4&quot;</code></td>
<td style="text-align:center">2</td>
<td style="text-align:center">error</td>
</tr>
<tr>
<td style="text-align:center"><code>&quot;1&quot;</code></td>
<td style="text-align:center">2</td>
<td style="text-align:center">7</td>
</tr>
<tr>
<td style="text-align:center"><code>&quot;-1&quot;</code></td>
<td style="text-align:center">1</td>
<td style="text-align:center">error</td>
</tr>
<tr>
<td style="text-align:center"><code>&quot;5&quot;</code></td>
<td style="text-align:center">1</td>
<td style="text-align:center">error</td>
</tr>
<tr>
<td style="text-align:center"><code>&quot;2&quot;</code></td>
<td style="text-align:center">1</td>
<td style="text-align:center">9</td>
</tr>
<tr>
<td style="text-align:center"><code>&quot;lizard&quot;</code></td>
<td style="text-align:center">2</td>
<td style="text-align:center">error</td>
</tr>
<tr>
<td style="text-align:center"><code>&quot;(*&amp;#$&amp;*^@&quot;</code></td>
<td style="text-align:center">2</td>
<td style="text-align:center">error</td>
</tr>
<tr>
<td style="text-align:center"><code>&quot;3&quot;</code></td>
<td style="text-align:center">2</td>
<td style="text-align:center">12</td>
</tr>
<tr>
<td style="text-align:center"><code>&quot;invalid&quot;</code></td>
<td style="text-align:center">1</td>
<td style="text-align:center">error</td>
</tr>
<tr>
<td style="text-align:center"><code>&quot;3&quot;</code></td>
<td style="text-align:center">1</td>
<td style="text-align:center">15</td>
</tr>
<tr>
<td style="text-align:center"><code>&quot;broken&quot;</code></td>
<td style="text-align:center">2</td>
<td style="text-align:center">error</td>
</tr>
<tr>
<td style="text-align:center"><code>&quot;2&quot;</code></td>
<td style="text-align:center">2</td>
<td style="text-align:center">17</td>
</tr>
<tr>
<td style="text-align:center"><code>&quot; &quot;</code></td>
<td style="text-align:center">1</td>
<td style="text-align:center">error</td>
</tr>
<tr>
<td style="text-align:center"><code>&quot;1&quot;</code></td>
<td style="text-align:center">1</td>
<td style="text-align:center">18</td>
</tr>
<tr>
<td style="text-align:center"><code>&quot;3&quot;</code></td>
<td style="text-align:center">2</td>
<td style="text-align:center">21</td>
</tr>
<tr>
<td style="text-align:center"></td>
<td style="text-align:center"></td>
<td style="text-align:center">Player 1 Wins</td>
</tr>
</tbody>
</table>
</section>

<section>
    <pre><code style="font-size: 35px; line-height: 40px" class="language-plaintext stretch">PROCEDURE read_input(player)
{
    DISPLAY("Enter 1, 2, or 3 for player " + player + ": ")
    x <- INPUT()
    REPEAT WHILE(x != "1" AND x != "2" AND x != "3")
    {
        DISPLAY("Invalid Input!\n")
        DISPLAY("Enter 1, 2, or 3 for player " + player + ": ")
        x <- INPUT()
    }
    RETURN NUMBER(x)
}
</code></pre>
</section>

<section>
    <pre><code style="font-size: 35px; line-height: 40px" class="language-plaintext stretch">PROCEDURE main()
{
    total <- 0
    player <- 1
    REPEAT WHILE(total <= 21)
    {
        # player's turn
        total <- total + read_input(player)
        IF(player = 1)
        {
            player = 2
        }
        ELSE
        {
            player = 1
        }
    }
    # game over
    DISPLAY("Player " + player + " wins!")
}
</code></pre>
</section>