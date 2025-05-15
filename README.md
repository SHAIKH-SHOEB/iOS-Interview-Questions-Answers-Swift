# iOS_Swift_Interview_QA
iOS Interview Questions And Answers In Swift

This document covers common iOS Swift interview questions and answers, helpful for quick revisions or interview preparations.

---

### 1) What is Delegate?
**Answer:** A delegate is a design pattern that allows one object to communicate back to another object in a decoupled way.

### 2) What is a Plist file?
**Answer:** In swift, a Plist (short for Property List) is a structured file used to store Serialized objects, like dictionaries, arrays, string, numbers, dates, and booleans. PList are commonly used for storing configuration settings or small amounts of persistent data in your app.\
**Optional:**
- Plist has the extension `.plist` and is usually written in XML format.
- You’Il often see a file called `Info.plist` in every Xcode project, it contains important configuration info about your app, like version number, permissions etc.
- You can also create custom `.plist` files to store app-specific settings or resources.


### 3) Explain Difference Between Var and Let?
**Answer:** In swift, both var and let are used to declare variables, but they have different mutability rules:
- Var - Mutable Variable:
  - Used to declare a variable whose value can be changed.
  - You can assign a new value to it later.
- let - Constant:
  - Used to declare a constant meaning the value cannot be changed once assigned.
  - You must assign it a value once, and it cannot be reassigned.


### 4) Compare Print and DebugPrint?
**Answer:** In swift, print and debugPrint are both used to output information to the console, but they serve slightly different purposes:
- Print(_:)
  - Used for user friendly output.
  - Formats output in a readable way.
  - Ideal for showing results clearly (especially for basic types like string, array, dictionaries).
- debugPrint()
  - Used for debugging.
  - Outputs the exact representation of an object (including escape characters, quotes, type information where available).
  - Useful for inspecting details during development.

### 5) What is a Guard Statement?
**Answer:** In swift a `Guard Statement` is used for early exit, it helps you exit a function, loop, or block early if a certain condition isn’t met, It’s a great way to write clean, readable, and safe code, especially when handling `Optionals` or `Validation`.

### 6) What are the Fundamental types of variables?
**Answer:** In swift, the fundamental types of variables refer to the basic built-in data types provided by the language. These types form the foundation for storing and maintaining data./
**Example:**
- Integer Type (32-bit or 64-bit)
- Float Type (32-bit)
- Double Type (64-bit)
- Boolean Type
- String Type
- Character Type
- Optional Type


### 7) How does swift handle Memory Management?
**Answer:** swift handles memory management automatically using a system called Automatic Reference Counting(ARC). ARC keeps track of how many strong references exist to a class instance, and automatically frees memory when that instance is no longer needed.

### 8) Explain ApplicationLife Cycle?
**Answer:** The application life cycle in swift (iOS) refers to the sequence of states an app goes through from launch to termination, managed by the system and monitored via the UIApplicationDelegate
- `Not Running:` The application has not been launched or was terminated.
- `Inactive:` The application is running in the foreground but not receiving events (e.g., during a phone call or alert).
- `Active:` The application is in the foreground and receiving user input.
- `Background:` The application is running but not visible, it can execute limited code.
- `Suspended:` The application is in memory but not executing code.


### 9) What is View Controller Life Cycle?
**Answer:** The View Controller Life Cycle refers to the sequence of methods called as a view controller’s view is loaded, appears, and disappears. The main methods are:
- `viewDidLoad():` Called once when the view is loaded into memory. Use it to set up data or UI.
- `viewWillAppear():` Called just before the view appears. Good for updating UI.
- `viewDidAppear():` Called after the view appears. Used for starting animations or data loading.
- `viewWillDisappear():` Called before the view disappears. Use it to pause tasks.
- `viewDidDisappear():` Called after the view disappears. Useful for cleanup.

