# CartPole-GA
> Assignment for university course (EECE 699 - Topics in AI @ AUB) where we have to implement a Genetic Algorithm to solve the Cart-Pole problem.

## Data generation
To generate the data, we ran the environment n_collect times, keeping track of the score and taking random actions. We would keep running this until either we reach our goal_steps or until the environment tells us it is done. If the score acquired is greater than th_score, we would save this game as training data.

## First GA model
For the first iteration, we were able to generate 2462 training data with an average score of 61: we had specified the threshold score to be 50. With a number of generations equal to 20, we were able to attain an average score of 130 (calculated on 1000 tries), and for the final run that generated the attached video labeled “low”, we achieved a score of 93.

https://user-images.githubusercontent.com/19833587/147213333-78ce442e-3385-463e-8826-0f4764d63fef.mp4

## Second GA model
For the second iteration, we were able to generate 673 training data with an average score of 113: we had specified the threshold score to be 100. With a number of generations equal to 50, we were able to attain an average score of 200 (calculated on 1000 tries), and for the final run that generated the attached video labeled “high”, we achieved a score of 200.

https://user-images.githubusercontent.com/19833587/147213354-85de6e90-ec67-4d30-98d2-840e30403402.mp4

## Comparison
We increased the number of n_collect from 1000 to 10000, th_score from 50 to 100 and num_generations from 20 to 50. This should increase the score that we get since we now have a higher acceptable score, and we will have more generations that would better perform.
The increase in average and total score is consistent with our changes in initial values. The average score increased from 130 to 200 (the max that we are aiming for since it is Cart-Pole v0), the final score increased from 93 to 200 as well. This can be clearly seen via the video where the one for the lower initial parameters is shorter and ends because of a very high angle, while the second ends because we achieved the 200-score mark.
