# Installing SystemVerilog on Ubuntu using apt

In this guide we'll show you, how to install all necessary tools for synthesing or simulating your SystemVerilog projects.

## Installing SystemVerilog

This guide was tested on *Ubuntu 20.04*.
If you're using an older verion of Ubuntu, you may get older version of those programms.

### Synthesis & simulation tools
Just run the following commands in a terminal.
```sh
sudo apt update
sudo apt install yosys graphviz iverilog gtkwave dos2unix
```

### Preparing files
Download and extract the .zip file from our Moodle course.
Now navigate to the `SystemVerilog/bin` directory and run
```sh
# Using the correct line ending for Unix
dos2unix sim.sh synth.sh
# Allow the shell scripts to be executed
chmod +x sim.sh synth.sh
```

You completed the installation of SystemVerilog. Now you can test it.

## Testing your installation

Go to the folder `SystemVerilog\src\comb` and run
```sh
# Testing the synthesis
../../bin/synth.sh example example.sv
# Testing the simulation
../../bin/sim.sh example_tb example.sv example_tb.sv
```

Now there should be a new file in the same folder called `example.pdf` which is the result of the synthesis and an application called GTKWave should open up, which displays measurements of the simulation.

Congratulations all nessesarry tools for SystemVerilog are working properly.