# Eikon Take Home Assignment

### What I did:
I first did some initial exploration of the data to see what aspects of it were sigmoidal. After splitting the data up by molecule type, the curves began to appear. 

I wrote two curve-fitting routines. The first one, plot_fit_curve, inputted the data for each molecule type into the Scipy curve_fit function and retrieved the optimal parameters. The second curve-fitting routine is least_squares_fit, which used the fact that the best least-squares estimate for any given point at X=x is E(Y|X). The least_squares_fit function ultimately performed worse than plot_fit_curve, so I decided to use plot_fit_curve for the rest of the assignment. I wrote a function for removing outliers which I also used. Documentation for all these functions is written in the docstrings.

The sigmoidal function I used is:
![equation](https://latex.codecogs.com/svg.image?y=%5Cfrac%7BL%7D%7B1&plus;e%5E%7B-k(x-x_0)%7D%7D%20&plus;%20b)

The curve fitting function returns the parameters ![equation](https://latex.codecogs.com/svg.image?L%20,x_0,%20k,%20b) in that order.

I also wrote functions to calculate general statistics about the plots such as r^2, standard deviation (of residuals), and root mean squared error. 
