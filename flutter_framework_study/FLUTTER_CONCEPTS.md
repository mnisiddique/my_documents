# State:  
State is data that can be read synchronously when widget is built and change during the lifetime of the widget. 

# Types of state: 

State can be divided into 2 categories: -
-  **App State**: Data that exists in the memory while app is running.
-  **Ephemeral State**: Data that exists only while a specific widget is on the screen.

# Stateless Widget: 
Widget of which data cannot be modified after once they built.

# Stateful Widget: 
Widget of which data can be modified after once they built.



# Inherited Widget: 
The widget that is able to pass data/state and data/state change events to its child/descendants without using the constructor is known as inherited widget. 

- Flutter framework itself uses inherited widget. For example, Theme, Navigator, MediaQuery etc. are inherited widgets.

- Fields declared in inherited widget are final as inherited widget is immutable.

- Flutter rebuilds only the widget that is using the data from inherited widget. (In case if the entire app is the child of an inherited widget, change in inherited widget data will not rebuild entire widget tree)

- updateShouldNotify is an unimplemented method of inherited widget class, which takes inherited widget with old value. Here we can decide whether the child widget should be rebuild based on the current and old data of inherited widget. If this method returns true then child widget will be rebuilt.

- dependOnInheritedWidgetOfExactType<InheritedNetworkHandler> is a method that tries to find concrete implementation of the given type above the current widget of the widget tree.

# Build Context: 
Build context in flutter is a locator, which locates widget in the widget tree. Each widget contains unique build context. The build function which has‘BuildContext’ param does not represents the tree location of the widget
returned by that function. For e.g.

```
class MyHomePage extends StatefulWidget {
  const MyHomePage({Key? key, required this.title}) : super(key: key);

  final String title;

  @override
  State<MyHomePage> createState() => _MyHomePageState();
}

class _MyHomePageState extends State<MyHomePage> {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text(widget.title),
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          // ignore: prefer_const_literals_to_create_immutables
          children: <Widget>[
            const Text(
              'You have pushed the button this many times:',
            ),
            // Text(
            //   '$_counter',
            //   style: Theme.of(context).textTheme.headline4,
            // ),
          ],
        ),
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: () => Scaffold.of(context)
            .showBottomSheet((context) => const Text("Hello")),
        tooltip: 'Increment',
        child: const Icon(Icons.add),
      ),
    );
  }
}

```
[Helpfull Viedo To Understand BuildContext](https://www.youtube.com/watch?v=MFNe7hdOCVs)

//Next Flutter Topic to Understand

# What is Stream in Flutter?
# Explain the different types of Streams?
# What are the similarities and differences of Future and Stream?


