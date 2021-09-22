## prerequisites
- [Install Docker](https://docs.docker.com/engine/install/)

## platon

https://github.com/oschwengers/platon

`docker-compose run platon`

`platon --db /database/platon --output /output /fasta/<filename>.fasta`

## viralVerify

https://github.com/ablab/viralVerify

`docker-compose run viralVerify`

`viralverify --hmm /database/viralVerify/<filename>.hmm -o /output/ -f /fasta/<filename>.fasta`

## Integron Finder

https://github.com/gem-pasteur/Integron_Finder

`docker-compose run integron`

`integron_finder --local-max --outdir /output/ --pdf --gbk --func-annot /fasta/<filename>.fsa_nt`

## abricate

https://github.com/tseemann/abricate

`docker-compose run abricate`

`abricate --csv /fasta/<filename>.fsa_nt > /output/<filename>.csv`