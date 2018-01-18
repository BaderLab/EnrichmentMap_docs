Quick Tour
==========

Creating the Network
--------------------

To create an Enrichment Map network go to the main menu and select **Apps > EnrichmentMap**.

.. image:: images/quicktour/menu.png
   :width: 50%

This will show the EnrichmentMap panels and open the **Create EnrichmentMap Dialog** [*]_.

.. [*] If the Create EnrichmentMap Dialog does not appear then click the (+) icon at the 
       top of the EnrichmentMap Main Panel.

The quickest way to import data is to scan a folder for enrichment analysis data files (for example
a GSEA results folder).

Click the |icon_scan| icon and select a folder. EnrichmentMap will scan the folder
for files containing enrichment data, expression data, ranks, classes and gene set definitions.
These files will be arranged into a **List of Data Sets**, each of which contains the data for 
one experiment. Click the **Build** button to create the network.

.. |icon_scan| image:: images/quicktour/icon_scan.png
   :width: 30px

.. image:: images/quicktour/create_dialog_dataset.png
   :width: 80%

For more details on creating the network see |Create EnrichmentMap Dialog|.


Panels
------

.. image:: images/quicktour/panels.png

1. **Main EnrichmentMap Panel**

   * Used to customize the look of the network in several ways.

2. **EnrichmentMap Network**

   * The Cytoscape network view shows the EnrichmentMap network.

3. **HeatMap (Expression) Panel**

   * Shows gene expression data for selected nodes and edges.


Interpreting the Network
------------------------

* Nodes represent gene sets.
* Node size represents the number of genes in the gene set.
* Edges represent overlap between gene sets.
* Edge width represents the number of genes that overlap.
* The default layout algorithm causes gene sets with high overlap to cluster together.
* Each node contains a chart that shows the enrichment scores, such as NES (for GSEA), 
  p-value or fdr q-value. The enriched phenotype is conveyed by a color gradient. The
  chart data can be changed using the **Style** section of the EnrichmentMap panel.

.. image:: images/quicktour/network.png
   :width: 80%

Clicking on a Node or Edge will show the attributes in the Table panel.
Attributes created by EnrichmentMap start with "EM".

.. image:: images/quicktour/table_panel.png
   :width: 80%

For more details on attributes see |Attributes|.


Main EnrichmentMap Panel
------------------------

The Main EnrichmentMap Panel can be used to customize the network in several ways.

.. image:: images/quicktour/main_panel.png
   :width: 40%

* Filter section

  * **Node cutoff slider**: Nodes with a p-value or q-value that do not pass the cutoff
    are hidden from view.
  * **Edge cutoff slider**: Edges with a similarity score that does not pass the cutoff
    are hidden from view.
  * **Data set list**: Lists Data Sets that were used to create the network. Unchecking
    the checkbox next to the name of a data set causes gene set nodes that are not
    contained in the data set to be hidden from view.
  * **Add signature gene sets button**: Opens the Post Analysis dialog which is used 
    to add more gene sets to the network.

* Style section

  * **Chart data**: Allows to pick which data columns are used by the node charts 
    (e.g. NES, p-value or q-value).
  * **Chart type**: Various chart visualizations are available.
  * **Chart colors**: Various color schemes are available for the charts.

For more details on the EnrichmentMap panel see |EnrichmentMap Panel|.


Legend Dialog
-------------

The legend dialog can be opened by clicking on the gear icon at the top of the main
panel and selecting **Show Legend**.

.. image:: images/quicktour/main_panel_gear.png
   :width: 40%

The Legend Dialog shows a legend with the visual representation of how the network
elements can be interpreted. In particualar it shows what data is visible on the
node charts. The legend can be exported as a PDF file.

.. image:: images/quicktour/legend_dialog.png
   :width: 60%



HeatMap (Expressions) Panel
---------------------------

The HeatMap panel shows gene expression data for selected nodes and edges.

.. image:: images/quicktour/heat_map_panel.png

* **Genes**: You may select multiple gene sets (by selecting several nodes or edges).
  When more than one gene set is selected you may choose to view 
  all of the genes (union) or just the genes that are common (intersection).
* **Expressions**: Allows to show the raw expression data or to normalize the data.
* **Compression**: If there is a large number of expression columns in the HeatMap they
  can be compressed down to the median, min or max value.
* **Show values**: When selected shows the actual expression values, otherwise just shows
  the color gradient.
* The contents of the HeatMap can be exported to a TXT or PDF file.


Post Analysis
-------------