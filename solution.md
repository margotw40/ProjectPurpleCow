# Proof of Concept for Project Purple Cow

## By Margot White

This web application API allows the user to retrieve, set, and delete items.

## Running the Project

To run and build this project use the command `make build run`.  The port that the web app is served on can be changed by editing the `PORT` value in `config.env`.  The API can be viewed at <http://0.0.0.0:3000/item> if the port has not been changed.

While the server is running, the following commands will allow the user to interact with the data:
`curl -X GET "http://0.0.0.0:3000/item/"`
`curl -X PUT -d "name=SOMENAME" "http://0.0.0.0:3000/item/ITEMID/"`
`curl -X POST -d "name=SOMENAME" "http://0.0.0.0:3000/item/"`
`curl -X DELETE "http://0.0.0.0:3000/item/ITEMID/"`
`SOMENAME` and `ITEMID` should be replaced with the intended name and id. The user can also add an item id to the end of the GET url to retrieve an individual item.

## System Requirements

* Docker version 20.10.5, build 55c4c88

## Assumptions

* Max name length is 100 characters
* The item id numbers do not have to be continuous
* The front end does not need to be as functional as the backend
* Setting items means adding an item to the database

## Future Considerations

* Add support for publishing Docker images to a repo
* Add support for AWS (or other cloud service)
* Consider a need for more url endpoints
* Create dev branches in github
* Add automated integration testing
* Migrate to a more common database, such as mysql
* Consider other properties for Item, such as an edited date/time
* Consider splitting name in to first/last
* Handle page errors, such as 404
