# Projects for NTDS 2018

All projects comprise the creation of a network and its analysis.
For each network created, the goal is to analyze its structure or use it to get valuable information about the dataset.
Among the many possibilities, we expect the use of several of the following approaches/tools/techniques:

* graph connectivity and degree distributions, graph model (connected components, hubs, scale free, mean degree...),
* existence and characterization of communities,
* Analysis of data on the nodes (correlation between data and network structure),
* filtering of values on the nodes / label propagation,
* dynamic activity on the network.

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

## Voting pattern of US senators
By Michaël

The goal of this project is to analyze the voting pattern of US senators.
We will build a graph between senators.
The signals on the graph are (i) their political party (i.e., republican, democrat, free) and (ii) their voting activity (i.e., what they voted on a list of issues).

Useful resources:
* [Congress API](https://projects.propublica.org/api-docs/congress-api/)
* [Blog post on using the API](http://www.storybench.org/use-propublicas-congress-api-see-senators-stand-issues/)

**This project requires to call a web API to gather the data. Be prepared for the additional work incured.**

## Projects related to the Wikipedia dataset
By Benjamin

Wikipedia is an enormous source of information visited dayly by millions on users. We can understand more about the human behavior by looking at how it is build and how it is accessed. In the following projects you will investigate the Wikipedia structure and learn more about our use, as human, of the largest encyclopedia ever.

## Project Wikipedia 1. Automatic selection/classification of pages.

The project Kiwix aims at diffusing Wikipedia to places with a limited internet access. The idea is to select subsets of Wikipedia that can fit on USB sticks or other small devices with reduced storage capacity in order to be shared more easily. For example they edit a subset of Wikipedia focused on medicine, to be used by physicians in poor countries.
The goal of the project is to help selecting relevant articles when choosing a subset of Wikipedia pages on a particular topic. Pages, with their hyperlinks, can be seen as a network, connecting related or similar pages. We will use graph algorithms taught in the course to analyze the graph and gather relevant pages together. Label propagation and community detection will help to group and categorize pages.

Dataset:
Wikipedia dump https://en.wikipedia.org/wiki/Wikipedia:Database_download


## Project Wikipedia 2: Human visits on Wikipedia pages. 

From the Wikipedia network of pages and the number of visits per hour given by Wikimedia, we can get some insight on the visitor's behavior.
In this projet we will associate to each node of a graph a time series. The graph will be the one of Wikipedia pages and the time series will be built from the recorded number of visits per hour for each page. In particular, we want to see how the popularity of a page can influence the popularity of its neighbors. 
We want to answer questions such as: what do human do when reading an article? Do they just read one article or do they tend to click on links and reach neighbor pages? Which link do they select, the ones at the beginning of the article, in the introduction or elsewhere? 
The investigators will make use of signal processing on graphs such as the computation of the signal smoothness, graph clustering or changing the graph structure using the dynamic evolution given by the time series.

Due to the huge amount of data, we will look at fluctuation of popularity during a short period of time (one month) and on a restricted number of pages.

Dataset:

Wikipedia dump + Wikipedia data on the number of visits per pages

* https://en.wikipedia.org/wiki/Wikipedia:Database_download
* https://dumps.wikimedia.org/other/pagecounts-ez/

## Project Wikipedia 3: Wikipedia edit activity.

In this project we want to have a better understanding of the editors behavior and of the interactions between them. The first step is to create a graph from a dataset of Wikipedia edits. In each edit is recorded: the article title, the editor ID (It can be its IP address), and the details of the modifications. From this information, we can build a graph of editors, connected if they have contributed to the same pages (the connection strength could be proportional to the number of pages edited in common). We can also build a graph of modified pages, where two pages are linked if they have been modified by the same editor (at least once). 

Exploring the structure of these graphs can bring many valuable informations. Is the graph connected? does it have hubs? What is the mean degree of the nodes? Can we find communities? Do these communities contain pages with a particular topic? Can we detect Wikipedia bots by looking at the pages they edit?...

Dataset:

https://snap.stanford.edu/data/wiki-meta.html


## The /r/place dataset, collaborative behavior on the web.
By Benjamin

The goal of this project is the get a better understanding of the interactions that can occur online. We will analyze the data from the /r/place reddit experiment. In this experiment, users had access to a page where they could choose one pixel of the page and change its color. They were allowed to make such a modification once every 5min. Very quickly, structured drawings appeared on the page, showing a collaborative behavior in action (see links below).
To get some insight on the users, we will build a graph of users with connections related to their action. We will assume that the modification of two adjacent pixels in a short period of time is a kind of user interaction. We can strengthen this connection if the color of the modified pixels was the same. Does this graph have communities?

Dataset:

* https://www.kaggle.com/residentmario/reddit-rplace-history
* https://www.youtube.com/watch?v=XnRCZK3KjUY
* https://rolandr.github.io/


## Graph of news.
By Benjamin

From a list of news sites, we want to analyze how users view them and intentionally or unintentionally associate them together. We see news sites as nodes of a graph. From some social network data, we connect news if they appear together in the same feed or are referenced by the same user (depends on the social network dataset).

the Gdelt project (see links below) provide several datasets related to the news and the news coverage. One of them relate news events to a unique ID and report any publication about this event in the online news. A network of news sites can be made to get a better picture on how much they share the same information. News that report the same events would be linked in the network. The connection weights would increase as the number of shared news increases. Can we make some interesting and clean visualizations of the news sites landscape? Can we categorize them? Are there news sites that are more central? Do we get different networks if we take into account news related to particular topics? Can we combine additional info present in the data with the graph to get additional insights?

Dataset:

* https://blog.gdeltproject.org/the-datasets-of-gdelt-as-of-february-2016/
* https://blog.gdeltproject.org/gdelt-2-0-our-global-world-in-realtime/

and the "mention" csv file 

## Twitter Activity of Researchers in CS
by Ersi

The [dataset](https://github.com/l3s/twitter-researcher) used consists of the activity of 52678 Twitter users. Of those 170 are Twitter screen names of 98 Computer Science Conferences. These 170 Twitter accounts are set as seeds and more Twitter nodes have been collected if they are i) following a seed or ii) being followed by a seed or iii) have re-tweeted at seed's tweet. Out of the 52678 Twitter users the 9191 are verified to be researchers (they have been matched to a DBLP author profile). 23 features are given for each Twitter user, including for instance a boolean feature demonstrating if the bio description includes words that are usually being used by researchers. The students will have to chose a subset of the 52678 Twitter users by selecting one or more of the seed Twitter pages and the Twitter pages connected to them that belong in this dataset. For this they will have to use Tweepy. 

* milestone 1: potentially a bit heavy for this project because there will have to be some data collection (but still, not too hard)
* milestone 2: normally, no problem
* milestone 3: they can use the features provided to build a feature graph and cluster (maybe for instance more famous reserachers and more junior researchers?)
* milestone 4: If we need labels: for the 9191 nodes we know they are researchers and for the 43.383=52.768-9.191 researchers for sure-170 seeds-24 companies we have labels (but noisy-results of the classification in the [paper](http://delivery.acm.org/10.1145/2620000/2615676/p23-hadgu.pdf?ip=128.179.162.160&id=2615676&acc=ACTIVE%20SERVICE&key=FC66C24E42F07228%2E7E17DDD1CCA0F75B%2E4D4702B0C3E38B35%2E4D4702B0C3E38B35&__acm__=1536082760_ba13d3bb439d6413f7e95e096c7aff7c))

## Facebook URL shares
by Ersi

[dataset](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/EIAACS)
(not sure about how to get access yet)

## Co-authorship network
by Ersi

[dataset](https://perso.liris.cnrs.fr/marc.plantevit/doku/doku.php?id=data_sets)

## Kenyan households contact network
by Ersi

[dataset](http://www.sociopatterns.org/datasets/kenyan-households-contact-network/)

## Patent citation network
by Ersi

[dataset](http://snap.stanford.edu/data/cit-Patents.html)

## Drosophila medulla connectomics of fly 
by Ersi

[dataset](http://awesome.cs.jhu.edu/graph-services/download/)

## Yelp Dataset
by Eda (I will add the corresponding challenges later!)

https://www.yelp.com/dataset

## Micro-Video Dataset
by Eda

http://acmmm16.wixsite.com/mm16

## Spammer Detection on Social Network
by Eda

https://linqs-data.soe.ucsc.edu/public/social_spammer/

## Cora Citation Network
by Eda

https://relational.fit.cvut.cz/dataset/CORA

## Global Terrorism Database
by Eda

https://www.start.umd.edu/gtd/contact/
http://www.cs.umd.edu/~sen/lbc-proj/LBC.html



## Bitcoin OTC trust weighted signed network

By Rodrigo

http://snap.stanford.edu/data/soc-sign-bitcoin-otc.html



## California road network

By Rodrigo

http://snap.stanford.edu/data/roadNet-CA.html



## Reddit pizza requests

By Rodrigo

http://snap.stanford.edu/data/web-RedditPizzaRequests.html



## Protein-protein interaction network in yeast

By Rodrigo

http://vlado.fmf.uni-lj.si/pub/networks/data/bio/Yeast/Yeast.htm



## IMDb co-appearance in films

By Rodrigo

https://www.imdb.com/interfaces/



## Flight routes

By Rodrigo

https://openflights.org/data.html

