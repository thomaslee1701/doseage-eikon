# Eikon Take Home Assignment

### What I did:
I first did some initial exploration of the data to see what aspects of it were sigmoidal. After splitting the data up by molecule type, the curves began to appear. 

I wrote two curve-fitting routines. The first one, plot_fit_curve, inputted the data for each molecule type into the Scipy curve_fit function and retrieved the optimal parameters. The second curve-fitting routine is least_squares_fit, which uses the fact that the best least-squares estimate for any given point at X=x is E(Y|X). The least_squares_fit function ultimately performed worse than plot_fit_curve, so I decided to use plot_fit_curve for the rest of the assignment. 

The sigmoidal function I $$L$$
