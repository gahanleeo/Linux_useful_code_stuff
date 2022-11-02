# Linux_useful_code_stuff

## `printif` use printif to create UCSC track text file

```printf "browser position chr22:38,700,000-39,300,000\nbrowser hide all\n" > custom_UCSC_track.bed```


### Add the track for overlapping regions:

```(printf "track name=\"overlap regions\" description=\"example for bedtools A intersect B\" visibility=1 color=0,0,255 useScore=1\n#chrom\tchromStart\tchromEnd\tname\tscore\tstrand\n" && cat intersect_overlap.bed)  >> custom_UCSC_track.bed```


### Add the track for full length of genes:

```(printf "track name=\"original genes\" description=\"example for bedtools A intersect B -wa\" visibility=3 color=255,0,0 useScore=1\n#chrom\tchromStart\tchromEnd\tname\tscore\tstrand\n" && cat intersect_full_length_genes.bed)  >> custom_UCSC_track.bed```


