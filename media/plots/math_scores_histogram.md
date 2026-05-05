
p_math_histogram <- bigclass %>%
  plot_ly(x = ~Math, type = 'histogram',
          marker = list(color = '#0072B2', line = list(color = 'white', width = 1))) %>%
  layout(title = list(text = 'Distribution of Math Scores', font = list(size = 20)),
         xaxis = list(title = list(text = 'Math Score', font = list(size = 18)), tickfont = list(size = 14)),
         yaxis = list(title = list(text = 'Frequency', font = list(size = 18)), tickfont = list(size = 14)),
         plot_bgcolor = 'white',
         paper_bgcolor = 'white')

# Save the plot as an HTML widget
htmlwidgets::saveWidget(p_math_histogram, 'media/plots/math_scores_histogram.html', selfcontained = TRUE)
