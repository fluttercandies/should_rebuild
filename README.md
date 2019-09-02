# ShouldRebuild

[![Star this Repo](https://img.shields.io/github/stars/fantasy525/should_rebuild)](https://github.com/fantasy525/should_rebuild)

ShouldRebuild is a Widget that can prevent Widget rebuilding.

### Add dependency
```yaml
dependencies:
  should_rebuild: 0.0.1  #latest version
```
## Super simple to use

```dart
ShouldRebuild<Todo>(
    shouldRebuild: (oldWidget, newWidget) => oldWidget.counter != newWidget.counter,
    builder: () => Todo(counter: counter,),
),
```
Todo Widget
```dart
class Todo extends StatelessWidget {
  final int counter;
  Todo({this.counter});
  @override
  Widget build(BuildContext context) {
    return Container(
      child: Text(counter.toString()),
    );
  }
}
```
The Todo widget only rebuilds if counter changes

ShouldeRebuild Widget is a generic StatefulWidget,this generic represents the type of Widget returned by the builder method


