# Flutter Learning Roadmap

# Chapter 1: Flutter အခြေခံများ
Lesson 1.1: Widget များ နှင့် Widget Tree

* Widget ဆိုတာဘာလဲ
* StatelessWidget vs StatefulWidget
* Widget Tree နှင့် Element Tree
* BuildContext နားလည်ခြင်း

Lesson 1.2: Layout Widget များ

* Container, Padding, Margin
* Row, Column, Stack
* Expanded, Flexible
* SizedBox, Spacer

Lesson 1.3: Basic UI Components

* Text, RichText
* Image (Network, Asset)
* Icon, IconButton
* Button များ (ElevatedButton, TextButton, OutlinedButton)

Lesson 1.4: Scaffold နှင့် AppBar

* Scaffold structure
* AppBar customization
* Drawer, BottomNavigationBar
* FloatingActionButton

# Chapter 2: State Management အခြေခံ
Lesson 2.1: setState() သုံးခြင်း

* StatefulWidget lifecycle
* setState() method
* State ပြောင်းလဲခြင်း၏ အလုပ်လုပ်ပုံ

Lesson 2.2: Form Handling

* TextEditingController
* Form validation
* TextFormField
* Global keys

Lesson 2.3: Lists နှင့် Scrollable Widgets

* ListView, ListView.builder
* GridView
* SingleChildScrollView
* CustomScrollView, Slivers

# Chapter 3: Navigation နှင့် Routing
Lesson 3.1: Basic Navigation

* Navigator.push(), Navigator.pop()
* MaterialPageRoute
* Data passing between screens

Lesson 3.2: Named Routes

* Route configuration
* Arguments passing
* onGenerateRoute

Lesson 3.3: Advanced Navigation

* Nested Navigation
* Tab Navigation (TabBar, TabBarView)
* Drawer Navigation

# Chapter 4: Styling နှင့် Theming
Lesson 4.1: Theme နှင့် Colors

* ThemeData
* ColorScheme
* Material Design Colors

Lesson 4.2: Typography နှင့် Text Styling

* TextStyle
* Font families
* Google Fonts integration

Lesson 4.3: Custom Styling

* BoxDecoration
* BorderRadius, Shadows
* Gradients

# Chapter 5: Advanced Widgets
Lesson 5.1: Animation အခြေခံ

* AnimationController
* Tween animations
* AnimatedContainer, AnimatedOpacity

Lesson 5.2: Custom Widgets

* Creating reusable widgets
* Widget composition
* Widget parameters နှင့် callbacks

Lesson 5.3: Gestures နှင့် Interactions

* GestureDetector
* InkWell, Material
* Touch events handling

# Chapter 6: Data နှင့် Networking
Lesson 6.1: HTTP Requests

* http package
* GET, POST requests
* JSON parsing

Lesson 6.2: Error Handling

* Try-catch blocks
* FutureBuilder error states
* Network error handling

Lesson 6.3: Local Storage

* SharedPreferences
* File system access
* Path provider

# Chapter 7: Advanced State Management
Lesson 7.1: Provider Pattern

* Provider package
* ChangeNotifier
* Consumer, Selector

Lesson 7.2: BLoC Pattern အခြေခံ

* BLoC concept
* Events နှင့် States
* flutter_bloc package

Lesson 7.3: Riverpod (Optional)

* Riverpod vs Provider
* StateProvider, FutureProvider
* Consumer widgets

# Chapter 8: Database Integration
Lesson 8.1: SQLite နှင့် sqflite

* Database setup
* CRUD operations
* Database migrations

Lesson 8.2: Hive (NoSQL)

* Hive setup
* Type adapters
* Box operations

# Chapter 9: Device Features
Lesson 9.1: Camera နှင့် Image Processing

* camera package
* Image picker
* Image manipulation

Lesson 9.2: Location Services

* Geolocator package
* Permission handling
* Maps integration basics

Lesson 9.3: Device Sensors

* Sensors package
* Accelerometer, Gyroscope
* Device info

# Chapter 10: Testing နှင့် Debugging
Lesson 10.1: Unit Testing

* Test structure
* Mock objects
* Testing widgets

Lesson 10.2: Widget Testing

* Widget test framework
* Finding widgets
* Interaction testing

Lesson 10.3: Debugging Tools

* Flutter Inspector
* Performance profiling
* Debug console

# Chapter 11: Performance Optimization
Lesson 11.1: Build Performance

* Widget rebuilding optimization
* const constructors
* RepaintBoundary

Lesson 11.2: Memory Management

* Memory leaks prevention
* Dispose methods
* Stream subscriptions

# Chapter 12: Deployment Preparation
Lesson 12.1: App Icons နှင့် Splash Screens

* flutter_launcher_icons
* Native splash screens
* Brand identity

Lesson 12.2: Build Variants

* Development vs Production builds
* Build configurations
* Environment variables

Lesson 12.3: Platform-specific Configurations

* Android permissions
* iOS Info.plist
* Platform channels basics
