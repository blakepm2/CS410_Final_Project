<p align="center">
    <img src="public/assets/logo.png" width="600" alt="logo">
</p>
<p align="center">
    Created by
    <img src="public/assets/test.svg" width="130" height="25" align="center">
</p>

---

![Python](https://img.shields.io/badge/Python-%233776AB?style=for-the-badge&logo=python&logoColor=white&labelColor=%233776AB)
![JavaScript](https://img.shields.io/badge/JavaScript-%23F7DF1E?style=for-the-badge&logo=javascript&logoColor=black&labelColor=%23F7DF1E&color=%23F7DF1E)

![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-%230C55A5.svg?style=for-the-badge&logo=scipy&logoColor=%white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Plotly](https://img.shields.io/badge/PLOTLY-%233F4F75?style=for-the-badge&logo=plotly&logoColor=white&labelColor=%233F4F75&color=%233F4F75
)
![Flask](https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white)
![Dash](https://img.shields.io/badge/Dash-%23008DE4?style=for-the-badge&logo=dash&logoColor=white
)

<br>

![Release](https://img.shields.io/badge/release-Pre--Alpha-%23B5FF84?style=flat&logo=github&labelColor=%23181717)<br>
![Downloads](https://img.shields.io/badge/%E2%AC%87%EF%B8%8F_downloads-0-%23F1F1F1?style=flat&labelColor=%23181717)


# 📋 Table of Contents

1. [📖 What is Historian?](#📖-what-is-historian)
2. [🎯 Objective](#🎯-objective)
3. [🚀 Usage](#🚀-usage)
4. [🛠 Buld](#🛠-build)
4. [💙 Contributors](#💙-contributors)

# 📖 What is Historian?

> Final project for CS 410 Text Information Systems at the University of Illinois Urbana-Champaign

**Historian** is a Google Chrome extension that builds a knowledge graph of your visited webpages based on their similarity with respect to each other.

<!-- <p>
    <img src="public/demos/HistorianDemoGIF.gif">
</p> -->

**Features**
* Builds graph of webpages visited 
* Visualizes the similarity of webpages in history
* Presents an intuitive way to research

<br>

# 🎯 Objective

Create a Google Chrome extension that acts as a [knowledge graph builder](https://www.ibm.com/topics/knowledge-graph#:~:text=A%20knowledge%20graph%2C%20also%20known,the%20term%20knowledge%20%E2%80%9Cgraph.%E2%80%9D) for webpages that the user visits while researching information online.

The extension should represent the user's visited webpages as nodes in a graph where the edges reflect the relative similarity between them such that similar webpages will be clustered together.

This will offer users an intuitive way to visualize their search history while performing online research and eliminate the reliance on other third party applications to track this information.

# 📌 Tasks

| Task | Assigned To |
| --- | --- |
| Learn how to make a Chrome extension | Everyone |
| Visualizing Graphs | Blake |
| Web Scraping | Megha |
| Similarity Algorithm | Michael |
| Build Frontend | Rohan |
| Build Backend | Kaushal |

# 🚀 Usage

> [!NOTE] 
> The section(s) that follow provide comprehensive instructins for getting **Historian** setup on your local device. After completing [Step 1](###step-1:-clone-this-repository) and [Step 4](###step-4:-load-the-unpacked-extension-into-chrome), you can run the [demo script](demo.py) to install dependencies, start the local server, and open some sample webpages to see an easy demonstration of how **Historian** works.

## Dependencies

The table below gives an overview of the dependencies for this project as well as the versions used. For the packages, you can download these directly or run the `setup.py` script as discussed in the next section.

<details><summary><b>Show dependencies</b></summary>

| Item | Version |
| --- | --- |
| Python | [3.12.0](https://www.python.org/downloads/release/python-3120/) | 
| NumPy | [1.26.1](https://pypi.org/project/numpy/#files) |
| SciPy | [1.11.3](https://pypi.org/project/scipy/#files) |
| SciKit-Learn | [1.3.2](https://pypi.org/project/scikit-learn/#files) |
| NLTK | [3.8.1](https://pypi.org/project/nltk/#files) |
| BeautifulSoup | [4.12.2](https://pypi.org/project/beautifulsoup4/#files) |
| Plotly | [5.18.0](https://pypi.org/project/plotly/#files) |
| Dash | [2.14.2](https://pypi.org/project/dash/#files) |
| Flask | [3.0.0](https://pypi.org/project/Flask/#files) |
| Flask-Caching | [2.1.0](https://pypi.org/project/Flask-Caching/#files) |
| Flask-Cors | [4.0.0](https://pypi.org/project/Flask-Cors/#files) |
| Regex | [2023.10.3](https://pypi.org/project/regex/#files) |
| Alive-Progress | [3.1.5](https://pypi.org/project/alive-progress/#files) |

</details>

## Setup

> [!IMPORTANT]
> Historian is not currently being hosted on a domain, which means that the only way to currently use this extension is by running the server locally on your machine. The instructions below will guide you through the setup process step-by-step.

### Step 1: Clone this Repository

First you need to clone this repo to your local machine to access the server as well as the extension. The instructions below are adapted from [GitHub's documentation](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository) on cloning repositories; for more information, please refer to the [docs](https://docs.github.com/en).

<details><summary><b>Show instructions</b></summary>

1. Navigate to the main page of the repository.

2. Above the list of files, click **<> Code**.

3. Copy the URL for the repository.
    - To clone the repository using HTTPS, under "HTTPS", click <img src="public/assets/misc/CopyIcon.png" width="17">.

4. Open Git Bash.

5. Change the current working directory to the location where you want the cloned repository. e.g.
    ```
    cd path/to/folder
    ```

6. Type `git clone`, and then paste the URL you copied earlier, e.g.
    ```
    git clone https://github.com/blakepm2/CS410_Final_Project
    ```

7. Press **Enter** to create your local clone.

</details>

### Step 2: Install dependencies

After cloning the repo, you can install the [dependencies](##dependencies) using the `setup.py` or manually with `pip`.

> [!NOTE]  
> **Python 3.12** is required in order to run `setup.py`. If you do not have **Python 3.12** installed, please download it [here](https://www.python.org/downloads/release/python-3120/) before proceeding.

<details><summary><b>Show instructions</b></summary>

#### Option 1: Using `setup.py`

1. Navigate to the directory where you saved the repository.
    ```
    cd path/to/repository
    ```

2. Run `setup.py` to install all dependencies.
    ```
    py -3.12 setup.py
    ```

#### Option 2: Using `pip`

1. Navigate to the directory where you saved the repository.
    ```
    cd path/to/repository
    ```

2. In the terminal, run the following command:
    ```
    py -3.12 -m pip install -r config/requirements.txt
    ```

</details>

### Step 3: Start the local server

Once you've successfully cloned the repo and installed the necessary dependencies, you can host the local server on your machine to enable the backend functionality of the extension.

<details><summary><b>Show instructions</b></summary>

1. Navigate to the directory where you saved the repository.
2. Run `server.py`.
    - This will begin hosting a server on your local network. 
3. Verify that the server is running.
    - You can verify that the server is running by visiting http://127.0.0.1:8050/ in a web browser.

</details>

> [!IMPORTANT]
> Historian works by sending a list of the URLs from your history to the server, which will then perform the computations needed to create the graph. Once completed, the server will asynchrononously update the graph on the frontend for you to see. Thus, it is imperative that you run the server in order to see your results visualized. 

### Step 4: Load the unpacked extension into Chrome

In order to use the extension in Chrome, you need to load an unpacked version into your extensions. The instructions below are adapted from [Google Chrome's documentation](https://support.google.com/chrome_webstore/answer/2664769?hl=en), which you can consult for more information.

<details><summary><b>Show instructions</b></summary>

1. On your computer, open **Chrome**.
2. At the top right, click **More** (three dots) **> Extensions > Manage Extensions**.
3. At the top right, enable **Developer mode**.
4. At the top left, click **Load unpacked**.
5. Navigate to the directory where you stored the repository, and select the `extension` folder.
6. Verify that the extension has been loaded.
    - Once the extension has been successfully loaded into Chrome, you should see **Historian** listed in **My extensions**.

</details>

### Step 5: Displaying the graph 

After the extension has been loaded into Chrome and the local server has been started, you should now be able to use **Historian** to see the hierarchical graph of your recent search history. 

1. On your computer, open **Chrome**.
2. Visit some webpages.
    - Try to visit different kinds of webpages so that the app can highlight the divisions between them (e.g. "best snack foods", "top 10 careers for computer science majors", "best nba players of all time"). 
    - If you're having trouble coming up with ideas or would rather use some pre-selected samples, **please use the [demo](demo.py)**.
3. In the top right, click <img src='public/assets/misc/ChromeExtensionsIcon.png' width='17'> and select **Historian** from the dropdown menu.
4. In **Historian**, click **Visualize History**.

You should see a graph populate with lines connecting nodes that represents the hierarchical clusters of your browsing history. 

# 🛠 Build

## Overview

**Historian** defines several modules to facilitate its functionality. The table below provides a high-level overview of these modules with links to their respective code and documentation. 

| Module | Purpose | Documentation | 
| --- | --- | --- |
| [Document](src/webScraping/document.py) | Represent webpages as documents | [Link](##document) | 
| [WebScraper](src/webScraping/webScraper.py) | Extract webpage text data | [Link](##webscraper) |
| [HierarchicalClustering](src/graphing/hierarchicalClustering.py) | Perform agglomerative hierarchical clustering | [Link](##hierarchicalclustering) |
| [Dendrogram](src/graphing/dendrogram.py) | Visualize hierarchical clusters | [Link](##dendrogram)

## [Document](src/webScraping/document.py)

A class to represent scraped webpages as documents

```
src.webScraping.document.Document(self, title, text, url)
```

### Parameters

- ***self*** `Document` : The `Document` object
- ***title*** `str` : The title of the webpage
- ***text*** `str` : The text data of the webpage
- ***url*** `str` : The url of the webpage

### Methods

---

None

---

## [WebScraper](src/webScraping/webScraper.py)

A class for extracting text data from webpages

```
src.webScraping.webScraper.WebScraper(self)
```

### Parameters

- ***self*** `WebScraper` : The `WebScraper` object

### Methods

---

**getWebpageText( *self*, *response* )**

Extracts and preprocesses the data from a webpage from a given `requests.Response` object

**Parameters**

- ***self*** `WebScraper` : The `WebScraper` object
- ***response*** `requests.Response` : A `requests.Response` object for a given URL

**Returns** `str`

---

**scrapeWebpages ( *self*, *urls* )**

Extracts text data from webpage(s) at a given url and saves their text data as a string into the `Webscraper.corpus` hashmap

**Parameters**

- ***self*** `WebScraper` : The `WebScraper` object
- ***urls*** `list` : A list of URLS for the webpages you want to scrape

**Returns** `dict`

---

## [HierarchicalClustering](src/graphing/hierarchicalClustering.py)

A class to perform agglomerative hierarchical clustering with average link for a collection of webpages

```
src.graphing.hierarchicalClustering.HierarchicalCluster(self)
```

### Parameters 

- ***self*** `HierarchicalClustering` : The `HierarchicalClustering` object

### Methods

---

**preprocess( *self*, *text* )**

Preprocesses text data from a document by performing normalization, tokenization, and lemmatization

**Parameters**

- ***self*** `HierarchicalClustering` : The `HierarchicalClustering` object
- ***text*** `str` : The text data from a webpage document

**Returns** `str`

---

**preprocess_docs( *self*, *docs* )**

Preprocesses text for a collection of documents by performing normalization, tokenization, and lemmatization

**Parameters**

- ***self*** `HierarchicalClustering` : The `HierarchicalClustering` object
- ***docs*** `list` : A list of the processed documents to 

**Returns** `list`

---

**extract_features( *self*, *docs* )**

Implements Term Frequency (TF) - Inverse Document Frequency (IDF) weighting to a set of (processed) documents

**Parameters**

- ***self*** `HierarchicalClustering` : The `HierarchicalClustering` object
- ***docs*** `list` : A list of the processed documents you want to analyze

**Returns** `numpy.ndarray`

---

**create_hierarchical_cluster( *self*, *tfidf_matrix* )**

Performs hierarchical/agglomerative clustering for a TF-IDF weighted matrix of text data from a collection of documents using Average-Link

**Parameters**

- ***self*** `HierarchicalClustering` : The `HierarchicalClustering` object
- ***tfidf_matrix*** `numpy.ndarray` : A TF-IDF weighted mattrix of text data

**Returns** `numpy.ndarray`

---

**create_dendrogram( *self*, *cluster*, *docs*)**

Creates a dendrogram to visualize a hierarchical/agglomerative cluster

**Parameters**

- ***self*** `HierarchicalClustering` : The `HierarchicalClustering` object
- ***cluster*** `numpy.ndarray` : The hierarchical cluster of the data
- ***docs*** `list` : A list of the original documents

---

**Returns** `Dendrogram`

## [Dendrogram](src/graphing/dendrogram.py)

A class to visualize a hierarchical clustering of webpages

```
src.graphing.dendrogram.Dendrogram(self, cluster, docs)
```

### Parameters

- ***self*** `Dendrogram` : The `Dendrogram` object
- ***cluster*** `np.ndarray` : The hierarchical cluster of the data
- ***docs*** `list` : A list of the original documents

### Methods

---

**create( *self* )**

Creates a dendrogram figure for a hierarchical/agglomerative cluster

**Parameters**

- ***self*** `Dendrogram` : The `Dendrogram` object

**Returns** `plotly.graph_objs.Figure` 

---

**create_lines( *self* )**

Creates the lines representing the relationships between nodes in a dendrogram

**Parameters**

- ***self*** `Dendrogram` : The `Dendrogram` object

**Returns** None

---

**create_nodes( *self* )**

Creates the nodes representing the documents in a dendrogram

**Parameters**

- ***self*** `Dendrogram` : The `Dendrogram` object

**Returns** None

---

**create_layout( *self* )**

Creates the layout of the dendrogram

**Parameters**

- ***self*** `Dendrogram` : The `Dendrogram` object

**Returns** None

---

# 💙 Contributors

**Blake McBride** (Team Captain) <br> blakepm2@illinois.edu <br><br>
**Kaushal Dadi** <br> kdadi2@illinois.edu <br><br>
**Rohan Parekh** <br> rohanjp2@illinois.edu <br><br>
**Megha Chada** <br> megharc2@illinois.edu <br><br>
**Michael Ma** <br> chiuyin2@illinois.edu<br>