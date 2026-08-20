# Robust Distributed Arrays - Generating Plots

This repository contains Python scripts to generate plots for the *robust distributed arrays* paper.

## Dependencies
To run the scripts, you need Python 3.9 or newer and the dependencies in `requirements.txt`.
You will also need a LaTeX installation containing `pgfplots`, `csvsimple`, and `subcaption` to compile the plot documents.

We recommend using a virtual environment:
```
python3 -m venv .venv
source .venv/bin/activate
python3 -m pip install -r requirements.txt
```

## Estimate Plots
You can generate plots visualizing the security bound and complexities from the theoretical analysis.
To do so, run
```
python3 estimates_to_csv.py
```
The script will generate csv files with the data.
You can generate the plots with
```
pdflatex estimates_plots.tex
```

## Simulation Plots
A specific join-leave schedule can be simulated. To do so, run
```
python3 simulation_show.py
```
It will take a short while and then show graphs with the simulation results.
You can also use
```
python3 simulation_to_csv.py
```
to write the plot data to a csv file, which can then be included in LaTeX, as shown in `simulation_plots.tex`.
Compile these plots with
```
pdflatex simulation_plots.tex
```

## License
MIT License.
