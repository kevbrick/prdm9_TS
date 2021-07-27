# Infer putative parentage among PRDM9 alleles
Script to infer putative template switching events that create new PRDM9 ZF arrays from others. Adapted from Alleva et al. 2021. 

## Requirements:
* Linux (tested on Ubuntu 20.04)
* Perl Getopt::Long module
* FASTA file with the DNA sequences of PRDM9 Zinc-finger arrays (not needed for initial tests)
 
## Notes:
See Alleva et al. 2021 for details.

### Installation: 
Simply download and run the test : `infer_PRDM9_template_switches --t `

### Run :
Get help: 
`infer_PRDM9_template_switches --h`

With a FASTA file: This will look for all possible parent:child relationships between sequences in the FASTA file. 
`infer_PRDM9_template_switches --f <<FASTA file>>`

For select child alleles: This will look for all possible parent:child relationships involving PRDM9-N as the child allele (all allele combinations will be explored).
`infer_PRDM9_template_switches --f <<FASTA file>> --c N`

For select parental & child alleles: This will look for all possible parent:child relationships involving PRDM9-N as the child allele anw with PRDM9-A and PRDM9-C as potential parental alleles.
`infer_PRDM9_template_switches --f <<FASTA file>> --c N --p A,C`
