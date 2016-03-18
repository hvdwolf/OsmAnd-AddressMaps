# OsmAnd-AddressMaps
scripts to create address maps for OsmAnd


# Requirements:
### General:
A 64bit Operating System with at least 4-6GB memory.
OsmAndMapCreator and a recent java version. 
Note that you need to be on a 64bit OS and that you need a 64bit java. The memory demands are always above 1.5GB which means a 64bit java environment.

### Linux users:
Download the necessary tools via your package manager. You need omsconvert, osmfilter and wget.
For Ubuntu and/or Debian that would be the package "osmctools" and "wget".

### Windows users:
Download the repository via git clone or download the zip.
Once unzipped/installed see "Create basic map for OsmAndMapCreator"


# Create basic map for OsmAndMapCreator

Open a terminal (linux) or a command/dox box (windows) and go to the folder where you downloaded the scripts (and .exe for windows)

Inside the directory you issue the following comand in case you want a "France" address map.

Windows: 
`create_address_rawmap.cmd france`

Linux:
`./create_address_rawmap.sh france`

(Important: Use lowercase characters).

After some time you should have some file like france-address.osm.pbf
*(Note that the france-latest.osm.pbf file is the orginal complete raw map downloaded from geofabrik. You can remove that one)*


# Create address map inside OsmAndMapCreator
Make sure you have downloaded and installed OsmAndMapCreator
Inside the script OsmAndMapCreator.sh or OsmAndMapCreator.bat make sure you change the value of the "-Xmx720M" to a value of at least 4096 like "-Xmx4096M" and preferably higher if memory allows.

Once updated start OsmAndMapCreator. **Only(!)** set the "build address index". All the other settings need to be "unchecked".

Depending on the speed of your pc and your disk (traditional harddisk or SSD) this will take 30 minutes to 8 hours.

