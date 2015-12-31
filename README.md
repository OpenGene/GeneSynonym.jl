# GeneMisc
[![Build Status](https://travis-ci.org/OpenGene/GeneMisc.jl.svg?branch=master)](https://travis-ci.org/OpenGene/GeneMisc.jl) 
[![Documentation Status](http://readthedocs.org/projects/genemiscjl/badge/?version=latest)](http://genemiscjl.readthedocs.org/en/latest/?badge=latest)

### What can GeneMisc do now?
* Given a location,  find gene.
* Given a location,  find nearest gene name and exon number.

* Given a gene nane, find its location.
* Given a gene name, find its synonyms genes, but the synonyms genes may not complete due to the limitation of our data.


### Add GeneMisc

	Pkg.clone("https://github.com/OpenGene/GeneMisc.jl.git")
	Pkg.build("GeneMisc")
	Pkg.test("GeneMisc")
	
This project is under active developing, if you encountered any troubles, open an issue please.

For more information, please refer to the [documentation](http://genemiscjl.readthedocs.org/en/latest/).

### Examples of Usage

**query a gene for its synonym**

	using GeneMisc
	query_gene("TP53")
	
**query a lot of genes**

	using GeneMisc
	genes = ASCIIString["TP53","KRAS","BRCA"]
	query_gene(genes)

**query a gene given its location**

	using GeneMisc
	chr = "chr1"
	pos = "12235"
	query_gene(chr,pos)
	
**query a lot of genes given their locations**

	using GeneMisc
	chr_pos = ["chr1" "123234";
               "chr2", "21424"]
	query_gene(chr_pos)
