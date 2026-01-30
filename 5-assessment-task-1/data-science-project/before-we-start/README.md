---
icon: book-open
---

# Before we Start

&#x20;

{% hint style="warning" %}
## KEEP IT SIMPLE!

This project is about **project management.** You do **NOT** need to have enormously complicated programs to succeed here.
{% endhint %}

You need to take the following steps to ensure effective documentation and version control:

* **Create Markdown Files**: Document the development process in **`PROJECT_DEVELOPMENT.md`** within your GitHub repository. Ensure clarity by adding comments to your code explaining each function and major steps.

{% embed url="https://www.markdownguide.org/basic-syntax/" %}
Markdown Basic Syntax Guide
{% endembed %}

* **Compose a README.md**: Write a concise README.md file detailing how to execute the application and any required dependencies.

### Example:

{% code title="README.md" %}
```markdown
# Project Title

Brief description of the project.

## Installation

Clone the repository and navigate to the project directory:
.....
```
{% endcode %}

Install the required dependencies:

```bash
pip install -r requirements.txt
```

* **Prepare requirements.txt**: Include a requirements.txt file to facilitate the installation process for users.&#x20;

### Example:

<pre data-title="requirements.txt"><code><strong>pandas==1.5.3
</strong>matplotlib==3.6.2
</code></pre>

* **Commit Changes**: Every time changes are made to the code or documentation, use a GitHub commit to describe the modifications. A scaffold will be provided to guide your reflective writing.





