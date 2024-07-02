# NanoGPT

- This is just a trial run inspired from @karpathy 's nanoGPT
- The following steps will help you to perform trial run easier
Step1) git clone https://github.com/karpathy/nanoGPT.git

Step2) pip install torch numpy transformers datasets tiktoken wandb tqdm

Step3) python data/shakespeare_char/prepare.py

Step4) Either:

>>    python train.py config/train_shakespeare_char.py  


(A100GPU approx 3 minutes,For me didn't worked)

>>    python train.py config/train_shakespeare_char.py --device=cpu --compile=False --eval_iters=20 --log_interval=1 --block_size=64 --batch_size=12 --n_layer=4 --n_head=4 --n_embd=128 --max_iters=2000 --lr_decay_iters=2000 --dropout=0.0



(in cpu ,it worked for me over 2000 iterations)



STep5)  python sample.py --out_dir=out-shakespeare-char --device=cpu

after running this line,a generated sample will be displayed
