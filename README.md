## Calibration
Start by checking the calibration you want to use: 
- If it is already in the calibration folder (EBT3 or EBT4), just call it at the beginning of the *DoseMeasurementScript* by assigning the right film type inside de "filmtype" variable, it will use the extracted intensities and corresponding doses stored in /calibration to calculate the right fit parameters.
  
- If not, analyse your new calibration films through the *CalibrationScript*. If you name your calibration film scans folder as *your_filmtype* and your calibration doses txt file as *your_filmtype_dose* inside /calibration (like the current EBT3 and EBT4 film types), you will just have to enter your film type inside the "filmtype" variable in the first cell of the script to have your fit parameters calculated. The extracted intensities will be stored in a txt file named "filmtype_int_channel" inside /calibration.
  
You can then use the *DoseMeasurementScript* with your new calibration by assigning your new film type inside de "filmtype" variable at the beginning.

## Dose Measurement

This part consists of two cells: 
- The first on is here to test and customize the zone of interest position in wich you want to measure the dose, typically on Hg.
  
- The second one is basically the same code but with a loop to go through the whole batch, with the defined zoi. You can also choose to have an "automatic" zoi, targetting the center of mass for each film.  

Results are stored in a txt file inside /DoseResults that you name inside the "result_path" variable at the beginning of the second cell.
