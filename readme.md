node-pagerank cn
=============

A library for looking up the Google PageRank of any given web page.

Installation
------------

    npm install -g pagerank-cn

Usage
-----

    var PageRank = require('pagerank-cn');
    
    // It's a ReadibleStream
    new PageRank('http://www.phodal.com/').pipe(myCoolWriteableStream);

    // It's an event Emitter
    // It will emit one data event with either a number or null
    new PageRank('http://www.phodal.com/').on('data', console.log).on('error', console.error);
 
    // And it accepts callbacks
    // pageRank will either be a number or null
    new PageRank('http://www.phodal.com/', function(error, pageRank) {
        console.log(error, pageRank);
    });

Or, use it via commandline (must be installed with -g):


    pagerank http://example.com/
