## Example

### The request

    SELECT *
    WHERE {
        ?e    <http://dbpedia.org/ontology/releaseDate>     ?date   .
        ?e    <http://dbpedia.org/ontology/episodeNumber>   1       .
        ?e    <http://dbpedia.org/ontology/seasonNumber>    1
    }
    ORDER BY DESC(?date)

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
