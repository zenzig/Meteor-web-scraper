WebScraper
==========

A library with tools used to scrape data from the internet

How to fetch the HTML of a url:

    var webpage   = Scraper.create('www.example.com');
    var pageTitle = webpage.title(),
    var metaData  = webpage.getMeta({
        fixRelativePaths: true,
        filterSelector: '[name="keywords"], [name="description"], [property^="og:"], [property^="twitter:"]',
        prunePrefixes: ['twitter', 'og']
    });
    
    // Will return an array like [{property: 'image', 'content':'/lol.jpg'}]

