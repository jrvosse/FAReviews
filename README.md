To run the experiment, first:

Install required Python 3 packages:

```bash
pip3 install -r requirements.txt
```


Download data (todo: download nltk stopwords)

```bash
wget -c "https://s3.amazonaws.com/dl4j-distribution/GoogleNews-vectors-negative300.bin.gz"
wget -c "http://deepyeti.ucsd.edu/jianmo/amazon/categoryFilesSmall/AMAZON_FASHION_5.json.gz"
python -m spacy download en_core_web_md
```

Perform feature extraction (this creates FAReviews\_reviews.csv and FAReviews\_prods.pkl)
```bash
python3 compute_scores.py 
```

Create the matrix with distance metrics: (FAReviews\_5\_prods\_mc.pkl)
```bash
python3 create_graph.py 
```
