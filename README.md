# public_data_crisprCas9

CRISPR/Cas9 benchmark data sets used for on- and off-target prediction, available for download.

------

## Data Ready for Machine Learning and Deep Learning Experiences

In this section, we provide encoded data sets ready for use in machine learning and deep learning experiments, without the need of data preprocessing. 

| Data Designation | Original Data Sets | Encoded Matrix Size | Data Link 
|:---:|:---:|:---:|:---:|
| Data Set 1 | [CIRCLE-Seq by Tasi et al. [1]](http://bio.info.uqam.ca/data/I_1_CIRCLE_seq_10gRNA_wholeDataset.csv), <br> [GUIDE-Seq I by Listgarten et al. [2]](http://bio.info.uqam.ca/data/I_2_elevation_6gRNA_wholeDataset.csv), <br> [Protein knockout detection by Doench et al. [3]](http://bio.info.uqam.ca/data/II_1_listgarten_elevation_cd33.csv), <br> [PCR, Digenome-Seq and HTGTS by Haeussler et al. [4]](http://bio.info.uqam.ca/data/II_2_listgarten_elevation_hmg.csv), <br> [SITE-Seq by Cameron et al. [5]](http://bio.info.uqam.ca/data/II_3_SITE-Seq_offTarget_wholeDataset.csv),<br> [GUIDE-Seq by Tasi et al. [6]](http://bio.info.uqam.ca/data/II_4_listgarten_elevation_guideseq.csv),<br> [GUIDE-Seq by Kleinstiver et al. [7]](http://bio.info.uqam.ca/data/II_5_Kleinstiver_5gRNA_wholeDataset.csv),<br> [GUIDE-Seq II by Listgarten et al. [2]](http://bio.info.uqam.ca/data/II_6_Listgarten_22gRNA_wholeDataset.csv) | 7x23 <br> (Lin et al. 2020 [8]) | [Direct Link for Download (2.0 GB)](http://bio.info.uqam.ca/data/encoded_data_for_experiments.pkl)
| Data Set 2 | [CRISPR-Cas9 by Lin and Wong 2018 [9]](http://bio.info.uqam.ca/data/lin_crispor_encoded_data.pkl.zip), <br> [GUIDE-Seq by Tsai et al. 2015 [6]](http://bio.info.uqam.ca/data/tsai_validated_offtargets.tsv) | 8x23 <br> (Charlier et al. 2021 [10]) | [Direct Link for Download (37.4 MB)](http://bio.info.uqam.ca/data/encoded_data_charlier_et_al.pkl)


Data Set 1 is a bunch data set (for more information, refer to [sklearn.utils.Bunch](https://scikit-learn.org/stable/modules/generated/sklearn.utils.Bunch.html)) containing 7 different data sets, presented in Table 1 of Lin et al. [8]. A brief description of the bunch data set is available on [this GitHub page](https://github.com/dagrate/transferlearning-bioinfo). 
Data Set 1 is encoded using the one-hot encoding technique introduced by Lin et al. [8].  <br>

Data Set 2 is a bunch data set (for more information, refer to [sklearn.utils.Bunch](https://scikit-learn.org/stable/modules/generated/sklearn.utils.Bunch.html)) containing both CRISPR and Guide-Seq data sets used in Charlier et al. [10].
Data Set 2 is encoded using the one-hot encoding technique introduced by Charlier et al. [10].  <br>

```python
# how to read the encoded Bunch data files
import pickle as pkl
with open('data_set_i.pkl', 'rb') as f: # change data_set_i by the name of your file
  data = pickle.load(f)
print(data)
```
Using the code above, the user can get access to one hot-encoded sgRNA-DNA sequence data (encoded as binary matrices) and to the positive/negative sample information (0 for non-validated off-targets and 1 for validated off-targets). For more information on how to process the Bunch data sets, we invite the reader to check the [demo notebook file](https://github.com/dagrate/public_data_crisprCas9/blob/main/a_demo_of_a_simple_classification_model.ipynb).

### Tutorial for Machine Learning and Deep Learning Experiences

A [demo notebook file](https://github.com/dagrate/public_data_crisprCas9/blob/main/a_demo_of_a_simple_classification_model.ipynb) is available to illustrate how to use the encoded Bunch data sets and how to train a simple machine learning model. 

------

## Data Set Description

### Off-Targets Data Sets Description

Data sets containing only off-targets activities.

Source | Year | Data description | Target | Original data source & Curated Data |
|:---:|:---:|:---:|:---:|:---:|
| GUIDE-seq data [6] | 2015 | CRISPR RNA-guided nucleases (RGNs) from two human cell lines: U2OS and HEK293; different sites such as VEGFA sites 1, 2 and 3, and HEK293 sites 2, 3 and 4 were studied | Off-targets | Original Data Source: <br> [Direct Link](https://github.com/tsailabSJ/guideseq/tree/master) |
| CIRCLE-Seq data [1] | 2017 | Contains mismatch, insertion, and deletion information, and includes sgRNA-DNA pairs from 10 guide sequences, 7,371 of which are off-targets (430 with bulges) | Off-targets | [Direct Link](https://github.com/tsailabSJ/circleseq) |
|SITE-Seq [5] | 2017 | gRNA-DNA pairs from nine guide sequences, 3,767 of which are active off-targets (no bulges) | Off-targets | Original Data Source: <br> [Direct Link](https://www.nature.com/articles/nmeth.4284) <br><br> Direct Link for Data Download: <br> [Github Link](https://github.com/dagrate/public_data_crisprCas9/tree/main/data/site_seq) |
| CHANGE-seq data [11] | 2020 | 110 sgRNA targets across 13 therapeutically relevant loci in human primary T-cells were studied to identify 201,934 off-target sites across the human genome | Off-targets | Original Data Source: <br> [Direct Link](https://github.com/tsailabSJ/changeseq)  <br><br> Direct Link for Data Download: <br> [NBCI GEO Link](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE149295) |
| Listgarten elevation hmg data [2] | 2018 | 10,129 human exome targets pre-computed | Off-targets | Original Data Source: <br> [Direct Link](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6037314/) <br><br> Direct Link for Data Download: <br> [Github Link](https://github.com/dagrate/public_data_crisprCas9/tree/main/data/listgarten_elevation_hmg) |
| Kleinstiver 5gRNA data [12] | 2015 | GUIDE-Seq pre-computed | Off-targets | Original Data Source: <br> [Direct Link](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4540238/pdf/nihms696684.pdf) <br><br> Direct Link for Data Download: <br> [Github Link](https://github.com/dagrate/public_data_crisprCas9/tree/main/data/kleinstiver2015) |


### On-Targets Data Sets Description

Data sets containing only on-targets activities.

Source | Year | Data description | Target | Original data source & Curated Data |
|:---:|:---:|:---:|:---:|:---:|
| Wang et al. data [13] | 2014 | A library containing 73, 000 sgRNAs | On-targets | Original Data Source: <br> [Direct Link](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3972032/#SD2) <br><br> Direct Link for Data Download: <br> [Github Link](https://github.com/dagrate/public_data_crisprCas9/tree/main/data/wang2014genetic) |
| Koike-Yusa et al. data [14] | 2014 | 87,897 gRNAs targeting 19,150 mouse protein-coding genes | On-targets | Original Data Source: <br> [Direct Publication Link](https://www.ebi.ac.uk/ena/browser/view/PRJEB4038) <br><br> Direct Link for Data Download: <br> [Direct Link](https://www.ebi.ac.uk/ena/browser/view/PRJEB4038) |
| Doench V1 data [15] | 2014 | 1,831 guides targeting three human (CD13, CD15, and CD33) and six mouse genes (Cd5, Cd28, H2-K, Cd45, Thy1, and Cd43) | On-targets | Original Data Source: <br> [Direct Link](https://portals.broadinstitute.org/gppx/crispick/public) |
| GenomeCRISPR database [16] | 2016 | Aggregate data for more than 550,000 sgRNAs derived from 84 experiments | On-targets  | Original Data Source: <br> [Direct Link](http://genomecrispr.org) |
| DeepHf data [17] | 2019 | Includes indel rates of over 50,000 gRNAs for each nuclease, covering about 20,000 genes. It is the largest gRNA on-target activity set reported for mammalian cells | On-targets | Original Data Source: <br> http://www.DeepHF.com <br> [Direct Link](https://github.com/izhangcd/DeepHF) <br><br> Direct Link for Data Download: <br> [Github Link](https://github.com/dagrate/public_data_crisprCas9/tree/main/data/deepHF) |
| DeepSpCas9 [18] | 2019 | SpCas9 activities at 12,832 integrated target sequences for a human cell library | On-targets | Original Data Source: <br> [Direct Link](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6834390/) <br><br> Direct Link for Data Download: <br> [NBCI SRA](https://www.ncbi.nlm.nih.gov/sra/SRP150719)
| SgDesigner [19] | 2020 | A unique plasmid library expressed in human cells used to quantify the potency of thousands of CRISPR/Cas9 sgRNAs (a pool of 12,472 oligonucleotides was studied) | On-targets | Original Data Source: <br> [Direct Link](https://academic.oup.com/bioinformatics/article/36/9/2684/5714741#supplementary-data) <br><br> Link for the sgDesigner Model [GitHub sgDesigner](https://github.com/wang-lab/sgDesigner) <br><br>  Direct Link for Data Download: [GitHub Link](https://github.com/dagrate/public_data_crisprCas9/tree/main/data/sgDesigner)



### On- & Off-Targets Data Sets Description

Data sets containing both on- and off-targets activities.

Source | Year | Data description | Target | Original data source & Curated Data |
|:---:|:---:|:---:|:---:|:---:|
| Doench V2 data [3] | 2016 | 2,549 unique guides targeting eight genes (CCDC101, MED12, TADA2B, TADA1, HPRT, CUL3, NF1, and NF2) from human A375 cells | Off-targets and On-targets | Original Data Source: <br> [Direct Publication Link](https://www.nature.com/articles/nbt.3437) <br><br> Direct Link for Data Download: <br> [Direct Link](https://www.nature.com/articles/nbt.3437#Sec24) |
| CRISPOR Database [4] | 2016 | Aggregate data for more than 50 genomes | Off-targets and On-targets | Original Data Source: <br> [Direct Link 1 (web server)](http://crispor.tefor.net/) <br><br> [Direct Link 2 (data)](https://github.com/maximilianh/crisporPaper/tree/master/effData#readme) <br><br> Direct Link for Data Download: <br> [Github Link](https://github.com/MichaelLinn/off_target_prediction/blob/master/data/crispor_encoded_data.pkl.zip) |
| DeepCRISPR platform [20] | 2018 | Includes approximately 0.68 billion sgRNA sequences derived from 13 human cell lines | Off-targets and On-targets | Original Data Source: <br> [Direct Link](https://github.com/bm2-lab/DeepCRISPR) <br><br> Direct Link for Data Download (samples): <br> [Github Link](https://github.com/dagrate/public_data_crisprCas9/tree/main/data/deepcrispr) |


------

## Citation

Sherkatghanad, Z., Abdar, M., Charlier, J. and Makarenkov, V., Using Traditional Machine Learning and Deep Learning Methods for On-and Off-Target Prediction in CRISPR/Cas9: A Review, submitted (2023).

------

## References 
[1]: Tsai, S.Q., Nguyen, N.T., Malagon-Lopez, J., Topkar, V.V., Aryee, M.J. and Joung, J.K., 2017. CIRCLE-seq: a highly sensitive in vitro screen for genome-wide CRISPR–Cas9 nuclease off-targets. Nature methods, 14(6), pp.607-614. <br>
[2]: Listgarten, J., Weinstein, M., Kleinstiver, B.P., Sousa, A.A., Joung, J.K., Crawford, J., Gao, K., Hoang, L., Elibol, M., Doench, J.G. and Fusi, N., 2018. Prediction of off-target activities for the end-to-end design of CRISPR guide RNAs. Nature biomedical engineering, 2(1), pp.38-47. <br>
[3]: Doench, J.G., Fusi, N., Sullender, M., Hegde, M., Vaimberg, E.W., Donovan, K.F., Smith, I., Tothova, Z., Wilen, C., Orchard, R. and Virgin, H.W., 2016. Optimized sgRNA design to maximize activity and minimize off-target effects of CRISPR-Cas9. Nature biotechnology, 34(2), pp.184-191. <br>
[4]: Haeussler, M., Schönig, K., Eckert, H., Eschstruth, A., Mianné, J., Renaud, J.B., Schneider-Maunoury, S., Shkumatava, A., Teboul, L., Kent, J. and Joly, J.S., 2016. Evaluation of off-target and on-target scoring algorithms and integration into the guide RNA selection tool CRISPOR. Genome biology, 17, pp.1-12. <br>
[5]: Cameron, P., Fuller, C.K., Donohoue, P.D., Jones, B.N., Thompson, M.S., Carter, M.M., Gradia, S., Vidal, B., Garner, E., Slorach, E.M. and Lau, E., 2017. Mapping the genomic landscape of CRISPR–Cas9 cleavage. Nature methods, 14(6), pp.600-606. <br>
[6]: Tsai, S.Q., Zheng, Z., Nguyen, N.T., Liebers, M., Topkar, V.V., Thapar, V., Wyvekens, N., Khayter, C., Iafrate, A.J., Le, L.P. and Aryee, M.J., 2015. GUIDE-seq enables genome-wide profiling of off-target cleavage by CRISPR-Cas nucleases. Nature biotechnology, 33(2), pp.187-197. <br>
[7]: Kleinstiver, B.P., Pattanayak, V., Prew, M.S., Tsai, S.Q., Nguyen, N.T., Zheng, Z. and Joung, J.K., 2016. High-fidelity CRISPR–Cas9 nucleases with no detectable genome-wide off-target effects. Nature, 529(7587), pp.490-495. <br>
[8]: Lin, J., Zhang, Z., Zhang, S., Chen, J. and Wong, K.C., 2020. CRISPR‐Net: A Recurrent Convolutional Network Quantifies CRISPR Off‐Target Activities with Mismatches and Indels. Advanced science, 7(13), p.1903562. <br>
[9]: Lin, J. and Wong, K.C., 2018. Off-target predictions in CRISPR-Cas9 gene editing using deep learning. Bioinformatics, 34(17), pp.i656-i663. <br>
[10]: Charlier J, Nadon R, Makarenkov V. Accurate deep learning off-target prediction with novel sgRNA-DNA sequence encoding in CRISPR-Cas9 gene editing. Bioinformatics. 2021 Aug 15;37(16):2299-307. <br>
[11]: Lazzarotto, C.R., Malinin, N.L., Li, Y., Zhang, R., Yang, Y., Lee, G., Cowley, E., He, Y., Lan, X., Jividen, K. and Katta, V., 2020. CHANGE-seq reveals genetic and epigenetic effects on CRISPR–Cas9 genome-wide activity. Nature biotechnology, 38(11), pp.1317-1327. <br>
[12]: Kleinstiver, B.P., Prew, M.S., Tsai, S.Q., Topkar, V.V., Nguyen, N.T., Zheng, Z., Gonzales, A.P., Li, Z., Peterson, R.T., Yeh, J.R.J. and Aryee, M.J., 2015. Engineered CRISPR-Cas9 nucleases with altered PAM specificities. Nature, 523(7561), pp.481-485. <br>
[13]: Wang, T., Wei, J.J., Sabatini, D.M. and Lander, E.S., 2014. Genetic screens in human cells using the CRISPR-Cas9 system. Science, 343(6166), pp.80-84. <br>
[14]: Koike-Yusa, H., Li, Y., Tan, E.P., Velasco-Herrera, M.D.C. and Yusa, K., 2014. Genome-wide recessive genetic screening in mammalian cells with a lentiviral CRISPR-guide RNA library. Nature biotechnology, 32(3), pp.267-273. <br>
[15]: Doench, J.G., Hartenian, E., Graham, D.B., Tothova, Z., Hegde, M., Smith, I., Sullender, M., Ebert, B.L., Xavier, R.J. and Root, D.E., 2014. Rational design of highly active sgRNAs for CRISPR-Cas9–mediated gene inactivation. Nature biotechnology, 32(12), pp.1262-1267. <br>
[16]: Rauscher, B., Heigwer, F., Breinig, M., Winter, J. and Boutros, M., 2016. GenomeCRISPR-a database for high-throughput CRISPR/Cas9 screens. Nucleic acids research, p.gkw997. <br>
[17]: Wang, D., Zhang, C., Wang, B., Li, B., Wang, Q., Liu, D., Wang, H., Zhou, Y., Shi, L., Lan, F. and Wang, Y., 2019. Optimized CRISPR guide RNA design for two high-fidelity Cas9 variants by deep learning. Nature communications, 10(1), pp.1-14. <br>
[18]: Kim, H. K., Kim, Y., Lee, S., Min, S., Bae, J. Y., Choi, J. W., ... & Kim, H. H. (2019). SpCas9 activity prediction by DeepSpCas9, a deep learning–based model with high generalization performance. Science advances, 5(11), eaax9249. <br>
[19]: Hiranniramol, K., Chen, Y., Liu, W. and Wang, X., 2020. Generalizable sgRNA design for improved CRISPR/Cas9 editing efficiency. Bioinformatics, 36(9), pp.2684-2689. <br>
[20]: Chuai, G., Ma, H., Yan, J., Chen, M., Hong, N., Xue, D., Zhou, C., Zhu, C., Chen, K., Duan, B. and Gu, F., 2018. DeepCRISPR: optimized CRISPR guide RNA design by deep learning. Genome biology, 19(1), pp.1-18. <br>
