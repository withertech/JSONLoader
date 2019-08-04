# JSONLoader

A simple library to quickly load JSON from your local bundle to a `Codable` object.

## How to use
Simply define your `struct` as `Codable` and then when you need to map your JSON file to that object just call the `load` function.

## Example
Say you had a JSON file named `people.json` like this:
``` 
[
  {
    "id": 1,
    "name": "Jane"
  },
  {
    "id": 2,
    "name": "John"
  }
]
```
Now you need a data model like so:
```
struct Person: Codable {
   var id:Int
   var name:String
}
```
Now you all you need to do to populate a array of these is call the load method (After importing JSONLoader):

```
var people:[Person] = load("people")
```
