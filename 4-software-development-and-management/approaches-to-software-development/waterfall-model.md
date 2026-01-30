---
icon: book-open
cover: >-
  https://images.unsplash.com/photo-1509018778968-5341380562c0?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHw2fHx3YXRlcmZhbGx8ZW58MHx8fHwxNzM5NjgzMzcxfDA&ixlib=rb-4.0.3&q=85
coverY: 0
---

# Waterfall Model

The structured approach to software development consists of distinct stages. Each stage needs to be completed before the next stage can commence. This is necessary as teams of developers with varying skills and responsibilities are involved in the development process. For example, the coding of the solution cannot commence until the solution has been thoroughly planned in its entirety. The personnel coding the solution are often different to those who plan the solution.&#x20;

The traditional stages of the Structured Approach to software development include:&#x20;

* Requirements definition
* Determining specifications&#x20;
* Design&#x20;
* Development&#x20;
* Integration&#x20;
* Testing and debugging
* Installation&#x20;
* Maintenance

This approach is generally used for large-scale projects where performance and reliability are vital requirements. A large audience will use the final product so even relatively minor errors may prove costly. It is worth spending extra time and money to ensure the final product is of the highest quality. This structured approach is also known as the Waterfall approach as each step leads to the next sequentially.&#x20;

<figure><img src="../../.gitbook/assets/image (25).png" alt=""><figcaption><p>The Waterfall model - a structured and linear approach to development</p></figcaption></figure>

Because of the structured nature of this method, it is particularly suited to software development where all the requirements and specifications can be defined before any design commences. Generally, these are large-scale projects requiring a full development team and the timeframe is long with a large budget. If safety is important and or a bespoke solution is required, then the Structured Approach is likely the most suitable.&#x20;

{% embed url="https://www.youtube.com/watch?v=5A5XCuWMG4o" %}
Waterfall Process
{% endembed %}

{% hint style="warning" %}
Please note that we have a very specific set of steps in the Software Engineering Syllabus (look to the diagram further up the page for these) - not everyone uses the same steps in industry, though they're similar enough it's not an issue.
{% endhint %}



### When is the Waterfall approach appropriate?

Waterfall is still used in industries where **stability, predictability, and regulatory compliance** are essential. These projects typically have **well-defined requirements** and require extensive upfront planning because changes later are costly or risky.

The following factors would likely lead to a waterfall approach:

* **Strict regulatory requirements** (e.g., FDA, FAA, ISO).
* **High-stakes environments** where failure is unacceptable.
* **Fixed budgets & timelines**, where changes are costly.
* **Hardware dependencies** that require finalised specifications.



### **Example: Developing Software for a Medical Device**

**Scenario:** A company is creating embedded software for a **pacemaker** (a device that regulates heartbeats).

**Why Waterfall?**

* **Strict Regulations** – Medical software must comply with government and industry standards (e.g., FDA, ISO).
* **Clear, Stable Requirements** – The software’s core functions (e.g., detecting heart arrhythmias, delivering electrical pulses) are well-defined upfront.
* **High-Risk Consequences** – Bugs could be life-threatening, so thorough planning and rigorous testing are required.

**Waterfall Process:**

* **Requirements Definition** – Engineers gather detailed requirements from doctors, regulators, and hardware teams, ensuring all safety and medical needs are documented.
* **Determining Specifications** – The team defines precise technical specifications, including response times, power consumption, and integration with heart monitoring sensors
* **Design** – A complete system architecture is created, outlining how the software will process heart data, trigger electrical impulses, and fail safely in case of errors.
* **Development** – Engineers write the software according to the approved design, ensuring it meets safety and performance standards.
* **Integration** – The software is integrated with the pacemaker hardware and tested with various heart conditions to ensure proper functionality.
* **Testing and Debugging** – Extensive simulations, lab tests, and regulatory audits are conducted to verify accuracy, reliability, and compliance with FDA guidelines.
* **Installation** – Once approved, the software is installed in pacemakers before they are shipped for medical use.
* **Maintenance** – Updates are rare due to strict regulations, but if necessary, patches go through rigorous re-certification before deployment.

