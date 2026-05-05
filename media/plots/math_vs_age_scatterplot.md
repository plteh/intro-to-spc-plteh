library(ggplot2); library(plotly); library(htmlwidgets)
p <- ggplot(bigclass, aes(x = age, y = Math, color = sex)) +
    geom_point(alpha = 0.7, size = 3) +
    scale_color_manual(values = c('F' = '#D55E00', 'M' = '#0072B2')) +
    labs(title = 'Math Scores vs. Age by Gender', x = 'Age', y = 'Math Score') +
    theme_minimal(base_size = 18) +
    theme(
        plot.title = element_text(size = 20),
        axis.title.x = element_text(size = 18),
        axis.title.y = element_text(size = 18),
        axis.text.x = element_text(size = 14),
        axis.text.y = element_text(size = 14),
        legend.position = 'bottom',
        legend.title = element_blank(),
        panel.background = element_rect(fill = 'white', colour = 'white'),
        plot.background = element_rect(fill = 'white', colour = 'white')
    )
