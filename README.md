# Portfolio Thilo Weber

Hi, my name is Thilo Weber, I am an experienced ML engineer & data scientist with a strong background in signal processing, machine learning and software engineering; expertise in data modeling, probabilistic reasoning, AI-powered process automation and integration of complex data sources; experience in academic research as well as industrial applications, especially in renewable energy and the development of innovative ML solutions. I am an intuitive and creative engineer consistently producing innovative solutions and high quality data products.

## Focus and expertise

- **Machine learning & AI:** Development of ML models for signal processing, computer vision & predictive analytics
- **Data integration & geoinformation:** Automated data processing from over 30 sources, geodata analysis & visualization
- **Software development & automation:** Creation of data-based applications, efficient model deployment in cloud environments
- **Research & prototyping:** Experience in scientific research, development & publication of ML methods

-----

## Projects

- [Knowledge management & AI agents](#knowledge-management-and-ai-agents)
- [Parsing ustructured PDFs & information extraction from documents](#parsing-ustructured-pdfs-and-information-extraction-from-documents)
- [Energy efficiency monitoring & treatment effect estimation](#energy-efficiency-monitoring-and-treatment-effect-estimation)
- [Energy and CO2 Monitoring for municipalities](#energy-and-co2-monitoring-for-municipalities)
- [Model-based signal processing with sparse, half-space, and box constraints](#model-based-signal-processing-with-sparse-or-half-space-or-box-constraints)
- [Machine learning-based lead generator & recommender system](#machine-learning-based-lead-generator-and-recommender-system)
- [Building renovation pressure & time-to-event prediction & survival analysis](#building-renovation-pressure-and-time-to-event-prediction-and-survival-analysis)
- [PV detection & image segmentation from classification labels only](#image-segmentation-from-classification-labels-only)
- [Scientific publications](#scientific-publications)

-----

## Knowledge management and AI agents

**Description:**

- Developing and evaluating **custom RAG agent** vs. off-the-shelf solutions (e.g., **NotebookLM**) for **knowledge management** (at Roche Diagnostics)
- Integrating *AI agents* into a **car shop ERP** (ZosimoLab collaboration)

**Methods:**

- AI agents
- Vector stores
- Evaluation with Ragas & MLFlow / LangSmith

**Specials:**

- **Possible applications 1:** knowledge management & sharing
- **Possible applications 2:** many possible task automations

**Technology:**

Python, MLflow, LangChain, RavenAI, Ragas, LangSmith

**Images:**

![Difflib HTML comparison](/img/raven-ai.png)

[Jump to top](#portfolio-thilo-weber)

-----

## Parsing ustructured PDFs and information extraction from documents

**Description:**

For [Demokratis](https://www.demokratis.ch/), I helped to make Legislative Consultation PDFs more accessible and interactive by parsing them into a structured data form using AI. I employed an evaluation driven development approach, that 
helps to navigate the landscape of innumerable possible parsing solutions.

**Methods:**

- **Evaluation driven Generative AI**: Constructing numeric and visual evaluation metrics using Python's difflib and tracking experiment code and results in MLflow.
- **LlamaParse**: Powerful AI tool for extracting data from documents, such as PDFs.
- **ChatGPT API with file upload**: Another approach evaluated, but less suited for this particular problem.

**Specials:**

- **Quality assurance & enhanced manual correction:** The great variety of structure in the input documents and the stochasticity of AI models make it difficult to ensure correct parsing. I developed an approach, where two (or more) different parsing approaches run in parallel and the results are compared using *difflib*. In case of discrepancies in results, the pipeline owner gets a notification along with indications of the differences to simplify fast manual corrections.
- **Possible applications:** Similar approaches can be used to convert a wide range of real world data and documents into a structured form, and thereby unlock great potential for a variety of new data analysis and processing use cases.

**Technology:**

Python, LlamaParse, openai APIs, MLflow, difflib

**Links:**

- [Blog: Parsing Legislative Consultation PDFs Using LlamaParse](https://medium.com/@thiloweber/parsing-legislative-consultation-pdfs-using-llamaparse-fdd4627b9094)

**Images:**

![Difflib HTML comparison](/img/output-difflib-html.png)

[Jump to top](#portfolio-thilo-weber)

-----

## Energy efficiency monitoring and treatment effect estimation

**Description:**

At geoimpact, I developed machine learning models for predicting the yearly heat and electricity demands of buildings. In the context of a Master’s thesis, we used these models to estimate the actual reduction in yearly heat consumption effected by different retrofit measures (roof/facade insulation, window replacement, ...). I published a paper in collaboration with HSLU that describes how to use this framework in order to build a monitoring of the treatment effects of different retrofit measures applied to buildings in a portfolio or a region.

**Methods:**

- **Heterogeneous treatment effects & causal inference:** Heterogeneous treatment effects refer to the variation in the impact of a treatment across individuals or subgroups, and causal inference aims to estimate and understand these effects by identifying the causal relationship between interventions and outcomes.
- **Partial dependence:** The plots below show the partial dependence of the heat consumption indicator (HCI) on construction year and heating degree days.
- **Combining domain knowledge & ML:**  In the plots below, the lines of the linear model and the neural network, which both integrate domain knowledge in the model architecture, show more realistic dependencies than the gradient boosting (without domain knowledge).

**Specials:**

- **Possible applications:** Apart from efficiency monitoring, such a framework can be used for a general root cause analysis of physical processes. For example, I introduced the framework to a friend who is working for a big chemical industry company. He quickly gained a lot of valuable insights into their production processes from it. He is since known as “the data leech” at his company.

**Technology:**

Python, Scikit-Learn, Tensorflow, CausalML, MLflow, PostgreSQL, PostGIS, Kubernetes

**Links:**

- [Scientific paper](https://doi.org/10.1016/j.enbuild.2025.116369) in collaboration with Hochschule Luzern.

**Images:**

![Framework diagram](/img/framwork_schema.png)

![Partial dependences for different input features](/img/pdp_heat_demand_indicator.png)

[Jump to top](#portfolio-thilo-weber)

-----

## Energy and CO2 Monitoring for municipalities

**Description:**

At geoimpact, in collaboration with the Federal Office of Energy, we developed the public web application Energy Reporter, which monitors the progress of all Swiss municipalities in the energy transition. I was responsible for the design and deployment of the methodology and data pipeline that imports public datasets and updates the six indicators every week. The indicators of Energy Reporter are published as open data. Building on the Energy Reporter, I further developed a comprehensive energy and CO2 monitoring containing over fifty fine granulated indicators, among which also the scope 1 and 2 CO2 emissions per municipality and year.

**Methods:**

This project involved reasearching and processing of many different public data sources. Especially the two indicators for electricity consumption and renewable electricity production rely on statistical models that build on more than ten different data sources each.

**Specials:**

The Energy Reporter is widely used by the public, especially by municipal officers and the media. It’s open data is used by many Swiss medias such as SRF, 20 min, Watson, and many local news papers. It uses an unconventional data visualization method encouraging users to interactively compare different municipalities, inspired by the Quartett card game.

**Technology:**

Python, Pandas, Scikit-Learn, PostgreSQL, PostGIS, Kubernetes, Hangfire

**Links:**

- [Energie Reporter Web-app](https://www.energiereporter.ch)
- [Energie Reporter Methodology](https://energiereporter.energyapps.ch/methodology)
- [Energie Reporter open data](https://opendata.swiss/en/dataset/energie-reporter)

**Images:**

![Energie Reporter](/img/energiereporter.png)

[Jump to top](#portfolio-thilo-weber)

-----

## Model-based signal processing with sparse or half-space or box constraints

**Description:**

In my Master’s thesis at ETH Zurich, I used statistical signal processing methods for separating positional eye movement measurements into different types (saccades, smooth pursuit, and fixation eye movements). I developed a novel approach to precessing eye movement signals based on estimating signals in a mechanistic physiological model of the eye muscles. Apart from signal separation, the framework is also able to estimate the neural inputs into the eye muscles from the positional measurements.

**Methods:**

- **Factor graphs:** They are a powerful probabilistic framework for working with structured models and have many applications, e.g., state space models, image models, error correcting codes, optimal control.
- **Sparse Bayesian learning:** This is a widely applicable and efficient method for modeling and estimating sparse (non-gaussian) priors in a probabilistic framework, which we applied to factor graphs.

**Specials:**

- **Possible applications:** The framework of **state-space-models** with **message passing** in combination with **sparse**, **discrete**, **half-space**, and **box constraits** (or priors) can be used for a variety of optimization problems and signal processing taskes, in particualr for long-term **model predictive control**.
- **Methodological innovation:** Firstly, the usage of a new sparsity prior within the factor graph framework, which allowed to appropriately set the sparsity level. Secondly, the usage of existing mechanistic eye movement models, which have been developed since the 1980s, for solving this problem.

**Technology:**

Matlab

**Links:**

- [Journal paper: Model-based separation, detection and classification of eye movements](https://doi.org/10.1109/TBME.2019.2918986)
- [Code github](https://github.com/magnetilo/mbsdc_code)

**Images:**

![mbsd_framework](/img/mbsd_framework.png)

![eye_movement_separation](/img/eye_movement_separation.png)

[Jump to top](#portfolio-thilo-weber)

-----

## ML-based lead generator and Thompson Sampling

**Description:**

At geoimpact, I developed a lead generator that suggests promising buildings for the sale of a renewable energy product based on a list of past sales of the product.

**Methods:**

- **Thompson sampling:** This is a method for addressing the exploration-exploitation tradeoff in contextual bandit problems, where we want to maximise a certain reward (i.e., contacting the most promising building owners) and at the same time to continuously improve our model predicting the reward.
- **Extra trees classifier:** I used a simple implementation of Thompson sampling by sampling different trees of an extra tree classifier.
  1. Train a Random Forest (RF) or an Extra Trees (ET) regressor with N trees.
  2. Sample B times N_s trees, where B is the batch size and N_s < N is a subset of all trees.
  3. Maximize (argmax) the target optimization function for all B "subforests" of N_s trees and evaluate the simulation or experiment at the B potential maximum arguments. Return to step 1.
- **Supervised clustering:** The extra tree classifier can also be used to create cluster of buildings that behave “similar” with respect to this sales-problem. These cluster were used for a **stratified sampling** approach that helps to enhance the diversity in the potential customer exploration. The plot below shows a similarity matrix clustered into ten clusters of “similar” buildings.

**Specials:**

We tested this method with a company selling photovoltaic systems. The project was stopped after the testing phase, as the cold acquisition process was too tedious. Here, I learned that a method can be theoretically very elaborated, but in the end it still needs to fit well into an end-to-end business workflow in order to be practical.

**Technology:**

Python, Scikit-Learn

**Links:**

- [Blog: Machine learning for MarketSense](https://www.swissenergyplanning.ch/post/machine-learning-for-marketsense-1)

**Images:**

![similarity_clustering](/img/similarity_clustering.png)

[Jump to top](#portfolio-thilo-weber)

-----

## Building renovation pressure and time-to-event prediction and survival analysis

**Description:**

At geoimpact, I developed multiple models for estimating the renovation pressure of a building. The underlying problem structure of calculating the time until a certain event happens has a variaty of applications apart from renovation rates in industry, medicine, churn rate (in e-commerce and human resources), and more.

**Methods:**

There are different ways to mathematically express such a pressure. We explored two approaches:

- **Cox hazard model**
- **Conditional density estimation** using neural networkds for calculating context- dependent survival functions

**Specials:**

The developed renovation pressure model has been integrated by different real- estate companies into their workflows and services.

**Technology:**

Python, lifelines, TensorFlow Probability

**Links:**

- [Blog: Sanierungsdruck auf Gebäudeebene](https://www.swissenergyplanning.ch/post/sanierungsdruck-auf-gebäudeebene-1)
- [Master Thesis Sarah Schneeberger: Energetic Restoration Pressure](https://github.com/Pflotsch/Energetic-Restoration-Pressure-Thesis/blob/master/Energetic_Restoration_Pressure.pdf)

**Images:**

![renovpress](/img/renovpress.png)

[Jump to top](#portfolio-thilo-weber)

-----

## Image Segmentation from Classification Labels only

**Description:**

At geoimpact, I developed a model for detecting photovoltaic (PV) systems in satellite images and estimating their area. The plan was to extract a Swiss-wide data base with all installed PV-systems and their installed capacity from arerial and satellite images.

**Methods:**

- **Convolutional neural networks (ConvNet):** They are a special sort of neural networks that are especially useful for different image and video tasks, such as, object detection, segmentation, image descriptions, and more.
- **Class activation mappings (CAM):** While the most common approach of semantic segmantation would require to manually mark a lot of PV systems with polygons in target images, I used a special approach based on class activation mappings (CAM) that required only classification labels if an image contains a PV system or not.

**Specials:**

Soon after we started the project, the Swiss Federal Office of Energy published an open data set containing all registered PV systems registered, which made our project basically obsolete. Here I learned, that there are often different ways to acquire a specific dataset. Sometimes, there are probably simpler and more accurate acquisition methods than rather complex image detection approaches.

**Technology:**

Python, PyTorch, OpenCV

**Images:**

![test_CAM](/img/test_CAM.jpg)

[Jump to top](#portfolio-thilo-weber)

-----

## Scientific publications

- T. Weber, S. Schneeberger, P. Schuetz, “Estimating Heterogeneous Treatment Effects of
Building Energy Efficiency Retrofits Using Machine Learning,” Energy Build., Aug. 2025,
[https://doi.org/10.1016/j.enbuild.2025.116369](https://doi.org/10.1016/j.enbuild.2025.116369).
- F. Wadehn, T. Weber, D. J. Mack, et al., “Model-Based Separation, Detection, and
Classification of Eye Movements,” IEEETans. Biomed. Eng., Feb. 2020,
[https://doi.org/10.1109/TBME.2019.2918986](https://doi.org/10.1109/TBME.2019.2918986).
- F. Wadehn, T. Weber, and H.-A. Loeliger, “State space models with dynamical and
sparse variances,” Europ. Signal Proc. Conf. (EUSIPCO), Sept. 2019,
[https://doi.org/10.23919/EUSIPCO.2019.8902815](https://doi.org/10.23919/EUSIPCO.2019.8902815).
- Z. Bjelobrk, P. M. Piaggi, T. Weber, T. Karmakar, M. Mazzotti and M. Parrinello,
“Naphthalene crystal shape prediction from moleculardynamics simulations,” Cryst. Eng.
Comm., April 2019, [https://doi.org/10.1039/C9CE00380K](https://doi.org/10.1039/C9CE00380K).
- F. Wadehn, D. J. Mack, T. Weber, and H.-A. Loeliger, “Estimation of neural inputs and
detection of saccades and smooth pursuit eye movements by sparse Bayesian learning,”
Int. Conf. IEEEEng. Med. Biol. Soc. (EMBC), Hawaii, July 2018,
[https://doi.org/10.1109/EMBC.2018.8512758](https://doi.org/10.1109/EMBC.2018.8512758).

[Jump to top](#portfolio-thilo-weber)
