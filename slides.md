---
title-slide: false
bibliography: references.bib
csl: vancouver.csl
citeproc: true
theme: serif
background-color: "#ffffff"
transition: slide
navigationMode: linear
hash: true
---

:::: {.columns}
::: {.column width="50%"}

## Sample slides
#### PlaceHolderName
#### Universiti Malaysia Perlis
#### [placeholder@email.com](mailto:placeholder@email.com)

<audio id="bg-music" src="media/audio/sb.m4a" loop></audio>

<div id="audio-credit"
     style="position: absolute; bottom: 40px; right: 20px; font-size: 0.6em; opacity: 0.6;">
  Music: “Adrift” by Scott Buckley (CC BY 4.0)
</div>

<script>
  document.addEventListener('DOMContentLoaded', () => {
    const audio = document.getElementById('bg-music');
    const credit = document.getElementById('audio-credit');

    // hide credit by default
    credit.style.display = 'none';

    const test = new Audio('media/audio/bgm.mp3');

    test.addEventListener('canplaythrough', () => {
      // bgm.mp3 exists → use it, keep credit hidden
      audio.src = 'media/audio/bgm.m4a';
    }, { once: true });

    test.addEventListener('error', () => {
      // bgm.mp3 missing → sb.m4a will play → show credit
      credit.style.display = 'block';
    }, { once: true });

    document.addEventListener('click', () => {
      if (Reveal.getIndices().h === 0) {
        audio.volume = 0.5;
        audio.play();
      }
    }, { once: true });

    Reveal.on('slidechanged', (event) => {
      if (event.indexh > 0) { audio.pause(); }
      else { audio.play(); }
    });
  });
</script>

:::

::: {.column width="50%"}
![](media/pics/logo1.png)
:::

::::

---

:::: {.columns}
::: {.column width="50%"}
### Slide one
**Key Concepts:**
- Energy conservation per @carnot1824.
- $\Delta U = Q - W$
:::

::: {.column width="50%"}
![](media/pics/sample.png)
:::
::::

---

<span class="slide-title" data-title="My Hidden Slide Name"></span>

![](media/pics/wide.jpeg)

---

:::: {.columns}
::: {.column width="50%"}
### The Master Equation
The fundamental relation of thermodynamics:

$$\Delta U = Q - W$$

The work done $W$ is positive when the system expands against an external pressure.
:::

::: {.column width="50%"}
<video data-src="media/videos/sample.mp4" data-autoplay loop muted width="100%"></video>
:::

::::

---

:::: {.columns}
::: {.column width="50%"}
### Visualizing the Gas Law
**Interactive Model:**

- P, V, and T relationships.
- Use the slider to adjust pressure.
- Observe the phase boundary.
:::

::: {.column width="50%"}
<iframe 
  data-src="media/plots/sample.html" 
  width="100%" 
  height="500px" 
  style="border:none;" 
  scrolling="no">
</iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Distribution of Math Scores

This histogram displays the frequency distribution of Math scores from the `bigclass` dataset. It provides insight into the spread and central tendency of student performance in mathematics. The bins are set to a width of 50 to show the grouping of scores.
:::

::: {.column width="50%"}
<iframe 
  data-src='media/plots/math_scores_histogram.html' 
  width='100%' 
  height='500px' 
  style='border:none;'>
</iframe>
:::

::::

---

:::: {.columns}
::: {.column width="50%"}
### Math Scores Boxplot

This boxplot illustrates the distribution of Math scores, showing the median, quartiles, and potential outliers. It complements the histogram by providing a different perspective on the score spread.
:::

::: {.column width="50%"}
<iframe 
  data-src='media/plots/math_boxplot.html' 
  width='100%' 
  height='500px' 
  style='border:none;'>
</iframe>
:::

::::

---

:::: {.columns}
::: {.column width="50%"}
### Verbal Scores Boxplot

This boxplot visualizes the distribution of Verbal scores, providing insights into their central tendency, variability, and any extreme values. It offers a quick summary of the score distribution.
:::

::: {.column width="50%"}
<iframe 
  data-src='media/plots/verbal_boxplot.html' 
  width='100%' 
  height='500px' 
  style='border:none;'>
</iframe>
:::

::::

---


---

:::: {.columns}
::: {.column width="50%"}
### Math Scores vs. Age

This scatter plot visualizes the relationship between students' Math scores and their age, with points colored by gender. It helps in identifying any trends or clusters related to age and gender in mathematical performance.
:::

::: {.column width="50%"}
<iframe
  data-src='media/plots/math_vs_age_scatterplot.html'
  width='100%'
  height='500px'
  style='border:none;'>
</iframe>
:::

::::


---

:::: {.columns}
::: {.column width="50%"}
### Verbal Scores by Gender

This bar chart illustrates the average Verbal scores for male and female students. It provides a clear comparison of verbal performance between genders in the dataset.
:::

::: {.column width="50%"}
<iframe
  data-src='media/plots/verbal_gender_bar_chart.html'
  width='100%'
  height='500px'
  style='border:none;'>
</iframe>
:::

::::

---

:::: {.columns}
::: {.column width="50%"}
### Distribution of Student Ages

This histogram illustrates the distribution of ages among students in the `bigclass` dataset. It provides a visual representation of how student ages are spread, helping to identify common age groups and any outliers.
:::

::: {.column width="50%"}
<iframe
  data-src='media/plots/age_histogram.html'
  width='100%'
  height='500px'
  style='border:none;'>
</iframe>
:::

::::
