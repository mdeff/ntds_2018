# Projects for NTDS'18

All projects comprise the creation of a network and its analysis.
For each network created, the goal is to analyze its structure or use it to get valuable information about the dataset.
Among the many possibilities, we expect the use of several of the following approaches/tools/techniques:

* graph connectivity and degree distributions, graph model (connected components, hubs, scale free, mean degree...),
* existence and characterization of communities,
* Analysis of data on the nodes (correlation between data and network structure),
* filtering of values on the nodes / label propagation,
* dynamic activity on the network.


For all projects, some degree of pre-processing is needed before obtaining usable data.
That is inherent to the work of a data scientist, and will mostly following steps

1. **Data acquisition.**
   Raw data may need to be (i) collected via a web API, (ii) collected by scraping a website, or (iii) already collected and packaged (for example in a CSV file).
2. **Data importation.**
   Raw data needs to be imported in a pandas DataFrame, where rows will be nodes of the network, and columns will be features (or characteristics or attributes) of those nodes.
3. **Data cleaning.**
   This step varies a lot from projects to projects.
   In the context of the course, it will mostly consist in reducing the size of the network so that it can be processed in a reasonable amount of time.
   The less packaged the raw data, the more cleaning will be necessary.
4. **Network creation.**
   The network structure may either be (i) given to you as an adjacency matrix, (ii) given to you as an edge list, or (iii) inferred from raw data.

While those steps are necessary for every project, the amount of pre-processing will however vary.
If the project requires raw data to be collected or the network to be created, that will be indicated in the project description.
So if you're a beginner and don't feel confident, choose a project which requires little pre-processing.
If you feel confident, be adventurous!
Keep in mind that the amount of work generally trades with flexibility for the second part of the semester.
Well packaged data usually serve a single task and may restrict your creativity.

## Free Music Archive
By Michaël

