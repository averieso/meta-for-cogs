# meta-cogs
modified code to meta-learn based on "[Universal linguistic inductive biases via meta-learning](https://github.com/tommccoy1/meta-learning-linguistic-biases)" for the [COGS dataset](https://github.com/najoungkim/COGS). 

# meta-learning
`python main.py --data_prefix data_v3 --method maml --save_prefix MODEL_PREFIX --hidden_size 512 --vocab_size 872 --inner_batch_size 5  --emb_size 512 --patience 10`

# 40-shot learning on generalization dataset (evaluation)
`python evaluation.py --data_v3 data_gen --vocab_size 872 --emb_size 512 --hidden_size 512 --lr_inner 1.0 --inner_batch_size 100 --save_prefix MODEL_PREFIX`
