# files from Taurus

The Makefile enclosed here collects all .tsv files that end with `-[0-9][0-9].tsv` and tries to condense them into one single tsv per unique item.

## How to use

``` bash
$ make condense
```

creates 

``` bash
ls *condensed.tsv
resnet32v1-short-bs128-condensed.tsv              resnet32v1-short-singularity-condensed.tsv
resnet32v1-short-bs128-singularity-condensed.tsv  resnet32v1-short-singularity-nfs-condensed.tsv
resnet32v1-short-condensed.tsv
```

