# go-ahead

[![](https://godoc.org/github.com/alextanhongpin/typeahead?status.svg)](https://godoc.org/github.com/alextanhongpin/typeahead)

A text autocompleter with golang. The goal is to create a google-like
  autocomplete. Based on some research done, it seems like google is
  implementing it using radix/patricia tree. The implementation here is
  probably a slightly more naive version than what google has. 

Radix tree is more storage efficient than a trie (?). 

Another interesting implementation is the _typeahead_ by Facebook.

## Installation

```bash
$ go get github.com/alextanhongpin/typeahead
```

## TODO

- Create an actual server that can add new search suggestions. 
- Improve the scoring/ranking algorithm.
- Look into a better way to identify performance issue
- Perform testing with quickcheck
- Persist datastructure using gob encoding
- Load the complete words dataset 
- Add context and include auto-correct capabilities
- Find ways to stream new data to increment the count and effectiveness of the radix trie

## References

- http://dhruvbird.com/autocomplete.pdf
