# IDAO 2020 Online Stage
**Team: CHAD DATA SCIENTISTS**

**Solution passed top 30 (Final LB score - 93.72) and got us to the IDAO 2020 finals**


* KUDOS to my teammates:
	- https://github.com/JustM57
	- https://github.com/blacKitten13

* common
   - input data folder from https://disk.yandex.ru/d/0zYx00gSraxZ3w

<hr>

## Instructions
1. Place input files into "input/" folder.
2. If necessary, install packages in `requirements.txt`.
3. Run FinalSolution.ipynb to generate predictions for the test set (Our solution was developed for track A only)
    - It takes 5-6 hours to predict for 300 satellites.

<hr>

## Model description
*Plyades library forever*
The solution is based on pure phisics and is using Plyades library as the main component. We take the last point of the training set of each satellite (w.r.t time) and  run the simulation using Plyades library, 
which takes into account the Earth gravity. While simulating we generate data until the last point of the test set and then for each time point in the test set we take the closest point of the simulated data by time.