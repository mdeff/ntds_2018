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

## List of proposed projects

* [Free Music Archive](#free-music-archive)
* [US Senators](#us-senators)
* [Wikipedia](#wikipedia)
* [Researchers on Twitter](#researchers-on-twitter)
* [Scientific co-Authorship](#scientific-co-authorship)
* [Spammers on Social Networks](#spammers-on-social-networks)
* [Citation Network](#citation-network)
* [Terrorist Attacks and Relations](#terrorist-attacks-and-relations)
* [IMDb Films and Crews](#imdb-films-and-crews)
* [Flight Routes](#flight-routes)

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

## US Senators
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

Wikipedia is an enormous source of information visited dayly by millions on users. We can understand more about the human behavior by looking at how it is build and how it is accessed. In this project you will investigate the Wikipedia structure and learn more about our use, as human, of the largest encyclopedia ever.
Pages, with their hyperlinks, can be seen as a network, connecting related or similar pages. We will use graph algorithms taught in the course to analyze the graph and gather relevant pages together. Label propagation and community detection will help to group and categorize pages.
In a second step, the number of visits per page (for ne month) will be added to analyze the popularity of the articles and check if it influences the popularity of the neighbor pages. The project is open and students can also have access to the evolution in time of the number of visits (visits per hour or per day). Depending on the students progress and motivation, the time series could be analyzed to get interesting information on Wikipedia. 

Due to the huge amount of data, we will look at a reduced number of pages.

Dataset:

Wikipedia dump + Wikipedia data on the number of visits per pages

* https://en.wikipedia.org/wiki/Wikipedia:Database_download
* https://dumps.wikimedia.org/other/pagecounts-ez/

A reduced dataset, extracted from the links above, will be provided to the students. 


|          | Description                                | Amount |
| -------- | ------------------------------------------ | ------:|
| nodes    | Wikipedia pages                            | ~10000 |
| edges    | hyperlinks                                 |    N/A |
| features | nb of visits for one month                 |      1 |
| labels   | category                                   |    3-5 |

## Researchers on Twitter
by Ersi

The goal of this project is to analyze the interactions of a sub-network of Twitter. The Twitter accounts in this project are Computer Science reasearchers or other accounts "related" to Computer Science.
The [dataset](https://github.com/l3s/twitter-researcher) used consists of the activity of 52678 Twitter users. Of those 170 are Twitter screen names of 98 Computer Science Conferences. These 170 Twitter accounts are set as seeds and more Twitter nodes have been collected if they are i) following a seed or ii) being followed by a seed or iii) have re-tweeted a seed's tweet. Out of the 52678 Twitter users the 9191 are verified to be researchers (they have been matched to a DBLP author profile). 22 features are given for each Twitter user, including for instance a boolean feature demonstrating if the bio description includes words that are usually being used to describe researchers. You can find a detailed description of the data in [this paper](https://dl.acm.org/citation.cfm?doid=2615569.2615676)


|          | Description                                | Amount |
| -------- | ------------------------------------------ | ------:|
| nodes    | Twitter accounts                           | 52,678 |
| edges    | similarity between Twitter accounts or     |        |
|          |  connections between Twitters accounts     |    N/A |
| features | numerical and boolean fetures describing   |        |
|          |  the Twitter profiles                      |     22 |
| labels   | reseracher or non-researcher               |        |
|          |  (beware:noisy labels)                     |      2 |

* **Data acquisition**: already collected and packaged (load tsv files). Some data cleaning will be needed.
* **Network creation**: If you chose to create a similarity graph between the Twitter users, it needs to be built from features. If you chose to build a graph with the connections between users, you must collect information using the Twitter API (Tweepy). As this can be time consuming, we recommend to build a feature graph for the milestones and to explore the connections graph at the last part of the course. Keep in mind that you might need to build different feature graphs for the different milestones. Alo, keep in mind that the labels for this project are noisy. They are the results of the classification of [the paper](https://dl.acm.org/citation.cfm?doid=2615569.2615676) mentioned before.

## Scientific co-Authorship
by Ersi

This project aims to explore the co-authorship behaviour of scientific authors.
The [dataset](https://perso.liris.cnrs.fr/marc.plantevit/doku/doku.php?id=data_sets) is a co-authorship graph built from the DBLP digital library. Each vertex represents an author that has published at least one paper in one of the major conferences and journals of the Data Mining and Database communities between January 1990 and February 2011. Each edge links two authors who co-authored at least one paper (no matter the conference or journal). The vertex properties are the number of publications in each of the 29 selected conferences or journals and 9 topological properties (Degree Cent., Closeness Cent., Betweenness Cent., EigenVector Cent., PageRank, Clustering Coeff., Size of Max. Quasi-Clique, Number of Quasi-Cliques, Size of Community).

|          | Description                                 |    Amount  |
| -------- | ------------------------------------------  |     ------:|
| nodes    | authors                                     |     42,252 |
| edges    | number of co-authorships in published papers|    210,320 |
| features | number of prublications in conferences and  |            |
|          |    topological features                     |         38 |
| labels   |                                             |        N/A |

* **Data acquisition**: already collected and packaged (load txt files)
* **Network creation**: The connections between the nodes are already provided.

Remark 1: There are no labels given for the nodes in this dataset. You can chose as your labels two subsets of the conferences (e.g. KDD and AAAI)

Remark 2: The creator of this dataset has agreed to provide the data for this project. However, they will be given to you through a private channel and you should not re-distribute it.

## Spammers on Social Networks
by Eda

The dataset contains 5.6 million users, which are described by 4 features; "user id", "gender", "age group", "spammer label". There are 7 different type of relations between the users indicating the action between them such as profile view, message, poke, etc., which may lead to 7 different directed graph. In total, there are 858 million link between the users. The original task associated with this dataset is to identify the spammers based on their features and links in the network.

Since this dataset is very big, it requires subsampling even during the loading the data and cleaning the network accordingly.

Resources:
* <https://linqs.soe.ucsc.edu/node/236>
* <https://linqs-data.soe.ucsc.edu/public/social_spammer>
* Paper: <http://www.cs.umd.edu/~shobeir/papers/fakhraei_kdd_2015.pdf>
* Code: <https://github.com/shobeir/fakhraei_kdd2015>
* Data: <https://linqs-data.soe.ucsc.edu/public/social_spammer/usersdata.csv.gz>, <https://linqs-data.soe.ucsc.edu/public/social_spammer/relations.csv.gz>

|          | Description                                                   |      Amount |
| -------- | ------------------------------------------------------------- | -----------:|
| nodes    | users of tagged.com                                           |   5,607,447 |
| edges    | action between users: includes a timestamp and one of 7 types | 858,247,099 |
| features | sex, timePassedValidation, ageGroup                           |           3 |
| labels   | spammer or not spammer                                        |           2 |

* **Data acquisition**: already collected and packaged
* **Requires down-sampling**: yes
* **Network creation**: network is given as a list of edges

## Citation Network
by Eda

CORA citation network is a graph containing 2708 vertices representing papers and 5429 edges representing citations. Each paper is described by a 1433-dimensional bag-of-words feature vector and belongs to seven classes (the field of the study). The feature vectors contain 0/1 values indicating the absence/presence of the corresponding word from the dictionary consisting of 1433 unique words. The asscoiated task with this dataset is usually label prediction.

Resources:
* <https://linqs.soe.ucsc.edu/node/236>
* <https://relational.fit.cvut.cz/dataset/CORA>
* Paper: <http://www.aaai.org/Papers/ICML/2003/ICML03-066.pdf>
* Data: <https://linqs-data.soe.ucsc.edu/public/lbc/cora.tgz>

|          | Description                                     | Amount |
| -------- | ------------------------------------------------| ------:|
| nodes    | scientific publications                         |  2,708 |
| edges    | a paper cites another paper                     |  5,429 |
| features | vector indicating the absence/presence of words |  1,433 |
| labels   | scientific field                                |      7 |

* **Data acquisition**: already collected and packaged
* **Requires down-sampling**: no
* **Network creation**: network is given as a list of edges

## Terrorist Attacks and Relations
by Eda

The first dataset consists of 1293 terrorist attacks (nodes), each of which is assigned to one of 6 labels indicating the type of the attack. Each attack is described by a 0/1-valued vector of attributes whose entries indicate the absence/presence of a feature. There are a total of 106 distinct features. The files in the dataset can be used to create two distinct graphs. In one of them edges of the graph connect the colocated attacks. On the other one, edges connect co-located terrorist attacks performed by the same terrorist organization.

The second dataset is designed for the classification of the relationships between the terrorists. The dataset contains 851 relations (aka; nodes of the graph). Each node is assigned to least one label (multiple labeling is also possible) among 4 labels; "Colleague", "Congregate", "Contact", "Family", and is described with 0/1 valued feature vector indicating absence/presence of the attributes, which are 1224 in total. There are 8592 edges on the graph, which connects the nodes involving the same terrorist group.
As the goal is the classification of links, we will here build the [line graph](https://en.wikipedia.org/wiki/Line_graph) of the social network between terrorists.
That is, instead of having terrorists as nodes and relationships between them as edges, relationships will be nodes and terrorists will be edges.

Resources:
* <https://linqs.soe.ucsc.edu/node/236>
* <http://www.cs.umd.edu/~sen/lbc-proj/LBC.html>
* Paper: <https://pdfs.semanticscholar.org/c047/f91ece3e9ec74bf42b8f69f375e27498a54a.pdf>
* Data: <https://linqs-data.soe.ucsc.edu/public/lbc/TerrorAttack.tgz>
* Data: <https://linqs-data.soe.ucsc.edu/public/lbc/TerroristRel.tgz>

|          | Description                                                                  | Amount |
| -------- | ---------------------------------------------------------------------------- | ------:|
| nodes    | relationships                                                                |    851 |
| edges    | terrorists                                                                   |  8,592 |
| features | 0-1 vector of attribute values                                               |  1,224 |
| labels   | type of relationship (non exclusive): colleague, congregate, contact, family |      4 |

|          | Description                                                     | Amount |
| -------- | --------------------------------------------------------------- | ------:|
| nodes    | terrorist attacks                                               |  1,293 |
| edges    | connect co-located attacks                                      |  3,172 |
| features | 0-1 vector of attribute values                                  |    106 |
| labels   | kind of attack: arson, bombing, kidnapping, weapon, nbcr, other |      6 |

* **Data acquisition**: already collected and packaged
* **Requires down-sampling**: no
* **Network creation**: network is given as a list of edges

## IMDb Films and Crews

By Rodrigo

[2018-09-13 Update] It is also possible to use the dataset here https://www.kaggle.com/tmdb/tmdb-movie-metadata/home, which is already subsampled from IMDb.

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

## Flight Routes
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
