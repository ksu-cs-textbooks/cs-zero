---
type: "reveal"
hidden: true
---
<section>
    <h3>String Concatenation</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-python stretch">first = "Hello"
second = "World"
print(first + second)
</code></pre>
    <br>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext"> 
</code></pre>
</section>
<section>
    <h3>String Concatenation</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-python stretch">first = "Hello"
second = "World"
print(first + second)
</code></pre>
    <br>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext">Hello World
</code></pre>
</section>
<section>
    <h3>Concatenating Numbers</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-python stretch">text = "Your total is $"
value = 2.75
print(text + str(value))
</code></pre>
    <br>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext"> 
</code></pre>
</section>
<section>
    <h3>Concatenating Numbers</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-python stretch">text = "Your total is $"
value = 2.75
print(text + str(value))
</code></pre>
    <br>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext">Your total is $2.75
</code></pre>
</section>
<section>
    <h3>Concatenating Numbers</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-python stretch">text = "Your total is $"
value = 2.75
print(text + <mark>value</mark>)
</code></pre>
    <br>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext"> 
</code></pre>
</section>
<section>
    <h3>Concatenating Numbers</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-python stretch">text = "Your total is $"
value = 2.75
print(text + <mark style="color:red">value</mark>)
</code></pre>
    <br>
    <pre><code style="font-size: 50px; line-height: 60px" class="language-plaintext">Traceback (most recent call last):
File "tutor.py", line 3, in &lt;module>
    print(text + value)
TypeError: must be str, not float
</code></pre>
</section>
<section>
    <h3>String Formatting</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-python stretch">name = input("Enter your name: ")
print("Hello {}".format(name))
</code></pre>
    <br>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext"><br>
</code></pre>
</section>
<section>
    <h3>String Formatting</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-python stretch">name = input("Enter your name: ")
print("Hello {}".format(name))
</code></pre>
    <br>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext">Enter your name: <mark> </mark><br>
</code></pre>
</section>
<section>
    <h3>String Formatting</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-python stretch">name = input("Enter your name: ")
print("Hello {}".format(name))
</code></pre>
    <br>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext">Enter your name: <mark>Willie Wildcat</mark><br>
</code></pre>
</section>
<section>
    <h3>String Formatting</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-python stretch">name = input("Enter your name: ")
print("Hello {}".format(name))
</code></pre>
    <br>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext">Enter your name: <mark>Willie Wildcat</mark>
Hello Willie Wildcat
</code></pre>
</section>
<section>
    <h3>String Formatting</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-python stretch">name = input("Enter your name: ")
print(<mark>"Hello {}"</mark>.format(name))
</code></pre>
    <br>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext">Enter your name: <mark>Willie Wildcat</mark>
Hello Willie Wildcat
</code></pre>
</section>
<section>
    <h3>String Formatting</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-python stretch">name = input("Enter your name: ")
print("Hello <mark>{}</mark>".format(name))
</code></pre>
    <br>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext">Enter your name: <mark>Willie Wildcat</mark>
Hello Willie Wildcat
</code></pre>
</section>
<section>
    <h3>String Formatting</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-python stretch">name = input("Enter your name: ")
print("Hello {}"<mark>.format(name)</mark>)
</code></pre>
    <br>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext">Enter your name: <mark>Willie Wildcat</mark>
Hello Willie Wildcat
</code></pre>
</section>
<section>
    <h3>String Formatting</h3>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-python stretch">name = input("Enter your name: ")
print("Hello <mark>{}</mark>".format(<mark>name</mark>))
</code></pre>
    <br>
    <pre><code style="font-size: 70px; line-height: 80px" class="language-plaintext">Enter your name: <mark>Willie Wildcat</mark>
Hello Willie Wildcat
</code></pre>
</section>
<section>
    <h3>String Formatting</h3>
    <pre><code style="font-size: 32px; line-height: 40px" class="language-python stretch">text_one = input("Enter the price of one item: ")
price = float(text_one)
text_two = input("Enter the quantity of items: ")
quantity = int(text_two)
cost = price * quantity
print("{} items at ${} each is ${} total".format(quantity, price, cost))
</code></pre>
    <br>
    <pre><code style="font-size: 40px; line-height: 50px" class="language-plaintext"><br><br>
</code></pre>
</section>
<section>
    <h3>String Formatting</h3>
    <pre><code style="font-size: 32px; line-height: 40px" class="language-python stretch">text_one = input("Enter the price of one item: ")
price = float(text_one)
text_two = input("Enter the quantity of items: ")
quantity = int(text_two)
cost = price * quantity
print("{} items at ${} each is ${} total".format(quantity, price, cost))
</code></pre>
    <br>
    <pre><code style="font-size: 40px; line-height: 50px" class="language-plaintext">Enter the price of one item: <mark>2.75</mark>
Enter the quantity of items: <mark>3</mark>
3 items at $2.75 each is $8.25 total
</code></pre>
</section>