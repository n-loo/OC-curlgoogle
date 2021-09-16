# OC curlgoogle

This script copies files using curl to an Oberlin College google drive account using the internal GCP application 'OC curlgoogle.' 

This is an informal 'fork' of the script [presented by Daniel Ellis](https://towardsdatascience.com/uploading-files-to-google-drive-directly-from-the-terminal-using-curl-2b89db28bb06) 

## Installation

### Prerequisites

- Python 2.7
- [Curl](https://curl.se/)

I recommend installing this to your home directory (~) so it may be used anywhere.

### Steps:

Copy over the script:
```
wget https://raw.githubusercontent.com/n-loo/OC-curlgoogle/main/curlgoogle
```

Make the script executable

```
chmod a+x curlgoogle
```
Done!

## Usage

To copy over a file with `curlgoogle` run the script as

```
~/curlgoogle file.txt
```

You may also recursively copy over an entire folder (with parent path) and its contents by running

```
~/curlgoogle ./folder/*
```
When running the script copy the code displayed and follow the link to your web browser. Input the code into the web browser and select your Oberlin account. Then click enter twice in the terminal and it should show up as the zip file `curldata` in your Google Drive shortly! 

If you wish to unzip the contents in Google Drive I recommend the Zip Extractor extension in Drive.

## `curlgoogle2`

The original curlgoogle script isn’t very great at uploading giant folders due to an issue with zipping the giant folders. `curlgoogle2` is a workaround using a different variation of the curlgoogle script called curlgoogle2. 

### Installation

The installation process is the same as with the original script but just with replacing `curlgoogle` with `curlgoogle2`.

### Usage

Since this is intended for dealing with large folders, first we zip the folder in the command line as:

```
zip -r -0 curldata.zip ~/folder/to/upload/
```

It is recommended to keep the `curldata.zip` as the name for the zip file. If you change it to something else you must edit the `name` variable in the script first.

Now we upload the folder using the command:

```
~/curlgoogle2 curldata.zip
```

Now you need to sign into google drive using the steps decribed for the original `curlgoogle` and the file will upload eventually.

