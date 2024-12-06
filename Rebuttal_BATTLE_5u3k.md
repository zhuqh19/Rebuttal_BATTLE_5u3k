Dear Reviewer ,

Thank you very much for your constructive comments and suggestions on our manuscript titled "BATTLE: Unsupervised Bi-Level Optimization with Implicit Relationship Mining for Attributed Graph Anomaly Detection" with Submission ID 732. We have carefully considered each point and have made significant revisions to address your concerns. Below, we provide a detailed response to your questions.

**Question 1 Respond:**

Thank you for your question. Indeed, validation with large graphs and real-world data is essential, and we have considered conducting such validations. However, due to practical constraints, we have not been able to carry out the relevant experiments.

For large graphs, we would like to emphasize that, conceptually, there is no inherent distinction between large graphs and the smaller ones we have included in our current dataset. The primary variance lies in the magnitude of computational resources required to process them. While we have indeed contemplated conducting validations on larger graphs, our current computational resources are unfortunately limited, which has restricted our ability to perform such extensive experiments at this stage. Nevertheless, based on the structural similarities between large and small graphs, we are confident that the BATTLE framework, which has demonstrated robust performance on smaller graphs, should exhibit similar efficacy when scaled up, provided that sufficient computational resources are available.

We are actively seeking to expand our computational capabilities to address this limitation and are committed to validating the scalability of our framework in future work. We believe that with the appropriate resources, the BATTLE framework will prove to be equally effective on larger graphs, maintaining its performance integrity.

Regarding real-world data, having examples from the real world would indeed provide a better validation of the effectiveness of our BATTLE framework. However, due to the current lack of publicly available real-world datasets relevant to our study, we have been constrained and have not been able to conduct such validations.

Your inquiry is very helpful for our work, and we will definitely take this into account in future studies, attempting to include validations for large graphs and real-world data.

**Question 2 Respond:** 

Thanks for your question. The primary contribution of BATTLE lies in incorporating implicit relationship into anomaly detection. Regarding the complexity of BATTLE, which comes mainly from the attention network learner, sparsification, graph convolutional network layer, contrastive loss, and implicit relationship prediction. We calculated the complexity of BATTLE as 

$$
O\left(nd(L_1 + b_1) + md_1L + nd_2^1L + nd_2^2L + m^2 + (2 + R)n^2\right)
$$

where \( n(m) \) is the number of nodes(edges), \( b_1 \) is the batch size of attention network. \( d/d_1/d_2 \) are the dimension of node attribute/representation/projection, \( L_1/L \) is the layer number of attention network and GCN, and \( R \) is the number of graph samples. Compared to ANEMONE (with complexity 

$$
O\left(md_1L + nd_2^1L + nd_2^2L + 6n^2\right)
$$

), CoLA (with complexity 

$$
O\left(md_1L + nd_2^1L + nd_2^2L + 4n^2 + c^2nR\right)
$$

), and Sub-CR (with complexity 

$$
O\left(md_1L + nd_2^1L + nd_2^2L + 5n^2 + n^2R\right)
$$

), our method does not have significantly higher complexity (all four methods are in \( O(n^2) \) order of magnitude), yet we achieve notable performance improvement. We will present the computational details of model complexity in the final version. Additionally, we conducted experiments comparing BATTLE with other baselines regarding computational efficiency. As shown in Table 1, the experimental results demonstrate that BATTLE does not significantly increase training time compared to several other methods. However, we achieve notable performance improvement.

**Table 1:** Training time for different methods

| Methods       | BlogCatalog | Flickr    |
| ------------- | ----------- | --------- |
| ANEMONE(2021) | 10.07 min   | 22.40 min |
| CoLA(2022)    | 9.35 min    | 20.60 min |
| Sub-CR(2022)  | 10.90 min   | 23.62 min |
| BATTLE(Ours)  | 11.71 min   | 25.04 min |

**Question 3 Respond:**

case study



We believe that these revisions have significantly improved the quality and clarity of our paper. We are confident that BATTLE provides a valuable contribution to the field and is worthy of presentation at WWW25.

Thank you once again for your thorough review and for giving us the opportunity to improve our work. We look forward to the possibility of presenting our research at WWW25.