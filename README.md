# FPC1500-to-SParam

This code can be used for converting dataset information from the FPC1500 VNA into Touchstone format, as a .s1p file

## Workflow:

1. Perform measurement using the FPC1500 in VNA mode
2. Press the "SAVE/RECALL" rubber button
3. Select "Save" soft-button, and then scroll down to \Public\Datasets
4. Press "Save" soft-button to commit the file into the file system; it will have a name like "Dataset001.set"
5. Use the InstrumentView PC software and connect to the FPC1500 and then go to Instrument->FileTransfer
6. Transfer across the .set file onto your PC
7. Click on the dataset file as shown on the right side of InstrumentView, and the click on the Eye icon to view the dataset graphically
8. Now you can click on "Save" on the left side of InstrumentView, choosing "Save as type" to be "CSV File"
9. Go to you PC's file explorer and copy the CSF file, renaming it "input.csv"
10. Run this Python code, by typing:   

  python ./csv2sparam.py
         
11. If all goes well, an output.s1p file will be generated
12. You can open the file using software such as Python scikit-rf library, or Iowa Hills Smith Chart, or SPARGraph