The [Free Music Archive](http://freemusicarchive.org/) is a free and open library directed by [WFMU](https://wfmu.org/), the longest-running freeform radio station in the United States.
Inspired by [Creative Commons](https://creativecommons.org/) and the open-source software movement, the FMA provides a platform for curators, artists, and listeners to harness the potential of music sharing.
The website provides a large catalog of artists and tracks, hand-picked by established audio curators. Each track is legally free to download as artists decided to release their works under permissive licenses.

The goal of this project is to analyze the content and interactions between the many types of users of an open community.
Relations can be studied in the form of similarity graphs between tracks.
The similarity can at first be established from audio features only.
Motivated students will explore other sources of information, at the level of the tracks, albums, or artists.
Relations between artists or even users (that requires scraping the website) are also feasible.

|          | Description                                | Amount |
| -------- | ------------------------------------------ | ------:|
| nodes    | audio tracks                               | 25'000 |
| edges    | similarity between tracks                  |    N/A |
| features | audio features pre-extracted from waveform |    518 |
| labels   | musical genre (e.g., Rock, Pop)            |     16 |

* **Data acquisition**: already collected and packaged
* **Network creation**: needs to be built from features

## Voting pattern of US senators
By Michaël

The goal of this project is to analyze the voting pattern of US senators.
We will build a graph between senators.
The signals on the graph are (i) their political party (i.e., republican, democrat, free) and (ii) their voting activity (i.e., what they voted on a list of issues).

We propose to first build a graph from the votes, i.e., measure the distance between voting vectors.
Going further, similarity might be measured from the other features, such as bill sponsoring or committee membership.

Useful resources:
* [ProPublica Congress API](https://projects.propublica.org/api-docs/congress-api/)
* [Blog post on using the API](http://www.storybench.org/use-propublicas-congress-api-see-senators-stand-issues/)

|          | Description                                              | Amount |
| -------- | -------------------------------------------------------- | ------:|
| nodes    | US senators                                              |   ~100 |
| edges    | similarity between senators                              |    N/A |
| features | votes, bill sponsoring, committee membership, statements |    N/A |
| labels   | political party (democrat, republican, independent)      |      3 |

* **Data acquisition**: need to be collected from a web API
* **Network creation**: needs to be built from features

## Wikipedia
By Benjamin

**TODO Benjamin**: merge and rephrase according to the unique wikipedia project.

Wikipedia is an enormous source of information visited dayly by millions on users. We can understand more about the human behavior by looking at how it is build and how it is accessed. In the following projects you will investigate the Wikipedia structure and learn more about our use, as human, of the largest encyclopedia ever.

Automatic selection/classification of pages.

The project Kiwix aims at diffusing Wikipedia to places with a limited internet access. The idea is to select subsets of Wikipedia that can fit on USB sticks or other small devices with reduced storage capacity in order to be shared more easily. For example they edit a subset of Wikipedia focused on medicine, to be used by physicians in poor countries.
The goal of the project is to help selecting relevant articles when choosing a subset of Wikipedia pages on a particular topic. Pages, with their hyperlinks, can be seen as a network, connecting related or similar pages. We will use graph algorithms taught in the course to analyze the graph and gather relevant pages together. Label propagation and community detection will help to group and categorize pages.

Dataset:
Wikipedia dump https://en.wikipedia.org/wiki/Wikipedia:Database_download

Human visits on Wikipedia pages.

From the Wikipedia network of pages and the number of visits per hour given by Wikimedia, we can get some insight on the visitor's behavior.
In this projet we will associate to each node of a graph a time series. The graph will be the one of Wikipedia pages and the time series will be built from the recorded number of visits per hour for each page. In particular, we want to see how the popularity of a page can influence the popularity of its neighbors.
We want to answer questions such as: what do human do when reading an article? Do they just read one article or do they tend to click on links and reach neighbor pages? Which link do they select, the ones at the beginning of the article, in the introduction or elsewhere?
The investigators will make use of signal processing on graphs such as the computation of the signal smoothness, graph clustering or changing the graph structure using the dynamic evolution given by the time series.

Due to the huge amount of data, we will look at fluctuation of popularity during a short period of time (one month) and on a restricted number of pages.

Dataset:

Wikipedia dump + Wikipedia data on the number of visits per pages

* https://en.wikipedia.org/wiki/Wikipedia:Database_download
* https://dumps.wikimedia.org/other/pagecounts-ez/

## The /r/place dataset, collaborative behavior on the web
By Benjamin

The goal of this project is to get a better understanding of the interactions that can occur online. We will analyze the data from the /r/place reddit experiment. In this experiment, users had access to a page where they could choose one pixel of the page and change its color. They were allowed to make such a modification once every 5min. Very quickly, structured drawings appeared on the page, showing a collaborative behavior in action (see links below).
To get some insight on the users, we will build a graph of users with connections related to their action. We will assume that the modification of two adjacent pixels in a short period of time is a kind of user interaction. We can strengthen this connection if the color of the modified pixels was the same. Does this graph have communities? What can we say about human interactions from this dataset? The dataset is large (16 million rows) how can we handle it?

Dataset:

* https://www.kaggle.com/residentmario/reddit-rplace-history
* https://www.youtube.com/watch?v=XnRCZK3KjUY
* https://rolandr.github.io/

A first tutorial explaining how to extract the data is given here:

https://www.kaggle.com/residentmario/reconstructing-r-place-images

## Graph of news
By Benjamin

From a list of news sites, we want to analyze how users view them and intentionally or unintentionally associate them together. We see news sites as nodes of a graph. From some social network data, we connect news if they appear together in the same feed or are referenced by the same user (depends on the social network dataset).

the Gdelt project (see links below) provide several datasets related to the news and the news coverage. One of them relate news events to a unique ID and report any publication about this event in the online news. A network of news sites can be made to get a better picture on how much they share the same information. News that report the same events would be linked in the network. The connection weights would increase as the number of shared news increases. Can we make some interesting and clean visualizations of the news sites landscape? Can we categorize them? Are there news sites that are more central? Do we get different networks if we take into account news related to particular topics? Can we combine additional info present in the data with the graph to get additional insights?

Dataset:

* https://blog.gdeltproject.org/the-datasets-of-gdelt-as-of-february-2016/
* https://blog.gdeltproject.org/gdelt-2-0-our-global-world-in-realtime/

and the "mention" csv file
Some info on the data (description of the columns) can be found here:

https://www.kaggle.com/gdelt/gdelt

## Twitter Activity of Researchers in CS
by Ersi

The [dataset](https://github.com/l3s/twitter-researcher) used consists of the activity of 52678 Twitter users. Of those 170 are Twitter screen names of 98 Computer Science Conferences. These 170 Twitter accounts are set as seeds and more Twitter nodes have been collected if they are i) following a seed or ii) being followed by a seed or iii) have re-tweeted at seed's tweet. Out of the 52678 Twitter users the 9191 are verified to be researchers (they have been matched to a DBLP author profile). 23 features are given for each Twitter user, including for instance a boolean feature demonstrating if the bio description includes words that are usually being used by researchers. The students will have to chose a subset of the 52678 Twitter users by selecting one or more of the seed Twitter pages and the Twitter pages connected to them that belong in this dataset. For this they will have to use Tweepy.

* milestone 1: potentially a bit heavy for this project because there will have to be some data collection (but still, not too hard)Here they should create a connections graph, because they won't know yet how to create a feature graph. They can usee last year's assignment 1 for help. If they chose to build a feature graph no API needed.
* milestone 2: normally, no problem
* milestone 3: they can use the features provided to build a feature graph and cluster (maybe for instance more famous reserachers and more junior researchers?)
* milestone 4: If we need labels: for the 9191 nodes we know they are researchers and for the 43.383=52.768-9.191 researchers for sure-170 seeds-24 companies we have labels (but noisy-results of the classification in the [paper](http://delivery.acm.org/10.1145/2620000/2615676/p23-hadgu.pdf?ip=128.179.162.160&id=2615676&acc=ACTIVE%20SERVICE&key=FC66C24E42F07228%2E7E17DDD1CCA0F75B%2E4D4702B0C3E38B35%2E4D4702B0C3E38B35&__acm__=1536082760_ba13d3bb439d6413f7e95e096c7aff7c))


remark 1: they should make sure that the graph is undirected?
remark 2: a bit hard project because they will have to do some data collection. Howver more interesting thing to look into. Could be interesting for students who want to expand a lot in the extra stuff part.

## Co-authorship network
by Ersi

The data set is a co-authorship graph built from the DBLP digital library. Each vertex represents an author that has published at least one paper in one of the major conferences and journals of the Data Mining and Database communities between January 1990 and February 2011. Each edge links two authors who co-authored at least one paper (no matter the conference or journal). The vertex properties are the number of publications in each of the 29 selected conferences or journals and we also consider 9 topological properties (Degree Cent., Closeness Cent., Betweenness Cent., EigenVector Cent., PageRank, Clustering Coeff., Size of Max. Quasi-Clique, Number of Quasi-Cliques, Size of Community).

* milestone 1: straightforward: the graph is already given
* milestone 2: ok
* milestone 3: # vertices=42.252, #edges=210.320. should be ok for decomposition, otherwise we can sparsify. There are indications of communities (look at topological attributes of vertices)
* milestone 4: maybe use as signal the number of publication at a conference??

Remark: The creator of this dataset has given me the data and I can use them form the project. However, they should not be released publicly throught Github, but through a private channel.
[dataset](https://perso.liris.cnrs.fr/marc.plantevit/doku/doku.php?id=data_sets)

## Spammer Detection on Social Network
by Eda

https://linqs-data.soe.ucsc.edu/public/social_spammer/

The dataset contains 5.6 million users, which are described by 4 features; "user id", "gender", "age group", "spammer label". There are 7 different type of relations between the users indicating the action between them such as profile view, message, poke, etc., which may lead to 7 different directed graph. In total, there are 858 million link between the users. The original task associated with this dataset is to identify the spammers based on their features and links in the network.

Since this dataset is very big, it requires subsampling even during the loading the data and cleaning the network accordingly.

## Cora Citation Network
by Eda

https://relational.fit.cvut.cz/dataset/CORA

CORA citation network is a graph containing 2708 vertices representing papers and 5429 edges representing citations. Each paper is described by a 1433-dimensional bag-of-words feature vector and belongs to seven classes (the field of the study). The feature vectors contain 0/1 values indicating the absence/presence of the corresponding word from the dictionary consisting of 1433 unique words. The asscoiated task with this dataset is usually label prediction.

## Terrorist Relations
by Eda

http://www.cs.umd.edu/~sen/lbc-proj/LBC.html

This dataset is designed for the classification of the relationships between the terrorists. The dataset contains 851 relations (aka; nodes of the graph). Each node is assigned to least one label (multiple labeling is also possible) among 4 labels; "Colleague", "Congregate", "Contact", "Family", and is described with 0/1 valued feature vector indicating absence/presence of the attributes, which are 1224 in total. There are 8592 edges on the graph, which connects the nodes involving the same terrorist group.

## Terrorist Attacks
by Eda

http://www.cs.umd.edu/~sen/lbc-proj/LBC.html

This dataset consists of 1293 terrorist attacks (nodes), each of which is assigned to one of 6 labels indicating the type of the attack. Each attack is described by a 0/1-valued vector of attributes whose entries indicate the absence/presence of a feature. There are a total of 106 distinct features. The files in the dataset can be used to create two distinct graphs. In one of them edges of the graph connect the colocated attacks. On the other one, edges connect co-located terrorist attacks performed by the same terrorist organization.

## Protein-protein interaction network in yeast
By Rodrigo

http://vlado.fmf.uni-lj.si/pub/networks/data/bio/Yeast/Yeast.htm

This dataset contains the interation network (2361 vertices and 7182 edges) of proteins in budding yeast.

- The network is given as an edge list (X interacts Y)
- The proteins are partitioned into 13 different clusters. The indicator function of each cluster could serve as the signal on the graph.

|          | Description                    | Amount |
| -------- | ------------------------------ | -----: |
| nodes    | cast/crew                      |   2361 |
| edges    | co-apearance in movies/TV/etc. |   7182 |
| features | N/A                            |    N/A |
| labels   | cluster assignment             |     13 |

## IMDb films and crew networks

By Rodrigo

https://www.imdb.com/interfaces/

The IMDd datasets contain information such as crew, rating, and genre for every entertainment product in its database.

- A possible approach could be to construct a social network of cast/crew, where the edges are weighted according to co-appearance (e.g. actor_1 is stringly connected to actor_2 if they have appeared in a lot of movies together).
  - After the graph is constructed, network properties can be analyzed as usual.
  - Then, a possible signal over this graph should be the aggregate ratings of movies each person has participated in (e.g. actor_1's signal value would be the average of the ratings of every movie he/she took part in).
  - We could then subsample those ratings and see if the co-apearance information is a good predictor of rating information.
  - The number of nodes in this graph is of the order of **millions**, so a smaller subset should be constructed.

|          | Description                            |         Amount |
| -------- | -------------------------------------- | -------------: |
| nodes    | cast/crew                              |       Millions |
| edges    | co-apearance in movies/TV/etc.         | O(10) per node |
| features | average rating of movies taken part in |              1 |
| labels   | movie genre                            |        unknown |

- Another approach could be to create a movie-network, in which movies are strongly connected if they share a lot of crew/cast members (or some other similarity measure combining this and whether they have similar genres, running times, and release years).
  - Again, once the graph is constructed, network properties can be analyzed as usual.
  - The signal on this graph could be either the movie ratings, or the genre labels.
  - The number of nodes in this graph is of the order of **millions**, so a smaller subset should be constructed (maybe restrict to feature films of only one genre?).

|          | Description                                           |         Amount |
| -------- | ----------------------------------------------------- | -------------: |
| nodes    | movies                                                |       Millions |
| edges    | count of common cast/crew + other feature similarity. | O(10) per node |
| features | average rating                                        |              1 |
| labels   | movie genre                                           |        unknown |

## Flight routes
By Rodrigo

https://openflights.org/data.html#route

This OpenFlights/Airline Route Mapper Route Database contains **67663** routes (EDGES) between **3321** airports (NODES) on **548** airlines spanning the globe dataset contains information on source and destination of flights throuout the globe.

- The graph should be fairly easy to construct, given that each route has a source and destination airport, which gives essentially an edge list.
- Visualization of the graph embedded on the globe could be assisted by the supplemented data in https://openflights.org/data.html, which contains, among others, information on latitute/longitude of each airport.
- The graph is given, so network analysis should be straighforward.
- The students could also see how well the laplacian eigenmaps explains the geographical embedding of the graph on the world map.
- A possible signal on the graph could be the (average) number of stops of flights leaving each airport. If we subsample this signal, can we reconstruct it via Tikhonov regularization?

|          | Description                                 | Amount |
| -------- | ------------------------------------------- | -----: |
| nodes    | airports                                    |   3321 |
| edges    | count of flights connecting airports        |  67663 |
| features | average number of stops of outbound flights |      1 |
| labels   | N/A                                         |    N/A |

## Uber dataset

by Hermina

Data on over 4.5 million Uber pickups in New York City from April to September 2014, and 14.3 million more Uber pickups from January to June 2015. Needs preprocessing to construct a graph, suggested to do so as in: https://arxiv.org/pdf/1611.01456.pdf

Data:
https://github.com/fivethirtyeight/uber-tlc-foil-response

## Crime involvment dataset
by Hermina

Data is given in terms of a bipartite network, which contains persons who appeared in at least one crime case as either a suspect, a victim, a witness or both a suspect and victim at the same time. A left node represents a person and a right node represents a crime. An edge between two nodes shows that the left node was involved in the crime represented by the right node.
To construct a graph, one should connect people that are involved in the same crime. The signal will be the number of crimes a person is involved in.

Data:
http://konect.uni-koblenz.de/networks/moreno_crime

## Amphoriskos point cloud dataset
by Hermina

Coloured pointcloud dataset. The graph can be constructed as a k-nn graph from coordinates, while signals are given in terms of colour. The original content is given in [1]. Various pre-processing steps took place, namely, Poisson Surface reconstruction, sampling of the reconstructed mesh to obtain point cloud vertices, and subsampling of the latter, in order to result in sets of points that correspond to smooth underlying surfaces.

[1] https://sketchfab.com/models/85cba491e0a84ce58dc4a75715073ad2
