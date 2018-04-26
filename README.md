## xsos-container

A lightweight, Fedora based [xsos](https://github.com/ryran/xsos) image which allows you to mount a local sosreport and use xsos. This is mostly due to xsos not working on MacOS

#### Building Locally

The following example shows how this image can be used to use xsos on a local sosreport.

Pull down this repository and run the following commands:

```
docker build -t fedora-xsos .     # creates a local image called "fedora-xsos"
docker run -it -v <path-to-local-sosreport-dir>:/tmp/sos/ fedora-xsos bash xsos /tmp/sos/ -a  # Outputs a xsos summary using -a

# To enter interactive mode use 
docker run -it -v <path-to-local-sosreport-dir>:/tmp/sos/ fedora-xsos bash
xsos /tmp/sos/ -a
```
