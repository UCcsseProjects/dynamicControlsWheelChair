# dynamicControlsWheelChair

# Windows Setup:

To install python on windows got to:

https://conda.io/miniconda.html
 
You will need to install PySerial, type the follwing into the anaconda terminal and hit enter:

conda install -c anaconda pyserial

In order to run the serial setup script (which you will be directed to if you try to run main.py) I had to update pythons setuptools package:

conda install setuptools

Make sure visual studio is installed, including the toolkit:

http://go.microsoft.com/fwlink/?LinkId=691126

You may also have to change an environment variable, go to:

https://stackoverflow.com/questions/2817869/error-unable-to-find-vcvarsall-bat

To build the crc8 python module: 

cd sf_crc8
python3 setup.py build_ext --inplace

Then to install opencv:

conda install -c conda-forge opencv

# Linux Setup:

Install pyserial, setuptools:

pip install pyserial
pip install setuptools

To build the crc8 python module: 

cd sf_crc8
python3 setup.py build_ext --inplace

Then to install opencv:

pip install opencv

# Running the code:

The wheel chair script is wheel_chair_auto.py, the -p "port_name" is required, where on windows it will be COM#, on ubuntu ttyUSB#:

python wheel_chair_auto.py -p /dev/ttyUSB0/ -d
