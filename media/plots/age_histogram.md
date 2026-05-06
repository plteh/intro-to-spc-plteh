library(ggplot2); library(plotly); library(htmlwidgets)
p <- ggplot(bigclass, aes(x = age)) +
    geom_histogram(binwidth = 1, fill = '#0072B2', color = 'white', alpha = 0.8) +
    labs(title = 'Distribution of Student Ages', x = 'Age', y = 'Frequency') +
    theme_minimal(base_size = 18) +
    theme(
        plot.title = element_text(size = 20),
        axis.title.x = element_text(size = 18),
        axis.title.y = element_text(size = 18),
        axis.text.x = element_text(size = 14),
        axis.text.y = element_text(size = 14),
        panel.background = element_rect(fill = 'white', colour = 'white'),
        plot.background = element_rect(fill = 'white', colour = 'white')
    )
