Metadata_mapping_exif_data-475-2151_Rojas_Schoenfeld
Mostly all pictures, videos, documents taken with a smartphone, or created with a computer will have metadata associated with it.  Some of this metadata allows us to create maps and timelines of where these pictures were taken.  Using ExifTool.exe, we can scrape out GPS coordinates from pictures and documents then using an API we can plot these coordinates in Google Maps or some similar mapping program.  This can help forensic investigators and law enforcement identify the location of interesting places in an investigation or show the origin in which a file was created.  
In order to run the tool you first need to install exiftool.exe from http://www.sno.phy.queensu.ca/~phil/exiftool Rename it exiftool.exe and store it in the same directory as the exifmappy.py Next, download the latest version of python from: 
https://www.python.org/downloads . 
Next Install the python libraries used in exifmapper.py if they are not installed already:
pip install string
pip install os
pip install subprocess
pip install re
pip install sys
In order to use the tool you need to register for a Google Maps Static API key at the link below:
https://developers.google.com/maps/documentation/static-maps/
Click “GET A KEY” to register.
Around line 125 (subject to change, may be a higher line number) you should enter in your key.
Command line help options can be seen with “-h” or “--help”.

To run the program and plot the images:
Rename exiftool(-k).exe to exiftool.exe
Copy exiftool.exe to the directory exifmapper.py is located.
Place the images to be plotted in the directory with exifmapper.py
type exifmapper.py “X:\Path to the directory that contains the images\”
If you wish for the output to be archived in a text file use the following command:
exifmapper.py “X:\Path to the directory that contains the images\” > FileName.txt
The text file will be located in the same directory exifmapper.py is located
Copy the individual URL into a web browser to view map plot for an individual image.
Or copy the URL at the bottom labeled “THE URL FOR YOUR MAP” to see the full map view with all the images plotted.
Alternatively, place the GPS coordinates in to maps.google.com for an exact location

