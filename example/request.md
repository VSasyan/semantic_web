## Example

### The request

Here is the text to enter in the form:

    SELECT *
    WHERE {
        ?e    <http://dbpedia.org/ontology/releaseDate>     ?date   .
        ?e    <http://dbpedia.org/ontology/episodeNumber>   1       .
        ?e    <http://dbpedia.org/ontology/seasonNumber>    1
    }
    ORDER BY DESC(?date)

You can acces the form here: http://dbpedia.org/snorql

You should [see this page](http://dbpedia.org/snorql/?query=SELECT+*%0D%0AWHERE+{%0D%0A++++%3Fe%09%3Chttp%3A%2F%2Fdbpedia.org%2Fontology%2FreleaseDate%3E%09%3Fdate%09.%0D%0A++++%3Fe%09%3Chttp%3A%2F%2Fdbpedia.org%2Fontology%2FepisodeNumber%3E%091%09.%0D%0A++++%3Fe%09%3Chttp%3A%2F%2Fdbpedia.org%2Fontology%2FseasonNumber%3E%091%0D%0A}%0D%0AORDER+BY+DESC%28%3Fdate%29%0D%0A).

### The response

See the all the reponses : [responses.json](responses.json)

	{
	  "head": {
		"link": [],
		"vars": [
		  "e",
		  "date"
		]
	  },
	  "results": {
		"distinct": false,
		"ordered": true,
		"bindings": [
		  {
			"e": {
			  "type": "uri",
			  "value": "http://dbpedia.org/resource/Now_is_Not_the_End"
			},
			"date": {
			  "type": "typed-literal",
			  "datatype": "http://www.w3.org/2001/XMLSchema#date",
			  "value": "2015-01-06"
			}
		  },
		  [...]
		  {
			"e": {
			  "type": "uri",
			  "value": "http://dbpedia.org/resource/Hot_Snow_(The_Avengers)"
			},
			"date": {
			  "type": "typed-literal",
			  "datatype": "http://www.w3.org/2001/XMLSchema#date",
			  "value": "1961-01-07"
			}
		  },
		  {
			"e": {
			  "type": "uri",
			  "value": "http://dbpedia.org/resource/Where_Is_Everybody%3F"
			},
			"date": {
			  "type": "typed-literal",
			  "datatype": "http://www.w3.org/2001/XMLSchema#date",
			  "value": "1959-10-02"
			}
		  },
		  {
			"e": {
			  "type": "uri",
			  "value": "http://dbpedia.org/resource/Huckleberry_Hound_Meets_Wee_Willie"
			},
			"date": {
			  "type": "typed-literal",
			  "datatype": "http://www.w3.org/2001/XMLSchema#date",
			  "value": "1958-10-02"
			}
		  }
		]
	  }
	}
