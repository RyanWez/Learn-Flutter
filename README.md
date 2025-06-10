Flutter Learning Roadmap (June - December 2025)
---

This roadmap is designed for a learner with a foundational understanding of the Dart Language and a completed Flutter installation.

Month: June 2025 - Flutter UI Fundamentals
---

Week 1 (June 11 - June 17)
Chapter 1: Flutter Core Concepts & Basic Widgets
Lesson 1: What is a Widget? Understanding the Widget concept and the Widget Tree.
Lesson 2: MaterialApp and Scaffold Widgets - The fundamental structure of an app.
Lesson 3: Basic Widgets - Utilizing Container, Text, Icon, and Image (from Asset and Network).
Lesson 4: Layout Widgets (Part 1) - Positioning UI elements with Column, Row, Center, and Padding.
Project: Digital Business Card App - Construct a simple UI displaying a name, title, phone number, and email using Column, Row, and Icon widgets.

Week 2 (June 18 - June 24)
Chapter 2: Advanced Layouts & Interactivity
Lesson 1: Layout Widgets (Part 2) - Study Stack, Positioned, Expanded, and Flexible.
Lesson 2: ListView & GridView - Building scrollable lists and grids.
Lesson 3: Card and ListTile - Organizing and presenting UI components effectively.
Lesson 4: User Interaction - Detecting user taps with GestureDetector and Buttons (ElevatedButton, TextButton).
Project: Simple Contact List App - Use ListView to display a list of mock contacts, utilizing ListTile and Card for presentation.


Week 3 (June 25 - July 1)
Chapter 3: State Management Fundamentals
Lesson 1: StatelessWidget vs StatefulWidget - Understanding the differences and use cases.
Lesson 2: State object and setState() - Learning how to make the UI dynamic in a StatefulWidget.
Lesson 3: Lifting State Up - Understanding the concept of passing state to a higher level in the widget tree.
Project: Dice Roller App - Build an application where a random dice face is displayed each time a button is pressed. This will primarily use StatefulWidget and setState().
Month: July 2025 - Navigation & Data Handling

Month: July 2025
---
Week 4 (July 2 - July 8)
Chapter 4: Navigation and Routing
Lesson 1: Basic Navigation - Navigating between screens using Navigator.push() and Navigator.pop().
Lesson 2: Passing Data Between Screens - Learning how to send data to a new screen and retrieve data upon returning.
Lesson 3: Named Routes - Managing routes systematically by assigning names.
Project: Multi-screen Quiz App - Navigate from a Home Screen to a Quiz Screen, and after answering questions, navigate to a Result Screen to display the score.


Week 5 (July 9 - July 15)
Chapter 5: User Input & Forms
Lesson 1: TextField and TextFormField - Capturing text input from the user.
Lesson 2: Form Validation - Validating user input using the Form widget and its validator property.
Lesson 3: Handling Form Submission - Saving form data using Form.save().
Project: Simple Login/Register UI - Build a UI with TextFields for email and password, a Login button, and implement input validation.


Week 6 (July 16 - July 22)
Chapter 6: Networking & APIs
Lesson 1: Introduction to HTTP - Understanding GET and POST requests.
Lesson 2: The http package - Fetching data from an online API.
Lesson 3: JSON Parsing - Converting JSON data from an API into Dart objects (both manually and using code generation).
Lesson 4: FutureBuilder - Displaying the results of asynchronous operations in the UI.
Project: Simple Weather App - Build an app that fetches and displays the current weather for a specific city using a free Weather API.


Week 7 (July 23 - July 29)
Chapter 7: Introduction to State Management (Provider)
Lesson 1: Why a State Management solution is needed; limitations of setState().
Lesson 2: The Provider package - Understanding ChangeNotifierProvider, ChangeNotifier, and Consumer.
Lesson 3: Separating UI from Business Logic - Writing application logic independently from the UI.
Project: Refactor the Weather App from Week 6 to use Provider. Manage the app's state (e.g., loading, data, error) with Provider.
Month: August 2025 - Persistence & Advanced UI


Month: August 2025
---
Week 8 (July 30 - Aug 5)
Chapter 8: Local Data Persistence (SharedPreferences)
Lesson 1: The shared_preferences package - Storing simple data (like settings or themes) on the device.
Lesson 2: Saving & Reading data using Key-Value pairs.
Project: Theme Switcher App - Create an app that can switch between Light and Dark themes and remembers the user's choice even after restarting.


Week 9 (Aug 6 - Aug 12)
Chapter 9: Local Database (hive/isar)
Lesson 1: Learn hive (or isar) for storing more complex data than shared_preferences allows.
Lesson 2: Setting up hive and creating Boxes.
Lesson 3: CRUD Operations (Create, Read, Update, Delete) with hive.
Project: Todo App - Build a Todo app where a user can add, edit, delete, and mark tasks as complete, with all data persisted locally using hive.


Week 10 & 11 (Aug 13 - Aug 26)
Chapter 10: Building a Complete App & Introduction to Animations
Lesson 1: Putting it all together: Combine navigation, state management, API calls, and a local database into one application.
Lesson 2: Implicit Animations - Adding simple animations with AnimatedContainer and AnimatedOpacity.
Lesson 3: Explicit Animations - A basic introduction to AnimationController and Tween.
Project: Simple News App - Fetch articles from a News API, manage state with Provider, allow users to save articles for offline reading with hive, and add simple animations to the UI.
Month: September 2025 - Firebase Integration


