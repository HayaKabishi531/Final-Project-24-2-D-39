Abstract
Climate changes provide substantial worldwide problems, ranging from severe weather phenomena to disturbances in ecosystems and human civilizations.
Long-term prediction of the changes is an important unsolved problem. Our project is directed to bring a new approach for solution:
consideration of an accumulated energy in the system. According to the model, this parameter would significantly influence the system's ability to change and conduct
the temperature, pressure and other properties. Our task is creating a tool collecting and analyzing the climate data and providing an estimate of the currently
accumulated energy through the Earth. We have provided and compared two independent solutions for this task: the first is based on solar radiation and albedo analysis, 
and the second is based on the atmospheric heat capacity estimation. The obtained results and the created tool were provided for scientists for further investigations.


---
Sharing files
Google Colab notebooks are used for:
- Data preprocessing: Convert ERA5 GRIB files to CSV format.
- Visualization of energy absorption: creating graphs to compare results from both methods.

---

Important note The code is divided into subfolders to upload it to GitHub
You need to download the code folder to a location and extract it in a folder
And inside it open a folder called data
Which will contain all our information and data files
In it will be placed The folders:
Pre_input_radiation_files.zip - contains the radiation files before the cumulative data processing process
input (2).zip
Contains the input files in CSV format
output.zip
Folder contains the output files of the process of dividing, associating and calculating the area of ​​a grid on the Earth
output_energy_calculation. zip
Contains the output files of the calculation processes according to our two models:
Radiance and Albedo
Temperature and Heat Capacity
DisplayEnergy.zip
Contains the output files for the visual representation.

CoolProp.7z contains the ready-to-use COOLPROP files. You need to put it inside the project folder and run it:
Setting up COOLPROP in Visual Studio
To properly include the COOLPROP library, follow these steps:

1. Open Visual Studio and navigate to:
Project → ConsoleApplication1 Pages Property
2. Go to C/C++ → General
3. In the "Additional Include Libraries" field, add the following paths (adjust according to your project location):

```
D:\Final_Project\ForStud1\CoolProp\include;
D:\Final_Project\ ForStud1\CoolProp\Backends;
D:\Final_Project\ForStud1\CoolProp\Backends\Cubics;
D:\Final_Project\ForStud1\CoolProp\Backends\Helmholtz;
D:\Final_Project\ForStud1\CoolProp\Backends\Helmholtz\Fluids;
D:\Final_Project\ForStud1\CoolProp;
$(VC_IncludePath);$(WindowsSDK_IncludePath);
$(FrameworkSDK_IncludePath);%(AdditionalIncludeDirectories)
```

4. Click "Apply" and then "OK"

This ensures that the COOLPROP headers are linked correctly and can be used in the project.

---

Project Summary
This project calculates the Earth's energy absorption using two independent methods:
1. Solar radiation-based method - uses radiation and albedo analysis to estimate the energy absorbed.
2. Heat capacity-based method - uses temperature calculations and atmospheric heat capacity, incorporating the
COOLPROP library.

The program processes climate data from ERA5, extracts key parameters, maps data points to a global grid, and generates CSV outputs for analysis and visualization.
