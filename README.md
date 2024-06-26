## Abstract
Our study delves into enhancing the robustness of Autonomous Systems (AS) networks, crucial for the reliability of the Internet's infrastructure. By employing Monte Carlo simulations and machine learning (ML) models, we evaluated the resilience of AS networks against various attack strategies, highlighting the importance of certain nodes in maintaining network integrity. The analysis, conducted on 52 real-world networks, revealed that targeted attacks, particularly those based on betweenness and degree centrality, pose significant threats compared to random attacks. The Random Forest (RF) model emerged as a standout in predicting network robustness, indicating that network density and node degree are key factors. Our research underscores the potential of ML in designing resilient networks and suggests future directions, including exploring network heterogeneity and simulating real-world attack scenarios, to fortify the digital connectivity underpinning today's Internet ecosystem.

![graph_mod](https://github.com/sajaddadgar/Robustness-Analysis-of-AS-Network/assets/47991444/edd8fd6d-3d15-46a6-8012-43630db92515)


## Dataset
Our study utilizes a subset of the "AS Relationships" dataset from The Center for Applied Internet Data Analysis (CAIDA)\cite{CAIDA2013}, which provides crucial insights into the business interactions between Autonomous Systems (ASes) on the Internet. This dataset, significant for understanding internet inter-domain routing and economic structures, spans from 2013 to the current date and encompasses around 500GB of data. Due to its extensive size, we selectively extracted the most pertinent segments for our analysis. The raw data encapsulates ASes interactions derived from BGP routing table analyses, structured in a detailed format that includes the organization collecting the data, the BGPstream collector's name, frequency of path observations, AS path, prefix, code, and peer IP address. This format meticulously records the dynamic interconnections and operational specifics of ASes, offering a granular view of the internet's backbone and its operational dynamics. Our focused extraction and analysis of this dataset facilitate an in-depth exploration of AS networks, shedding light on their complex relationships and the foundational role they play in the global internet infrastructure.



## Methods
In our study on network structure robustness, we implemented a comprehensive computational method that combines theoretical and empirical analysis through two main approaches designed to enhance understanding of how network robustness can be quantified, enhanced, and potentially protected against failures and targeted attacks. The first approach utilizes Monte Carlo simulations to evaluate the network's resilience against various attacks. The second approach focuses on analyzing network attributes and their impact on resilience using various machine learning algorithms. This dual approach allows us to quantify network robustness and identify attributes that contribute to its resilience, offering insights into both the immediate effects of attacks and long-term strategies for network reinforcement.

## Results

### Approach 1. Monte Carlo Simulation for Robustness Calculation

![G1](https://github.com/sajaddadgar/Robustness-Analysis-of-AS-Network/assets/47991444/ed10d418-84e7-4069-9b0f-04123545fd51)

Our comprehensive analysis, combining Monte Carlo simulations and Machine Learning, reveals key insights into the robustness of Autonomous Systems networks against various attack strategies. Initial Monte Carlo simulations, with a single iteration, identified crucial nodes and vulnerabilities, offering a preliminary view of network resilience. Expanding this to 100 iterations refined our understanding, with the average R metric pinpointing areas prone to attack more accurately. Our ML exploration, particularly through Random Forest, excelled in predicting network resilience, underscoring its capability to handle complex network data effectively. The betweenness strategy yielded a robustness score of 0.0186, emphasizing the importance of nodes that connect others, while the degree strategy's R of 0.0159 highlighted the significance of highly connected nodes. Conversely, random attacks had a minimal impact, with a robustness score of 0.4207, and the closeness strategy resulted in an R of 0.1150, showing a moderate effect. These findings demonstrate the varying impacts of different attack strategies on network robustness and underscore the importance of strategic node connectivity and redundancy to enhance network resilience.

![G100](https://github.com/sajaddadgar/Robustness-Analysis-of-AS-Network/assets/47991444/60d240c3-67ab-4f4a-8113-43203d3b0c90)





### Approach 2. Machine Learning Models for Robustness Prediction

#### Prediction of RD robustness:

| Model              | Mean Absolute Error | Mean Squared Error | Root Mean Squared Error | R-squared          |
|--------------------|---------------------|--------------------|-------------------------|--------------------|
| Random Forest      | 0.060028            | 0.004145           | 0.064383                | 0.575149           |
| SVM                | 0.045393            | 0.002461           | 0.049613                | 0.162101           |
| Decision Tree      | 0.068600            | 0.006537           | 0.080854                | 0.110316           |
| Linear Regression  | 0.074860            | 0.005933           | 0.077026                | 0.192567           |
| Ridge Regression   | 0.074813            | 0.007631           | 0.087358                | -0.038579          |
| Lasso Regression   | 0.067566            | 0.008107           | 0.090038                | -0.103279          |
| Elastic Net Regression | 0.067555        | 0.008105           | 0.090029                | -0.103041          |

![RD-ML](https://github.com/sajaddadgar/Robustness-Analysis-of-AS-Network/assets/47991444/210eeb33-3dbd-4d33-be6d-39027204ed38)



#### Prediction of IB robustness:

| Model              | Mean Absolute Error | Mean Squared Error | Root Mean Squared Error | R-squared          |
|--------------------|---------------------|--------------------|-------------------------|--------------------|
| Random Forest      | 0.072956            | 0.009135           | 0.095578                | 0.420584           |
| SVM                | 0.103772            | 0.012430           | 0.111489                | 0.211613           |
| Decision Tree      | 0.062800            | 0.007032           | 0.083855                | 0.579283           |
| Linear Regression  | 0.033904            | 0.002237           | 0.047292                | 0.497674           |
| Ridge Regression   | 0.051074            | 0.003789           | 0.061553                | 0.149053           |
| Lasso Regression   | 0.060359            | 0.005063           | 0.071157                | -0.137207          |
| Elastic Net Regression | 0.060360        | 0.005064           | 0.071158                | -0.137255          |



![IB-ML](https://github.com/sajaddadgar/Robustness-Analysis-of-AS-Network/assets/47991444/3805b460-a98d-4b90-af27-10720aacae8c)


