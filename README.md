# OC curlgoogle

This script copies files using curl to an Oberlin College google drive account using the internal GCP application 'OC curlgoogle.' 

This is an informal 'fork' of the script [presented by Daniel Ellis](https://towardsdatascience.com/uploading-files-to-google-drive-directly-from-the-terminal-using-curl-2b89db28bb06) 

## Installation

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
