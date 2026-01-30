---
icon: book-open
---

# Structure Charts

Structure charts illustrate the hierarchical organisation and execution sequence of subroutines within a system, including data exchanges to clarify their interrelations. These charts facilitate a top-down design approach, detailing how subroutines are called, including conditions and repetitions for these calls.

Essential for software development, structure charts serve as blueprints for coding, helping allocate tasks among developers and aiding in maintenance and upgrades by identifying potential error or upgrade sites.

Various names and drawing techniques exist for these diagrams, but they share a focus on depicting a system's hierarchical design, execution sequence, and decision-making processes.

Symbols used include rectangles for subroutines, lines for subroutine calls, diamonds for decisions, circular arrows for repetitions, and circles for data parameters, with filled circles representing control parameters that influence execution order.

Structure charts are read top-to-bottom for hierarchy and left-to-right for execution order, with subroutines appearing multiple times if called by different higher-level tasks.

## Symbols

<figure><img src="../../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>

## Example 1

<figure><img src="../../.gitbook/assets/image (38).png" alt=""><figcaption><p>Example of a Library Management System</p></figcaption></figure>

Further detail for each of the lower-level subroutines can be shown in a separate structure chart, using the same name as the subroutine used in the main structure chart. This method of providing successively more detail as required is known as refinement.

## Example 2 (with code)

The following is a **very simple** example to show you how this might look with a very basic Python program. It has no control variables (such as a login to check credentials), but has parameters, a decision structure and repetition.

To make it easy, the 'subroutines' of a Python program are simply functions within `main()`.

<figure><img src="../../.gitbook/assets/image (39).png" alt=""><figcaption><p>Simple Example with Python Code</p></figcaption></figure>

## Further Examples and Support

{% embed url="https://www.youtube.com/watch?v=kVV1TJ_VR0o" %}
Introduction to Structure Charts
{% endembed %}

{% embed url="https://www.youtube.com/watch?t=&v=1OfQ9f9-G7E" %}
Structure Chart Example - Streaming Software
{% endembed %}

