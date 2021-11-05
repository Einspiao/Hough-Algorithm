# Hough-Algorithm for UWA

Fitting resonators' data by Hough transformation.
Developed for Prof. Michael Tobar's group under Dr. Cindy Zhao's supervision and guidance.

What can it do :

Find resonant peaks in wide spectrum data and extract resonant frequency and quality factor by Qkit, a python package developed by Prof. Ustinov's group in KIT. If standard file format (format used in Prof. Tobar's group) is provided, it can also analyze data under different temperatures.

How to use it :

1. Make sure all three documents in zip file are under one directory.
2. Open the GUI code file and run it. In first window, please select the directory you use to store experiment data and file number for a full spectrum scan (for example, full spectrum is 1GHz ~ 10GHz and each file store data in 1GHz span, then the file number is 9). In second window, only the last two parameters need to be determined by YOUR data, which is explained in that window. Other parameters' functions are shown for further adjustment while their default value fit general case.
3. Click button "Fit", the fitting results will be loaded to a HDF5 file under the same directory. Another python program is provided to readout the found peaks in HDF5 file and fit it by Qkit package.

Please be adviced :

This algorithm search for resonant modes at a reletively high resolution and as a result it takes more time. For a typical full spectrum scan (10000 data points), it takes approximately 20 minutes. Since a full spectrum scan experiment takes several hours, I assume 20-minute running time is acceptable. Large step length (Data points between two steps, in the second parameters setting window) can speed up it at the cost of worse resolution.

All details about this program can be found in "Research Summary".
