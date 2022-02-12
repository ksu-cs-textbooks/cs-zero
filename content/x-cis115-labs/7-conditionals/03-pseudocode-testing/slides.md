---
type: "reveal"
hidden: true
---
<section>
    <h3>Testing</h3>
    <div style="float: right; width: 50%">
        <img class="stretch plain" width="100%" src="/cc110/images/lab7/control.png">
    </div>
    <div style="float: left; width: 50%">
        <pre><code style="font-size: 30px; line-height: 35px" class="language-plaintext stretch">PROCEDURE main()
{
    DISPLAY("Enter a number: ")
    x <- NUMBER(INPUT())
    DISPLAY("Enter another number: ")
    y <- NUMBER(INPUT())
    IF (x + y > 10)
    {
        DISPLAY("Branch 1")
    }
    ELSE
    {
        DISPLAY("Branch 2")
    }
    IF (x - y > 10)
    {
        DISPLAY("Branch 3")
    }
    ELSE
    {
        DISPLAY("Branch 4")
    }
}<br>
main()
</code></pre>
</div>
</section>
<section>
    <h3>x = 6 | y = 6</h3>
    <div style="float: right; width: 50%">
        <img class="stretch plain" width="100%" src="/cc110/images/lab7/control.png">
    </div>
    <div style="float: left; width: 50%">
        <pre><code style="font-size: 30px; line-height: 35px" class="language-plaintext stretch">PROCEDURE main()
{
    DISPLAY("Enter a number: ")
    x <- NUMBER(INPUT())
    DISPLAY("Enter another number: ")
    y <- NUMBER(INPUT())
    IF (x + y > 10)
    {
        <mark>DISPLAY("Branch 1")</mark>
    }
    ELSE
    {
        DISPLAY("Branch 2")
    }
    IF (x - y > 10)
    {
        DISPLAY("Branch 3")
    }
    ELSE
    {
        <mark>DISPLAY("Branch 4")</mark>
    }
}<br>
main()
</code></pre>
</div>
</section>
<section>
    <h3>x = 6 | y = -6</h3>
    <div style="float: right; width: 50%">
        <img class="stretch plain" width="100%" src="/cc110/images/lab7/control.png">
    </div>
    <div style="float: left; width: 50%">
        <pre><code style="font-size: 30px; line-height: 35px" class="language-plaintext stretch">PROCEDURE main()
{
    DISPLAY("Enter a number: ")
    x <- NUMBER(INPUT())
    DISPLAY("Enter another number: ")
    y <- NUMBER(INPUT())
    IF (x + y > 10)
    {
        DISPLAY("Branch 1")
    }
    ELSE
    {
        <mark>DISPLAY("Branch 2")</mark>
    }
    IF (x - y > 10)
    {
        <mark>DISPLAY("Branch 3")</mark>
    }
    ELSE
    {
        DISPLAY("Branch 4")
    }
}<br>
main()
</code></pre>
</div>
</section>
<section>
    <h3>Branch Coverage</h3>
    <ul>
        <li>x = 6 | y = 6 -> Branches 1 & 4</li>
        <li>x = 6 | y = -6 -> Branches 2 & 3</li>
    </ul>
</section>
<section>
    <h3>x = 12 | y = 0</h3>
    <div style="float: right; width: 50%">
        <img class="stretch plain" width="100%" src="/cc110/images/lab7/control.png">
    </div>
    <div style="float: left; width: 50%">
        <pre><code style="font-size: 30px; line-height: 35px" class="language-plaintext stretch">PROCEDURE main()
{
    DISPLAY("Enter a number: ")
    x <- NUMBER(INPUT())
    DISPLAY("Enter another number: ")
    y <- NUMBER(INPUT())
    IF (x + y > 10)
    {
        <mark>DISPLAY("Branch 1")</mark>
    }
    ELSE
    {
        DISPLAY("Branch 2")
    }
    IF (x - y > 10)
    {
        <mark>DISPLAY("Branch 3")</mark>
    }
    ELSE
    {
        DISPLAY("Branch 4")
    }
}<br>
main()
</code></pre>
</div>
</section>
<section>
    <h3>x = 4 | y = 4</h3>
    <div style="float: right; width: 50%">
        <img class="stretch plain" width="100%" src="/cc110/images/lab7/control.png">
    </div>
    <div style="float: left; width: 50%">
        <pre><code style="font-size: 30px; line-height: 35px" class="language-plaintext stretch">PROCEDURE main()
{
    DISPLAY("Enter a number: ")
    x <- NUMBER(INPUT())
    DISPLAY("Enter another number: ")
    y <- NUMBER(INPUT())
    IF (x + y > 10)
    {
        DISPLAY("Branch 1")
    }
    ELSE
    {
        <mark>DISPLAY("Branch 2")</mark>
    }
    IF (x - y > 10)
    {
        DISPLAY("Branch 3")
    }
    ELSE
    {
        <mark>DISPLAY("Branch 4")</mark>
    }
}<br>
main()
</code></pre>
</div>
</section>
<section>
    <h3>Path Coverage</h3>
    <ul>
        <li>x = 6 | y = 6 -> Branches 1 & 4</li>
        <li>x = 6 | y = -6 -> Branches 2 & 3</li>
        <li>x = 12 | y = 0 -> Branches 1 & 3</li>
        <li>x = 4 | y = 4 -> Branches 2 & 4</li>
    </ul>
