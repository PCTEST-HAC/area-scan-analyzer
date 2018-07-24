# T-Coil Area Scan Data - Analysis and Visualization Toolkit
This project was built to facilitate the analysis and visualization of T-Coil area scan results. The program takes ‘.txt’ data files from the T-Coil area scans and generates plots/tables displaying the data and analysis results. The generated results and figures can be exported into ‘.xlsx’ Excel files and separate ‘.png’ image files.
The project was developed in Python 3.6.

## Getting Started
### Overview
#### Programs
-	[Anaconda3/Miniconda3]( https://www.anaconda.com/download/)
o	Python projects often implement a variety of different third party libraries which, as projects scale up, can be hard to manage in an organized fashion. As a Python distribution, Anaconda provides the core Python language, hundreds of core packages, a variety of different development tools (e.g. IDEs), and ***conda***, Anaconda’s package manager that facilitates the downloading and management of Python packages. 
-	[Python 3.6]( https://www.python.org/downloads/) (included in Anaconda3/Miniconda3)
o	Python is the main programming language for this project. It has an active open-source community and easily readable code syntax, making Python a great language of choice for projects like these. 
-	An Integrated Development Environment (IDE) supporting Python – [PyCharm]( https://www.jetbrains.com/pycharm/download/) is recommended
o	While PyCharm is not necessary to run this program, we highly recommend it for Python-based development. It is easy to integrate it with Anaconda and provides fantastic tools/shortcuts/hotkeys that make development faster and easier.

#### Packages (can be installed using Anaconda):
-	openpyxl
-	NumPy
-	Pandas
-	Matplotlib
-	WxPython

### Installation
1.	First, install [Anaconda3/Miniconda3]( https://www.anaconda.com/download/), which comes with the latest stable version of Python (3.6 at the time of writing this README) included. Choose the appropriate installation for your respective operating system.
2.	Install [PyCharm]( https://www.jetbrains.com/pycharm/download/) or any other IDE that supports Python.

Note: the following steps will show how to set up the environment using Anaconda and PyCharm, but the project is not restricted to these tools exclusively.

3.	We will now install the different packages required to run the scripts.
o	Open ***Anaconda Navigator*** and click on ***Environments*** tab on the left.
[docs/anaconda.png] 
o	Select ***Not installed*** from the dropdown menu.
[docs/anaconda1.png]
o	From here, we can search for each of the different packages listed above (in the Packages subsection of the Overview). To download the packages, check the box next to the package and click ***Apply*** at the bottom. Keep in mind that some of these packages may already have come with the full Anaconda installation.
o	Some packages may not be found using the Navigator. In this case, they must be downloaded using ***Anaconda Prompt***. Open the prompt and type the following: `conda install -c anaconda <package_names_space-separated>`.
[docs/anacondaprompt.png]

Note: Alternatively, you can add the packages in the ***Project Interpreter*** section of the project settings in PyCharm. However, this must be done after the project has been opened and the project interpreter has been selected, which will be done in the next few steps.

4.	Open PyCharm and open the project – select the ***hac*** folder in the “Open File or Project” window.
5.	Select ***File->Settings…*** and select the ***Project Interpreter*** tab on the left. Click on the cog and select ***Add…***.
[docs/projectinterpreter.png]
o	Click on the ***System Interpreter*** tab on the left and select the location of the python.exe file from your Anaconda/Miniconda installation (most probably found in `C:\Users\<user>\AppData\Local\Continuum\anaconda3\python.exe`).

## Deployment
Open `hac/hactolerance/hactolerance.py` and click run (green play button at the top right of PyCharm). To run from the command line, open the Anaconda Prompt and enter: 
```bash
python hactolerance.py
```
while in the `hac/hactolerance` directory.
Alternatively, you can run the program directly from the Windows command line, but you must first add python to the PATH variables of the system. Follow the steps [here] (https://superuser.com/questions/143119/how-to-add-python-to-the-windows-path).

A basic GUI will appear with preset/default analysis parameters.
[docs/hacgui.png]

### Single File Analysis
The single file analysis function determines which coordinates of the area scan readings are over the specified threshold (dB A/m).
The analysis takes the raw ‘.txt’ input file specified in the ***Input ‘.txt’ File (ABM1 or Single File)*** text line. To begin the analysis, click on the ***Run*** button at the bottom right of the GUI window. Once the analysis has been completed, the plot subsection will display a heatmap built from the original data and a region of interest composed of points greater than or equal to the threshold. The figures and data tables can be exported into an ‘.xlsx’ file. [TODO: Specify the different sheets]

### Dual File Analysis (ABM1, ABM2)
The dual file analysis function provides a more thorough analysis that includes the signal to noise ratio (ABM1 – ABM2), the sizes and dimensions of the different tolerance regions, the number of tolerance compliant points, etc., as well as visualizations of these results.
The analysis takes two raw ‘.txt’ files specified in the ***Input ‘.txt’ File (ABM1 or Single File)*** and ***Input ‘.txt’ File (ABM2)*** text lines. To begin the analysis, click on the ***Run*** button at the bottom right of the GUI window – the program will automatically perform the dual file analysis without having to specify it elsewhere in the GUI.
The figures and data tables can be exported into an ‘.xlsx’ file and separate png files in a directory. [TODO: Specify the different sheets]

## Packages

## Contributing

## Authors
•	Chang Hwan ‘Oliver’ Choi – Biomedical Engineering Intern – changhwan95
Originally developed for the internal use of PCTEST Engineering Labs, Inc.

## License
[TODO: Add all licenses]

## Acknowledgements
•	Thomas
•	Andrew
•	PCTEST Engineering Labs, Inc.
