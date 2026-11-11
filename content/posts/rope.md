+++
date = '2026-10-03T00:05:53-04:00'
draft = false
title = 'Understanding RoPE'
+++


## Need for Positional Encodings (PE)

A transformer language model[1] maps a sequence of vectors to a probability distribution over the next vector in the sequence. 
In language models, each of these vectors represent tokens. However, the tokens are invariant to their positions in the sequence. [add_citation?] and this is a problem because the order of tokens clearly matters for the next token prediction task.

This problem is solved with the introduction of positional Encodings (PE). A PE is a vector that contains information about the position of the token in the sequence. PE's ideally should have the following properties : 

1. Provide information about token position
2. Be able to handle arbitrary sequence lengths 
3. Relative position : Ideally, the positional relationship between two tokens should depend on they're relative position to each other, not where they are in the sequence.

Generally, if we shift both positions by the same amount \(k\), their positional relationship should stay the same:

$relationship(PE_i, PE_j)=relationship(PE_{i+k}, PE_{j+k}).$

In other words, the relationship between $PE_i$ and $PE_j$ should only depend on the relative distance \(j-i\).

The PE's of each token is then integrated into the transformer architecture (in some way), so that the next token prediction task taken position into account. 

## How RoPE works 
- 

```
1. need for positional encoding (comparison to RNN)
2. problems w/ trivial PE's 
3. how RoPE solved it
4. how RoPE works and design choices
5. possible problems/limitations 
```




## References 
[1] Vaswani et al., *Attention Is All You Need*, 2017. [arXiv][def]
[2] Su et al., *RoFormer: Enhanced Transformer with Rotary Position Embedding*, 2021. [arXiv][def2]

[def]: https://arxiv.org/abs/1706.03762
[def2]: https://arxiv.org/abs/2104.09864