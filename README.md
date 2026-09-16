# py-racecar-performance-sim
A VERY simple and basic racecar performance simulator, written using Python and appropriate libraries, by me. It recieves inputs from the user which is then converted into a real-time graph display. It models vehicle acceleration as well as maximum velocity, as well as the time it takes to get to max. velocity, etc.

The sim provides a GUI for the user, as it will become more accessible this way.

GUI: built with Tkinter

Matplotlib: Displays simulated vehicle performance

## Features

* Graphical user interface using Tkinter.
* Vehicle parameters for user to modify.
* (somewhat) real-time simulation animation.
* Velocity vs distance graph.
* Maximum velocity calculation.
* 0–100 km/h acceleration calculation.
* Simulation history, showing the five most recent results.
* Adjustable vehicle parameters.

## Vehicle Parameters

The simulator currently allows the following variables to be changed:

Parameter        | Unit | Description
---------------- | ---- | ------------
Mass             | kg   | Vehicle mass.
Engine Power     | kW   | Power produced by engine.
Downforce        | N    | Aerodynamic downforce.
Wing Angle       | °    | Wing angle used.
Drag Coefficient | -    | Aerodynamic drag coefficient.
Frontal Area     | m²   | Approximate frontal area of the vehicle.
Tyre Grip        | -    | (SIMPLIFIED) Tyre grip coefficient.

The program displays a recommended range for each parameter, but does not prevent the user from entering values outside the ranges.

## How It Works

The simulator uses a simplified vehicle dynamics model.

Aerodynamic drag is calculated from air density, drag coefficient, frontal area and velocity.

Downforce is used to increase the normal force acting on the tyres. This is then combined with the tyre grip value to determine the maximum available traction.

Engine force is calculated from engine power and vehicle velocity.

The resulting (net) force is converted into acceleration using F = m*a.

Then, the simulation advances in small time steps and updates the vehicle's velocity and position.

The graph is updated during the simulation so the user can watch the change in relationship.

The simulation stops when the acceleration becomes small, which represents the vehicle approaching its maximum velocity.

## Requirements

Python 3

The following libraries are required:

* Tkinter
* Matplotlib

Matplotlib can be installed using:

```bash
pip install matplotlib
```

## To run the program:

Download and execute the .py file labelled 'performance-sim-VX' where X is the version of the program.

## Current Project Structure

```text
py-racecar-performance-sim/
│
├── performance-sim-VX.py
└── README.md
```

## Limitations

This project is intended as an educational and experimental simulator rather than a professional motorsport simulation, as I do not have the experience or knowledge to create anything more advanced.

The physics model is simplified and does not currently simulate features such as:

* Gear ratios
* Individual gears
* Engine torque curves
* Vehicle suspension
* Braking
* Track elevation
* Tyre temperature
* Tyre degradation
* Fuel consumption
* ERS deployment
* DRS zones
* Detailed aerodynamic maps
* Weight distribution
* Suspension geometry

As a result, the calculated performance figures should not be treated as accurate predictions of a real vehicle. They should purely be used for fake scenarios.

## Possible Future Improvements

Possible additions (if I become more experienced) include:

* Separate front and rear aerodynamic settings
* DRS
* ERS
* Different tyre compounds
* Braking simulation
* Lap-time simulation
* Track configuration
* Sector timing
* More advanced aerodynamic calculations
* Telemetry export
* Saving and loading vehicle configurations

Basically more like a motorsport performance simulator, where Formula or famous tracks are added with shapes going around the track.

## Libraries and Programs I have Used:

Python

Tkinter

Matplotlib

## License

This project is provided for educational and experimental purposes. Anyone may use this for any reason, and is not required to give any credit.
