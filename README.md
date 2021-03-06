# About #
JBlockCreator is an open-source framework for custom pattern drafting and fit analysis. Framework is based on a 
high-level `Block` class which contains geometric elements necessary for recreating pattern drafting techniques 
digitally. Software also reads measurements from input files exported from body scanning cameras to facilitate custom 
fit. A selection of existing drafting methods are shipped with the source code, but the framework allows the creation of
custom methods as desired by extending the `Pattern` class and adding the relevant UI code. Software copyright is 
retained by the The University of Manchester.

# Compiling and Running #
Release builds are available from the master branch at tagged commits. These releases are shipped with *.jar
which may be executed directly to run the application. You may also wish to build from source which you can do using
`javac` from the command line.

# Known Issues #
The current release has no known bugs, however testing has identified a
limitation. The Bodice pattern from Beazley and Bond requires the user to supply
a measurement corresponding to the width of the armhole in order to drive the
armhole curve geometry in the pattern. The current sample input file supplied
with the software is generated by a scanning system incapable of determining
this measurement. Therefore, the bodice pattern implementation is built using
`Depth of Sleevehead 2 [A36]` measurement as an approximation of the
armhole width assuming the armhole is circular.This approximation does not hold
for all sizes and shapes of individual and on occasion may produce armhole
shapes which are irregular when the sample input files are used. In such
circumstance, the pattern may be imported into drawing or drafting software and
the nodes of the armhole corrected manually. Alternatively, the input
measurement may be modified in the input file directly. Future release of the
software will be enhanced to perform some kind of bounds check to determine
whether the measurement is suitable and warn the user if not.

# Release Notes #

**Version: 1.2**        
Issue #37: Added dynamic preview capability as output options are selected with checkbox. Removed redundant box on analysis pane.    
Issue #57: Reworked output to conform to ASTM standard. Testing shows it can be read into Lectra as an AAMA file so there is still a deficiency in the output and issue remains open.    

Small fixes to Aldrich trouser pattern and Gill skirt pattern.
Proprietary pattern information removed for future releases prior to open source publication.    

**Version: 1.1**    
Issue #41: Added more input files to the input folder for users to test behaviour.    
Issue #39: Menu bar added to UI to provide alternative navigation.    
Issue #35: Added option to choose the information layers written out to the DXF files.    
Issue #46: File chooser has been made easier to use and folders are now remembered.    
Issue #40: Measurements which are marked as "unavailable" by computer-generated data files are now handled correctly.    
Issue #36: A help button has been added to GUI.    
Issue #38: Run button now shows "running" when in progress and dialog box alerts user on completion. Also moved execution to a background thread to stop UI locking.    
Issue #51: Analysis tab added which allows pairs of measurements to be comapred in rectangle plots.    
Issue #37: Some visual guide to what the output will look like added to the UI.    

**Version: 1.0**    
Issue #4: Batch files of scan data can now be used.    
Issue #5: Keypoints have been added as a new layer on the DXF output files.    
Issue #6: Construction lines have been added as a new layer on the DXF output files.    
Issue #8: Darts have been fixed so they work as intended in all cases.    
Issue #9: Single scan data set files now work without manual manipulation.    
Issue #10: GUI added to the software for ease of use.    
Issue #13: Coordinates of keypoints have been added as a new layer on the DXF output files.    
Issue #17: Circular curves work as intended.    
Issue #21: Batch files of any size now work as intended.    
Issue #23: Output DXF files are now organised in a Method/Pattern/ file directory system.    
Issue #30: All custom measurements needed for the Beazley Bond sleeve now available.    
Issue #34: File input and outputs for the GUI fixed so they work as intended.    
Issue #42: Created a user guide for v1.0.

New patterns added include:    
Beazley Bond Straight Sleeve    
Aldrich Skirt    
Gill Skirt    

**Version: 0.2**    
Issue #1: Patterns can now store the name of the input file and use it when writing DXFs.    
Issue #2: Patterns now have a 10cm square drawn on a separate layer to indicate scaling.    
Issue #3: Patterns now have their name written on a separate layer.    

**Version: 0.1**    
Initial Evaluation Version
