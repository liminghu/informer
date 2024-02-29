# informer

This repository will review and be tutoring transformer for time series (classification, regression), computer vision and NLP

## 1. Transformer for NLP

* Attention is All You Need

## 2. Transformer for computer vision

* Vision Transformer
* Swin Transformer
* Swin Transformer 2

## 3. Transformer for time series (classification, regression)

* A Transformer-based Framework for Multivariate Time Series Representation Learning

** We propose a transformer-based framework for unsupervised representation learning of multivariate time series. Pre-trained models can be potentially used for downstream tasks such as regression and classification, forecasting and missing value imputation. By evaluating our models on several benchmark datasets for        multivariate time series regression and classification, we show that not only does our modeling approach represent the most successful method employing unsupervised learning of multivariate time series presented to date, but also that it exceeds the current state-of-the-art performance of supervised methods; it does so even when the number of training samples is very limited, while offering computational efficiency. Finally, we demonstrate that unsupervised pre-training of our transformer models offers a substantial performance benefit over fully supervised learning, even without leveraging additional unlabeled data, i.e., by reusing the same data samples through the unsupervised objective. This paper was presented at KDD 2021. Full Research Paper: <https://arxiv.org/abs/2010.02803> (Video: https://www.youtube.com/watch?v=K5U9v2SW7_Q)

* Autoformer: Decomposition Transformers with Auto-Correlation for Long-Term Series Forecasting
* Are Transformers Effective for Time Series Forecasting?
* Informer: Beyond Efficient Transformer for Long Sequence Time-Series Forecasting

module.exports = {
  "names": [ "any-blockquote" ],
  "description": "Rule that reports an error for any blockquote",
  "information": new URL("https://example.com/rules/any-blockquote"),
  "tags": [ "test" ],
  "function": function rule(params, onError) {
    params.parsers.markdownit.tokens.filter(function filterToken(token) {
      return token.type === "blockquote_open";
    }).forEach(function forToken(blockquote) {
      var lines = blockquote.map[1] - blockquote.map[0];
      onError({
        "lineNumber": blockquote.lineNumber,
        "detail": "Blockquote spans " + lines + " line(s).",
        "context": blockquote.line.substr(0, 7)
      });
    });
  }
};