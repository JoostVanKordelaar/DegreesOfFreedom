

#' @export
dof <- function(){
  # Define UI for application that draws a histogram
  ui <- shiny::fluidPage(

    # Application title
    shiny::titlePanel("Constraints on the data determine Degrees of Freedom"),

    # Initiate sidebarlay-out
    shiny::sidebarLayout(
      # Iniate sidebar panel
      shiny::sidebarPanel(

        # Add sliders
        #n1
        shiny::sliderInput("n1", "n1:",
                           min = -5, max = 5,step = 0.01,
                           value = 0),
        #n2
        shiny::sliderInput("n2", "n2:",
                           min = -5, max = 5,step = 0.01,
                           value = 0),
        #n3
        shiny::sliderInput("n3", "n3:",
                           min = -5, max = 5,step = 0.01,
                           value = 0),
        #n4
        shiny::sliderInput("n4", "n4:",
                           min = -5, max = 5,step = 0.01,
                           value = 0),
        #n5
        shiny::sliderInput("n5", "n5:",
                           min = -5, max = 5,step = 0.01,
                           value = 0),
        #n6
        shiny::sliderInput("n6", "n6:",
                           min = -5, max = 5,step = 0.01,
                           value = 0),
        #n7
        shiny::sliderInput("n7", "n7:",
                           min = -5, max = 5,step = 0.01,
                           value = 0),
      ),

      # Show a plot of the data sliders
      # but first initiate a main panel
      shiny::mainPanel(
        # show the plot
        shiny::plotOutput("dataPlot")
      )
    )
  )

  # Define server logic required to plot the data
  server <- function(input, output) {

    output$dataPlot <- shiny::renderPlot({
      # generate bins based on input$bins from ui.R
      yData <- c(input$n1,input$n2,input$n3,input$n4,input$n5,input$n6,input$n7)
      sliderData <- data.frame(xData = 1:7,yData = yData)

      # draw the scatter plot with the data points defined by the sliders
      p <- ggplot2::ggplot(data = sliderData,mapping = ggplot2::aes(x=xData,y=yData)) +
        ggplot2::geom_point() +
        ggplot2::coord_cartesian(xlim = c(0,8),ylim = c(-6,6))
      p
    })
  }

  # Run the application
  shiny::shinyApp(ui = ui, server = server)
}
