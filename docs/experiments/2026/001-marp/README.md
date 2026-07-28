# EXP-2026-001 — Marp

Experiment with creating presentations using Markdown and Marp.

* **Started:** 2026-07-28
* **Status:** In progress

## Step 1 — First presentation

Install the **Marp for VS Code** extension and create a first presentation.

Create:

```text
steps/001-first-presentation/presentation.md
```

The presentation contains:

1. A title slide
2. A short introduction to Marp
3. The goal of the experiment
4. Planned next steps

```markdown
---
marp: true
theme: default
paginate: true
---

# Marp Experiment

Creating presentations with Markdown.

---

# What is Marp?

Marp is a tool for creating presentations using Markdown.

Slides are separated using three dashes.

---

# Experiment Goal

Explore how Marp can be used to:

- create presentations;
- preview slides in Visual Studio Code;
- add images and styling;
- export presentations.

---

# Next Steps

- Test slide layouts
- Add images
- Test themes
- Export the presentation
```

Open the Markdown preview in Visual Studio Code to view the presentation.

### Result

A presentation should be visible. The actual result will be saved as PDF in the next step.


## Step 2 — Export to PDF

Export the presentation so it can be viewed outside Visual Studio Code.

Click the Marp icon in the editor toolbar:

![Marp icon in the Visual Studio Code toolbar](./_images/marp-export-icon.png ':size=420')

Select **Export slide deck...**, choose **PDF** and save the result as:

```text
steps/001-first-presentation/presentation.pdf