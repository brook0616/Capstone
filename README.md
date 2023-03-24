# Capstone

Brook B andreas 
ROb Rhea 
Dijlukrishian Vijay 



Networks are always under the threat of malicious intrusions. Deep learning models are used to help identify and mitigate intrusions before damage can occur. Various types of deep learning models have been researched, built, and tested with the goal of improving intrusion detection and efficiencies. In this study, a two-phase deep learning model technique called a Hybrid Intrusion Detection System (HIDS) is proposed that uses Bidirectional Long Short-Term Memory Recurrent Neural Network (BLSTM-RNN). The model analyzes both flow-based network data and packet-based data in a two-step process. The model is tested using the UNSW-NB15 data set and performance is assessed using accuracy, precision, recall, and F1-measure. The flow-based binary classification generated an accuracy of 46%, precision of 58%, recall of 46% and F1-measure of 44%. The packet-based classification generated an accuracy of 76%, precision of 76%, recall of 72% and F1-measure of 73%. The proposed work showed that the models were able to achieve an average accuracy of 61% for the hybrid model. The results of the analysis between the deep learning models suggests that the use of deep learning in NIDS would be a suitable solution to improving detection accuracy on unclean data.

1. Business Problem
1.1. Description
Source: https://www.unsw.adfa.edu.au/unsw-canberra-cyber/cybersecurity/ADFA-NB15-Datasets

Data: CISCO Networking Dataset - The UNSW-NB15 Dataset

Download UNSW-NB15 - csv file.

Problem statement :
Classify the given network is intrusion or normal based on evidence from The raw network packets of the UNSW-NB 15 dataset. it was created by the IXIA PerfectStorm tool in the Cyber Range Lab of the Australian Centre for Cyber Security (ACCS).



We have multiple data files: download the UNSW-NB15 - csv file this file contains a following structure

  a part of training and testing set - folder contains train and test data csv files
  NUSW-NB15_features.csv - Feature description
  NUSW-NB15_GT.csv
  The UNSW-NB15 description.pdf
  UNSW-NB15_1.csv
  UNSW-NB15_2.csv
  UNSW-NB15_3.csv
  UNSW-NB15_4.csv
  UNSW-NB15_LIST_EVENTS.csv
  
These features are described in UNSW-NB15_features.csv file.

The total number of records is two million and 540,044 which are stored in the four CSV files, namely, UNSW-NB15_1.csv, UNSW-NB15_2.csv, UNSW-NB15_3.csv and UNSW-NB15_4.csv.

The ground truth table is named UNSW-NB15_GT.csv and the list of event file is called UNSW-NB15_LIST_EVENTS.csv.

A partition from this dataset is configured as a training set and testing set, namely, UNSW_NB15_training-set.csv and UNSW_NB15_testing-set.csv respectively.

The number of records in the training set is 82,332 records and the testing set is 175,341 records from the different types, attack and normal.Figure 1 and 2 show the testbed configuration dataset and the method of the feature creation of the UNSW-NB15, respectively.

Data file's information:

both train and test files contains 45 columns

['dur', 'spkts', 'dpkts', 'sbytes', 'dbytes', 'rate', 'sttl', 'dttl', 'sload', 'dload', 'sloss', 'dloss', 'sinpkt', 'dinpkt', 'sjit', 'djit', 'swin', 'stcpb', 'dtcpb', 'dwin', 'tcprtt', 'synack', 'ackdat', 'smean', 'dmean', 'trans_depth', 'response_body_len', 'ct_srv_src', 'ct_state_ttl', 'ct_dst_ltm', 'ct_src_dport_ltm', 'ct_dst_sport_ltm', 'ct_dst_src_ltm', 'is_ftp_login', 'ct_ftp_cmd', 'ct_flw_http_mthd', 'ct_src_ltm', 'ct_srv_dst', 'is_sm_ips_ports']

Categorical (4) columns
Numerical (41) columns
2.2. Mapping the real-world problem to an ML problem
2.2.1. Type of Machine Learning Problem
        There are two different class normal or attack. Find the network is normal or intrusion. => Binary class classification problem
2.2.2. Performance Metric

metric used to identify the performance of the model

Metric(s):

AUC and f1-score
Confusion matrix
FAR - false alarm rate should be as minimum as possible
2.2.3. Machine Learing Objectives and Constraints
        Objective: Predict the probability of each data-point whether the network is normal or attack.
        
        
Model Evaluation
+---------------------+----------+--------+-------+-------+-------+
|        Model        | F1 Score |  AUC   | FPR % | FNR % | FAR % |
+---------------------+----------+--------+-------+-------+-------+
| Logistic Regression |  0.9307  | 0.8447 |  30.6 |  0.47 | 15.53 |
|      Linear SVM     |  0.8934  | 0.7701 | 43.03 |  2.96 | 22.99 |
|    Random Forest    |  0.9524  | 0.9021 | 18.29 |  1.29 |  9.79 |
| Stacking Classifier |  0.9425  | 0.8759 | 23.99 |  0.84 | 12.41 |
+---------------------+----------+--------+-------+-------+-------+



This study has shown BLSTM to be an effective way to identify network attacks and prevent the ever-increasing cyberattacks occurring all over the world on daily basis. The RNN deployed for packet-based detection and BLSTM deployed for flow-based detection showed to be effective machine learning algorithms for classifying and distinguishing bad network and good network events. The models were able to achieve an average accuracy of 61% (46% for flow-based; 76% for packet-based). The results indicate there is a lot of room for fine-tuning the two models to achieve better accuracy. Additionally, the models will be tested on the Canadian dataset to ensure quality and scalability of the model. The results of the analysis between the deep learning models suggests that the use of deep learning in NIDS would be a suitable solution to improving detection accuracy on unclean data; however building an environment that is specifically designed for this purpose would go a long way to further improve and could greatly impact the decision on which model would work best in a given environment. 
Conclusion


