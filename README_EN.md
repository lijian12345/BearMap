# BearMap

[README_CN](README.md)

Project source address: [CS61B-sp18 Proj3](https://sp18.datastructur.es/materials/proj/proj3/proj3)

This project, from CS61B, is a map project inspired by Google Map, implementing routing search, navigation and other features.

This project records my version.

### How to Run

- Firstly we can execute this command as following:

  ```bash
  mvn clean compile assembly:single
  ```

- Then run the main() method of **MapServer** class.

  - Or we can execute these commands as following:

    ```bash
    cp target/bearmap-1.0-jar-with-dependencies.jar .
    java -jar bearmap-1.0-jar-with-dependencies.jar
    ```

- Finally open the browser and type the localhost:4567, a map will display.

### Simple Deployment

- Firstly execute this command:

  ```bash
  nohup java -jar bearmap-1.0-jar-with-dependencies.jar >/dev/null 2>log &
  ```

- If we choose caddy to deploy, we only need to add one line(reverse_proxy localhost:4567) in caddyfile. Of course we need to prepare the domain name and A record well before this operation.

### How to Use

- In browser we can find a area of map and we can drag or scroll the mouse to control the concrete area of this map.

- Double click left mouse button, we can select start point and end point. Then a shortest path will display in the map, click the upright button we can get the navigation information.

  <img src="route_example.png" style="zoom:60%;" />

- In search bar we can type some location prefix, browser will display some autocompleted locations.

  <img src="map_example.png" alt="map_example" style="zoom:60%;" />

### Features

- Map Rastering: Rastering is the job of converting information into a pixel-by-pixel image. Given the longitude, latitude and LonDPP from the browser, the project can show the concrete map images in the browser.
- Routing & Location Data: Use a real world dataset combined with an industrial strength dataset parser to construct a graph. This graph contains all Location data and route information.

- Route Search: Find the shortest path between start point and end point using A\* algorithm.

- Autocompletion: User can search a point they want through autocompletion. This feature is implemented through constructing a trie.

- Nearest Neighbor Search: User can get the nearest neighbor location of the mouse double click point. This feature is implemented through constructing a k-d tree.
