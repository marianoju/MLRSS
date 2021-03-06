MLRSS
=====

Machine Learning RSS News Aggregator

MLRSS is an attempt at applying the K-means algorithm to RSS feeds to filter the most popular articles from thousands of links in an attempts to reduce my personal RSS reading time.

[MLRSS Demo (copy & paste-able asciinema rec)](https://asciinema.org/a/11252)

##Usage

Presently, the algorithm works with a bit of tweaking to the t (threshold) variable at [Line 136](opml_cluster_agg.py#L136) - depending on similarity of feeds this can be adjusted (0.65 has been my most sucessful) to reduce, or increase results.

Further, you can adjust the number of keywords generated by the algorithm, which also affects results 

- less keywords => fewer pairs, strict matching 
- more keywords => more pairs, loose matching

To affect number of keywords see [Line 97](opml_cluster_agg.py#L97)

To change sites being used for dataset see: agg_links.opml

If you export an OPML file from any handful of popular rss readers (feedly, newsblur, etc.) and rename your export opml file to agg_links.opml and place in the same directory as opml_cluster_agg.py, or change the filename in opml_cluster_agg.py you can run the application on your own custom selected links.

### Get

```bash
git clone https://github.com/ype/MLRSS.git
```

### Install

```bash
pip install -r requirements.txt
```

### Run

```bash
python opml_cluster_agg.py

```

*****
