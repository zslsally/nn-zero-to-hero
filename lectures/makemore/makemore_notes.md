# makemore

## Part 1

### Bigram

one character predicts the next one with a lookup table of counts

build dict to count the frequency of (prev_char, next_char) pairs

`itos` and `stoi` to convert between string and idx

`torch.Generator().manual_seed` set seed to get reproducible results

`