# State of the art

In this chapter some key aspects for this paper that will be of relevance later on will be exposed, some of this aspects include the main focus of this work: disinformation and complex networks; the main tool used to make this possible: topic modelling; and how all of this concepts relate to each other including other research on this field.

## Information, misinformation and disinformation
Information has always been a powerful tool, influencing various aspects of human life, from sharing a simple recipe to devising complex military strategies, it is present in every aspect of our lives and has an extreme influence in it, shaping our understanding, decisions and actions. How many historic-changing events could have been prevented or changed if the right individuals knew the right information at the right moment? Wars, financial crises, terrorist attacks or revolutions are often the result of what the individuals surrounding them did and didn't knew at crucial moments.

The role of information in society has transformed dramatically over the past decades, fueled by advancements in technology, the proliferation of the internet, and the ubiquitous presence of social media. Its influence has grown exponentially in recent years due to the sheer volume, speed, and accessibility of data in our digital age.

A decade ago, access to information was more constrained by the limitations of traditional media. People relied heavily on printed newspapers, television, and radio broadcasts as their primary sources of news and updates. These mediums inherently restricted the flow of information to scheduled intervals and limited formats. According to a study conducted by the International Telecommunications Union (ITU), global internet usage in 2012 was approximately 2.4 billion users, a big contrast to the 5.4 billion users recorded in 2023 @noauthor_facts_nodate @noauthor_statistics_nodate . This increase in connectivity has fundamentally altered the dynamics of information dissemination and consumption.

In the current era, individuals are exposed to unprecedented amounts of information daily. A 2017 article from the Frontiers revealed that the average individual now consumes around **74 GB of data** per day through digital platforms @s_too_nodate, a figure that has only increased with the COVID-19 pandemic an the more recent AI.

Another important factor is the amount of data being generated now days. According to a Statista report @noauthor_data_nodate @noauthor_breaking_nodate in 2023 global data generation stood at 0.337 zettabytes per day (337.000.000 terabytes) and its still rising day by day. 

In today's world, where vast amounts of information are generated and consumed every day, ensuring its accuracy and safeguarding it from malicious intent is a complex and crucial task. This challenge highlights the importance of distinguishing between different types of information. These distinctions are essential for understanding the nature of the information we encounter and its potential impact:

- **Disinformation**: refers to "false information deliberately and often covertly spread (as by the planting of rumors) in order to influence public opinion or obscure the truth" @noauthor_definition_2024-1. The intent to harm or manipulate distinguishes disinformation from other forms of false information​ .
- **Misinformation**: means "incorrect or misleading information" @noauthor_definition_2024. It is the result of errors in comprehension, communication or misinterpretation and lacks the purposeful drive to deceive​ .
- **Malinformation**: on the other hand, is true information meant to cause harm @oxford_english_dictionary_misinformation_2024.

With this, researches classify information based on intent, content or both, although for this classification, everything is found under the umbrella of "*fake news*", which is a much more known name for disinformation, misinformation and all types of false information, but one term with no agreed definition in the literature @aimeur_fake_2023. In this paper we will use it to encapsulate all types of false information including all the types listed previously.

**Content-based** fake news are classified using false text, hyperlinks, embedded content, images, false videos, audios, etc. In general, they are classified by the multimedia they posses.

**Intent-based** fake news are more discussed and include clickbait, hoax, rumor, satire, propaganda, framing, conspiracy theories and others:

- Clickbait. Refers to misleading headlines and thumbnails of content on the web that tend to be fake stories with catchy headlines.
- Hoax. False or inaccurate stories used to masquerade the truth and is represented as factual.
- Rumor. Ambiguous claims that are disseminated with a lack of evidence to support them.
- Satire. Stories that contain a lot of irony and humor.
- Propaganda. News stories created by political entities to mislead people.
- Framing. Refers to employing some aspect of reality concealing the truth and misguiding people, often out of context.
- Conspiracy theories. The belief that an event is the result of secret plots generated by powerful conspirators.

Although it is of interest to differentiate all of these types, it is important to highlight that there exist an overlap in the types listed before and thus is possible to have false information falling within multiple categories.

### Risk and interest in fake news

Fake news and all of its categories poses profound risks across societal, political, and economic domains. These risks, amplified by the rapid evolution of communication technologies, make it a pressing challenge for modern societies:

