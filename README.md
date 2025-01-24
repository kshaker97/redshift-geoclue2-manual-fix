<h1 align="center">
  redshift-geoclue2-manual-fix
</h1>

<h4 align="center">Setting manual coordinates is a straightforward way to solve the issue without needing to rely on geoclue2. Here's how you can configure Redshift with manual coordinates.</h4>

## Table of Contents:
- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Usage](#usage)

## Introduction:
This repository provides a solution for fixing the error "Failed to run Redshift: Trying location provider geoclue2" on Debian-based systems. This error often occurs when Redshift is unable to communicate with the geoclue2 service, which is used for getting the user's location to adjust the screen's color temperature accordingly.
## Prerequisites:
1. Redshift installed
2. geoclue2 installed 
## Usage:
1. **Create or modify the Redshift configuration file:**
You'll need to create a configuration file in ~/.config/redshift/redshift.conf if it doesn’t already exist. If it does exist, you can simply edit it.
```
nano ~/.config/redshift/redshift.conf
```
2. **Set the location to manual:**
In the configuration file, add the following lines to specify your latitude and longitude manually. Replace 51.5074 and -0.1278 with your actual coordinates. You can obtain them from https://www.latlong.net/.
```
[redshift]
location-provider=manual
       
[manual]
lat=51.5074
lon=-0.1278
```
3. **Save the file and exit the text editor**
4. **Test Redshift:**
Run Redshift to make sure it uses the manual location
