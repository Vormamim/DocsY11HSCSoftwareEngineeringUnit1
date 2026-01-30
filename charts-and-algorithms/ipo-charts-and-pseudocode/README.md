---
icon: book-open
---

# IPO Charts and Pseudocode

Your old primary school teacher has heard that you are studying Software Engineering and has approached you with a request for help.

‘My Year 4 maths class are learning about different types of triangles and I would like some educational software that would help them identify each type.’

In discussion with this ‘client’ you have familiarised yourself with the rules for identifying triangles:

* All triangles have 3 sides.
* Equilateral: equilateral triangles have 3 equal sides and 3 equal angles of 60°.
* Isosceles: isosceles triangles have 2 equal sides and 2 equal angles.
* Right-angled: one of the angles is a right angle (90°) in right-angled triangles.
* Scalene: scalene triangles have no equal sides and no equal angles.

**Specification 1:** To keep your software simple and age appropriate you will keep the entry of data into the software as the length of each side of the triangle:

* Side a=?
* Side b=?
* Side c=?

**Specification 2:** The user will click a button  labelled "What type of triangle has these sides?" to reveal the triangle type and the reason why it is classified as such to reinforce the key facts.

## IPO Chart

A useful tool to understand the problem and clarify the design is to use an IPO (Input, Process, Output) chart.

**Step 1**: Start with the output - specify what the program is required to do.

![IPO Outputs](https://github.com/jamesking020773/jamesking020773.github.io/blob/main/images/ipo1.jpg?raw=true)

**Step 2**: What are the inputs you need to get to the output?

![IPO Inputs](https://github.com/jamesking020773/jamesking020773.github.io/blob/main/images/ipo2.jpg?raw=true)

**Step 3**: What processes will change the inputs (calculate/combine/collate) to get to the output?

![IPO Process](https://github.com/jamesking020773/jamesking020773.github.io/blob/main/images/ipo3.jpg?raw=true)

{% embed url="https://www.youtube.com/watch?v=a10a11oxjrA" %}



## Processes

The processes used to turn inputs into outputs at the fundamental level are;

* **Sequence** - step by step commands
* **Selection** - binary IF statements or multiway.
* **Iteration** - looping (counted, pre- or post-test loops).

These processes can be combined in many ways to solve most problems.&#x20;

#### Process 1

**Check for Equilateral Triangle**

An equilateral triangle has all three sides of equal length.

Logical Check: If a=b AND b=c then the triangle is equilateral.

#### Process 2

**Check for Isosceles Triangle**

An isosceles triangle has at least two sides of equal length.

Logical Check: If a=b OR b=c then the triangle is isosceles.

#### Process 3

**Check for Scalene Triangle**

A scalene triangle has all sides of different lengths.

Logical Check: If a<>b AND b<>c AND a<>c then the triangle is scalene.

#### Process 4

**Check for Right-Angled Triangle**

A right-angled triangle satisfies Pythagorean theorem.

Logical Check: If a^2 + b^2 = c^2 where c is the length of the longest side of the triangle.

## Processes as Algorithms - Pseudocode

We use pseudocode in the design phase to represent how an algorithm will function without having to program and test it. Pseudocode is a great tool for simplifying our algorithms in plain language.&#x20;

We will complete more activities on this later, but for now, here are a few examples of the above program:

#### Process 1

<pre class="language-python"><code class="lang-python">BEGIN Equilateral
<strong>    Get SideA
</strong>    Get SideB
    Get SideC
    IF SideA = SideB = SideC THEN
        Display “Equilateral triangle”
    ENDIF 
END Equilateral 
</code></pre>

#### Process 2

```python
BEGIN triangle
    Get SideA
    Get SideB
    Get SideC
    IF SideA = SideB OR SideB = SideC OR SideA = SideC THEN
        Display “Isosceles triangle”
    ENDIF
END triangle
```

#### Process 3

```python
BEGIN triangle
    Get SideA
    Get SideB
    Get SideC
    IF SideA <> SideB <> SideC THEN
        Display “Scalene triangle”
    ENDIF
END triangle
```

#### Process 4

```python
BEGIN triangle
    Get SideA
    Get SideB
    Get SideC
    IF SideC^2 = SideA^2 + SideB^2 THEN
        Display “Right angle triangle”
    ENDIF
END triangle
```
