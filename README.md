# ShouldRebuild

[![Star this Repo](https://img.shields.io/github/stars/fantasy525/should_rebuild)](https://github.com/fantasy525/should_rebuild)

A widget can prevent Widget unnecessary rebuild.

### Add dependency
```yaml
dependencies:
  should_rebuild:
      git:
        url: https://github.com/fantasy525/should_rebuild
```

## Super simple to use

```dart
ShouldRebuild<Todo>(
    shouldRebuild: (oldWidget, newWidget) => oldWidget.counter != newWidget.counter,
    child: Todo(counter: counter,)
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
The Todo widget only rebuild if counter changes

ShouldRebuild Widget is a generic StatefulWidget,this generic represents the type of Widget returned by the builder method


