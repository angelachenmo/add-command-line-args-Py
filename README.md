# Add command line arguments (Python)
Copyright: Tiffany Timbers, 2023

## Introduction to this repository

This is a template repository to act as a practice playground 
to get experience writing scripts with command line arguments.

Currently the `src/count_classes.py` script only works 
on the `cancer_train.csv` data set in the `data` directory. 
And it only writes the results as a csv file to the 
`results/cancer` directory. 
It must also be run from the root of the project to work.

You can test that the script works by running the following 
from the root of the project's directory:

```
python src/count_classes.py
```

## Exercise

Your task is to use the Python package 
[`click`](https://click.palletsprojects.com/en/8.1.x/)
to add command line arguments so that other data files 
can be passed to it, 
and so that the results can be written to other directories.

To help get you started, 
take a look at the `click` docs for arguments:
<https://click.palletsprojects.com/en/8.1.x/arguments/#basic-arguments>.


Below, we also provide you an example of a python script 
that uses `click` so that it can be run at the command line 
to print the sum of two numbers.

```{python}
import click

@click.command()
@click.argument('num1', type=int)
@click.argument('num2', type=int)
def main(num1, num2):
    """Simple program that adds two numbers."""
    result = num1 + num2
    click.echo(f"The sum of {num1} and {num2} is {result}")

if __name__ == '__main__':
    main()
```

To run this script from the terminal, 
you would navigate to the directory containing `sum.py` 
and run:

```{bash}
python sum.py 5 7
```

This will lead to the script running using `5` as the 
value for the `num1` argument, 
and `7` as the value for the `num2` argument.  
And the result being printed to the terminal:

```
The sum of 5 and 7 is 12
```

## Optional/advanced exercise:

When you get the `src/count_classes.py` script working using 
positional command line arguements (as in the example above),
try to improve it further by naming the arguments 
(we call this adding command line "options").
The `click` docs for this are here: 
<https://click.palletsprojects.com/en/8.1.x/options/#basic-value-options>

# License
Add command line arguments (Python) exercise contained herein are licensed under the [Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0) License](https://creativecommons.org/licenses/by-nc-sa/4.0/).
See [the license file](LICENSE.md) for more information. If
re-using/re-mixing please provide attribution and link to this webpage.
The software code contained within this repository is licensed under the
MIT license. See [the license file](LICENSE.md) for more information.
