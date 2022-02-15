# Action Quantization based on Information Bottleneck

## Installation

1. Install our `rl_utils` module:

```bash
cd rl-algorithm
pip install -e .
```

2. Install mujoco: please follow the instruction of [official website](https://github.com/openai/mujoco-py).
3. Install Atari and Box2d:

```bash
sudo apt-get install swig or brew install swig
pip install gym[atari]
pip install gym[box2d]
pip install box2d box2d-kengz
```

## Instruction

1. Train the agent (details could be found in each folder):

```
cd rl_algorithms/ppo/
python train.py --env-name=Hopper-v2 --cuda --env-type=mujoco --num-workers=1 --nsteps=2048 --clip=0.2 --batch-size=32 --epoch=10 --lr=3e-4 --ent-coef=0 --total-frames=1000000 --vloss-coef=1 --dist quantization --alg ib
```

2. Plot

```python
python plot.py
```