1. **Erosion of public trust**. One of the most significant risks of disinformation is its ability to undermine trust in key institutions such as governments, media, and scientific organizations. When disinformation campaigns spread false narratives about elections, public health, or climate change, they create doubt in the legitimacy and credibility of these institutions. For instance, during the 2020 U.S. presidential election, coordinated disinformation campaigns targeted the integrity of voting systems, leading to widespread mistrust and civil unrest @mckay_disinformation_2021. Such erosion of trust destabilizes democratic processes and makes societies more vulnerable to further manipulation.
2. **Threats to public health**. The global COVID-19 pandemic highlighted the dangerous intersection of disinformation and public health. False claims about the origins of the virus, vaccine efficacy, and alternative cures led to widespread confusion and vaccine hesitancy, prolonging the pandemic and increasing mortality rates @van_der_linden_inoculating_2020. For instance, rumors that the virus was a hoax or that certain unproven remedies like drinking bleach could cure it resulted in preventable deaths and widespread panic. Public health authorities struggled to counter the infodemic @noauthor_infodemic_nodate that spread faster than official health advisories.
3. **Economic disruption**. Disinformation can disrupt markets and undermine economic stability. False reports about companies, stock values, or economic policies can cause fluctuations in financial markets, leading to losses for investors and businesses. For example, during the GameStop stock surge in early 2021, false narratives about market manipulation circulated widely, contributing to panic and confusion among retail investors @michaels_gamestop_2021. Furthermore, businesses targeted by disinformation campaigns may suffer reputational damage, which can affect consumer trust and sales.
4. **National security threats**. Disinformation is increasingly being used as a tool in cyber warfare. Foreign actors deploy coordinated campaigns to destabilize nations, influence elections, and undermine public confidence in governments. For instance, Russian interference in the 2016 U.S. presidential election involved the dissemination of false information to manipulate voter behavior and sow discord among the electorate @bessi_social_2016. These activities represent a growing national security threat, as they weaken the social fabric and leave nations vulnerable to external manipulation.
5. **Psychological and cognitive impacts**. Persistent exposure to disinformation affects individuals' mental health and cognitive processing. Fake news, particularly during crises, can lead to heightened anxiety, fear, and confusion. Moreover, individuals who consume disinformation repeatedly may develop a distorted perception of reality, becoming more susceptible to conspiracy theories and less capable of critical thinking @gwiazdzinski_psychological_2023. This can erode rational decision-making at both individual and societal levels.

All of this risks can be clearly identified in Thomas Rid's book "Active Measures:  The Secret History of  Disinformation and  Political Warfare" @rid_active_nodate where he goes through some of the most relevant events in history and how many of them where surrounded by fake news, or as Thomas describes them: *active measures*.

But not everything is bad news, since increasing prevalence and impact of fake news have sparked significant interest among academics, policymakers, and international organizations. In this regard it is possible to differentiate multiple advances to combat fake news:

- **Academic research**.  Fake news have become a focal point in disciplines such as sociology, psychology, and computer science. Researchers are examining the psychological mechanisms that make individuals susceptible to disinformation, including cognitive biases, confirmation bias, and emotional triggers @britt_reasoned_2019. Studies also explore how social media algorithms amplify disinformation and how misinformation spreads through network structures, using models from network science and data analytics @mazzeo_investigating_2022.
- **Policy and regulation**. Policymakers worldwide are grappling with the challenge of regulating disinformation without infringing on free speech. Initiatives like the European Union’s Code of Practice on Disinformation aim to hold social media platforms accountable for the spread of false information @noauthor_2022_2024.
- **Technological interventions**. The development of artificial intelligence (AI) and machine learning tools has garnered interest for their potential to combat disinformation. These technologies analyze patterns in content dissemination, detect fake news, and identify bot-driven campaigns. However, their effectiveness is limited by the sophistication of disinformation tactics, including the use of AI-generated deepfakes @garimella_how_2024.
- **Media literacy campaigns**. Public education initiatives are gaining momentum as an essential tool to counter disinformation. Media literacy programs aim to teach individuals how to critically evaluate information sources, recognize manipulation techniques, and verify facts. These campaigns are particularly effective in schools, where they can equip future generations with the skills needed to navigate the complex digital landscape @noauthor_journalism_nodate.
- **Global collaborations**. The international nature of disinformation requires a coordinated global response. Organizations like the World Health Organization @noauthor_disinformation_nodate and the United Nations nations_united_nodate are working to address disinformation during crises such as pandemics and armed conflicts. Collaborative frameworks like the Global Internet Forum to Counter Terrorism (GIFCT) bring together governments, tech companies, and civil society to combat the spread of harmful content @noauthor_gifct_nodate.
- **Corporate responsibility**. Social media companies have come under increased scrutiny for their role in enabling the spread of disinformation. Platforms like Facebook, Twitter, and YouTube are investing in fact-checking partnerships, content moderation algorithms, and user awareness campaigns. However, critics argue that these efforts are often insufficient and that greater accountability is needed @safieddine_corporate_2016.

