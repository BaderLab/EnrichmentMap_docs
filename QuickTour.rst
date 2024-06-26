Quick Start
===========

Open EnrichmentMap
------------------

To create an Enrichment Map network go to the Cytoscape main menu and select **Apps > EnrichmentMap**.

.. image:: images/quicktour/menu.png
   :width: 50%

This will show the EnrichmentMap panels and open the **Create EnrichmentMap Dialog**.
If the Create EnrichmentMap Dialog does not appear then click the (+) icon at the top of 
the EnrichmentMap Main Panel.


Prepare Data Files
------------------

The best way to import data is to first organize the data files into a folder.
EnrichmentMap will scan the folder and automatically detect enrichment, expression, class and gene set files. 
These files are automatically assembled into data sets based on naming conventions. 
This scanning process works well for GSEA because GSEA outputs a folder of results files.
For more details on how EnrichmentMap determines the type of each file see :ref:`scanning`.

Here is some sample GSEA data that can be used for the rest of this tutorial.
Download and extract :download:`enrichmentmap_gsea_tutorial_readthedocs.zip <downloads/enrichmentmap_gsea_tutorial_readthedocs.zip>`.


Load Data Files
---------------

Click the |icon_add| button and select **Scan folder for data sets to add**, then choose folder that contains the data files.
EnrichmentMap will scan the folder
for files containing enrichment data, expression data, ranks, classes and gene set definitions.
These files will be arranged into a **List of Data Sets**, each of which contains the data for 
one experiment. You can also initiate a scan by dragging and dropping folders onto the Data Sets List panel.
Click the **Build** button to create the network.

.. |icon_add| image:: images/quicktour/icon_add.png
   :width: 60px

.. image:: images/quicktour/create_dialog_dataset_2.png
   :width: 90%

.. note:: For more details see :ref:`creating_network`


Panels
------

.. image:: images/quicktour/panels.png

1. **Main EnrichmentMap Panel**

   * Used to customize the look of the network in several ways.

2. **EnrichmentMap Network**

   * The Cytoscape network view shows the EnrichmentMap network.

3. **Expression Panel (Heat Map)**

   * Shows gene expression data for selected nodes and edges.


Interpreting the Network
------------------------

* Nodes represent gene sets.
* Node size represents the number of genes in the gene set.
* Edges represent overlap between gene sets.
* Edge width represents the number of genes that overlap.
* The default layout algorithm causes gene sets with high overlap to cluster together.
* Each node contains a chart that shows the enrichment scores, such as NES (for GSEA), 
  P-value or FDR Q-value. The enriched phenotype is conveyed by a color gradient. The
  chart data can be changed using the **Style** section of the EnrichmentMap panel.

.. image:: images/quicktour/network.png
   :width: 80%

EnrichmentMap creates several columns in the node and edge tables. They can
be seen in the **Node Table** and **Edge Table** panels. Columns created by
EnrichmentMap are in the ``EnrichmentMap`` namespace.

.. image:: images/quicktour/table_panel.png
   :width: 80%

.. note:: For more details see :ref:`em_network`.


Main EnrichmentMap Panel
------------------------

The Main EnrichmentMap Panel can be used to customize the network in several ways.

.. image:: images/quicktour/main_panel4.png
   :width: 40%
   :align: right

* Filter section

  * **Node cutoff slider**: Nodes with a p-value or q-value that do not pass the cutoff
    are hidden from view.
  * **Edge cutoff slider**: Edges with a similarity score that does not pass the cutoff
    are hidden from view.
  * **Data Set list**: Lists Data Sets that were used to create the network. De-selecting
    the checkbox next to the name of a data set causes gene set nodes that are not
    contained in the data set to be hidden from view.
  * **Options button**: Contains options for working with the data set list.


* Style section

  * **Chart data**: Allows to pick which data columns are used by the node charts 
    (e.g. NES, p-value or q-value).
  * **Chart type**: Various chart visualizations are available.
  * **Chart colors**: Various color schemes are available for the charts.

.. note:: For more details see :ref:`main_panel`


Legend Dialog
-------------

The legend dialog can be opened by clicking on the menu icon at the top of the main
panel and selecting **Show Legend**.

.. image:: images/quicktour/main_panel_menu.png
   :width: 50%

The Legend Dialog shows a visual representation of how the network
elements can be interpreted, including what data is visible on the
node charts. The legend can be exported as a PDF file.

.. image:: images/quicktour/legend_dialog.png
   :width: 60%

.. note:: For more details see :ref:`legend_dialog`


Expression Panel (Heat Map)
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

.. note:: For more details see :ref:`heat_map_panel`


Post Analysis (Add Signature Gene Sets)
---------------------------------------

The **Add Signature Gene Sets** panel allows you to add more gene sets to an existing network. This is
also called **Post Analysis**.

To access the dialog click the **Options** button at the top right of the Data Set List,
then select **Add Signature Gene Sets...** in the pop-up menu.

.. image:: images/quicktour/main_panel_pa_button2.png
   :width: 80%

The dialog allows gene set (GMT) files to be loaded from the local file system or downloaded
from the web.

.. image:: images/quicktour/post_analysis_dialog.png
   :width: 500px

.. image:: images/pa/signature_network.png
   :width: 30%
   :align: right

The result of running Post Analysis is a new node for each signature gene set (yellow diamond) 
and edges from the signature gene set to each existing gene set when the similarity passes the 
cutoff test. A new data set for the signature gene sets is added to the data set list on the
Main EnrichmentMap panel.

.. note:: For more details see :ref:`post_analysis`

