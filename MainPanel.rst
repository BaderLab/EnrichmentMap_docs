.. image:: images/main_panel/main_panel_red.png
   :width: 30%
   :align: right

.. _main_panel:

Main Panel
==========


The main EnrichmentMap panel has the following sections:

1. Toolbar
2. Filter section
3. Style section

Each of these sections will be explained in more detail below.

If the main panel is not visible go to the Cytoscape main menu and select **Apps > EnrichmentMap**.

To hide the panel click the **Close** button at the bottom right.


Toolbar
-------

.. image:: images/main_panel/toolbar.png
   :width: 40%

.. |plus_button| image:: images/main_panel/plus_button.png
   :width: 20px

.. |gear_button| image:: images/main_panel/gear_button.png
   :width: 20px

.. |refresh_button| image:: images/main_panel/refresh_button.png
   :width: 20px

* Network combo box

  * This combo box can be used to quickly switch between EnrichmentMap networks without having
    to navigate to the *Network* tab. Only networks created by EnrichmentMap are listed. 

* Plus button |plus_button|

  * Opens the *Create EnrichmentMap Dialog*.

* Gear button |gear_button|

  * Opens the panel menu (explained in more detail below).


Panel Menu
~~~~~~~~~~

.. image:: images/main_panel/gear_menu.png
   :width: 40%

.. |none| image:: images/main_panel/filter_none.png
   :width: 140px

.. |highlight| image:: images/main_panel/filter_highlight.png
   :width: 140px

.. |hide| image:: images/main_panel/filter_hide.png
   :width: 140px

* Show Legend
 
  * Opens the :ref:`legend_dialog`.

* Hide/Highlight filtered nodes and edges

  * Changes the appearance of nodes and edges that are filtered out. See `Filter Section`_ below.

============  ============  ============
No Filter     Highlight     Hide           
============  ============  ============
|none|        |highlight|   |hide|  
============  ============  ============


Filter Section
--------------

.. image:: images/main_panel/filter_section.png
   :width: 40%
   :align: right

The filter section is used to hide nodes and edges in the network.

* Node cutoff

  * Use the radio buttons to switch between p-value and q-value.
  * The slider is initially set all the way to the right, which corresponds to the value that was entered
    in the *Create EnrichmentMap Dialog* when the network was created. 
  * As the slider is moved to the left nodes with a p-value/q-value greater than the cutoff are hidden.
    Edges connected to hidden nodes are also hidden.
  * P-values can be found in the *Node Table* in columns that start with *EM#_pvalue*.
  * Q-values can be found in the *Node Table* in columns that start with *EM#_fdr_qvalue*.

* Edge cutoff

  * This slider is initially set all the way to the left, which corresponds to the smallest edge similarity
    score in the network.
  * As the slider is moved to the right edges with a similarity score less than the cutoff are hidden.
  * Similarity scores can be found in the *Edge Table* in the column named *EM#_similarity_coefficient*.

* Data Sets list

  * The data set list shows then names of all the data sets as well as the number of gene sets in each data set.
  * Initially the checkbox next to each data set is selected.
  * De-selecting the checkboxes hides gene set nodes that are only contained in those data sets.

* Add Signature Gene Sets button

  * Click to open the :ref:`post_analysis` dialog.

The number of hidden nodes and edges can be seen in the status bar under the network view.

.. image:: images/main_panel/hidden.png
   :width: 60%

 
.. _style_section:

Style Section
-------------

.. image:: images/main_panel/style_section.png
   :width: 40%
   :align: right


The style panel is mainly used to manipulate chart visualizations on nodes.

For more details on chart visualizations see :ref:`chart_visualization`.

* Chart Data

  * -- None --

    * If there is 1 data set then node shows a pre-computed color gradient for the p-value. 
      If there are 2 or more data sets then the node color has no meaning and is set to grey.

  * NES Columns

    * Enrichment values from the *EM#_NES* columns are used.
    * Only available if the analysis type is GSEA.

  * P-value Columns

    * Enrichment values from *EM#_pvalue* columns are used.

  * Q-value (FDR) Columns

    * Enrichment values from *EM#_fdr_qvalue* columns are used.

* Chart Type

  * Field is enabled if *Chart Data* is set to a value other than *-- None --*.

  * Three chart types are available: Radial Heat Map, Heat Map, and Heat Strips.
    For more details see :ref:`chart_visualization`.

* Color Scheme

  * Several `Color Brewer <http://colorbrewer2.org/#type=diverging&scheme=BrBG&n=3>`_ colorblind 
    safe palettes are available.
  * When *NES Columns* is chosen for Chart Data then the **RdBu-9** palette will be available.
    This palette is the same as the standard color gradient used in EnrichmentMap 2.0.

* Show chart labels

  * Enable this option to show enrichment values for each chart segment.

* Publication-Ready

  * Makes the network view ready for printing. Removes node labels and sets the network background
    to white.

* Set Signature Edge Width...

  * Opens a dialog that has several options for how the width of signature edges is calculated.
    For more details see :ref:`edge_width_dialog`.

* Refresh Button |refresh_button|

  * Resets the visual style.
  * Sometimes Cytoscape does not update the visual style properly. To fix any inconsistencies
    between the network view and the Style section of the main panel click this button.