### Disinformation data sets

One of the biggest bottle-necks when researching fake news is data. It may be contradictory after knowing the quantity of information generated and consumed worldwide, but most of the time this data is in a raw state and not appropriate for research.  Fake news data sets are defined as curated collections of digital content specifically compiled for studying, detecting, and analyzing. These data sets typically include:

- **Fake and real news articles**: to train and test algorithms in distinguishing genuine content from fake.
- **Social media posts**: often annotated to identify patterns in disinformation propagation.
- **Fact-checking databases**: verified true or false claims, often sourced from professional fact-checking organizations. If a data sets includes this kind of information 

Another important factor when talking about disinformation data sets are the main use that they are applied to since this will dramatically influence which data sets are useful and which aren't for a specific use case. Generally, there are four main goals when working with this data sets:

1. **Training ML models**. These data sets provide the foundation for training algorithms to classify content as fake or real. By offering labeled examples, they enable models to learn patterns and features associated with disinformation, such as linguistic markers, propagation patterns, and metadata anomalies.
2. **Understanding disinformation dynamics**. Researchers use these data sets to study how disinformation spreads across digital platforms, identifying critical nodes, influences, and pathways of dissemination. Insights from these studies inform counter-strategies to disrupt false information flows.
3. **Benchmarking detection techniques**. Disinformation data sets offer standardized benchmarks for evaluating the effectiveness of detection algorithms. By comparing performance across different data sets, researchers refine methods to improve accuracy and scalability @islam_deep_2020.
4. **Evaluating fact-checking tools**. Fact-checking initiatives rely on annotated disinformation data sets to verify claims and enhance their algorithms. These data sets help identify gaps in automated tools and improve their reliability in real-world scenarios.

Some of the most relevant data sets that fall under some of this characteristics are:

- **LIAR Data Set**. This data set comprises 12,836 short statements sourced from *Politifact.com*, categorized into multiple truthfulness levels. It serves as a benchmark for NLP tasks aimed at detecting false claims. Studies like Wang @wang_liar_2017 utilized LIAR to train algorithms that classify statement veracity accurately. Another usage for this data set is from Bahad et al. @bahad_fake_2019 where it was used to train bidirectional LSTM (Long Short-Term Memory) models, achieving high accuracy in distinguishing fake from real statements.
- **FakeNewsNet**. Combining content and social context, this data set includes news articles and user interactions from fact-checking organizations. Researchers leverage it to study how user engagement contributes to the spread of fake news. Shu et al. @shu_fakenewsnet_2019 used it to develop propagation-based disinformation detection models.
- **2016 X election data**. Formerly known as Twitter, this data set includes millions of tweets tied to the known disinformation campaign from the 2016 U.S. presidential election. It enables the study of bot-driven campaigns and their influence on public discourse. Bessi and Ferrara analyzed this data to reveal the critical role of automated accounts in spreading fake news @bessi_social_2016. Another study made in 2019 @grinberg_fake_2019 revealed even more information about this data.
- **Hyperpartisan sources**. Comprising news articles labeled as fake, real, or satirical, this data set supports content-based disinformation detection. Pennycook and Rand made it to explore public susceptibility to false narratives and public perception of different sources @pennycook_fighting_2019.
- **COVID-19 fake news**. With the rise of the COVID-19 "infodemic" various data sets focusing on pandemic-related disinformation emerged. These include annotated posts, articles, and videos with credibility labels. Micallef et al. @micallef_role_2020 used these data sets to study misinformation's impact on public health and real-time mitigation strategies.

As previously mentioned, real-world data isn't suitable for direct research on fake news. After examining several datasets, it becomes clear that the primary challenge lies in labeling. Determining whether information is true or false, or whether it is intentionally misleading, is a complex and challenging task that can only be solved using mixed approaches like crowd-sourcing and ML.

