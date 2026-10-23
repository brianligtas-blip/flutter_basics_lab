build() called: 1 glasses
build() called: 2 glasses
build() called: 3 glasses

When I removed Expanded from the Rain StatBox, it no longer shared the available width equally with the Humidity and Wind boxes. The Rain box became narrower because its width depended on its content and layout constraints, while the other two boxes continued to expand. This demonstrated that Expanded helps distribute the available space equally among widgets in a Row.

The buttons became more rounded because the corner radius increased from 8 to 20, giving the interface a softer appearance.

1. A StatelessWidget does not manage changing state, while a StatefulWidget can update its UI when its state changes. An example of a StatelessWidget is ProfileCard in Activity 1, while WaterTrackerPage in Activity 2 is a StatefulWidget.
2. A StatefulWidget uses two classes because one defines the widget and the other manages its changing state. The StatefulWidget class creates the widget, while the State class stores changing data and rebuilds the UI when setState() is called.
3. The value of _glasses changed, but the UI did not update immediately because Flutter was not notified to rebuild the widget. The setState() method tells Flutter that the state has changed and the UI needs to be rebuilt.
4. The build() method is called when the widget is first displayed and whenever Flutter needs to rebuild the UI, such as after setState() is called.
5. In a Row, the main axis is horizontal and the cross axis is vertical. In a Column, the main axis is vertical and the cross axis is horizontal.
6. When I removed Expanded from a StatBox, that box no longer shared the available width equally with the other boxes and could become narrower. Expanded allows a widget to occupy its share of the available space along the main axis.
7. We use GridView.builder because it arranges menu items in a grid, supports scrolling, and builds items as needed. This makes it more efficient for displaying a large number of menu items than a Column containing all the children.
8. Stack places widgets on top of one another, allowing the badge to appear over a menu item. Positioned specifies the badge's location, such as the top-right corner of the item.
9. ThemeData applies shared styles throughout the app, while styling an individual widget changes only that widget's appearance. In Activity 5, changing the button corner radius in buildTheme() customizes the buttons through the theme, while setting a TextStyle on a Text widget customizes that specific text.
10. The _ThemeDemoAppState class holds the dark-mode state in a variable such as _isDark. When the switch changes, the app calls setState(), which rebuilds the widget and updates MaterialApp to use either the light or dark theme.