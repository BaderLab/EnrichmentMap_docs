.. _em_network:

Network Visualization
=====================

.. image:: images/quicktour/network.png
   :width: 80%

Style
-----

EnrichmentMap creates a separate visual style for each network. 
The visual style has the following characteristics:

* Nodes represent gene sets.
* Node size represents the number of genes in the gene set.
* Edges represent overlap (similarity) between gene sets.
* Edge width represents the number of genes that overlap between a pair of gene sets. 

* Node fill represents enrichment scores, such as NES (for GSEA), p-value or q-value. 

  * When there is only 1 data set the enriched phenotype is conveyed using a color gradient.
  * When there are 2 or more data sets nodes are overlayed with charts, where each segment 
    of the chart shows enrichment using a color gradient.

The network is arranged by a force directed layout which causes gene sets with 
high overlap to cluster together.

Expression data is visualized in a separate panel called the Heat Map panel.
For more details see :ref:`heat_map_panel`.


Visual Properties
-----------------

.. warning:: EnrichmentMap automatically maintains the visual properties described below.
             If you manually change these visual properties EnrichmentMap will overwrite
             your changes. If you want to create a custom visual style you must first create a
             copy and then make changes to the copy.

Visual properties are available on the **Style** tab of the Control Panel.

.. image:: images/network/style_tab.png
   :width: 40%

Node Visual Properties
----------------------

.. |node_enr| image:: images/network/node_enr.png

.. |node_sig| image:: images/network/node_sig.png

There are two types of nodes:

  1. Enrichment gene set nodes

     * Regular gene set nodes that are created when the network is first created. 
     * Enrichment nodes can have many different visualizations depending on the 
       settings in the Style section of the :ref:`main_panel`.

  2. Signature gene set nodes

     * Added to an existing network by :ref:`post_analysis`.
     * Do not have chart visualizations.
     * Edges connected to signature nodes are dashed.

  ============ ============
  Enrichment   Signature
  ============ ============
  |node_enr|   |node_sig|
  ============ ============

Visual properties:

=================  ===================  ====================  ==================================
Visual Property    Value                Meaning               Column(s)
=================  ===================  ====================  ==================================
Shape              Circle               Enrichment Gene Set
Shape              Diamond              Signature Gene Set
Fill Color         Discrete Mapping     NES, p/q-value        EM#_pvalue, EM#_fdr_qvalue, EM_NES
Label              Passthrough Mapping  Gene set name         EM#_GS_DESCR
Size               Continuous Mapping   Size of gene set      EM#_gs_size
Image/Chart 1      Chart                NES, p/q-value        EM#_pvalue, EM#_fdr_qvalue, EM_NES
=================  ===================  ====================  ==================================

Edge Visual Properties
----------------------

If the network has only one data set, or if the *Combine edges across data sets* option was
chosen, then all the edges between enrichment gene sets will have the same color.

If there are 2 or more data sets, and the *Separate edge for each data set* option
was chosen, then edges will have different colors for each data set. The edge color corresponds
to the icon next to the data set name in the main panel.




Edges connected to signature gene sets have a different color and are dashed.


Visual properties:

========================  ===================  =============================      =============
Visual Property           Value                Meaning                            Column(s)
========================  ===================  =============================      =============
Line Type                 Solid                Enrichment Gene Sets           interaction
Line Type                 Dashed               Signature gene sets
Stroke Color              
========================  ===================  =============================      =============

Charts
======

