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

<--! TODO TODO !-->