## Topic Modelling

Topic modeling is a statistical and computational technique used to identify hidden topics within large collections of unstructured text data. It is particularly useful in NLP and text mining applications for organizing, understanding, and summarizing vast amounts of textual information @kherwa_topic_2018 @vayansky_review_2020 @noauthor_what_2024.

This section, though inherently complex, aims to provide an overview of the general principles and some of the most commonly employed techniques in the field. However, our focus will be to emphasize the concepts that are directly relevant to the development of this paper.

The primary goal of topic modeling is to group words in a corpus into clusters or "topics," where each topic is a distribution over words, and each document is a distribution over topics. This probabilistic representation allows researchers to uncover the thematic structure of a text corpus, even when the documents are not explicitly labeled with categories or topics.

### Key concepts

As stated before topic modeling is a machine learning technique that uncovers latent structures in large collections of unstructured text data. This large collections are called *corpus* and are composed of multiple documents. This documents can be as large as research papers or as short as a few lines of text. 

The primary goal of topic modeling is to group words in a corpus into groups or "*topics*", where each *topic* represents a collection of words that frequently occur together in a meaningful context. For instance, a topic on "sports" might include words like "team", "game", "score" and "player".

In this context a document inside the corpus is represented as a distribution over topics. For example, an article about a sporting event might be 70% "sports" and 30% "entertainment".

To accomplish this, topic modelling uses different mathematical foundation, but the most relevant is BoW (Bag-of-Words) model, where text is transformed into a matrix of word frequencies or term-document occurrences in which word order is ignored.

### Common Techniques

To extract topics from a corpus, there exists multiple techniques, each one more appropriate and suitable for certain use cases, but with the a similar final result.
 
In first place there is the **Latent Dirichlet Allocation** or LDA, which was introduced in ML by Blei et al. @blei_latent_nodate @noauthor_what_2024-1 and is one of the most popular algorithms for topic modeling. It assumes:

- Each document is a mixture of fixed number of topics.
- Topics are probability distributions over a vocabulary.

Conceptually LDA assumes documents have been generated through random sampling of pre-document topics and it attempts to reverse engineer this sampling. Mathematically, LDA defines the following process:

1. Assigning each document a multinomial distribution over topics, parameterized by a Dirichlet variable $α$.
2. Assigning each topic a multinomial distribution over words, with another Dirichlet variable $β$.
3. Generating documents by sampling words based on their topic distributions.

LDA employs inference algorithms like Gibbs Sampling @blei_latent_nodate to estimate this variables mentioned before:

$$
P\left(z_i=t \mid z^{-i}, w\right)=\frac{n_{m,t}^{-i}+\alpha}{\sum_{t^{\prime}=1}^T\left(n_{m,t^{\prime}}^{-i}+\alpha\right)} \times \frac{n_{t,w_i}^{-i}+\beta}{\sum_{v^{\prime}=1}^V\left(n_{t,v^{\prime}}^{-i}+\beta\right)}
$$

However to understand this algorithms requires foundational knowledge in statistics and Monte Carlo techniques @noauthor_what_2021  which are outside of the scope of this paper. A schematic representation LDA can be seen in Figure \ref{dirichlet} to better understand the process.

![Schematic representation of LDA @blei_latent_nodate \label{dirichlet}](03_01_dirichlet_diagram.png){width=70%}

Other techniques include @vayansky_review_2020:

- **Latent Semantic Analysis (LSA)**. An algebraic approach that uses Singular Value Decomposition (SVD) to identify latent patterns. Although fast, it is sensitive to noise and lacks probabilistic interpretability.
- **Probabilistic Latent Semantic Analysis (PLSA)**. A precursor to LDA that models topics as probability distributions but struggles with scalability and overfitting.
- **Correlated Topic Models (CTM)**. Builds on LDA by capturing correlations between topics using logistic normal distributions.
- **Pachinko Allocation Model (PAM)**. Introduces topic hierarchies, enabling the modeling of more complex relationships.
- **Dynamic Topic Models (DTM)**. An extension of LDA to capture temporal evolution in topics across time.

### Evaluation Metrics

Evaluating the quality of topics is crucial in ensuring that the inferred topics are meaningful and useful. Several metrics are available for this purpose:

