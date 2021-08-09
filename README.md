# Letterboxd - Count films by director (updated)

A small utility script that, given an exported [Letterboxd](http://letterboxd.com) user data file, outputs a text file with directors grouped by the count of films directed by them that the user has watched:

```
15 films (1 director):
Krzysztof Kieślowski

10 films (1 director):
Lars von Trier

8 films (3 directors):
Wes Anderson
Stanley Kubrick
Sion Sono

(and so on, and so forth...)
```

The script gets the director(s) of a film by scraping its Letterboxd page. It stores (film, director) pairs in a cache file (``cache.csv`` by default) to avoid unnecessary requests.

## Usage
1. Export your user data from [Letterboxd settings page](https://letterboxd.com/settings/data/).
2. Run the script: ``python letterboxd_count_by_director.py path/to/downloaded_data_file.zip``.
3. See ``output.txt`` for results.