### 10) Explain Difference between AppDelegate and SceneDelegate?
**Answer:** In iOS development, both `AppDelegate` and `SceneDelegate` are responsible for handling lifecycle events of the iOS application.But they have different roles, especially since iOS 13.
- AppDelegate
  - AppDelegate is a Process Lifecycle.
  - Launching the app (application(_:didFinishLaunchingWithOptions:))
  - Responding to push notifications.
  - Handling background tasks.
  - Managing app wide services like analytics, logging, etc.
- SceneDelegate
  - SceneDelegate is a UI (UIWindow) Lifecycle.
  - Creating and managing iOS application UIWindow
  - Responding to scene lifecycle events like sceneDidBecomeActive, sceneWillResignActive
  - Supporting multiple windows on iPadOS/macOS.

### 11) What is CoreData in iOS?
**Answer:** CoreData is Apple’s framework for managing local data in iOS apps. It lets you store, fetch, update, and delete data in a structured and efficient way, and it supports features like data persistence, relationships, and undo/redo.

### 12) What is the difference between SQLite and CoreData?
**Answer:** SQLite is a low-level relational database engine where you write SQL queries, while CoreData is an object graph management framework that provides higher-level abstractions for managing complex data models and relationships in iOS applications.

### 13) What are Persistent Containers in Swift?
**Answer:** A `Persistent Container` is a core concept in CoreData that helps manage the CoreData stack, including the managed object context, persistent store coordinator, and the model. It simplifies the setup and management of CoreData, especially in apps with complex data models.

### 14) What is Context or ViewContext in CoreData?
**Answer:** In CoreData, the Managed Object Context `(NSManagedObjectContext)` is a key component that serves as a Scratchpad or working space where you create, fetch, update, and delete Managed objects. It’s a crucial part of interacting with CoreData object graphs.

### 15) What is Firebase Remote Configuration?
**Answer:** Firebase Remote Configuration is a cloud service that lets you change the behavior and appearance of an iOS application without requiring users to download an update from the AppStore.
- Changing app themes or button colors.
- Turning features on/off (feature flags).
- Updating welcome messages, pricing, or tips.
- Configuring app behavior by region, language, or user segment.

### 16) What is Generic Function with an example?
**Answer:** A Generic Function allows you to write flexible, reusable functions that can work with any data type (like Int, String, CustomClass, etc) without duplicating code.\
**Optional:** Instead of specifying a concrete type, you use type placeholders (usually T, U, etc.) which are replaced by actual types when the function is called.

### 17) Difference between Any and AnyObject?
**Answer:** Use Any if you need to accept or store any kind of value, and use AnyObject if you are working with APIs that expect reference type.

### 18) What is Automatic Reference Counting (ARC)?
**Answer:** Swift handles memory management automatically using a system called `Automatic Reference Counting(ARC)`. ARC keeps track of how many strong references exist to a class instance, and automatically frees memory when that instance is no longer needed.

### 19) What is Class and Struct?
**Answer:** In Swift, Class and Struct are both used to create custom data types, but they have different behaviors and use cases.
- **Class:** A Class is Reference Type, meaning it is Shared when assigned or passed around.
- **Struct:** A Struct is a Value Type, meaning it is Copied when assigned or passed around.

### 20) Difference between Method and Function?
**Answer:** A `Function` is a standalone block of code that performs a specific task and is not tied to any type (line a Class or Struct). and A `Method` is a function that belongs to a class, struct, or enum. It operates on instances of that type.

### 21) What is Lazy Property in swift?
**Answer:** A Lazy Property is a property whose value is only calculated when it’s first accessed, not when the object is created. It helps improve performance by delaying expensive setup until needed.

### 22) Difference Between Weak Reference Vs Unowned Reference?
**Answer:** Both Weak and Unowned are used to avoid strong reference cycles, but they behave differently: use Weak when the reference can be nil, use Unowned when it should never be nil.

### 23) Difference Between Weak Reference Vs Strong Reference?
**Answer:** A Strong Reference keeps the object alive, a Weak Reference allows it to be deallocated.

### 24) What is SwiftLint? (Optional)
**Answer:** SwiftLint is a tool for enforcing swift style and conversion in your codebase. It helps you write clean, consistent, and maintainable code by checking your code against a set of predefined or custom rules.

