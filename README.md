
# BatterySimulator

## Installation
1. Make sure OpenFOAM6 is already installed on your computer correctly. If not, follow the steps on <a href="https://github.com/OpenFOAM/OpenFOAM-6">github site</a>.
    - **OpenFoam-6 installation** : 
	    - Unzip the `OpenFOAM-6.zip` into your preffered folder (you can find it also in `3rdparty` folder)
	    - Open a terminal and execute : `source /installation_dir/OpenFOAM-6/etc/bashrc`
	    - Into `OpenFoam-6` folder execute `./Allwmake -j`
2. Find the file */installation_dir/openfoam6/etc/controlDict* (use `sudo` command to open it if it is located on a system directory). Find the line `dimensionSet 1;`(You can use `ctrl+f` to locate), then change `1` to `0` and save it.
3. Use <a href="https://www.qt.io/download-open-source">QtCreator</a> to open project file in *src* directory and complile it into *build* directory (define *build* as output folder in the project options)
4. Open terminal under *build* folder and execute :
    - `source /installation_dir/OpenFOAM-6/etc/bashrc` 
	- `./BatterySimulator`, then you can use the simulator.

**Alternative method to compile the project** :
Open a terminal and execute in the project folder : 
- `mkdir build`
- `cd build`
- `qmake ../src/BatterySimulator.pro` or `/path_to/qmake ../src/BatterySimulator.pro`
- `make -j`

In the two cases, *OpenfoamModule* folder will be created in *build* while compiling.

**Run the code** :
In the project folder execute :
- `source /installation_dir/OpenFOAM-6/etc/bashrc`
- `build/BatterySimulator`
or
- `./Allrun`

## User guide
To use this simulator is very simple, you only need to follow the hints on the interfaces and start to create your own projects!  
There are only a few things that need a bit more explanations:
1. If you are the first time to run a project, you **must** click **Modify* button on Geometry interface at least once even if you do not change parameters on this interface.
2. The GUI embeds the linux terminal function. You don`t need to input any command during the process, however, if you want to execute commands, you can do it.
3. You can view your geometry through *View Geometry* once you clicked **Modify* button on Geometry interface(This means related geometry files will be generated). This will open ParaView and later operations will be perforamed through ParaView instead of BatterySimulator.
4. Once you generated related results files through *Run/Resume* button on Control interface, you can click *View Results*. This will open a new interface, and you can view kinds of graphs intuitively.

## License

This project is licensed under the GPL-3 license.