One of the most relevant is **perplexity**. Perplexity measures how well a probabilistic model predicts a set of unseen data. In ML it represents the number of words a model has to chose from when generating content. Perplexity values go from 1 to infinity, 1 being the ideal score. For example, if a ML model has a perplexity of $23.12$ it means the model had to chose between 23 different words when generating content. The $0.12$ decimal indicates slight deviations of the model and the closer they are to 0 the better @kherwa_topic_2018 @vayansky_review_2020 @noauthor_what_2024 @saxena_understanding_2024.

In the context of topic modeling, perplexity evaluates the likelihood of the test data given the model.  Mathematically, it is defined as:

$$
\text { Perplexity }=\exp \left(-\frac{1}{N} \sum_{d=1}^D \log P(\text { d } d)\right)
$$

Where $P(d)$ is the accumulated likelihood or probability of document $d$ and $N$ is the number of words in the corpus. Going deeper, to calculate $P(d)$ is necessary to accumulate all the probabilities of each word $w$ given the document $d$. This is defined as:

$$
P(w \mid d)=\sum_t P(w \mid t) \cdot P(t \mid d)
$$

Where $P(w \mid t)$ is the likelihood of word $w$ given the topic $t$ and $P(t \mid d)$ is the likelihood of topic $t$ being present in document $d$.

However, perplexity has limitations, as improvements do not always correlate with more coherent and better topics, but a less confused model that *can subsequently imply* better topics.

Other useful metrics are:
- The **coherence score**, which evaluates the semantic similarity of words within a topic. For instance, a topic with high coherence would have words that fall under the same theme (football, ball, player), while one which low coherence will have words hardly related to each other (tree, glass, numbers)
- Topic diversity and **exclusivity** are also relevant since they indicate the overlap between words across topics.
- Surprisingly, **human interpretation** is a key aspect when evaluating topics

Thanks to all of this metrics, its possible to overcome some challenges when using topic modelling like choosing the number of topics to generate or properly preprocessing the corpus.

## Complex networks

Complex networks are mathematical representations of systems composed of nodes (or vertices) and edges (or links) that describe relationships or interactions between them. These networks emerge in diverse fields, such as biology, sociology, computer science, physics, etc. reflecting the interconnected nature of real-world phenoms. Examples include social networks (e.g., Facebook or X), transportation networks (e.g., airline routes), biological systems (e.g., protein interaction networks), and the World Wide Web @menczer_first_2020 @barabasi_network_2016 @noauthor_network_nodate @wang_complex_2003 @mata_complex_2020.

The field of complex network science is rooted in graph theory, which dates back to Euler’s solution to the *Seven Bridges of Königsberg* problem in 1736 @noauthor_euler_nodate. In Figure \ref {sevenBridgesAbstract} an abstract representation of the bridges is shown. With this representation, Euler made the following observation: if there is a path crossing all bridges, but never the same bridge twice, then nodes with odd number of links must be either the starting or the end point of this path. Therefore, this path doesn't exist since all the nodes in the seven bridges of Königsberg have odd number of links.

![Graph of the seven Königsberg bridges.\label{sevenBridgesAbstract}](03_02_seven_bridges_abstrac.png){width=40%}

As stated before, networks are often composed by nodes and links; nodes are normally used for representing entities or concepts, while the links represent the relationship or interactions between those entities or concepts. With this almost anything can be represented with networks since it's up to us to decide what are the "*nodes*" and what are the "*links*".

Another important feature of networks is that they can be *undirected* or *directed*. In a directed network, links go only one way: from the origin to the destination; while in a undirected network links are bi-directional and the order of the two nodes in a link does not matter. 

Unlike regular graphs (e.g., grids or trees), complex networks exhibit irregular and heterogeneous patterns in their topology. They often possess characteristics such as **small-world** effects (short path lengths between nodes), **high clustering**, and **scale-free** properties (degree distributions following a power law). These features allow them to capture the complexity and diversity of real-world systems @menczer_first_2020 @wang_complex_2003.

The study of complex networks is a multidisciplinary one, combining graph theory, statistical physics, data science and more. By analyzing their structure and dynamics, researchers can uncover underlying principles governing the behavior of interconnected and real-world systems, such as the resilience of networks to failures, the spread of information, or the emergence of collective behavior.

