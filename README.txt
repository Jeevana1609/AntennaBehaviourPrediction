As there is no readily available dataset for our problem, we have simulated the required dataset using FEKO simulation software.

We have generated 800 samples in total.Where we tuned the parameters in such a way so that no two samples are similar to each other.
Here is the pattern we followed to tune the parameters.

For all 800 samples we have taken frequency as 1 GHz, Impedance as 50 Ω, wire
radius as 1 mm and relative permittivity which is infinite for perfect electric
conductor.
● Lambda is calculated using the formula c/f and in our case, it is 0.2997.
● For the first 400 samples we have taken ‘Radius of curvature (a)’ as lambda which is
equal to 0.2997.
● We tuned the angle(θ) from 15 ° to 45 ° considering 15 °, 20 °, 30 ° and 45° degrees.
● Distance between the curved surface and the antenna is dependent on a and θ.
● The minimum distance(d) is a/cosθ and we considered 20 values of d as 1*a/cosθ,
1.5*a/cosθ, 2*a/cosθ and so on 10.5*a/cosθ.
● We varied ‘h’ (height) as follows lambda/2, lambda/4, lambda, lambda*1.5, lamda*2.
● For each variation of ‘h’ we get 80 samples (20 from each angle).
● For all 5 variations of ‘h’ we got 400 samples.
● Then for next 400 samples we have taken ‘a’ as 2*lambda and repeated remaining
steps.
● In such a way we have generated 800 data samples.



Process of extracting one data sample in FEKO:

After tuning the parameters of the antenna in the variables column in feko, we need to click the feko solver in CADFEKO, select re-mesh, and select yes. Once the modifications are made to the model, save it now. Click on the POSTFEKO, a new window will open. There will be a requests option under the model browser and model in that window. Right-click
"FarField2'' under requests, and then select “Add to new '', Polar graph. The polar graph will now show up. By observing the polar graph, we can know the reflection pattern as
unidirectional or multidirectional. Right click on the polar graph and click “to file.” Save and open the file, and copy the values in the excel and find the maximum gain from the second column and its respective directivity from the first column. For each simulation, we observe the pattern of reflection and note down the maximum gain and direction of the maximum gain and pattern of reflection from the polar plot of the far-field.


We have attached a python file in zip folder which contains codes of all models that we used.
Upload the data set and run the files.