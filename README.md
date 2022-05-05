# BiteNet

## Data Preparation
dataset.data_prepararion.py for MIMIC III dataset

## Train Model
```bash
python BiteNet_mh_RE.py \
        --data_source mimic3  --model Bite --verbose True --task BiteNet \
        --predict_type re --visit_threshold 2 --max_epoch 50 --train_batch_size 16 \
        --gpu 0 --valid_visits 10 --num_hidden_layers 5 --pos_encoding encoding \
        --min_cut_freq 5 --embedding_size 120 --dropout 0.1 --only_dx_flag False
```



```bash
python BiteNet_mh_DX.py \
        --data_source mimic3  --model Bite --verbose True --task BiteNet \
        --predict_type dx --visit_threshold 2 --max_epoch 50 --train_batch_size 16 \
        --gpu 0 --valid_visits 10 --num_hidden_layers 5 --pos_encoding encoding \
        --min_cut_freq 5 --embedding_size 120 --dropout 0.1 --only_dx_flag False
```
