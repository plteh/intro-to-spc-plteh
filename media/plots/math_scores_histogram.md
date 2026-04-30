# R Code for Math Scores Histogram

```R
library(tidyverse)
library(plotly)

p <- ggplot(bigclass, aes(x = Math)) +
  geom_histogram(binwidth = 50, fill = '#0072B2', color = 'white', alpha = 0.8) +
  labs(
    title = 'Distribution of Math Scores',
    x = 'Math Scores',
    y = 'Frequency (count)'
  ) +
  theme_minimal() +
  theme(
    plot.title = element_text(size = 20, face = 'bold'),
    axis.title.x = element_text(size = 18),
    axis.title.y = element_text(size = 18),
    axis.text.x = element_text(size = 14),
    axis.text.y = element_text(size = 14),
    panel.background = element_rect(fill = 'white', colour = 'white'),
    plot.background = element_rect(fill = 'white', colour = 'white')
  )

htmlwidgets::saveWidget(plotly::ggplotly(p), 'media/plots/math_scores_histogram.html', selfcontained = TRUE)
```
