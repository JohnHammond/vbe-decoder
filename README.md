# vbe-decoder.py

Decode one or multiple encoded VBScript files, often seen with a `.vbe` file extension into decoded `.vbs` files.

## Installing requirements

The following command will install the packages according to the configuration file requirements.txt.

```shell

usage: pip install -r requirements.txt
```

Note the -r option; without it, pip thinks you want to install a package named requirements.txt, which doesn't exist.

## Usage

```shell
usage: vbe-decoder.py [-h] [-o output] file [file ...]

Decode an encoded VBScript, often seen as a .vbe file

positional arguments:
  file                  file to decode

optional arguments:
  -h, --help            show this help message and exit
  -o output, --output output
                        output file (default stdout)
```

## Examples

```bash
# install the packages
$ pip install -r requirements.txt

# display on stdout
$ python3 vbe-decoder.py encoded.vbe

# write to file
$ python3 vbe-decoder.py encoded.vbe -o decoded.vbs
```


---------------------------------

Credit for this baseline code goes to Didier Stevens, from his original repo.
https://github.com/DidierStevens/DidierStevensSuite/blob/master/decode-vbe.py

All I have done is merely cleaned the code a bit, made it Python3 friendly,
and handled support for multiple #@~...#~@ markings. 