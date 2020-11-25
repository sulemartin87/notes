## Rules

### JSON parsing

- an object is called a map in dart

- begins with curly braces = **map** basically a javascript object

  ```json
  {
    "id":"487349",
    "name":"Pooja Bhaumik",
    "score" : 1000
  }
  ```

- begins with square brackets = **list** basically and array

## Create json parser from json 

​	go to ['app.quicktype.io'](https://app.quicktype.io/)

  - paste json and get a classes from it

    use a try catch method when getting data in getusers for example

    return an empty user class when it fails or show an error somehow

- auth.login returns a message in the response and a user class as an instance 

- goes to userprovider to set user 

- find out what that does

- json parsing should be less than 16 milliseconds

- flutter uses a separate [isolate](https://api.flutter.dev/flutter/dart-isolate/Isolate-class.html)

- 

# Parse json workflow

1. Make a network request by using the http client - returns a future

2. get a response from the http client as a string 

3. cast that string into a map of <string, dynamic> because we know the key is a string but the value can be something else 

4. return previous value and map it to a map of photo class

   1. photo class is 

      ```dart
      class Photo {
        final int id;
        final String title;
        final String thumbnailUrl;
      
        Photo({this.id, this.title, this.thumbnailUrl});
      
        factory Photo.fromJson(Map<String, dynamic> json) {
          return Photo(
            id: json['id'] as int,
            title: json['title'] as String,
            thumbnailUrl: json['thumbnailUrl'] as String,
          );
        }
      }
      ```

   5. 

## State management 

- Flutter is a declarative framework 
- can not update it simply with a function bacause it has to be rebuilt 
- every time data is changed the widget is reconstructed
- if you want to change contents, it needs to live in MyCart’s parent or above.
- widgets are immutable, they don't change they get replaced 
- Flutter has mechanisms for widgets to provide data and services to their descendants (in other words, not just their children, but any widgets below them)
- use provider package for providing data to other widgets 
-With provider, you don’t need to worry about callbacks or InheritedWidgets. But you do need to understand 3 concepts:

- ChangeNotifier
- ChangeNotifierProvider
- Consumer

```
ChangeNotifier is a simple class included in the Flutter SDK which provides change notification to its listeners. In other words, if something is a ChangeNotifier, you can subscribe to its changes. (It is a form of Observable, for those familiar with the term.)

 (You don’t need to use ChangeNotifier with provider at all, but it’s an easy class to work with.)
```
