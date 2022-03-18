---
type: "reveal"
hidden: true
---
<section>
    <pre><code style="font-size: 29px; line-height: 35px" class="language-python stretch">def input_percentage():
    x = float(input("Enter a percentage as a decimal number from 0 to 1: "))
    while(x < 0 or x > 1):
        print("Invalid Input!")
        x = float(input("Enter a percentage as a decimal number from 0 to 1: "))
    return x
</code></pre>
</section>

<section>
    <pre><code style="font-size: 29px; line-height: 35px" class="language-python stretch">def input_percentage():
    x = float(input("Enter a percentage as a decimal number from 0 to 1: "))
    while(x < 0 or x > 1):
        print("Invalid Input!")
        x = float(input("Enter a percentage as a decimal number from 0 to 1: "))
    return x
<br>
def main():
    print("This program will compute weighted average for three exam scores")
    print("Enter the first exam's score")
    exam1_score = input_percentage()
    print("Enter the first exam's weight")
    exam1_weight = input_percentage()
    print("Enter the second exam's score")
    exam2_score = input_percentage()
    print("Enter the second exam's weight")
    exam2_weight = input_percentage()
    print("Enter the third exam's score")
    exam3_score = input_percentage()
    print("Enter the third exam's weight")
    exam3_weight = input_percentage()
    total = exam1_score * exam1_weight + 
            exam2_score * exam2_weight + 
            exam3_score * exam3_weight
    print("Your total score is {}".format(total))
<br>
main()
</code></pre>
</section>

<section>
	<img class="stretch plain" src="/images/lab11/input.png">
</section>
