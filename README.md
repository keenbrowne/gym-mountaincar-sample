# gym-mountaincar-sample

### INSTALLATION
1. Review [requirements](http://docs.bons.ai/getting-started/lets-get-started) for installing the Bonsai CLI.
1. Install the Bonsai Command Line Interface (CLI).
```
pip install bonsai-cli
bonsai configure
```
1. git clone this repository
2. Install the simulator's requirements:
```
cd gym-mountaincar-sample
pip install -r requirements.txt
```

### HOW TO TRAIN YOUR BRAIN
Training involves loading inkling and associated files into the AI Engine. The
commands below operate on the mountaincar.bproj Bonsai project file.

1. If you haven't already created a BRAIN at the website, create one now. This
   command adds a link from the local Bonsai project file to the BRAIN:
```
bonsai brain create <brain_name>
```

2. Load your Inkling project into your brain. Review our [Inkling Guide](http://docs.bons.ai/inkling-guide-pages/introduction)   
   for help with Inkling.
```
bonsai load
```
1. Enable training mode for your brain. Please note that training may take many hours.
```
bonsai train start
```
1. When training has hit a sufficient accuracy, disable training mode.
```
bonsai train stop
```

Questions? View the FAQ

### USE YOUR BRAIN

1. Run the simulator using predictions from your brain.
```
python mountaincar_simulator.py --predict-brain=<your_brain> --predict-version=latest
```
