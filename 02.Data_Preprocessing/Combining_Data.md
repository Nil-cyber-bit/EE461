
# Processing the Original Data
<a name="beginToc"></a>

## Table of Contents
&emsp;[Joining Data\-sets](#joining-data-sets)
 
&emsp;&emsp;&emsp;[Normal data combining](#normal-data-combining)
 
&emsp;&emsp;&emsp;[Faulty Data combining](#faulty-data-combining)
 
&emsp;&emsp;&emsp;[Unknown Data combining](#unknown-data-combining)
 
&emsp;[Loading the Data](#loading-the-data)
 
&emsp;[Observing the Data](#observing-the-data)
 
<a name="endToc"></a>

# Joining Data\-sets
-  Joining mutliple files into the 3 classes 
-  This header file takes int he folder path that containes the numrous identical dataset and joins them into one data file. 

Three Classes:

-  Fault State: 11 files  Saved as Faulty\_all.xlxs 
-  Normal State: 25 files  Saved as Normal\_all.xlxs 
-  Unkown state: 25 files  Saved as Unkown\_all.xlxs 

Note

-  this code needs to run once to create 3 file(each representattive of a class) therefore you do not need to run this code all the time since the time since the Output files have already been created. 
-  If you choose to do so, change the input folder for each state, and the ouptut file name and location. 

### Normal data combining
```matlab
% Define folder (already in path)
folder = "1.Original_Data";
filePattern = fullfile(folder, '*.xls');
excelFiles = dir(filePattern);

% Initialize as table
Normal_all = table();

% Loop through each file
for k = 1:length(excelFiles)
    fullFileName = fullfile(folder, excelFiles(k).name);
    data = readtable(fullFileName);  % Keep it as table
    Normal_all = [Normal_all; data]; % Append tables
end

% Write to Excel
outputFileName = fullfile('2.Combined_Data', 'Normal_all.xlsx');
writetable(Normal_all, outputFileName);

disp('All files have been combined successfully!');
```

### Faulty Data combining
```matlab
% Define the folder where the Excel files are located
folder =  "1.Original_Data";
filePattern = fullfile(folder, '*.xls'); % Change to '*.xls' if using .xls files
excelFiles = dir(filePattern);

% Initialize a variable to hold combined data
Faulty_all = [];

% Loop through each file
for k = 1:length(excelFiles)
    % Get the full file name
    baseFileName = excelFiles(k).name;
    fullFileName = fullfile(folder, baseFileName);
    
    % Read the data from the current Excel file
    % Assuming the data is in the first sheet and starts from the first row
    data = readtable(fullFileName);
    
    % Append the data to combinedData
    Faulty_all = [Faulty_all; data]; % Concatenate the data
end

% Write the combined data to a new Excel file
outputFileName = fullfile('2.Combined_Data', 'Faulty_all.xlsx');
writetable(Faulty_all, outputFileName);

disp('All files have been combined successfully!');
```

### Unknown Data combining
```matlab
% Define the folder where the Excel files are located
folder =  "1.Original_Data";
filePattern = fullfile(folder, '*.xls'); % Change to '*.xls' if using .xls files
excelFiles = dir(filePattern);

% Initialize a variable to hold combined data
Unknown_all = [];

% Loop through each file
for k = 1:length(excelFiles)
    % Get the full file name
    baseFileName = excelFiles(k).name;
    fullFileName = fullfile(folder, baseFileName);
    
    % Read the data from the current Excel file
    % Assuming the data is in the first sheet and starts from the first row
    data = readtable(fullFileName);
    
    % Append the data to combinedData
    Unknown_all = [Unknown_all; data]; % Concatenate the data
end

% Write the combined data to a new Excel file
outputFileName = fullfile('2.Combined_Data', 'Unknown_all.xlsx');
writetable(Unknown_all, outputFileName);

disp('All files have been combined successfully!');
```

# Loading the Data
```matlab
% Reading Normal Data
normal = readtable('2.Combined_Data\Normal_all.xlsx');
% Reading Faulty Data
faulty = readtable('2.Combined_Data\Faulty_all.xlsx');
% Reading Unknown Data
unknown = readtable('2.Combined_Data\Unknown_all.xlsx');
```

# Observing the Data

this section we turn the data into a usable format for most plots. In addtion we view what the data looks like.

```matlab
% Displaying  Normal Data
disp('Normal Data')
disp(['Amount of data: ',num2str(size(normal,1))])
disp(normal)

% Displaying Faulty Data
disp('Faulty Data')
disp(['Amount of data: ',num2str(size(faulty,1))])
disp(faulty)

% Displaying Unknown Data
disp('Unknown Data')
disp(['Amount of data: ',num2str(size(unknown,1))])
disp(unknown)
```
