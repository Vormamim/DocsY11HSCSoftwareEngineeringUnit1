---
icon: clipboard-list-check
---

# Flowchart Activities

Before we start, it's worth noting that in an **online exam environment** you will actually need to create flowcharts using blocks in the exam window itself. We will look at this later in the course, but it is in that spirit that I would suggest we use Lucid Chart for now so you get used to creating charts in a digital environment. You could also just use the drawing tools in Google Docs. You are also welcome to draw them on paper first if you would like.

{% embed url="https://www.lucidchart.com/" %}



1. **Create a flowchart based on the following algorithms (one at a time):**
   1. ```
      BEGIN 
          read (num1)
          read (num2)
          Set total to num1 + num2
          Set average to total / 2
          Display average
      END
      ```
   2. <pre><code><strong>BEGIN
      </strong>    read (score)
          IF score >= 85
              Display "Excellent"
          ELSEIF score >= 70
              Display "Good"
          ELSEIF score >= 50
              Display "Average"
          ELSE
              Display "Fail"
          ENDIF
      END
      </code></pre>
   3. ```
      BEGIN
          read (N)
          Set totalSum to 0
          FOR i = 1 to N
              Add i to totalSum
          NEXT i
          Display totalSum
      END
      ```
   4. ```
      BEGIN
          read (N)
          Set totalSum to 0
          FOR i = 1 to N
              Call CheckEven (i, totalSum)
          NEXT i
          Display totalSum
      END

      BEGIN CheckEven (num, totalSum)
          IF num MOD 2 = 0
              Add num to totalSum
          ENDIF
      END CheckEven
      ```



2. **Write pseudocode AND produce a flowhcart for each of the following Python programs:**
   1. ```python
      total_sum = 0

      for number in range(1, 11):
          total_sum += number

      print("The total sum is:", total_sum)


      ```
   2. ```python
      age = int(input("Enter your age: "))


      if age < 13:
          print("You are a Child.")
      elif 13 <= age <= 19:
          print("You are a Teenager.")
      elif 20 <= age <= 64:
          print("You are an Adult.")
      else:
          print("You are a Senior.")
          
          
      ```
   3. ```python
      N = int(input("Enter a number N: "))

      for i in range(1, N+1):  
          print(f"Checking number {i}:")
          
          if i < 10:
              print(f"{i} is less than 10.")
          elif i > 10:
              print(f"{i} is greater than 10.")
          else:
              print(f"{i} is equal to 10.")
              
              
      ```
   4. <pre class="language-python"><code class="lang-python"><strong>def calculate_factorial(num):
      </strong>    factorial = 1
          for i in range(1, num + 1):
              factorial *= i
          return factorial
          
      number = int(input("Enter a number: "))

      factorial_result = calculate_factorial(number)

      print(f"The factorial of {number} is {factorial_result}.")


      </code></pre>

