#subtract a small file from a bigger file
```
grep -vf filesmall filebig
```
#use awk to rearrange columns
```
awk '{print $2 " " $1}' file.txt
```

#sort a bed file by chrom, position
```
sort -k1,1 -k2,2n file.bed > file.sort.bed
```

#strip header
```
tail +2 file > file.nh
```

#find and replace over multiple files
```
perl -pi -w -e 's/255,165,0/255,69,0/g' *.wig
```

#print line 83 from a file
```
sed -n '83p'
```
#insert a header line
```
sed -i -e '1itrack name=test type=bedGraph' file.bed
```

#sum column one from a file
```
awk '{s+=$1} END {print s}' mydatafile
```