</section>
<section>
    <h3>Edge Cases</h3>
    <div style="float: right; width: 50%">
        <img class="stretch plain" width="100%" src="/cc110/images/lab7/control.png">
    </div>
    <div style="float: left; width: 50%">
        <pre><code style="font-size: 30px; line-height: 35px" class="language-plaintext stretch">PROCEDURE main()
{
    DISPLAY("Enter a number: ")
    x <- NUMBER(INPUT())
    DISPLAY("Enter another number: ")
    y <- NUMBER(INPUT())
    IF (<mark>x + y > 10</mark>)
    {
        DISPLAY("Branch 1")
    }
    ELSE
    {
        DISPLAY("Branch 2")
    }
    IF (<mark>x - y > 10</mark>)
    {
        DISPLAY("Branch 3")
    }
    ELSE
    {
        DISPLAY("Branch 4")
    }
}<br>
main()
</code></pre>
</div>
</section>
<section>
    <h3>x = 10 | y = 0</h3>
    <div style="float: right; width: 50%">
        <img class="stretch plain" width="100%" src="/cc110/images/lab7/control.png">
    </div>
    <div style="float: left; width: 50%">
        <pre><code style="font-size: 30px; line-height: 35px" class="language-plaintext stretch">PROCEDURE main()
{
    DISPLAY("Enter a number: ")
    x <- NUMBER(INPUT())
    DISPLAY("Enter another number: ")
    y <- NUMBER(INPUT())
    IF (x + y > 10)
    {
        DISPLAY("Branch 1")
    }
    ELSE
    {
        <mark>DISPLAY("Branch 2")</mark>
    }
    IF (x - y > 10)
    {
        DISPLAY("Branch 3")
    }
    ELSE
    {
        <mark>DISPLAY("Branch 4")</mark>
    }
}<br>
main()
</code></pre>
</div>
</section>
<section>
    <h3>x = 11 | y = 0</h3>
    <div style="float: right; width: 50%">
        <img class="stretch plain" width="100%" src="/cc110/images/lab7/control.png">
    </div>
    <div style="float: left; width: 50%">
        <pre><code style="font-size: 30px; line-height: 35px" class="language-plaintext stretch">PROCEDURE main()
{
    DISPLAY("Enter a number: ")
    x <- NUMBER(INPUT())
    DISPLAY("Enter another number: ")
    y <- NUMBER(INPUT())
    IF (x + y > 10)
    {
        <mark>DISPLAY("Branch 1")</mark>
    }
    ELSE
    {
        DISPLAY("Branch 2")
    }
    IF (x - y > 10)
    {
        <mark>DISPLAY("Branch 3")</mark>
    }
    ELSE
    {
        DISPLAY("Branch 4")
    }
}<br>
main()
</code></pre>
</div>
</section>
<section>
    <h3>x = 9 | y = 0</h3>
    <div style="float: right; width: 50%">
        <img class="stretch plain" width="100%" src="/cc110/images/lab7/control.png">
    </div>
    <div style="float: left; width: 50%">
        <pre><code style="font-size: 30px; line-height: 35px" class="language-plaintext stretch">PROCEDURE main()
{
    DISPLAY("Enter a number: ")
    x <- NUMBER(INPUT())
    DISPLAY("Enter another number: ")
    y <- NUMBER(INPUT())
    IF (x + y > 10)
    {
        DISPLAY("Branch 1")
    }
    ELSE
    {
        <mark>DISPLAY("Branch 2")</mark>
    }
    IF (x - y > 10)
    {
        DISPLAY("Branch 3")
    }
    ELSE
    {
        <mark>DISPLAY("Branch 4")</mark>
    }
}<br>
main()
</code></pre>
</div>
</section>
<section>
    <h3>Path Coverage</h3>
    <ul>
        <li>x = 6 | y = 6 -> Branches 1 & 4</li>
        <li>x = 6 | y = -6 -> Branches 2 & 3</li>
        <li>x = 12 | y = 0 -> Branches 1 & 3</li>
        <li>x = 4 | y = 4 -> Branches 2 & 4</li>
    </ul>
    <h3>Edge Cases</h3>
    <ul>
        <li>x = 9 | y = 0 -> False</li>
        <li>x = 10 | y = 0 -> False</li>
        <li>x = 11 | y = 0 -> True</li>
    </ul>
</section>