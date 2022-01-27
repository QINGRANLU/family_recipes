# Finding the greenest track Group1
## Setup:
This is  a  package called tracknaliser. 
- greentrack.py : could expose a command-line interface to specify the details of the trip they plan to do and request a simple or verbose output:
    - inputs: for --start and --end are x and y coordinates for the start and end of the travel planned. 
    - outputs: The program should return three properties for the greenest path: 
      - the coordinates pairs (x, y) of the path, i.e., the start, end and corners of the trip
      - the total CO2 emission in kg
      - the total time of travel (as HH:MM:SS).
    - If the --verbose flag is passed, then that indicates that the program should report the journey in a human readable way, as shown in the example below.
    - The command line interface should: 
      - check the validity of the inputs before making the query (i.e, coordinates should be in the range from 0 up to 300) and produce helpful messages if they are invalid. \
      - produce a meaningful error message if there’s no internet connection or the webapp is inaccessible
- load_tracksfile and query_tracks functions: return a Tracks object.
- query_tracks function: takes as many arguments as needed to query the webapp and an optional  save argument that if set to True will save the obtained data as a JSON file, with the following patterntracks_{date}_{n_tracks}_{start}_{end}.json.
-
## Tasks: 
Following information are inclued in installing package.  Subtasks are fulfilled for the main task required assignment2
- Task1：Interface and packaging (packaging the project and make it runnable by typing pip install . in command line)
  - command.py: used for print greenest 
  - tracknaliser.py: library style interface which make interactions with command line tool
  - greentrack.py: interface with the greentrack
  - docs folder: documentation for python file, in ./build/html/index.html could be found the document. 
- Task2: Main code
  - _init_.py
  - singleTrack.py: Create a singletrack object and calculate the required value (co2, time, etc.)
  - trakcs.py: Create a tracks object which contain several singleTrack object and calculate the relative track(fastest, shortest, greenest, etc.)
 
- Task3: Improving k-means algorithm
  - clustering.py: original verson of algorithm with refactoring. 5 changes should be applied
  - clustering.numpy.py: numpy structures and functions are introduced.
  - performance.py: compare 2 versions of code (used numpy or not)
- Task4: Testing and Validation
  - utils_validation.py: check the functions input validaty and give correct error type message
  - test: automated tests to test functionality, in the test folder

- Task5: Collaboration
Using Github to manage collaboration, problems are solved using issue, details please check: https://github.com/UCL-MPHY0021-21-22/tracknaliser-Working-Group-1



