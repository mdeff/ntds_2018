# Projects for NTDS 2018

All projects comprise the creation of a network and its analysis.
For each network created, the goal is to analyze its structure or use it to get valuable information about the dataset. Among the many possibilities, we expect the use of several of the following approaches/tools/techniques:

* graph connectivity and degree distributions, graph model (connected components, hubs, scale free, mean degree...),
* existence and characterization of communities,
* Analysis of data on the nodes (correlation between data and network structure),
* filtering of values on the nodes / label propagation,
* dynamic activity on the network.



## Project title
By Michaël Defferrard

Description

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

There was an [article](http://blogs.lse.ac.uk/impactofsocialsciences/2017/10/03/new-media-familiar-dynamics-academic-hierarchies-influence-academics-following-behaviour-on-twitter/) about what determines the behaviour of academics on social media (in particular Twitter). The [dataset](https://github.com/l3s/twitter-researcher) used consists of the activity of 1,481 Twitter users. It includes users with at least one publication in the field of computer science who have followed at least one computer science conference on Twitter. 570 professors and 911 PhD students can be identified by using self-descriptions from their Twitter profiles.

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

