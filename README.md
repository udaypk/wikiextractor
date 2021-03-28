# wikiextractor
Modified wikiextractor package to extract Wikipedia data filtered on Category


This package can be used to extract wikitext from Wikipedia xml dumps https://dumps.wikimedia.org/wikidatawiki/latest/

Every Wikipedia page is associated with a set of predefined categories. 
This package gives you the ability to extract specific category pages instead of the whole wikipedia data.

#Usage
Git clone and run the following command from one level above wikiextractor folder

	python -m wikiextractor.WikiExtractor <Input xml> -o <Output folder> -ns <Category name>

Example:
For extracting all pages related to Category Cricket https://en.wikipedia.org/wiki/Category:Cricket

	python -m wikiextractor.WikiExtractor enwiki-latest-pages-articles-multistream.xml.bz2 -o out_cricket -ns "Cricket"

For extracting all pages related to Category Team sports https://en.wikipedia.org/wiki/Category:Team_sports

	python -m wikiextractor.WikiExtractor enwiki-latest-pages-articles-multistream.xml.bz2 -o out_team_sports -ns "Team sports"
	
For extracting all pages related to both categories Team sports and Cricket  

	python -m wikiextractor.WikiExtractor enwiki-latest-pages-articles-multistream.xml.bz2 -o out_both -ns "Cricket,Team sports"	
