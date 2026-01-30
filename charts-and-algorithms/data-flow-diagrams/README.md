---
icon: book-open
---

# Data Flow Diagrams

Data Flow Diagrams (DFDs) map the journey of data through a system, focusing on data movement and transformation without detailing the timing or the step-by-step logic of processes.

DFD's are similar to a railroad map that shows tracks but not schedules, DFDs illustrate where and how data flows and changes across processes, which always modify data.

The diagrams use labelled arrows for data flow direction, circles for processes (emphasising action with verbs), and open rectangles for data stores—places where data rests before or after processing, allowing for process independence.

Data stores are depicted as files or databases, enabling processes to operate asynchronously or remain idle as needed.

DFDs facilitate a top-down design approach by breaking down a system into increasingly detailed subprocesses, from the overview provided by a Level 0 Context Diagram through to detailed lower-level diagrams that outline specific subprocesses, potentially excluding already-defined external entities or data stores for clarity.

## Symbols

<figure><img src="../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

## Example

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption><p>DFD for a Voting System</p></figcaption></figure>



## System Scope & Boundaries (Level 0 DFD)

Context Diagrams, or Level 0 Data Flow Diagrams, depict the entire system as a single process, focusing on the data inputs from and outputs to the external environment, without detailing internal processes.

These diagrams highlight the sources (inputs) and destinations (outputs) of data, termed "external entities," which are outside but interact with the system.

* System is shown as a circle
* External entities are represented by squares.
* Data flow is illustrated with arrows, labelling the type of data and its flow direction.

Context diagrams serve as high-level views, showing how the system exchanges data with its environment, including users, other organisations, and systems, without delving into the system’s internal workings.

<figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption><p>Context Diagram (Level 0 DFD) of a Voting System</p></figcaption></figure>

## Further Explanation and Support

### Intro to Context / Level 0 DF Diagrams

{% embed url="https://www.youtube.com/watch?list=PLyH7UFQzuDWekJIt3TEzDtE-TORqGkz_r&v=7pgSHVIOX-g" %}
Context Diagrams (Level 0 DFD)
{% endembed %}

### **Intro to DFDs**

{% embed url="https://www.youtube.com/watch?index=2&list=PLyH7UFQzuDWekJIt3TEzDtE-TORqGkz_r&v=vOIsQc1S3pA" %}

### **Example: YouTube**

{% embed url="https://www.youtube.com/watch?index=3&list=PLyH7UFQzuDWekJIt3TEzDtE-TORqGkz_r&v=hiMeEswjWuk" %}
Example: YouTube Context and DF Diagram
{% endembed %}

### Example: Red Light Camera

{% embed url="https://www.youtube.com/watch?index=6&list=PLyH7UFQzuDWekJIt3TEzDtE-TORqGkz_r&v=aY-BRagWGN0" %}
Example: Red Light Camera
{% endembed %}

