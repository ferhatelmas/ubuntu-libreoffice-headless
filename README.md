## Build Image

> docker build -t ubuntu-libreoffice-headless .

## Convert office documents

> docker run -v /HOST_PATH/:/tmp ubuntu-libreoffice-headless libreoffice --headless --convert-to CONVERSION_PARAMS /tmp/OFFICE_FILE --outdir /tmp

Where `HOST_PATH` is the place your file located in your host filesystem and `OFFICE_FILE` is the office file name.

Conversion parameters change according to your needs:

* PDF: pdf
* CSV: csv:"Text - txt - csv (StarCalc)":59,34,76,1,1,0,true

For details, see filter options in [wiki](https://wiki.openoffice.org/wiki/Documentation/DevGuide/Spreadsheets/Filter_Options).

Base image is `Ubuntu 16.04 latest`.
