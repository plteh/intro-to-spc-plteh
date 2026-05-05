library(ggplot2); library(plotly); library(htmlwidgets)
p <- ggplot(bigclass, aes(x = sex, y = Verbal, fill = sex)) +
    geom_bar(stat = 'summary', fun = 'mean', color = 'white') +
    scale_fill_manual(values = c('F' = '#D55E00', 'M' = '#0072B2')) +
    labs(title = 'Average Verbal Scores by Gender', x = 'Gender', y = 'Verbal Score') +
    theme_minimal(base_size = 18) +
    theme(
        plot.title = element_text(size = 20),
        axis.title.x = element_text(size = 18),
        axis.title.y = element_text(size = 18),
        axis.text.x = element_text(size = 14),
        axis.text.y = element_text(size = 14),
        legend.position = 'none',
        panel.background = element_rect(fill = 'white', colour = 'white'),
        plot.background = element_rect(fill = 'white', colour = 'white')
    )