### Basic metrics
Understanding the structure of complex networks requires the computation of various metrics, which quantify aspects like connectivity, centrality, and clustering. These metrics serve as tools to analyze and compare networks systematically @barabasi_network_2016 @noauthor_network_nodate.

The **degree** of a node is the number of edges connected to it. In directed networks, nodes have both an in-degree (incoming edges) and out-degree (outgoing edges). Formally, for a node $i$, the degree is:

$$
k_i=\sum_j A_{i j}
$$

Where $A_{ij}$ is the adjacency matrix of the network, and $A_{ij} = 1$ if nodes $i$ and $j$ are connected.

Another related concept is **degree distribution**, which refers to the probability distribution of node degrees across the network. Many real-world networks exhibit a heavy-tailed degree distribution, where most nodes have a small degree, but a few hubs have a very high degree. In scale-free networks, this distribution follows a power law like the following:

$$
P(k) \propto k^{-\gamma}
$$

Scale-free networks, characterized by this distribution, are resilient to random failures but vulnerable to targeted attacks on hubs.

The **average path length** is the mean or average of the shortest paths between all pairs of nodes in the network. Networks with a small average path length exhibit the small-world phenomenon, where most nodes can be reached from any other node in a few steps. it is represented as:

$$
L=\frac{1}{N(N-1)} \sum_{i \neq j} d_{i j}
$$

Where $N$ represents the nodes of the network and $d_{ij}$ is the shortest path between nodes $i$ and $j$.

The **clustering coefficient** measures the tendency of nodes to form tightly-knit groups. It is calculated for each node as the ratio of the number of existing links between its neighbors to the maximum possible links between them. For a node $i$, the clustering coefficient would be:

$$
C_i=\frac{2 T_i}{k_i\left(k_i-1\right)}
$$

Where $T_i$ is the number of groups involving node $i$, and $k_i$ is its degree. The average clustering coefficient is the mean of $C_i$ across all nodes, indicating the network's overall tendency to form tightly-knit groups @barabasi_network_2016 @noauthor_network_nodate.

### Centrality measures

Centrality measures help identify the most relevant or influential nodes in a network. Different centrality metrics capture various aspects of "importance", such as connectivity, intermediary roles, or influence @barabasi_network_2016 @noauthor_network_nodate.

**Degree centrality** is the simplest centrality measure, based on the number of edges a node has. This measure is particularly useful in undirected networks, where the number of connections directly correlates with influence. 

**Closeness centrality** quantifies how close a node is to all other nodes in the network. Nodes with shorter distances to others have higher closeness centrality. For a node $i$, it is calculated as:

$$
C_C(i)=\frac{1}{\sum_j d(i, j)}
$$

Where $d(i, j)$ is the shortest path between nodes $i$ and $j$.

The is also the **betweenness centrality** that measures the extent to which a node lies on the shortest paths between other nodes. Nodes with high betweenness centrality often serve as bridges or bottlenecks. This can be critical when undestanding control points or vulnerabilities in networks. For a node $i$, it is calculated as:

$$
C_B(i)=\sum_{s \neq i \neq t} \frac{\sigma_{s t}(i)}{\sigma_{s t}}
$$

Where $\sigma_{s t}$ is the total number of shortest paths from node $s$ to node $t$, and $\sigma_{s t}(i)$ is the number of those paths going through $i$.

Lastly, the **eigenvector centrality** assigns importance to nodes based on the importance of their neighbors. This "importance" can be calculated through the connectivity or centrality of a given node.

### Community detection

A *community* is a group of nodes within a network that have stronger interactions among themselves than with the rest of the network. For example, in social networks, communities often represent groups with shared interests or activities @menczer_first_2020 @mata_complex_2020. 

 Community detection algorithms aim to identify densely connected groups of nodes within a network and can lead to unrevealing hidden information in complex networks such as data patterns or unique behaviors.
 
Regardless of the algorithm chosen, the quality of the detected communities must be evaluated using metrics such as:

- **Modularity**. Higher values indicate better-defined communities.
- **Normalized Mutual Information (NMI)**. Quantifies agreement between detected and ground-truth communities.
- **Conductance**. Evaluates the fraction of edges that leave a community relative to the total number of edges within and leaving the community.

