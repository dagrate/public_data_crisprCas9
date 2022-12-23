# public_data_crisprCas9

Summary of the most popular CRISPR/Cas9 benchmark data sets and databases used for on- and off-target prediction

------

## Data Set Description

Source | Year | Data description | Target | Original data source & Curated Data |
|:---:|:---:|:---:|:---:|:---:|
|Wang et al. data [1] | 2014 | A library containing 73, 000 sgRNAs | Off-targets and On-targets | https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3972032/#SD2 <br><br> Direct Link for Data Download : <br> https://github.com/dagrate/public_data_crisprCas9/tree/main/data/wang2014genetic |
| Koike-Yusa et al. data [2] | 2014 | 87,897 gRNAs targeting 19,150 mouse protein-coding genes | Off-targets and On-targets | https://www.ebi.ac.uk/ena/browser/view/PRJEB4038 <br> Data Download Direct Link: <br> https://www.ebi.ac.uk/ena/browser/view/PRJEB4038 | 
| Doench V1 data [3] | 2014 | 1,831 guides targeting three human (CD13, CD15, and CD33) and six mouse genes (Cd5, Cd28, H2-K, Cd45, Thy1, and Cd43) | Off-targets and On-targets | https://portals.broadinstitute.org/gppx/crispick/public |
| GUIDE-seq data [4] | 2015 | CRISPR RNA-guided nucleases (RGNs) from two human cell lines: U2OS and HEK293; different sites such as VEGFA sites 1, 2 and 3, and HEK293 sites 2, 3 and 4 were studied | Off-targets | https://github.com/tsailabSJ/guideseq/tree/master |
| Doench V2 data [5] | 2016 | 2,549 unique guides targeting eight genes (CCDC101, MED12, TADA2B, TADA1, HPRT, CUL3, NF1, and NF2) from human A375 cells | Off-targets and On-targets | https://www.nature.com/articles/nbt.3437 <br> Data Download Direct Link <br> https://www.nature.com/articles/nbt.3437#Sec24 |
|CRISPOR Database [6] | 2016 | Aggregate data for more than 50 genomes | Off-targets and On-targets | http://crispor.tefor.net/ <br> Data Download Direct Link: <br> https://github.com/MichaelLinn/off_target_prediction/blob/master/data/crispor_encoded_data.pkl.zip |
| GenomeCRISPR database [7] | 2016 | Aggregate data for more than 550,000 sgRNAs derived from 84 experiments | On-targets  | http://genomecrispr.org |
| CIRCLE-Seq data [8] | 2017 | Contains mismatch, insertion, and deletion information, and includes sgRNA-DNA pairs from 10 guide sequences, 7,371 of which are off-targets (430 with bulges) | Off-targets | https://github.com/tsailabSJ/circleseq |
|SITE-Seq [9] | 2017 | gRNA-DNA pairs from nine guide sequences, 3,767 of which are active off-targets (no bulges) | Off-targets | https://www.nature.com/articles/nmeth.4284 <br> Data Download Direct Link: <br> https://github.com/dagrate/public_data_crisprCas9/tree/main/data/site_seq |
| DeepCRISPR platform [10] | 2018 | Includes approximately 0.68 billion sgRNA sequences derived from 13 human cell lines | Off-targets and On-targets | https://github.com/bm2-lab/DeepCRISPR <br> Data Download Direct Link (samples): https://github.com/dagrate/public_data_crisprCas9/tree/main/data/deepcrispr |
| DeepHf data [11] | 2019 | Includes indel rates of over 50,000 gRNAs for each nuclease, covering about 20,000 genes. It is the largest gRNA on-target activity set reported for mammalian cells | On-targets | http://www.DeepHF.com <br> https://github.com/izhangcd/DeepHF <br> Data Download Direct Link: <br> https://github.com/dagrate/public_data_crisprCas9/tree/main/data/deepHF |
| CHANGE-seq data [12] | 2020 | 110 sgRNA targets across 13 therapeutically relevant loci in human primary T-cells were studied to identify 201,934 off-target sites across the human genome | Off-targets and On-targets | https://github.com/tsailabSJ/changeseq |
| CRISPRon data [13] | 2021 | A pool of 12,000 gRNA oligos, targeting 3,834 human protein-coding genes | On-targets | https://rth.dk/resources/crispr/ |




------

## Citation

to be completed soon


------

## References 

