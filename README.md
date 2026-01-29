# RoboFinder

RoboFinder is a more advanced tool that allows you to search for old 'robots.txt' files of a given URL on archive.org. By leveraging the vast archives of the internet, RoboFinder retrieves historical versions of the 'robots.txt' file and presents all the old paths and parameters associated with it.

## Features

- **Archive.org Integration**: RoboFinder seamlessly integrates with the archive.org platform, providing access to an extensive collection of historical 'robots.txt' files.
- **URL Searching**: Simply input the URL you wish to search, and RoboFinder will retrieve all available historical versions of the 'robots.txt' file associated with that URL.
- **Path and Parameter Extraction**: RoboFinder not only retrieves the old 'robots.txt' files, but it also extracts and displays all the paths and parameters found within them.

## Installation 

To use RoboFinder, follow these steps:

```bash
git clone https://github.com/Nima-Mollaei/RoboFinder.git
cd RoboFinder
pip install -r requirements.txt
```

## Usage

```bash
- `--debug`: Enable debugging mode.
- `--url` or `-u`: Specify the URL for which you want to perform the search. This argument is required.
- `--output` or `-o`: Specify the output file path. This argument is optional.
- `--threads` or `-t`: Specify the number of threads to use. The default value is 10.
- `-extract-path`: Enable path extraction and save it separately to `$domain-path.txt`.
- `-extract-params`: Enable parameter extraction and save it separately to `$domain-params.txt`.
- `-parse-url`: When number of robots.txt are more than 2000 it\'s better to process less URL`.
- `-silent`: There isn\'t stdout`.


```

## Example usage:

```bash
python3 RoboFinder.py -u https://target.com -o path.txt

output will be :
https://target.com/PATH
```
```bash
python3 RoboFinder.py -u https://target.com -extract-path -extract-params

output will be :
target.com-path.txt :
/PATH1
/PATH2
/PATH3
----------
target.com-params.txt :
All the finable parameters that exists in robots.txt
```

## Contributing

Contributions to RoboFinder are welcome! If you have any ideas, bug reports, or feature requests, please open an issue. Feel free to submit pull requests as well.

Please ensure that your contributions align with the project's coding style and guidelines.

## License

RoboFinder is released under the [MIT License](https://opensource.org/licenses/MIT). 
