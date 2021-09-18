# EC601 project 1

## Problem statement:

In recent years, due to the popularity of graph structure data, graph-based deep learning has begun to attract attention in the field of artificial intelligence. However, most of the deep learning work on graphs focuses on supervised or semi-supervised learning scenarios. In this scenario, the model is trained for downstream tasks based on manual annotation information. Despite the success of supervised and semi-supervised graph learning, it relies heavily on label information. The cost of obtaining ground-truth tags is too high, over-fitting occurs, and robustness is poor. In other fields, such as the medical field, obtaining sufficient data is itself a challenge.

Self-supervised learning (SSL) is a promising method to solve the problems of supervised and semi-supervised learning, with important potential and research prospects. SSL optimizes well-designed auxiliary tasks through training models, which can help the model learn more generalized representations from unlabeled data, thereby achieving better performance and generalization in downstream tasks. The specific points are as follows: 

First, most of the work of graph learning relies too much on tags and less considers the underlying structure, so designing various SSL auxiliary tasks can help improve this situation and help understand the structure and attribute data of the graph data. Secondly, the cost of collecting image tag information is too high, and it is difficult to apply most of the existing methods to real-world data, but SSL reduces the dependence on artificial tags. Thirdly, graphics are universal and complex data structure This makes SSL pre-tasks work better in this situation, and is more suitable for constructing various SSL pre-tasks to obtain supervision signals than the CV/NLP field.

## APPLICATIONS

Graph SSL is applied to Graph Convolutional Networks (GCNs) to counter attacks. I saw in the paper "When Does Self-Supervision Help Graph Convolutional Networks" that the researchers studied the introduction of self-supervised standards and adversarial performance in graph convolutional networks (GCNs); taking multi-task learning as the research object, designed Several new self-supervised learning tasks; integrate multi-task self-supervision into graph confrontation training, and demonstrate its enhanced robustness to confrontation attacks. 

The experiments of the paper show that self-monitoring is beneficial to the generalization and robustness of GCNs under the condition of rationally designing the task form and integration mechanism. Multi-task self-supervision in adversarial training improves the robustness of GCN against various graph attacks. Node clustering and graph partitioning provide a priori information of features and links, which can better defend against feature attacks and link attacks, respectively. Both features and links have (joint) perturbation prior graph completion, which can continuously and sometimes significantly improve the robustness for the most destructive features and link attacks.

Graph SSL has also been applied to a wide range of disciplines. Such as recommendation system. Graph-based recommendation systems have been welcomed by many researchers because they can use the network to model products and users, and use the potential connections between them to generate high-quality recommendations. In recent years, in order to solve the problem of cold start of the recommendation system, the pre-training of the recommendation model, and selection bias, researchers have introduced graph SSL into the recommendation system. I saw some researchers【】 proposed a refactoring-based excuse task to pre-train GNN on cold-start users and projects. Some researchers also use comparison tasks to learn hypergraph representations based on social and conversational recommendations; by introducing a graph comparison learning module with debiasing loss, the problem of message loss in the GNN-based recommendation system is overcome and the selection bias is reduced; Two generation-based tasks are used to capture multi-mode side information for recommendation.

GRAPH SSL has also been applied to biology and chemistry. In the field of chemistry, researchers usually model molecules or compounds as graphs, where atoms and chemical bonds are represented as nodes and edges, respectively. Researchers use SSL to focus on molecular data; use a comparative learning framework to solve drug targeting and drug interaction prediction problems, and so on.

But while optimizing various neural network learning with SSL, I am also curious about how this method is implemented.

