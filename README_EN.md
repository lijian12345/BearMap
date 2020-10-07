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

### How to Use

- In browser we can find a area of map and we can drag or scroll the mouse to control the concrete area of this map.

- Double click left mouse button, we can select start point and end point. Then a shortest path will display in the map, click the upright button we can get the navigation information.

  <img src="route_example.png" style="zoom:60%;" />

- In search bar we can type some location prefix, browser will display some autocompleted locations.

  <img src="map_example.png" alt="map_example" style="zoom:60%;" />
