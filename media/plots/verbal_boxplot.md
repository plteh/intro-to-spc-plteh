# R Code for Verbal Scores Boxplot

```R
library(tidyverse)
library(plotly)

p_verbal_boxplot <- ggplot(bigclass, aes(y = Verbal)) +
  geom_boxplot(fill = '#D55E00', color = 'black', alpha = 0.8) +
  labs(
    title = 'Distribution of Verbal Scores (Boxplot)',
    y = 'Verbal Scores'
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

htmlwidgets::saveWidget(plotly::ggplotly(p_verbal_boxplot), 'media/plots/verbal_boxplot.html', selfcontained = TRUE)
```
