minimind目前训练的模型版本见下表：

| Model Name        | params | len_vocab | n_layers | d_model | kv_heads | q_heads | share+route | TopK |
| ----------------- | ------ | --------- | -------- | ------- | -------- | ------- | ----------- | ---- |
| bert-base         | 110M   | 30522     | 12       | 768     | 12       | 12      |             |      |
| minimind-v1-small | 26M    | 6400      | 8        | 512     | 8        | 16      | -           | -    |
| minimind-v1-moe   | 4×26M  | 6400      | 8        | 512     | 8        | 16      | 2+4         | 2    |

Experiment

| Model Name        | batch_size | pretrain_time     | sft_time          |
| ----------------- | ---------- | ----------------- | ----------------- |
| minimind-v1-small | 64         | ≈2 hour (1 epoch) | ≈2 hour (1 epoch) |
| minimind-v1-moe   | 40         | ≈6 hour (1 epoch) | ≈5 hour (1 epoch) |

