# R Code for Math Scores Boxplot

```R
library(tidyverse)
library(plotly)

p_math_boxplot <- ggplot(bigclass, aes(y = Math)) +
  geom_boxplot(fill = '#0072B2', color = 'black', alpha = 0.8) +
  labs(
    title = 'Distribution of Math Scores (Boxplot)',
    y = 'Math Scores'
  ) +
  theme_minimal() +
  theme(
    plot.title = element_text(size = 20, face = 'bold'),
    axis.title.y = element_text(size = 18),
    axis.text.y = element_text(size = 14),
    axis.text.x = element_blank(),
    axis.ticks.x = element_blank(),
    panel.background = element_rect(fill = 'white', colour = 'white'),
    plot.background = element_rect(fill = 'white', colour = 'white')
  )

htmlwidgets::saveWidget(plotly::ggplotly(p_math_boxplot), 'media/plots/math_boxplot.html', selfcontained = TRUE)
```