```bibtex
[1]:
@article{wang2014genetic,
  title={Genetic screens in human cells using the CRISPR-Cas9 system},
  author={Wang, Tim and Wei, Jenny J and Sabatini, David M and Lander, Eric S},
  journal={Science},
  volume={343},
  number={6166},
  pages={80--84},
  year={2014},
  publisher={American Association for the Advancement of Science}
}

[2]:
@article{koike2014genome,
  title={Genome-wide recessive genetic screening in mammalian cells with a lentiviral CRISPR-guide RNA library},
  author={Koike-Yusa, Hiroko and Li, Yilong and Tan, E-Pien and Velasco-Herrera, Martin Del Castillo and Yusa, Kosuke and others},
  journal={Nature biotechnology},
  volume={32},
  number={3},
  pages={267--273},
  year={2014},
  publisher={Nature Publishing Group}
}

[3]:
@article{doench2014rational,
  title={Rational design of highly active sgRNAs for CRISPR-Cas9--mediated gene inactivation},
  author={Doench, John G and Hartenian, Ella and Graham, Daniel B and Tothova, Zuzana and Hegde, Mudra and Smith, Ian and Sullender, Meagan and Ebert, Benjamin L and Xavier, Ramnik J and Root, David E},
  journal={Nature biotechnology},
  volume={32},
  number={12},
  pages={1262--1267},
  year={2014},
  publisher={Nature Publishing Group}
}

[4]:
@article{tsai2015guide,
  title={GUIDE-seq enables genome-wide profiling of off-target cleavage by CRISPR-Cas nucleases},
  author={Tsai, Shengdar Q and Zheng, Zongli and Nguyen, Nhu T and Liebers, Matthew and Topkar, Ved V and Thapar, Vishal and Wyvekens, Nicolas and Khayter, Cyd and Iafrate, A John and Le, Long P and others},
  journal={Nature biotechnology},
  volume={33},
  number={2},
  pages={187--197},
  year={2015},
  publisher={Nature Publishing Group}
}

[5]:
@article{doench2016optimized,
  title={Optimized sgRNA design to maximize activity and minimize off-target effects of CRISPR-Cas9},
  author={Doench, John G and Fusi, Nicolo and Sullender, Meagan and Hegde, Mudra and Vaimberg, Emma W and Donovan, Katherine F and Smith, Ian and Tothova, Zuzana and Wilen, Craig and Orchard, Robert and others},
  journal={Nature biotechnology},
  volume={34},
  number={2},
  pages={184--191},
  year={2016},
  publisher={Nature Publishing Group}
}

[6]:
@article{haeussler2016evaluation,
  title={Evaluation of off-target and on-target scoring algorithms and integration into the guide RNA selection tool CRISPOR},
  author={Haeussler, Maximilian and Sch{\"o}nig, Kai and Eckert, H{\'e}l{\`e}ne and Eschstruth, Alexis and Miann{\'e}, Joffrey and Renaud, Jean-Baptiste and Schneider-Maunoury, Sylvie and Shkumatava, Alena and Teboul, Lydia and Kent, Jim and others},
  journal={Genome biology},
  volume={17},
  number={1},
  pages={1--12},
  year={2016},
  publisher={BioMed Central}
}

[7]:
@article{rauscher2016genomecrispr,
  title={GenomeCRISPR-a database for high-throughput CRISPR/Cas9 screens},
  author={Rauscher, Benedikt and Heigwer, Florian and Breinig, Marco and Winter, Jan and Boutros, Michael},
  journal={Nucleic acids research},
  pages={gkw997},
  year={2016},
  publisher={Oxford University Press}
}

[8]:
@article{tsai2017circle,
  title={CIRCLE-seq: a highly sensitive in vitro screen for genome-wide CRISPR--Cas9 nuclease off-targets},
  author={Tsai, Shengdar Q and Nguyen, Nhu T and Malagon-Lopez, Jose and Topkar, Ved V and Aryee, Martin J and Joung, J Keith},
  journal={Nature methods},
  volume={14},
  number={6},
  pages={607--614},
  year={2017},
  publisher={Nature Publishing Group}
}

[9]:
@article{cameron2017mapping,
  title={Mapping the genomic landscape of CRISPR--Cas9 cleavage},
  author={Cameron, Peter and Fuller, Chris K and Donohoue, Paul D and Jones, Brittnee N and Thompson, Matthew S and Carter, Matthew M and Gradia, Scott and Vidal, Bastien and Garner, Elizabeth and Slorach, Euan M and others},
  journal={Nature methods},
  volume={14},
  number={6},
  pages={600--606},
  year={2017},
  publisher={Nature Publishing Group}
}

[10]:
@article{chuai2018deepcrispr,
  title={DeepCRISPR: optimized CRISPR guide RNA design by deep learning},
  author={Chuai, Guohui and Ma, Hanhui and Yan, Jifang and Chen, Ming and Hong, Nanfang and Xue, Dongyu and Zhou, Chi and Zhu, Chenyu and Chen, Ke and Duan, Bin and others},
  journal={Genome biology},
  volume={19},
  number={1},
  pages={1--18},
  year={2018},
  publisher={Springer}
}

[11]:
@article{wang2019optimized,
  title={Optimized CRISPR guide RNA design for two high-fidelity Cas9 variants by deep learning},
  author={Wang, Daqi and Zhang, Chengdong and Wang, Bei and Li, Bin and Wang, Qiang and Liu, Dong and Wang, Hongyan and Zhou, Yan and Shi, Leming and Lan, Feng and others},
  journal={Nature communications},
  volume={10},
  number={1},
  pages={1--14},
  year={2019},
  publisher={Nature Publishing Group}
}

[12]:
@article{lazzarotto2020change,
  title={CHANGE-seq reveals genetic and epigenetic effects on CRISPR--Cas9 genome-wide activity},
  author={Lazzarotto, Cicera R and Malinin, Nikolay L and Li, Yichao and Zhang, Ruochi and Yang, Yang and Lee, GaHyun and Cowley, Eleanor and He, Yanghua and Lan, Xin and Jividen, Kasey and others},
  journal={Nature biotechnology},
  volume={38},
  number={11},
  pages={1317--1327},
  year={2020},
  publisher={Nature Publishing Group}
}

[13]:
@article{xiang2021enhancing,
  title={Enhancing CRISPR-Cas9 gRNA efficiency prediction by data integration and deep learning},
  author={Xiang, Xi and Corsi, Giulia I and Anthon, Christian and Qu, Kunli and Pan, Xiaoguang and Liang, Xue and Han, Peng and Dong, Zhanying and Liu, Lijun and Zhong, Jiayan and others},
  journal={Nature communications},
  volume={12},
  number={1},
  pages={1--9},
  year={2021},
  publisher={Nature Publishing Group}
}

```
