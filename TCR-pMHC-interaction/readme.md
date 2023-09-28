###############
# Description #
###############
This directory contains raw data and data filtered at 3 levels:
- raw: GEMs containing both TCR and pMHC reads. TCR CDR3 sequences must be IUPAC encoded.
- opt_thr: raw data filtered by optimal UMI thresholds defined by ITRAP.
- hla_match: opt_thr data additionally filtered by matching HLA ofpMHC with donor HLA profile.
- tcr: hla_match data additionally filtered to only contain GEMs with both TCRa- and TCRb-chain.

###########
# Columns #
###########
gem	Unique identifier for each droplet capture (10x barcode)
clonotype	Identifier for each clonotype (annotated by 10x)
ct	Identifier for each clonotype (annotated by ITRAP)
genes_TRA	The set of TCRa-chain genes with highest UMI count in a GEM (annotated by 10x)
genes_lst_TRA	List of all TCRa-chain genes detected in a GEM (sep="|")
genes_TRB	The set of TCRb-chain genes with highest UMI count in a GEM (annotated by 10x)
genes_lst_TRB	List of all TCRb-chain genes detected in a GEM (sep="|")
cdr3_TRA	The a-chain CDR3 sequence derived from genes_TRA
cdr3_lst_TRA	List of all a-chain CDR3 sequences detected in a GEM (sep="|")
cdr3_TRB	The b-chain CDR3 sequence derived from genes_TRB
cdr3_lst_TRB	List of all b-chain CDR3 sequences detected in a GEM (sep="|")
umi_count_TRA	UMI count of most abundant TCRa-chain in a GEM
umi_count_lst_TRA	List of all TCRa UMI detected in a GEM (sep="|")
umi_count_TRB	UMI count of most abundant TCRb-chain in a GEM
umi_count_lst_TRB	List of all TCRb UMI detected in a GEM (sep="|")
peptide_HLA	peptide and cognate MHC molecule used for staining
peptide_HLA_lst	List of all pMHC barcodes detected in a GEM (sep="|")
umi_count_mhc	UMI count of most abundant pMHC in a GEM
umi_count_lst_mhc	List of all pMCH UMI detected in a GEM (sep="|")
sample_id	Identifier for donor
sample_id_lst	NA
umi_count_cd8	NA
umi_count_lst_cd8	NA
HLA_cd8	HLA profile of donor
HLA_match	Boolean label for match between HLA of pMHC and donor HLA profile
valid_ct	Boolean label for whether clonotype was used for ITRAP threshold optimization
ct_pep	Indication of expected binder for given clonotype
