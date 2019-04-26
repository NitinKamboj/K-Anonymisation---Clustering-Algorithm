Clustering Based k-Anonymisation
===========================

This repository is an **open source python implementation for Clustering based k-Anonymisation**. I implement these algorithms (k-nearest neighbor, k-member[1] and OKA[2]) in python for further study.

### Motivation 
Big Data challenges growth in privacy and researches on data privacy that lasted for more than ten years, an enormous amount of papers been published. However, few open source projects are available on the Internet, most open source projects are using algorithms proposed prior to 2004! A very few projects have been used in real life. In addition, there is not a lot of awareness among people as they don't hear about it.  

### Attention
I used **both adult and INFORMS** dataset in this implementation. For clarification, **we transform NCP to percentage**. This NCP percentage is computed by dividing NCP value with the number of values in dataset (also called GCP[5]). The range of NCP percentage is from 0 to 1, where 0 means no information loss, 1 means loses all information (more meaningful than raw NCP, which is sensitive to size of dataset). 


### Usage and Parameters:
My Implementation is based on **PYTHON 3.7.3 64BIT ARCHITECTURE**. Please make sure your Python environment is correctly installed. You can run Clustering in following steps: 

1) Download (or clone) the whole project. 

2) Run `anonymizer.py` in root dir with CLI or IDLE.

3) Default K value is set to 10

CLI Parameters:

	#Usage: python anonymizer [a | i] [knn | kmember | oka] [k | qi | data]
	#a: adult dataset, i: INFORMS ataset
	#knn:k-nearest neighbor, kmember: k-member, oka: one time pass k-means algorithm
	#k: varying k, qi: varying qi numbers, data: varying size of dataset
	# run Clustering based algorithm with adult data and oka with K(K=10)
	python anonymizer.py a oka 10
	
	# evalution knn by varying k
	python anonymizer.py a knn k

IDLE execution
    #Usage: Open Python IDLE 
	Open File anonymiser.py
	Run / F5 

### For more information:
[1] Lin J.L, Wei M.C. An efficient clustering method for k-anonymization[C], In Proceedings of the 2008 international workshop on Privacy and anonymity in information society(PAIS), 2008.

[2] Byun J.W, Kamra A, Bertino E, et al. Efficient k-anonymization using clustering techniques[C], In Proceedings of the 12th international conference on Database systems for advanced applications(DASFAA), 2007.

[3] [UTD Anonymization Toolbox](http://cs.utdallas.edu/dspl/cgi-bin/toolbox/index.php?go=home)

[4] [ARX- Powerful Data Anonymization](https://github.com/arx-deidentifier/arx)

[5] G. Ghinita, P. Karras, P. Kalnis, N. Mamoulis. Fast data anonymization with low information loss. Proceedings of the 33rd international conference on Very large data bases, VLDB Endowment, 2007, 758-769

[6] Cluster based generalization for k-anonymity(https://github.com/qiyuangong/Clustering_based_K_Anon)

==========================
by Nitin Kamboj	
nitin.kamboj@gmail.com
24/April/2019