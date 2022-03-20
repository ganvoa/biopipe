## prerequisites
- [Install Docker](https://docs.docker.com/engine/install/)

## platon

https://github.com/oschwengers/platon

`docker-compose run platon`

### example

`platon --db /database/platon --output /output /fasta/<filename>.fasta`

### batch

`for FILE in /fasta/*; do platon --db /database/platon --output /output $FILE ; done`

## viralVerify

https://github.com/ablab/viralVerify

`docker-compose run viralVerify`

### example

`viralverify --hmm /database/viralVerify/nbc_hmms.hmm -o /output/ -f /fasta/<filename>.fasta`

### batch

`for FILE in /fasta/*; do viralverify --hmm /database/viralVerify/nbc_hmms.hmm -o /output/ -f $FILE ; done`

## Integron Finder

https://github.com/gem-pasteur/Integron_Finder

`docker-compose run integron`

### example

`integron_finder --local-max --outdir /output/ --pdf --gbk --func-annot /fasta/<filename>.fsa_nt`

### batch

`for FILE in /fasta/*; do integron_finder --local-max --outdir /output/ --pdf --gbk --func-annot $FILE ; done`

## abricate

https://github.com/tseemann/abricate

`docker-compose run abricate`

### example

`abricate --csv /fasta/<filename>.fsa_nt > /output/<filename>.csv`

### batch

`for FILE in /fasta/*; do abricate --csv $FILE > /output/$(basename "$FILE").csv  ; done`

## unicycler

https://github.com/rrwick/Unicycler.git

### Illumina-only assembly:

`docker-compose run --rm  unicycler -1 fasta/<fasta1>.gz -2 fasta/<fasta2>.gz -o output`
### Hybrid assembly:

`docker-compose run --rm  unicycler -1 fasta/<fasta1>.gz -2 fasta/<fasta2>.gz -l <long_reads.fastq>.gz -o output`

## mobsuite

https://github.com/phac-nml/mob-suite

### mob recon:

`docker-compose run --rm mobsuite mob_recon -i fasta/<fasta>.fasta -t -o output/<folder-name>`

## ariba

https://github.com/sanger-pathogens/ariba

### example:

`docker-compose run --rm ariba test /output/<folder-name>`