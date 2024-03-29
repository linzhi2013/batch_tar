# batch-tar

## 1 Introduction

`batch-tar` is a tool to tar (and compress) files or directories in batch mode.

## 2 Installation

    pip install batch-tar

There will be a command `batch_tar` created under the same directory as your `pip` command.

## 3 Usage

    $ batch_tar

    usage: batch_tar [-h] [-l <file>] [-L [<str> [<str> ...]]]
                     [-workdir <directory>] [-tarfile <str>] [-regex <str>]
                     [-compress {z,j}] [-rm] [-p] [--version]

    To tar/compress files/directories in batch mode. By Guanliang Meng, see
    https://github.com/linzhi2013/batch_tar. version: 0.1

    optional arguments:
      -h, --help            show this help message and exit
      -l <file>             path list to be dealed with
      -L [<str> [<str> ...]]
                            basenames of files/subdirecotries in `-workdir`. If
                            `-workdir` was not specified, `-workdir ./` is
                            assumed.
      -workdir <directory>  working directory. must specify `-regex` together
      -tarfile <str>        group all the files/subdirecotries into one file.tar
                            (.bz2 or .gz). only works with `-L` and `-workdir`
      -regex <str>          deal with only the files/subdirecotries in `-l` or
                            `-workdir` whose basenames match the regular
                            expression
      -compress {z,j}       For the subdirecotries, when executing `tar -cf`, also
                            add parameter `z` or `j` for `tar` command. The files
                            will always be gzipped if this option was not set.
      -rm                   delete the files/subdirecotries when tar finishs.
      -p                    only print out the commands, not run. then you can use
                            qsub-sge.pl to submit multiple jobs. Useful to handle
                            a lot of files because I run in single thread mode
                            only! [False]
      --version             show program's version number and exit

## Author
Guanliang MENG

## Citation

Currently I have no plan for publishing this script.

**However, if you use this program in your analysis, or you "steal" the idea/codes of this program into your script, I should be one of the co-authors in your publication!!!**