### 25) What is a Constructor in Swift?
**Answer:** In Swift, a Constructor (called an initializer, using init) is a special method used to create and set up a new instance of a class, struct, or enum.

### 26) What are efficient ways to cache data in swift?
**Answer:** Use NSCache for in memory caching, UserDefaults for small persistent data, and the file system or database for large or structured data. (Like: NSCache, UserDefaults, FileManager, CoreData, Third-Party Libraries)

### 27) What is a Retain Cycle?
**Answer:** A Retain Cycle happens when two or more class instances strongly reference each other, so their reference counts never reach zero, which means they never get deallocated, causing a memory leak.\
**Note:** A Retain Cycle prevents objects from being deallocated, leading to memory leaks. Use Weak or Unowned to break the cycle.

### 28) What is GCD?
**Answer:** In swift, GCD stands for Grand Central Dispatch. It’s a low-level API Provided by Apple to manage concurrent operations by dispatching tasks to different queues. It helps you execute code asynchronously or synchronously on background threads, which improves performance and responsiveness especially important for tasks like network requests, file I/O, or image processing.\
**Example:**
- **Dispatch Queues:** Queues on which tasks are executed.
- **Main queues:** Executes tasks on the main thread (used for UI updates).
- **Global queues:** Concurrent queues provided by the system.
- **Custom queues:** Created using DispatchQueue(label:).
- **Sync vs Async:**
- **Sync:** Waits until the task finishes.
- **Async:** Doesn’t wait, executes the task in the background.

### 29) What is Stream API?
**Answer:** Stream generally refers to handling sequences of data over time, such as continuous input/output or reactive data flows.

### 30) Access Modifiers in Swift
**Answer:** An Access Modifier controls what parts of your code can access a variable, class method, or property. It helps encapsulate and protect data in your application.
- **Open:** Accessible and subclassable outside the module.
- **Public:** Accessible but not subclassable outside the module.
- **Internal:** (default): Accessible within the same module.
- **FilePrivate:** Accessible within the same file.
- **Private:** Accessible only within the enclosing scope.

### 31) What is a layout? Provide an example using a scroll view and adding views.
_(You can include code for setting up a scroll view with views)_

### 32) What is the default UITableViewDelegate Function?
**Answer:** UITableViewDelegate and UITableViewDataSource default function
- UITableViewDelegate: 
  - didSelectRowAt
- UITableViewDataSource:
  - numberOfRowsInSection
  - cellForRowAt

### 33) The difference between Set and Array?
**Answer:** `Array` is an ordered collection that allows duplicates, while a `Set` is an unordered collection that only stores unique elements. Arrays keep the order and are good when duplicates matter, but Set are faster for checking if an item exists because they use hashing.

### 34) Explain the MVVM Architecture.
**Answer:** `MVVM` stands for `Model-View-ViewModel`. It’s a design pattern used to separate the UI from the business logic, making code more modular and testable.
- **Model:** Represents the data and business logic. It handles data retrieval and storage (e.g., API calls, database).
- **View:** The UI layer that displays data to the user. It observes the ViewModel for changes.
- **ViewModel:** Acts as a bridge between the Model and the View. It transforms raw data from the Model into a format the View can display and handles user actions from the View.

### 35) Explain the MVC Architecture
**Answer:** `MVC` stands for `Model-View-Controller`, it’s a design pattern that helps organize code in a clean, maintainable way by separating concerns.
- **Model:**
  - Represents the data and business logic.
  - Does not depend on the UI.
  - Responsible for getting, saving, and processing data.
- **View:**
  - Handles everything the user sees in the UI.
  - It’s passive: just displays data and sends user actions to the controller.
- **Controller:**
  - The middleman between Model and View.
  - Handles user input, updates the model, and refreshes the view.

### 36) What is Asynchronous Function in Swift
**Answer:** An Asynchronous Function in Swift is a function that performs its work in the background and doesn’t block the main thread. It’s marked with the async keyword and allows you to write non-blocking code that looks synchronous using await.
