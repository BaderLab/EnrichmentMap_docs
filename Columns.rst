.. _columns:

Columns
=======

EnrichmentMap creates several columns in the node and edge tables. They can
be seen in the **Node Table** and **Edge Table** panels. 

.. image:: images/quicktour/table_panel.png
   :width: 80%

Columns created by EnrichmentMap have the following pattern: ::

  EM#_column_name (data set name)

Where...

* # is a number that is automatically assigned to each network
* *Data set name* is used to differentiate between data sets. 
  There will be one such column for each data set.


Node Columns
~~~~~~~~~~~~

  EM#_Name
    The gene set name.

  EM#_Formatted_name
    A wrapped version of the gene set name so it is easy to visualize.

  EM#_GS_DESCR
    The gene set description (as specified in the second column of the gmt file).

  EM#_Genes
    The list of genes that are part of this gene set. 

  EM#_gs_size
    Number of genes the union of the gene set across all data sets.

  EM#_GS_Type
    Used by the visual style to discern between regular enrichment nodes and 
    signature gene set nodes.

Additionally there are attributes created for each dataset:

  EM#_pvalue (...)
    Gene set p-value, as specified in GSEA enrichment result file.

  EM#_fdr_qvalue (...)
    Gene set q-value, as specified in GSEA enrichment result file.

  EM#_Colouring (...)
    Enrichment map parameter calculated using the formula 1-pvalue multiplied by the sign 
    of the ES score (if using GSEA mode) or the phenotype (if using the Generic mode)

GSEA specific attributes (these attributes are not populated when creating an enrichment 
map using the generic mode).

  EM#_ES_dataset (...)
    Enrichment score, as specified in GSEA enrichment result file.

  EM#_NES_dataset (...)
    Normalized Enrichment score, as specified in GSEA enrichment result file.

  EM#_fwer_qvalue (...)
    Family-wise error score, as specified in GSEA enrichment result file. 


Edge Columns
~~~~~~~~~~~~

For each Enrichment map created the following attributes are created for each edge:

  EM#_Data Set
    Contains the name of the data set that the edge is associated with, or 'compound'
    if the *Combine edges across data sets* option was selected when the network was created.

  EM#_Overlap_size
    The number of genes associated with the overlap of the two gene sets that this edge connects.

  EM#_Overlap_genes
    The names of the genes that are associated with the overlap of the two gene sets that this 
    edge connects.

  EM#_similarity_coefficient
    The calculated coefficient for this edge. 