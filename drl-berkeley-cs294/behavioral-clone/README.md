# Work related to CS294-112 HW 1: Imitation Learning

# Dependencies: 
- TensorFlow
- MuJoCo version 1.31
- OpenAI Gym

# Usage
- Create directories, `/logs`, `/rollouts`.
- Generate expert rollouts
 
`$ ./runexpert.sh`

Will run `run_expert.py` for rollouts of 5, 10, 20, 40, 100 for the Humanoid-v1
environment. The rollouts will be stored in directory `/rollouts`, thus make sure
to create the directory before running.

- Clone based on samples from expert policy.

`$ ./runclone.sh`

Will run `behave_clone.py`, which will train on the provided data and output
results to the directory `/logs`.

The course provided the following files and directors.
- /experts
- load_policy.py
- run_expert.py
- tf_util.py

In `/experts`, the provided expert policies are:
* Ant-v1.pkl
* HalfCheetah-v1.pkl
* Hopper-v1.pkl
* Humanoid-v1.pkl
* Reacher-v1.pkl
* Walker2d-v1.pkl

The name of the pickle file corresponds to the name of the gym environment.

To solve the assignment, the following were created.
- bc_util.py
- bc_callbacks.py
- behave_clone.py
- runexpert.sh
- runclone.sh
