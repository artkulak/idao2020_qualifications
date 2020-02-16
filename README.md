# IDAO 2020 Online Stage
**Team: CHAD DATA SCIENTISTS**

**Solution passed top 30 (Final LB score - 93.72) **


* KUDOS to my teammates:
	- https://github.com/JustM57
	- https://github.com/blacKitten13

* How to get the data
   - input data folder from https://disk.yandex.ru/d/0zYx00gSraxZ3w

<hr>

## Instructions
1. Create "input" folder in the main directory and place input files into the folder.
2. If necessary, install packages in `art/requirements.txt`.
3. Run `art/FinalSolution.ipynb` to generate predictions for the test set (Our solution was developed for track A only)
    - It takes 5-6 hours to predict for 300 satellites.
4. You could check our other notebooks as well, these were our ideas that did not succeed.

<hr>

## Task description
IDAO participants are asked to clarify the prediction of a Simpliﬁed General Perturbations-4 (SGP4) model. 
SGP4 is able to predict a lot of effects but is applied to near-Earth objects with an orbital period of fewer than 225 minutes, while high orbit space objects have orbital periods up to 200 hours. 
For the true position of the satellites, the position obtained using a more accurate simulator will be taken. 
Subsequently, the obtained models will be applied to real classiﬁed data and will help to predict the positions of these space objects.

## Model description
The solution is based on pure phisics and is using Plyades library as the main component. We take the last point of the training set of each satellite (w.r.t time) and  run the simulation using Plyades library, 
which takes into account the Earth gravity. While simulating we generate data until the last point of the test set and then for each time point in the test set we take the closest point of the simulated data by time.
