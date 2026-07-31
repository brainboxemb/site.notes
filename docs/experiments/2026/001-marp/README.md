# EXP-2026-001 — Marp

Experiment with creating presentations using Markdown and Marp.

* **Started:** 2026-07-28
* **Status:** In progress

## Background information / Tutorials

- https://dev.to/chris_ayers/unleash-your-creativity-with-marp-presentation-customization-1cpn  
Nice general introduction
- https://miriam-mueller.com/marp-vscode-setup/  
  Information on style sheet



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
```

## Step 3 — Align content to the top

By default, Marp places the slide content vertically in the middle.

Add the following style to the front matter of `presentation.md`:

```yaml
---
marp: true
theme: default
paginate: true
style: |
  section {
    align-content: start;
  }
---
```

The content of each slide now starts at the top.

### Result

*To be completed after performing this step.*


## Step 4 — Create a two-column slide

Create a slide with three images and short captions on the left and text on the right.

Add the following style to the front matter of `presentation.md`:

```yaml
style: |
  section {
    align-content: start;
  }

  .columns {
    display: grid;
    grid-template-columns: 40% 60%;
    gap: 30px;
  }

  .images {
    display: flex;
    flex-direction: column;
    gap: 12px;
  }

  .image-block {
    text-align: center;
  }

  .image-block img {
    width: 100%;
    max-width: 320px;
    max-height: 140px;
    object-fit: contain;
  }

  .caption {
    margin-top: 3px;
    font-size: 15px;
    line-height: 1.2;
  }
```

Create the slide using:

```html
---

# Two-column layout

<div class="columns">

<div class="images">

<div class="image-block">
<img src="./images/image-1.png" alt="First image">
<div class="caption">Short explanation of the first image.</div>
</div>

<div class="image-block">
<img src="./images/image-2.png" alt="Second image">
<div class="caption">Short explanation of the second image.</div>
</div>

<div class="image-block">
<img src="./images/image-3.png" alt="Third image">
<div class="caption">Short explanation of the third image.</div>
</div>

</div>

<div>

## Text

The text is displayed on the right side of the slide.

- First observation
- Second observation
- Third observation

</div>

</div>
```

The image size can be adjusted using `max-width` and `max-height`.

### Result

*To be completed after performing this step.*


## Step 6 — Create a reusable theme

Move the presentation styling from the Markdown file to a separate reusable Marp theme.

Create the theme file:

```text
themes/theme_basic.css
```

Register the theme in:

```text
.vscode/settings.json
```

```json
{
  "markdown.marp.themes": [
    "./themes/theme_basic.css"
  ]
}
```

The CSS file starts with a theme name and imports the default Marp theme:

```css
/* @theme theme-basic */

@import 'default';
```

Use the theme in the presentation front matter:

```yaml
---
marp: true
theme: theme-basic
paginate: true
---
```

The presentation styling can now be reused without including the CSS in every Markdown file.

### Result

*To be completed after performing this step.*
