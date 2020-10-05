# Command-line Statistics Tools

A growing collection of handy scripts to do minor statistical computations and 
plotting from the command line.

## Installation

Simply clone this repository and add the ``scripts`` directory to your 
``PATH`` variable. For instance, in ``~/.bashrc`` add:

```bash
export PATH=$PATH:/path/to/cli_stats/scripts
```

## Examples

### Paired t-test

This was added when I changed part of 
[CleverCSV](https://github.com/alan-turing-institute/CleverCSV) and wanted to 
test whether the runtime was significantly improved. I had a file 
``old_runtime.log`` and a file ``new_runtime.log`` each in the format 
``<filename>,<runtime>`` with observations for the same set of files 
(important for the paired t test!).

```
$ paste <(cat old_runtime.log | sort | cut -d',' -f2) <(cat new_runtime.log | sort | cut -d',' -f2) | paired_t_test
Test statistic: 3.6666 (p = 0.0003)
```

## Notes

MIT License, written by [Gertjan van den Burg](https://gertjan.dev).
