# multiplefilesdownload

Many times users want to download multiple files by a single click. 
For example user wants to download selected photos from an album.
Naive solution is to zip all files and once done allow user to download
zip file with selected images. The latency between user clicks download
button and the download starts can be very long especially for big files.
This library is designed to solve this problem. It allows to start download 
of file immediately. The library will create a container for files on the fly.

The first realization will just concatenate files content into one file.
The second realization will use TAR container to keep files content.
The third realization will use ZIP as a container. I'm not absolutely sure 
that's technically achievable. 

The main accent of thi library is put on manipulating binary streams instead
of files on a file system. 
