# Templated graphviz

## Requirements
* jq,dot,j2 needs to be installed
  * `brew install graphviz jq`
  * `pip2.7 install j2cli`

## Usage
* `./compile` 
* `./compile json_data/nodes_1.json` 

## Example

### json input
```
...
  "nodes":[
    {
      "id":"node1",
      "name": "label for node 1",
      "bgcolor":"blue"
    },
    {
      "id":"node2",
      "style":"note"
    },
...
    {
      "id":"node6"
    }
  ],
  "edges": [
    {
      "nodes":["node1","node2"]
    },
...
    {
      "nodes":["node5","node6"],
      "attributes":"color=green;constraint=false;dir=back;xlabel=\"edge label\";"
    },
    {
      "nodes":["node1","node6"],
      "style":"note"
    }
  ]
...
```

### Rendered PNG

[[/rendering/example.png|example.png]]

