# meta-for-cogs
This is a modified code to meta-learn based on "[Universal linguistic inductive biases via meta-learning](https://github.com/tommccoy1/meta-learning-linguistic-biases)" for the [COGS dataset](https://github.com/najoungkim/COGS). 

This work is done for the term paper of the seminar Compositional Generalisation, Summer Semester 2022, University of Saarland. The goal is to assess the ability of an LSTM to compositionally generalise with a meta-learning approach. The accompanying paper can be found [here](https://github.com/averieso/meta-for-cogs/blob/master/Compositional%20generalisation%20with%20linguistically%20motivated%20meta-learning.pdf).

# meta-learning
`python main.py --data_prefix DATA_PREFIX --method maml--hidden_size 512 --vocab_size 872 --inner_batch_size 5  --emb_size 512 --patience 10 --lr_inner 0.1 --save_prefix MODEL_PREFIX`

## evaluate on test data (in-distribution)
`python evaluation.py --data_prefix DATA_PREFIX --vocab_size 872 --emb_size 512 --hidden_size 512 --lr_inner 0.1 --inner_batch_size 1 --save_prefix MODEL_PREFIX`

# One-shot learning on generalization dataset (evaluation)
`python evaluation.py --data_prefix data_gen_v2 --vocab_size 872 --emb_size 512 --hidden_size 512 --lr_inner 0.1 --inner_batch_size 1 --save_prefix MODEL_PREFIX`
