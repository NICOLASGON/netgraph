# Netgraph

Web application to visualize network topology graph with an MQTT api.

## Getting Started

Open the index.html with a browser and try to add a node :

```
mosquitto_pub -t "netgraph/" -h iot.eclipse.org -m '{"id": "node_01", "neighbors": []}'
```

Add a new node with a link to the first one :

```
mosquitto_pub -t "netgraph/" -h iot.eclipse.org -m '{"id": "node_02", "neighbors": ["node_01"]}'
```

## Built With

* [d3js](https://d3js.org/) - The svg manipulation framework
* [mqttws31](https://www.eclipse.org/paho/clients/js/) - MQTT javascript client library

## Authors

* **Ross Kirsling** - *Initial work* - [Directed Graph Editor](http://bl.ocks.org/rkirsling/5001347)
* **Nicolas Gonzalez**
* **Benjamin Freeman**

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details