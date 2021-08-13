# Machine Learning Project
Andrew Anastasiades | @andrew-ana

### Overview   
This project involved predicting a three-value category from 40 predictor fields.  
To be perfectly honest, I did not have time to inspect all 40 fields, learn about koi fish, determine which fields are independent and repeatedly test possible ML models on the appropriate data.  

INSTEAD I....  

### Method  
Ran a random forest to determine field importance and establish a baseline for my neural networks. The RF gave me the following importances:  
0	0.107377	koi_fpflag_co
1	0.096194	koi_fpflag_nt
2	0.067372	koi_fpflag_ss
3	0.054523	koi_model_snr
4	0.049234	koi_prad
5	0.037165	koi_fpflag_ec
6	0.035924	koi_duration_err1
7	0.033818	koi_prad_err2
8	0.032746	koi_duration_err2
9	0.030580	koi_steff_err1  

Honestly I didn't know whether these fields were interdependent, so I ran a neural net with the top 5 features.  


### Trials  
The trials felt more like tribulations. Here are the results:
Trial 0 - 5 Fields - 1 Hidden Layer. 
Loss >1, ~0.50 accuracy, I didn't even save the notebook. 

Trial 1 - 40 Fields - 1 Hidden Layer.  
Loss: 0.26194465160369873, Accuracy: 0.8810068368911743

Trial 2 - 6 (arbitrarily unique sounding) Fields - 1 Hidden Layer.  
Loss: 0.5450627207756042, Accuracy: 0.7408466935157776

#### More fields is better

Trial 3 - 40 Fields - 2 Hidden Layers (5 Nodes each) 
Loss: 0.2409825325012207, Accuracy: 0.9067505598068237

Trial 4 - 40 Fields - 2 Hidden Layers (10 Nodes each) 
Loss: 0.23507530987262726, Accuracy: 0.9090389013290405

### Conclusion

I guess the meme holds up. Don't bother understanding the data. Don't try to learn algorithms. JUST. ADD. MORE. NODES. ADD. MORE. LAYERS.