Some of the most used algorithms for community detection are:
- The **Louvain** method. This is one of the most popular and efficient algorithms for community detection. It is based on the optimization of **modularity**, a metric that quantifies the density of edges within communities relative to edges between communities. Although really good, it has its limitations, like producing disconnected communities in networks with low modularity and its processing being order dependent. The algorithm procedure cam be defined in 3 steps:
	- Initially, each node is assigned to its own community.
	- Nodes are iteratively reassigned to neighboring communities if doing so increases modularity.
	- Once no further improvement is possible, communities are aggregated into "super-nodes," creating a new network. The process is repeated on the aggregated network until modularity converges.
- Related to the previous, the **Leiden** method builds upon the Louvain algorithm, addressing some of its limitations, particularly the issue of disconnected or poorly connected communities. The key difference lies in a refinement step in its procedure that ensures communities remain well-connected by splitting and merging disconnected components before proceeding to the next iteration.

## Disinformation and complex networks

Once reached this point it is necessary to make an intersection between disinformation and complex networks and explore how researchers have employed various methodologies to analyze the structure, behavior, and impact of fake within complex networks:

- **Investigating Fake and Reliable News Sources Using Complex Networks**: This study aimed to identify disinformation spreaders by analyzing the relationships among websites using audience overlap metrics, commonly employed in SEO. A network of approximately 12,200 nodes was constructed, combining sub-networks based on these metrics. Complex network analysis was applied to visualize and analyze website relationships, highlighting the potential of SEO metrics and network analysis to identify communities of websites, including those disseminating fake news @mazzeo_investigating_2022.
- **Modeling Disinformation Networks on Twitter: Structure, Behavior, and Impact**. This research investigated the structural and behavioral differences between disinformation sources and legitimate accounts on Twitter. Using interaction-based network structures, it examined the number of nodes, edges, clustering and other key metrics. Additionally, it explored dynamic aspects such as the speed and patterns of disinformation spread. The findings underscored the role of network topology in understanding and combating disinformation @munoz_modeling_2024.
- **Disinformation Detection Using Graph Neural Networks: A Survey**. This survey reviewed approaches for automatic detection of disinformation, focusing on Graph Neural Networks (GNNs). It highlighted the strengths of GNNs in processing graph data and their suitability for social networks. The study emphasized that GNNs effectively model complex relationships and interactions, making them powerful tools for detecting disinformation on platforms like Twitter and Facebook @lakzaei_disinformation_2024.
- **A Unified Graph-Based Approach to Disinformation Detection Using Contextual and Semantic Relations**. This study proposed a graph-based framework that combines contextual and semantic information to improve disinformation detection. Using a meta-graph that integrates relational, semantic, and topical data, the approach was applied to Twitter datasets from the 2016 US election. The framework consistently improved accuracy in disinformation detection, demonstrating the value of combining multiple dimensions of graph data @paraschiv_unified_2021.
- **Automatic Detection of Influential Actors in Disinformation Networks**. Focusing on identifying key actors in disinformation campaigns, this study integrated natural language processing, machine learning, and graph analytics with a novel causal inference approach. Applied to hostile information campaigns, including datasets from the 2017 French elections, it achieved high precision in detecting disinformation accounts, mapped critical communities, and identified high-impact actors @smith_automatic_2021.
- **Behavioral Forensics in Social Networks: Identifying Misinformation, Disinformation, and Refutation Spreaders Using Machine Learning**. This research proposed a method to identify actors spreading misinformation, disinformation, and its refutation based on user behavior. By extracting network features through deep learning-based graph embedding models and training a machine learning classifier, the study demonstrated effective detection of malicious actors with high precision, highlighting the relevance of behavioral analysis in combating disinformation @khan_behavioral_2023.

The approach of this paper although not at the same level as others previously mentioned, integrates multiple techniques such as topic modeling, complex networks, and community detection to explore disinformation in a new way.

A particularly novel aspect is the use of the **Minimum Spanning Tree (MST)** to distill the network into its core structure, retaining only the most critical relationships. This simplification enhances interpretability, which is often lacking in dense network analyses. Few studies employ MSTs in disinformation research, making this a standout feature.

Community detection on the MST adds another layer of insight. By identifying clusters of thematically and structurally similar documents, this approach uncovers **narrative communities** that highlight how disinformation themes propagate and interlink. Unlike approaches that stop at topic prevalence, this method integrates **content and structure**, offering a **system-wide perspective**.

Applying these techniques and topic modelling to PolitiFact.com (a dataset traditionally studied for classification accuracy) shifts the focus to structural relationships within fake news narratives.