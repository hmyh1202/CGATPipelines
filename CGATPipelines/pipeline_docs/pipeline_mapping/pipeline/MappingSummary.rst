===============
Mapping summary
===============

This section gives an overview over the mapping results.

Please be aware that there is a difference between :term:`read` and :term:`alignment`
counts. A single :term:`read` might map to several genomic positions and give rise
to several alignments. Only if the mapper employs unique-ness filtering will 
:term:`read` and :term:`alignment` counts be the same.

Alignment summary
=================

This section presents an overview of the :term:`alignments` in the 
BAM files for each :term:`track`. Note that a read can have multiple alignments.

.. report:: Mapping.BamSummary
   :render: table
   :slices: mapped,reverse,rna,duplicates

   Mapping summary

.. report:: Mapping.BamSummary
   :render: interleaved-bar-plot
   :slices: mapped,reverse,rna,duplicates

   Mapping summary

.. report:: Mapping.MappingFlagsMismatches
   :render: line-plot
   :as-lines:
   :layout: column-3
   :width: 200
   :split-at: 10

   Number of alignments per number of mismatches in alignment.

Reads summary
=============

This section presents an overview of the mapping results in terms 
of :term:`reads`.

.. report:: Mapping.BamSummary
   :render: table
   :slices: reads_total,reads_mapped,reads_norna,reads_norna_unique_alignments

   Mapping summary

.. report:: Mapping.BamSummary
   :render: interleaved-bar-plot
   :slices: reads_total,reads_mapped,reads_norna,reads_norna_unique_alignments

   Mapping summary

.. report:: Mapping.MappingFlagsHits
   :render: line-plot
   :as-lines:
   :layout: column-3
   :width: 200
   :xrange: 0,10
   :split-at: 10

   Number of reads per number of alignments (hits) per read.