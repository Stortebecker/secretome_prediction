Galaxy workflow for secretome protein prediction via GO annotations and WoLF PSORT
----------------------------------------------------------------------------------

This approach combines Gene Ontology (GO) annotation and WoLF PSORT [1] localization prediction to determine proteins that are expected to be part of the cellular secretome, i.e. proteins either secreted by cells or shed from the cellular surface. For this workflow, we chose to include all proteins annotated or predicted as lysosomal proteins. Lysosomal proteins are routinely secreted by malignant and non-malignant cells in high amounts, due to "leakiness" of the mannose-6-phosphate receptor pathway [2,3]. Furthermore, we chose to exclude proteins annotated as being part of extracellular organelles, e.g. exosomes. While exosomes are secreted by malignant and non-malignant cells, exosomal proteins are expected in the secretome at very low amounts, if not especially enriched for.

.. image::  https://github.com/Stortebecker/secretome_prediction/blob/master/Galaxy-Workflow-Secreted_Proteins_via_GO_annotation_and_WoLF_PSORT.png


[1] P. Horton, K.J. Park, T. Obayashi, N. Fujita, H. Harada, C.J. Adams-Collier, et al., WoLF PSORT: Protein localization predictor, Nucleic Acids Res. 35 (2007) 585–587. doi:10.1093/nar/gkm259.

[2] B. Schröder, C. Wrocklage, A. Hasilik, P. Saftig, The proteome of lysosomes., Proteomics. 10 (2010) 4053–76. doi:10.1002/pmic.201000196.

[3] J. Reiser, B. Adair, T. Reinheckel, Specialized roles for cysteine cathepsins in health and disease, J. Clin. Invest. 120 (2010) 3421–3431. doi:10.1172/JCI42918.

Input Data
==========

The workflow needs three input files:

  1) A tabular file, the first column containing uniprot accession numbers of the proteins of interest.
  2) The complete uniprot GO database for the organism of interest.
  3) The complete GO Open Biomedical Ontology (OBO), i.e. "GO term tree", accessible at http://purl.obolibrary.org/obo/go/go.obo.

Example Dataset
===============

As an example dataset for input 1, you can use a list of human proteins, identified by LC-MS/MS in the cellular supernatant of MDA-MB-231 cells.

* `MDA-MB-231_sample_proteins <https://github.com/Stortebecker/secretome_prediction/blob/master/MDA-MB-231_sample_proteins.tabular>`_

Citation
========

If you use this workflow directly, or a derivative of it, in work leading to a scientific publication,
please cite:

Sigloch, FC, Knopf, JD, Weisser, J, Gomez-Auli, A, Biniossek, ML, and Schilling, O, Proteomic analysis of silenced cathepsin B expression suggests non-proteolytic cathepsin B functionality, BBA Mol.Cell., submitted

Licence (MIT)
=============

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
