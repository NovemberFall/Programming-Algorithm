## Hidden Markov models

- Why use HMMS?
  - Model sequences of data
  - Stock prices, language, credit scoring, webpage visits


---

### Outline

- Markov models
- Google PageRank
- Analyze website visitor data, bounce rate
- Hidden Markov Model [隐马尔可夫模型](https://baike.baidu.com/item/%E9%9A%90%E9%A9%AC%E5%B0%94%E5%8F%AF%E5%A4%AB%E6%A8%A1%E5%9E%8B/7932524?fr=aladdin)
  - Probability of a sequence
  - Most likely sequence of hidden states
  - Training
  - But we won't stop there...
  - Gradient descent + Theano(deep learning technology)
- Hidden Markov Models for real-valued data
- Examples


---

- HMM are for modeling sequences: x(1), x(2), ...,  x(t), ..., x(T)
  - Thre's no label here
- But can be used for calssification as well, e.g. recognizing if a sound signal is a male voice or 
  feaml voice.

---

### Classification
- How can we use the HMM to classify if the sound signal is male or female?
- Haven't we just modeled the signal, p(x)?
- Key idea is Bayes' rule
- We model p(X | male) and p(X | female)
  - p(X | male) collect all the male samples, train an HMM
  - p(x | female) collect all the female samples, train another HMM
- Bayes' rule reverses the conditional
  - p(male | X) and p(female | X)

---

## Conclusion

- HMM is unsupervised
- But can easily be used for classification using Bayer rule and creating a separate model for each class,
  and choosing the class that gives us the maximum posterior probability