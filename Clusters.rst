.. _clusters:

Finding Clusters with AutoAnnotate
==================================

.. image:: images/clusters/main_panel_cluster_button.png
   :width: 50%
   :align: right

The **AutoAnnotate** app must be installed for this functionality.
https://apps.cytoscape.org/apps/autoannotate


At the bottom of the main EnrichmentMap panel there is a button that says
**Find Clusters**.


This button provides two options:

* **Use AutoAnnotate to find clusters of similar nodes**

  * This option simply opens the AutoAnnotate dialog. For more information
    on all the options for finding and highlighting clusters see the AutoAnnotate docs: 
    https://autoannotate.readthedocs.io/en/latest/CreatingAnAnnotationSet.html

.. image:: images/clusters/clusters.png
   :width: 90%

* **Highlight significant nodes**

  * This option runs AutoAnnotate automatically. It finds clusters of highly
    significant nodes and simply highlights the most significant node in each cluster.
    Highlighted nodes are given larger labels.

  * The clusters can be seen in the AutoAnnotate main panel.
    https://autoannotate.readthedocs.io/en/latest/WorkingWithAutoAnnotate.html

.. image:: images/clusters/significant_nodes.png
   :width: 90%


Significance
~~~~~~~~~~~~

The attribute used to determine significance is based on the current **Chart Data** setting
in the Style panel. If you change the Chart Data attribute it will update the highlighted
nodes accordingly.

.. image:: images/clusters/style_panel.png
   :width: 40%

.. image:: images/clusters/significant_nodes_nes.png
   :width: 90%