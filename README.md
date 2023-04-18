# Grid-Cutting
Introducing the Grid Cutting Method for removing gingiva from full arch Intraoral 3D photoscans.  
This method is introduced in (insert publication link here) [Publication name](https://where_is.com/publication)  

(Insert picture from publication here) ![Picture from publication](image.jpg)

## Dependencies
This method was made and tested using Python 3.10.6 with dependencies described in *requirements.txt*.

## Getting startet
It is recommended building a virtual environment for installing the required dependencies.  
For conda, the following approach can be used after cloning this repository:  
`$ conda create -n env_name python==3.10`  
`$ conda activate env_name`  
`$ pip install -r requirements.txt`  
Now the environment is ready for use.  

## Usage 
usage: grid_cut.py [-h] [-A {man,max}] [-I INCLUSION] [-G GRID_SIZE] [--inspection] [-IN INPUT_PATH]  
                   &emsp;&emsp;&emsp;[-OUT OUTPUT_PATH] [-N NAME]
  
options:  
  -h, --help            &emsp;&emsp;&emsp;show this help message and exit  
  -A {man,max}, --arch_type {man,max}  
                        &emsp;&emsp;&emsp;Arch type: Either 'man' for mandible or 'max' for maxilla. Default: man  
  -I INCLUSION, --inclusion INCLUSION  
                        &emsp;&emsp;&emsp;I value for inclusion threshold. Default: 8  
  -G GRID_SIZE, --grid_size GRID_SIZE  
                        &emsp;&emsp;&emsp;Grid size. Default: 5  
  --inspection          &emsp;&emsp;&emsp;Save intermediate files for inspection.  
  -IN INPUT_PATH, --input_path INPUT_PATH  
                        &emsp;&emsp;&emsp;Path to input file.  
  -OUT OUTPUT_PATH, --output_path OUTPUT_PATH  
                        &emsp;&emsp;&emsp;Path to output directory.  
  -N NAME, --name NAME  Name of the final dentition model after cutting.  
  
  ## Examples
  `$ python grid_cut.py -A max -I 7 -G 10 --inspection -IN path/to/input/file.stl -OUT path/to/output/directory`  
  `$ python grid_cut.py --arch_type man --inclusion 2 --grid_size 5 --input_path path/to/input/file.vtp --output_path path/to/output/directory`  
