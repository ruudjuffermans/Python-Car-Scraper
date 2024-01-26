# Python-Car-Scraper
This is a Scrapy project to scrape cars from http://marktplaats.nl


## Extracted data

This project extracts adds from marktplaats.
The extracted data looks like this sample:

    {
        'author': 'Douglas Adams',
        'text': '“I may not have gone where I intended to go, but I think I ...”',
        'tags': ['life', 'navigation']
    }


## Spiders

This project contains two spiders and you can list them using the `list`
command:

    $ scrapy list
    toscrape-css
    toscrape-xpath

Both spiders extract the same data from the same website, but `toscrape-css`
employs CSS selectors, while `toscrape-xpath` employs XPath expressions.

You can learn more about the spiders by going through the
[Scrapy Tutorial](http://doc.scrapy.org/en/latest/intro/tutorial.html).


## Running the spiders

You can run a spider using the `scrapy crawl` command, such as:

    $ scrapy crawl toscrape-css

If you want to save the scraped data to a file, you can pass the `-o` option:
    
    $ scrapy crawl toscrape-css -o quotes.json