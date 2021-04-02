#                                                                  Assignment-4
## AIM
In this assignment we will be using python to find the fourier series cofficient of the two functions e(x) and cos(cos(x)) using the known formulae. After that we will try to find out the best possible cofficients using least square method and then we will compare both the cofficients and plot their graphs
### INTRODUCTION
we begin by plotting the two graphs in the interval -2pi to 4pi.
Plot e(x) in semilogy because it increases rapidly.
After this we will find the fourier series cofficients using the least square method and compare them
![Figure1](https://user-images.githubusercontent.com/81006760/113396951-f3982780-93b9-11eb-9f6f-77d388b8b964.png)
Figure1 cos(cos(x)) plot
![Figure_2](https://user-images.githubusercontent.com/81006760/113397438-ab2d3980-93ba-11eb-8429-07040d320a2c.png)
Figure2 semilogy plot of e(x)
#### FOURIER COFFICIENTS
Calculating the fourier cofficients
We calculate the fourier cofficients using the formula given in the assignment.Then we store the value in the format of a vector(a0,a1,b1,a2,b3,......,a25,b25).
Plotting the cofficients
We plot the cofficients an,bn vs n using the semilogy and loglog plots
![Figure_3](https://user-images.githubusercontent.com/81006760/113398001-8b4a4580-93bb-11eb-8c65-742f6f665ba9.png)
Figure3 semilogy plot of Cofficients of e(x) vs n
![Figure_4](https://user-images.githubusercontent.com/81006760/113398007-8d140900-93bb-11eb-891c-26551e431920.png)
Figure4 loglog plot of cofficients of e(x) vs n
![Figure_5](https://user-images.githubusercontent.com/81006760/113398010-8dac9f80-93bb-11eb-88da-e78946726861.png)
Figure5 Semilogy plot of cofficients of cos(cos(x)) vs n
1.Since the cos(cos(x)) is basically a modified cosine function ,the fourier cofficients of sine in the series will be very close to zero.
2.The exponential function contains many harmonics of different frequencies whereas the cos(cos(x)) contains limited harmonics hence they decay faster.
3.In the first case e(x) the fourier cofficients are very large and decay after many harmonics whereas in the second case [cos(cos(x))] the fourier cofficients decay quickly.
![Figure_6](https://user-images.githubusercontent.com/81006760/113398515-5b4f7200-93bc-11eb-942b-12154ac258b8.png)
Figure6 loglog plot of cofficients of cos(cos(x))
##### Least Square Cofficients
Calculating the cofficients
We will use the least square method to minimise the lstsq error and find out the best possible cofficients for both the functions. We first construct a matrix and then find out the best possible cofficients satisfying the equation.
AX=Y
where Y is vector containing values of the function and X is the vector containing cofficients
Plotting the cofficients 
This is done in the same way as in the fourier cofficients ,using yhe same code.These cofficients are also plotted in semilogy and loglog for both the functions.They can be seen in Figure 3,4,5,6.We also find out the max deviation between the cofficients,it turns out to be
![Figure_7](https://user-images.githubusercontent.com/81006760/113399237-84243700-93bd-11eb-9a64-96d92c881177.png)
Figure7 cos(cos(x))
![Figure_8](https://user-images.githubusercontent.com/81006760/113399253-8ab2ae80-93bd-11eb-8284-c7178bb3a904.png)
Figure8 e(x)
###### Conclusion
We have observed that both fourier cofficients and lstsq cofficients do not vary much.When we plot both the original function and the computed function us- ing cofficients, we see that in the case of the exponential function there is a lot of variation but in the case of cos(cos(x)) it is the same. This is because exponential has many harmonics, we considered only 51 coefficients.This causes considerable error. In the case of cos(cos(x)) 51 cofficients are enough to represent the function accurately as the cofficients decay rapidly.