Week 12 (Aug 27 - Sep 2)
Chapter 11: Firebase Setup & Authentication
Lesson 1: Creating a Firebase project and integrating it with a Flutter app.
Lesson 2: firebase_auth package - Implementing Sign Up and Sign In with Email & Password.
Lesson 3: Managing User State - Using StreamBuilder to listen for authentication state changes and update the UI accordingly.
Project: Connect the Login/Register UI from Week 5 to Firebase Authentication to make it fully functional.


Month: September 2025
---
Week 13 (Sep 3 - Sep 9)
Chapter 12: Cloud Firestore (Database)
Lesson 1: The Firestore Data Model - Collections, Documents, Fields.
Lesson 2: CRUD Operations - Writing, reading, updating, and deleting data using the cloud_firestore package.
Project: Simple Note-Taking App - Build an app where individual users can save and view their own private notes in Firestore.


Week 14 (Sep 10 - Sep 16)
Chapter 13: Real-time Data with Firestore
Lesson 1: Using .snapshots() (Stream) - Enabling real-time UI updates whenever data changes in Firestore.
Lesson 2: Using StreamBuilder in conjunction with Firestore streams.
Project: Simple Chat App - Build a chat application for two or more users using Firestore's real-time capabilities.


Week 15 (Sep 17 - Sep 23)
Chapter 14: Firebase Storage
Lesson 1: The firebase_storage package - Uploading files like images and videos.
Lesson 2: Retrieving download URLs and displaying images from Firebase Storage.
Project: Enhance the Chat App with profile picture uploads or the Note-Taking App to support image attachments using Firebase Storage.


Month: October 2025 - Advanced Topics
---
Week 16 & 17 (Sep 24 - Oct 7)
Chapter 15: Advanced State Management & Architecture
Lesson 1: Exploring other state management solutions: A basic study of Riverpod or BLoC.
Lesson 2: App Architecture - Understanding the fundamental principles of design patterns like MVVM (Model-View-ViewModel) or Clean Architecture.
Project: Refactor a previous project (e.g., the News App) using Riverpod or BLoC. Systematically restructure the code according to an architectural pattern.


Week 18 & 19 (Oct 8 - Oct 21)
Chapter 16: Testing
Lesson 1: Unit Testing - Testing individual Dart functions and logic.
Lesson 2: Widget Testing - Testing the UI and functionality of individual widgets.
Lesson 3: Integration Testing - Testing the complete user flow of an application from start to finish.
Project: Write test cases for the business logic and widgets of previously developed applications.


Week 20 (Oct 22 - Oct 28)
Chapter 17: Advanced UI & Platform Channels
Lesson 1: CustomPainter and Canvas - Drawing custom shapes and graphs.
Lesson 2: Platform Channels (Basics) - Invoking native Android (Kotlin/Java) or iOS (Swift/Objective-C) code from Flutter.
Project: Draw a simple pie chart using CustomPainter.


Month: November 2025 - Capstone Project
---
Week 21 to Week 24 (Oct 29 - Nov 25)
Chapter 18: Capstone Project
Goal: Synthesize all learned concepts by building a complete application from scratch.
Project Ideas:
E-commerce App: Display products, add to cart, and simulate checkout (can use Firebase).
Recipe App: Search, view, and allow users to submit their own recipes.
Fitness Tracker: Log workouts and track progress.
Process:


Week 21: Select an idea, define features, and create a UI/UX design (using Figma or pen & paper).

Week 22-23: Begin development of core features.

Week 24: Test the application, resolve bugs, and polish the UI.

Month: December 2025 - Deployment & Final Polish
---
Week 25 & 26 (Nov 26 - Dec 9)
Chapter 19: Preparing for Release & Google Play Store
Lesson 1: Implementing an app icon and splash screen.
Lesson 2: Setting the app version and build number.
Lesson 3: Generating an Android App Bundle (AAB) file.
Lesson 4: Study the requirements for the Google Play Console and publish the app.
Project: Publish the capstone project to the Play Store as a beta release.


Week 27 & 28 (Dec 10 - Dec 23)
Chapter 20: Apple App Store & Continuous Learning
Lesson 1: Learn about Apple Developer Account requirements and App Store Connect.
Lesson 2: Archive the app for iOS and test with TestFlight.
Lesson 3: Submit the app to the App Store (note: a Mac device may be required).
Lesson 4: Basic introduction to CI/CD (Continuous Integration/Continuous Deployment) concepts (e.g., Codemagic, GitHub Actions).
Project: Study the steps required to submit the capstone project to the App Store.


Week 29 (Dec 24 - Dec 31)
Chapter 21: Review and Future Path
Activity 1: Review all topics learned throughout the year.
Activity 2: Explore the latest packages and techniques in the Flutter Community (pub.dev, Medium, YouTube).
Activity 3: Build a professional GitHub profile and upload completed projects.

This document outlines a comprehensive learning path for Flutter. The most critical component for mastery is the practical application of concepts through the completion of each week's designated project. For challenges encountered, refer to resources such as Google, Stack Overflow, and the official Flutter community.
